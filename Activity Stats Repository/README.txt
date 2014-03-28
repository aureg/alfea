Activities Stats Repository
===========================

Author: ALFEA Consulting

This project defines a repository module used by a dashlet that graphically displays activities statistics. 
The statistics can be opened in a complete page for more precise reports based on filters.

Project home : http://forge.alfresco.com/projects/activitystats/
See also : Project 'Activities Stats dashlet and page for Alfresco Share'

Installation
------------

This project generate an Alfresco Module Package (AMP).  
For more details on the supported layout of files, see:
   http://wiki.alfresco.com/wiki/Module_Management_Tool

Use ANT to generate the AMP file from the build script:
   ant -f build.xml
   
Copy and rename build.properties.default to build.properties.
Adapt properties depending your environment. 