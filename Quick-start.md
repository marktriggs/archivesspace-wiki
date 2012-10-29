If you have the Java 1.6.0 JRE (or above) you can download and run a demo server with the following commands:

```sh
wget https://s3.amazonaws.com/archivesspace/public-files/archivesspace.v0.2.0-1.jar
java -jar archivesspace.v0.2.0-1.jar
```

This will start the ArchivesSpace application running on `http://localhost:8080/` and the backend web service running on `http://localhost:8089/`.

## java.lang.OutOfMemoryError: PermGen space

On OS X, I needed to add `-XX:PermSize=128m -XX:MaxPermSize=256m` to avoid the above error.

```sh
java -XX:PermSize=128m -XX:MaxPermSize=256m -jar archivesspace.v0.2.0-1.jar
```

## different ports

If you’d like to use different ports, you can run:

```sh
java -jar archivesspace.v0.2.0-1.jar [frontend port] [backend port]
```