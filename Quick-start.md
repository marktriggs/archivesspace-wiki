If you have the Java 1.6.0 JRE (or above) you can download and run a demo server.  [Download java](http://www.java.com/en/download/index.jsp).  Note, after February 2013, Oracle will no longer post updates of Java SE 6 to its public download sites, so you might want to use java 7.

Download the file from [`http://s3.amazonaws.com/archivesspace/public-files/archivesspace.v0.2.0-1.jar`](http://s3.amazonaws.com/archivesspace/public-files/archivesspace.v0.2.0-1.jar)

Then, get to a command prompt and enter this command (this has been tested on Windows and Linux, see below for OS X).

```sh
java -jar archivesspace.v0.2.0-1.jar
```

This will start the ArchivesSpace application running on `http://localhost:8080/` and the backend web service running on `http://localhost:8089/`.

## OS X: java.lang.OutOfMemoryError: PermGen space

On OS X, I needed to add `-XX:PermSize=128m -XX:MaxPermSize=256m` to avoid the above error.

```sh
java -XX:PermSize=128m -XX:MaxPermSize=256m -jar archivesspace.v0.2.0-1.jar
```

## listen on different ports

If you’d like to use different ports, you can run:

```sh
java -jar archivesspace.v0.2.0-1.jar [frontend port] [backend port]
```