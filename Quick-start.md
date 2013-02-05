If you have the Java 1.6.0 JRE (or above) you can download and run a demo server.  [Download java](http://www.java.com/en/download/index.jsp).  Note, after February 2013, Oracle will no longer post updates of Java SE 6 to its public download sites, so you might want to use Java 7.

1. [[Download|downloads]] the most recent version's JAR file. 
1. Then, get to a command prompt and enter this command (where X and Y are placeholders for the version numbers):
```sh
java -XX:MaxPermSize=128m -Dfile.encoding=UTF-8 -jar archivesspace.v0.X.Y.jar
```
1. This will start the ArchivesSpace front application running at [http://localhost:8080/](http://localhost:8080).
   * The backend web service is running on http://localhost:8089/ 
1. To set up the application, browse to [http://localhost:8080/](http://localhost:8080) and log in using the adminstrator account:
   * Username: `admin`
   * Password: `admin`

## Listen on different ports

If you’d like to use different ports, you can run:

```sh
java -XX:MaxPermSize=128m -Dfile.encoding=UTF-8 -jar archivesspace.v0.X.Y.jar [frontend port] [backend port]
```
[frontend port] and [backend port] are placeholders for actual numbers, such as 8081 8082