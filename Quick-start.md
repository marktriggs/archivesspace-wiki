If you have the Java 1.6.0 SDK (or above) you can build and run a demo server with the following commands:

```sh
wget https://github.com/downloads/archivesspace/archivesspace/archivesspace.v0.2.0.jar
java -jar archivesspace.v0.2.0.jar
```

This will start the ArchivesSpace application running on `http://localhost:8080/` and the backend web service running on `http://localhost:8089/`.

If you’d like to use different ports, you can run:

```sh
java -jar archivesspace.v0.2.0.jar [frontend port] [backend port]
```