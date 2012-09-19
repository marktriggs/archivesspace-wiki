ArchivesSpace Dependencies

 * [`git`](http://git-scm.com) is needed to clone the source repository.
 * JDK 1.6 or JDK 1.7 (from either Oracle or OpenJDK) is needed by embedded `ant` to build (should run okay on JRE)
 * [`node`](http://nodejs.org) on the $PATH will speed up the sprockets asset pipeline generation phase of the build
 * J2EE server such as [`tomcat`](http://tomcat.apache.org) 6 or 7; two instances will need to be set up (one for the front end, one for the back end) [TODO: go into more details about how to set up two CATALINA_HOME directories that share a common CATALINA_BASE].

Once these are installed, the directions at [[Tomcat Mysql Deployment]] should work.