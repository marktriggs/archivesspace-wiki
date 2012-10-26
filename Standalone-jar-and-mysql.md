**untested**

Download the jar file

```sh
wget https://github.com/downloads/archivesspace/archivesspace/archivesspace.v0.2.0.jar
```

Download the mysql driver from http://dev.mysql.com/downloads/connector/j/

edit a `config.rb` file
```ruby
# path/to/my/config.rb
AppConfig[:db_url] = "jdbc:mysql://localhost:3306/archivesspace?user=as&password=as123"
AppConfig[:backend_url] = "http://localhost:8081"
AppConfig[:frontend_url] = "http://localhost:8080"
```

Set a java system property `aspace.config` equal to the path to your config file

```sh
java -Daspace.config=path/to/my/config.rb \
  -cp mysql-connector-java-5.1.22-bin.jar:archivesspace.v0.2.0.jar \
  org.archivesspace.Main
```