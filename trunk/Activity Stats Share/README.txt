Activities Stats dashlet and page for Alfresco Share
=====================================================

Author: ALFEA Consulting

This project defines a custom dashlet that graphically displays activities statistics. 
The statistics can be opened in a complete page for more precise reports based on filters.

Project home : http://forge.alfresco.com/projects/activitystats/
Requires : Project 'Activities Stats Repository'

Installation
------------

The add-on has been developed to install on top of an existing Alfresco 3.4 installation.

An Ant build script is provided to build a JAR file containing the 
custom files, which can then be installed into the 'tomcat/shared/lib' folder 
of your Alfresco installation.

Copy and rename build.properties.default to build.properties.
Adapt properties depending your environnemnt. 

To build the JAR file, run the following command from the base project directory.

    ant clean dist-jar

The command should build a JAR file named activities-stats.jar
in the 'build/dist' directory within your project.

To deploy the dashlet files into a local Tomcat instance for testing, you can 
use the hotcopy-tomcat-jar task. You will need to set the tomcat.home
property in Ant.

    ant -Dtomcat.home=C:/Alfresco/tomcat clean hotcopy-tomcat-jar
    
Once you have run this you will need to restart Tomcat so that the classpath 
resources in the JAR file are picked up.

Using the dashlet
-----------------

Log in to Alfresco Share and navigate to your user dashboard. Click the 
Customize Dashboard button to edit the contents of the dashboard and drag 
the dashlet into one of the columns from the list of dashlets.

As well as user dashboards the dashlet can also be used on site dashboards.