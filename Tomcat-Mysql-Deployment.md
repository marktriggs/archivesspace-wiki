This should work with other servlet containers as well. 

Assumes a mysql database on `localhost` port `3306` named `archivesspace`, user: `as`, password: `as123` as seen on [Getting started | Running with MySQL](https://github.com/archivesspace/archivesspace/blob/master/backend/README.md#running-with-mysql).

(set user and password to match your database)

```
git clone http://github.com/archivesspace/archivesspace.git
cd archivesspace
```

Configuration is handled via `config/config.rb` and a traditional RoR `database.yml` is not required.  Defining a mysql database for the frontend will cause nothing but confusion.

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