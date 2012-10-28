**untested**

Download the jar file for archivesspace (ECL2.0) and the jar file for the mysql driver (GNU2.0) 

```sh
mkdir lib
curl https://s3.amazonaws.com/archivesspace/public-files/archivesspace.v0.2.0-1.jar -o lib/archivesspace.jar
curl http://repo1.maven.org/maven2/mysql/mysql-connector-java/5.1.21/mysql-connector-java-5.1.21.jar -o lib/mysql-connector-java-5.1.21.jar
curl https://s3.amazonaws.com/archivesspace/public-files/build.jar
```

edit a `config/config.rb` file
```ruby
# config/config.rb
AppConfig[:db_url] = "jdbc:mysql://localhost:3306/archivesspace?user=as&password=as123"
AppConfig[:backend_url] = "http://localhost:8081"
AppConfig[:frontend_url] = "http://localhost:8080"
```

unzip the build.zip and run the database migrations:
```sh
unzip build.zip
./build/run db:migrate
```

Set a java system property `aspace.config` equal to the path to your config file

```sh
java -Daspace.config=config/config.rb \
  -cp lib/mysql-connector-java-5.1.22-bin.jar:lib/archivesspace.jar \
  org.archivesspace.Main
```