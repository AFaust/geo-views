Geo Views add-on for Alfresco Share
===================================

Author: Will Abson

This project provides the following components which display geotagged content
items within the site in a map view:

  * Site Geotagged Content Dashlet
  * Document Library 'Geographic' View

Installation
------------

The dashlet has been developed to install on top of an existing Alfresco
3.3/3.4 or 4.x installation.

An Ant build script is provided to build a JAR file containing the 
custom files, which can then be installed into the 'tomcat/shared/lib' folder 
of your Alfresco installation.

To build the JAR file, run the following command from the base project 
directory.

    ant clean dist-jar

The command should build a JAR file named `geo-views-<version>.jar`
in the 'dist' directory within your project.

To deploy the dashlet files into a local Tomcat instance for testing, you can 
use the hotcopy-tomcat-jar task. You will need to set the tomcat.home
property in Ant.

    ant -Dtomcat.home=C:/Alfresco/tomcat clean hotcopy-tomcat-jar
    
Once you have run this you will need to restart Tomcat so that the classpath 
resources in the JAR file are picked up.

Usage
-----

### Using the Dashlet

Log in to Alfresco Share and navigate to a site dashboard. Click the 
Customize Dashboard button to edit the contents of the dashboard and drag 
the dashlet into one of the columns from the list of dashlets.
