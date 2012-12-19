If you have the Java 1.6.0 JRE (or above) you can download and run a demo server.  [Download java](http://www.java.com/en/download/index.jsp).  Note, after February 2013, Oracle will no longer post updates of Java SE 6 to its public download sites, so you might want to use java 7.

[[Download|downloads]] the most recent version's JAR file. 

Then, get to a command prompt and enter this command (this has been tested on Windows and Linux, see below for OS X).

```sh
java -XX:MaxPermSize=128m -Dfile.encoding=UTF-8 -jar archivesspace.v0.X.Y.jar
```

This will start the ArchivesSpace application running on `http://localhost:8080/` and the backend web service running on `http://localhost:8089/`.

## listen on different ports

If you’d like to use different ports, you can run:

```sh
java -XX:MaxPermSize=128m -Dfile.encoding=UTF-8 -jar archivesspace.v0.X.Y.jar [frontend port] [backend port]
```
[frontend port] and [backend port] are placeholders for actual numbers, such as 8081 8082