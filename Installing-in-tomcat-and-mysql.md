This should work with other servlet containers as well.  If you test it out, please let us know or even just note it on this page.

ArchivesSpace has a "frontend" web application and a "backend" web application.
The current recommended deployment scenario is to use two tomcat servers, one listening on a public port for the frontend, and one running on a port that is only available to the local machine or private network.  [Twincat](https://github.com/tingletech/twincat) has some shell scripts that can help you set up two tomcat servers.  

The steps below assume there is a mysql database listening on `localhost` port `3306` named `archivesspace`, user: `as`, password: `as123` as seen on [Getting started | Running with MySQL](https://github.com/archivesspace/archivesspace/blob/master/backend/README.md#running-with-mysql).
Set user and password to match your database.

```
git clone http://github.com/archivesspace/archivesspace.git
cd archivesspace
```

Configuration is handled via `config/config.rb`.

```ruby
# config/config.rb
AppConfig[:db_url] = "jdbc:mysql://localhost:3306/archivesspace?user=as&password=as123"
AppConfig[:backend_url] = "http://localhost:8081"
AppConfig[:frontend_url] = "http://localhost:8080"
```
(consider `chmod 600 config/config.rb`?)

```
build/run backend:war
build/run frontend:war
build/run db:migrate
```

Then, copy the `war` files into the tomcat webapps directory:

```sh
cp backend/backend.war .../backend-tomcat-8081/webapps/ROOT.war
cp frontend/frontend.war .../frontend-tomcat-8080/webapps/ROOT.war
```

See also [#44](https://github.com/hudmol/archivesspace/issues/44)

## security note

Frontend/login should probably happen over https, this deployment scenario has not been tested yet. 

Right now, there are no access controls on the backend API.  Leave the backend (`8081` in this example) behind a firewall.  Open up `8080`, or `80` and then set up something along these lines, redirecting 80 to 8080:

```
iptables -A PREROUTING -t nat -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 8080
```