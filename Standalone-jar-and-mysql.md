**untested**

Download the jar file for archivesspace (ECL2.0) and the jar file for the mysql driver (GNU2.0) 

```sh
mkdir lib
curl https://github.com/downloads/archivesspace/archivesspace/archivesspace.v0.2.0.jar -o lib/archivesspace.v0.2.0.jar
curl http://repo1.maven.org/maven2/mysql/mysql-connector-java/5.1.21/mysql-connector-java-5.1.21.jar -o lib/mysql-connector-java-5.1.21.jar
```

edit a `config.rb` file
```ruby
# config/config.rb
AppConfig[:db_url] = "jdbc:mysql://localhost:3306/archivesspace?user=as&password=as123"
AppConfig[:backend_url] = "http://localhost:8081"
AppConfig[:frontend_url] = "http://localhost:8080"
```

**TODO: dbmigrate**

Set a java system property `aspace.config` equal to the path to your config file

```sh
java -Daspace.config=config/config.rb \
  -cp lib/mysql-connector-java-5.1.22-bin.jar:lib/archivesspace.v0.2.0.jar \
  org.archivesspace.Main
```