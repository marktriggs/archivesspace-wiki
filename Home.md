## ArchivesSpace
### Building a next-generation archives management tool

The ArchivesSpace project is in an alpha release stage.  This is the page you can come to for directions about how to install and help us test this tool during the alpha and beta development phases.

## [[Quick Start]]
How to run a test version with an embedded database.

## [[Standalone JAR and mysql]]
Run the standalone jar (embedded jetty) with a mysql database.

## [[Installing in Tomcat and Mysql]]
How to deploy `.war` on tomcat using mysql database.

## [ArchivesSpace google group](http://groups.google.com/group/archivesspace)
Join our community of archivists and technologists working together to build a next-generation archives management tool. 

## [Source Code Documentation](http://archivesspace.github.com/archivesspace/doc/alpha_index.html)
Class, method, [Backend API] and schema documentation.

## Source Code
The master branch of the [`archivesspace/archivesspace` repository on github](https://github.com/archivesspace/archivesspace) is the current stable-for-testing release of the code.  New versions are released every two weeks.

The [`hudmol/archivesspace` repository on github](https://github.com/hudmol/archivesspace) is the upstream repository with active development.

## Migration Framework

Note: this is now accessible from the web interface as well.

Before following the [instructions in `migrations/README.md`](https://github.com/archivesspace/archivesspace/blob/master/migrations/README.md) you will need to install [RVM](https://rvm.io) and execute these commands.

```sh
rvm install jruby-1.6.7
rvm use jruby-1.6.7
export JRUBY_OPTS=--1.9
gem install nokogiri json-schema psych json
```

## Why another page of docs?

Right now, the [`README.md`](https://github.com/archivesspace/archivesspace/blob/master/README.md) has some directions and a link to [`http://hudmol.github.com/archivesspace/`](http://hudmol.github.com/archivesspace/) which is the `gh-pages` branch (which is also [here](http://hudmol.github.com/archivesspace/)) so why start another place for documentation?  This page, at least right now, is focused on the alpha and beta testing phases and how the community can get involved in this phase.