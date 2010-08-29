= Parental Events README =

Some pretty rough app sketch for a event app in OpenSAGA, basically just two DomainTypes 

Needs a little more than java default memory when deployed in tomcat, ( e.g. -XX:MaxPermSize=128m -Xmx256m)

== Introduction ==

The project is an all-in-one OpenSAGA extension based on maven.

All the magic is in the app model below

http://github.com/fforw/parental-events/tree/master/src/main/webapp/WEB-INF/resources/extensions/parental-events/models/

Build with maven. Project is configured to be deployed under "/parental-events".

