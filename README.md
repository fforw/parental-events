= Parental Events README =

Some pretty rough app sketch for a event app in OpenSAGA, basically just two DomainTypes 

Needs a little more than java default memory when deployed in tomcat, ( e.g. -XX:MaxPermSize=128m -Xmx256m)

== Introduction ==

The project is an all-in-one OpenSAGA extension based on maven.

All the magic is in the app model below

http://github.com/fforw/parental-events/tree/master/src/main/webapp/WEB-INF/resources/extensions/parental-events/models/

Build with maven. Project is configured to be deployed under "/parental-events".

== Project overview ==

src
 `-- main
     `-- webapp
         |-- index.jsp
         `-- WEB-INF
             |-- cfg
             |   |-- log4j
             |   |   `-- log4j.properties	logging config
             |   `-- opensaga-project.cfg	configuration for active extensions and stages and context path
             `-- resources
                 `-- extensions
                     `-- parental-events
                         `-- models
                             |-- domain
                             |   |-- relations.xml		Domain Type Relations
                             |   `-- types
                             |       |-- d_event.xml		Event Domain-Type
                             |       `-- d_person.xml	Person Domain-Type
                             |-- i18n
                             |   |-- definitions
                             |   |   `-- resources.xml	Translations
                             |   `-- translations.xml
                             |-- layout
                             |   `-- layout.xml			layout variables
                             |-- navigation
                             |   `-- n_applications.xml	navigation entries
                             |-- portal.xml				main model for the portal. references domain types and processes
                             |-- processes
                             |   `-- p_events			events process
                             |       |-- p_events.xml
                             |       `-- views						detail and list views for the domain types
                             |           |-- v_detail_event.xml
                             |           |-- v_detail_person.xml
                             |           |-- v_list_event.xml
                             |           `-- v_list_person.xml
                             `-- stages.xml							top very basic stage definitions
