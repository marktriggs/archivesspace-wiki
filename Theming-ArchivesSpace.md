## I just want to change some of the labels and messages!

All the messages and labels are stored in a locales file, which is part of the [Rails Internationalization (I18n)](http://guides.rubyonrails.org/i18n.html) API. For example, all the English labels are store in a file in the config/locales/en.yml file. 
 
You can see these files here: 
[ Staff Frontend Application] (https://github.com/archivesspace/archivesspace/tree/master/frontend/config/locales)
[Public Application](https://github.com/archivesspace/archivesspace/tree/master/public/config/locales)

These values are pulled into the views using the I18n.t() methoded, like  I18n.t("brand.welcome_message"). 

You can override these values using the plugins directory. For example, if you want to change the welcome message on the public frontend, make a file in your ArchivesSpace distribution called 'plugins/local/public/locales/en.yml' and put the following values: 

	en:
		brand:
		title: My Archive 
		home: Home
 		welcome_message: HEY HEY HEY!! 

If you restart ArchivesSpace, these values will take effect.

If you're using a different language, simply swap out the en.yml for something else ( like fr.yml ) and update locale setting in the config.rb file ( i.e.,  AppConfig[:locale] = :fr ) 



## I just want to change a few things on the pages!!

For small edits, it's also  easiest to do this as a plugin. With a plugin, we can override default views, controllers, models, etc. without having to do a complete rebuild of the source code. 
 
For example, let's say we wanted to change the branding logo on the public interface. So, first we need to find where in the views this is being rendered. A good first place to go is the [layouts/application.html.erb](https://github.com/archivesspace/archivesspace/blob/master/public/app/views/layouts/application.html.erb) file, which is the Rails default layout for the entire site. Looking through this file, we can see the branding is being rendered in the [site/branding.html.erb](https://github.com/archivesspace/archivesspace/blob/master/public/app/views/site/_branding.html.erb) file, which is a very simple file with pretty much just a link and image tag. 

So, first let's add out image file to the "plugins/local/public/assets/images/my_archive/logo.png" then let's override the default view by making a file in  plugins/local/public/views/site/_branding.html.erb

	   <h1>                                                                            
	      <img src="/assets/images/my_archive/logo.png" alt = <%= I18n.t("brand.title") %> />                                                            
	   </h1>                                                                           
		         

( Note: Since anything we add to plugins directory will not be precompiled by the Rails asset pipeline, we cannot use some of the tag helpers (like img_tag ), since that's assuming the asset is being managed by the asset pipeline.  )

Restart the application and you should see your logo in the default view.

## I want to heavily theme my site and make a lot of CSS changes and template changes!

If you're wanting to really trick out your site, you could do this in a plugin using the override methods show above, although there are some big disadvantages to this. The first is that assets will not be compiled by the Rails asset pipeline. Another is that you won't be able to take advantage of the variables and mixins that Bootstrap and Less provide as a framework, which really helps keep your assets well organized. 

A better way to do this is to pull down a copy of the ArchivesSpace code and build out a new theme. A good resource on how to do this is [this video](https://www.youtube.com/watch?v=Uny736mZVnk) .
This video covers the staff frontend UI, but the same steps can be applied to the public UI as well. 

Also become a little familiar with the [build system instructions ](https://github.com/hudmol/archivesspace/blob/master/build/README.md)


First, pull down a new copy of ArchivesSpace using git and be sure to checkout a tag matching the version you're using or wanting to use.

     $ git clone https://github.com/hudmol/archivesspace/blob/master/build/README.md
     $ git checkout v1.0.9

You can start your application development server by executing:

	     $ ./build/run bootstrap
	     $ ./build/run backend:devserver
	     $ ./build/run frontend:devserver
	     $ ./build/run public:devserver

( Note: you don't have to run all these commands all the time. The bootstrap command really only has to be run the first time your pull down the code..it will also take awhile.  You also don't have to start the frontend or public if you're not working on those interfaces. Backend does have to be started for either the public or frontend interfaces to work. ) 


Follow the insturctions in the video to create a new theme. A good way is to copy the existing default theme to a new folder and start making your updates. Be sure to take advantage of the existing variables set in the Less files to make your assets nice and organized. 

Once you've updated you theme and have got it working, you can package your application. You can use the ./scripts/build_release to build a totally fresh AS distribution, but you don't need to do that if you've simply made some minor changes to the UI. Instead, use the "./build/run public:war " to compile your assets and package a war file. You can then take this public.war file and replace your ASpace distrubtion war file. 

Be sure to update your theme setting in the config.rb file and restart ASpace. 


