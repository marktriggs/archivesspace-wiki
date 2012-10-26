If you have the Java 1.6.0 SDK (or above) you can build and run a demo server with the following commands:

```sh
git clone git://github.com/archivesspace/archivesspace.git
cd archivesspace
build/run dist
java -jar archivesspace.jar
```

This will start the ArchivesSpace application running on `http://localhost:8080/` and the backend web service running on `http://localhost:8089/`.

If you’d like to use different ports, you can run:

```sh
java -jar archivesspace.jar [frontend port] [backend port]
```
Note: If you have already run the service in demo mode, you may need to remove the existing demo database in order to avoid a ‘java.sql.SQLException: Failed to create database’ error:

```sh
build/run db:nuke
```