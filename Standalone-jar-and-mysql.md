Download the jar file for archivesspace (ECL2.0) and the jar file for the mysql driver (GNU2.0) 

```sh
mkdir lib
curl https://s3.amazonaws.com/archivesspace/public-files/archivesspace.v0.2.0-1.jar -o lib/archivesspace.jar
curl http://repo1.maven.org/maven2/mysql/mysql-connector-java/5.1.13/mysql-connector-java-5.1.13.jar -o lib/mysql-connector-java-5.1.13.jar
curl https://s3.amazonaws.com/archivesspace/public-files/as-build.v0.2.0-1.zip -o as-build.zip
     
```

unzip the build.zip and run the database migrations:
```sh
unzip as-build.zip  # unpacks build/ and config/ directories (needs backend as well...)
cp lib/mysql-connector-java-5.1.13.jar build/gems/gems/jdbc-mysql-5.1.13/lib/
```

create a `config/config.rb` file
```ruby
# config/config.rb
AppConfig[:db_url] = "jdbc:mysql://localhost:3306/archivesspace?user=as&password=as123"
AppConfig[:backend_url] = "http://localhost:8089"
AppConfig[:frontend_url] = "http://localhost:8080"
```

run the db:migration ant task

```sh
./build/run db:migrate
```

Set a java system property `aspace.config` equal to the path to your config file and start the server.

```sh
java -Daspace.config=config/config.rb \
  -cp lib/mysql-connector-java-5.1.13-bin.jar:lib/archivesspace.jar \
  org.archivesspace.Main
```