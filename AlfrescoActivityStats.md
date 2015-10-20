# 1 Introduction #
<p>
The module <b>Activity Stats</b> is a simple activity reporting tool for Alfresco Share.<br>
</p>
<p>
It gives to the Alfresco administrator a easy way to monitor the user connections and activities. An administrator can easily send a message to all currently connected users, i.e.to warn them before a maintenance operation.<br>
</p>
<p>
It also gives to all regular users a graphical overview of what happened in their sites of interest.<br>
</p>
<p>
The module <b>Activity Stats</b> was designed with ease of use and simplicity as a primary goal. Just install and add it to your dashboard to give it a try.<br>
</p>
<p>
The information displayed is based on the built-in Alfresco activity feeds. So no additionnal content model or service (such as the Audit service) needs to be activated, and the general performance of the Alfresco server is thus not decreased.<br>
</p>
<p>
You could however want to fine control the maximal size and duration of activity feeds. If so, please refer to section <b>Error! Reference source not found.</b> further in this document.<br>
</p>

# 2 Features #
## 2.1 Regular features ##
<p>
After installation, all Alfresco users have new available dashlet named <b>Activity Stats</b> to add to their personnal dashboard.<br>
</p>
The dashlet displays :
<ul>
<blockquote><li>The number of current user connections</li>
<li>The number of today¡¦s activities in user sites</li>
</ul>
<img src='http://alfea.googlecode.com/svn/wiki/images/Activity-Stats-Dashlet-User.png' /></blockquote>

<p>
The link Full report opens a full page showing activity summary for the user’s sites.<br>
</p>
This page displays:
<ul>
<blockquote><li>My sites activity timeline: the number of activities by type and site for the selected period<br>
</li>
<li>My sites activitiy overview: the pie chart of activities by site for the selected period<br>
</li>
</ul></blockquote>

## 2.2 Administrators features ##
<p>
Administrators will have a few additionnal features.<br>
</p>
<p>
On the Activity Stats dashlet, the action Email to the X connected users creates an email destinated to all connected users.<br>
</p>
![http://alfea.googlecode.com/svn/wiki/images/Activity-Stats-Dashlet-Admin.png](http://alfea.googlecode.com/svn/wiki/images/Activity-Stats-Dashlet-Admin.png)

<p>
The link Full report opens a full page showing activity summary for all sites, even those for which administrator is not member of.<br>
</p>
<img src='http://alfea.googlecode.com/svn/wiki/images/Activity-Stats-Timeline-Admin.png' width='800px' />

<img src='http://alfea.googlecode.com/svn/wiki/images/Activity-Stats-Overview-Admin.png' width='800px' />
# 3 Installation #
<a href='#Installation'></a>
## 3.1 System requirements ##
<ul>
<li>Actitivity Stats module is designed for Alfresco 3.4.x Enterprise or Community.</li>
<li>Actitivity Stats was tested on Alfresco 3.4.d Community.</li>
</ul>

<img src='http://alfea.googlecode.com/svn/wiki/images/Activity-Stats-Timeline-User.png' width='800px' />

<img src='http://alfea.googlecode.com/svn/wiki/images/Activity-Stats-Overview-User.png' width='800px' />

## 3.2 Install procedure ##
The procedure to install Activity Stats is the standard Alfresco procedure to install an AMP extension:

  1. Download the latest release from https://code.google.com/p/alfea/downloads/detail?name=Activity-Stats-1.0.zip&can=2&q=
  1. Copy **activity-stats.jar** to `<`ALFRESCO>/tomcat/shared/lib/
  1. Copy **activity-stats.amp** to `<`ALFRESCO>/amps
  1. Run the apply\_amps.bat (Windows) or apply\_amps.sh (Linux) script.Note that the “ALFRESCO\_HOME” environment variable should be configured correctly.
  1. Restart Alfresco server
<p>
After installation, a new dashlet is available in all users dashboard personalization.<br>
</p>
<img src='http://alfea.googlecode.com/svn/wiki/images/Activity-Stats-Dashlet-Selector.png' width='800px' />
# 4 Configuration #
<p>
The information displayed by Activity Stats module Is based on built-in activity feeds. Some Alfresco properties control the maximal size and duration of activity feeds.<br>
</p>
Default property values are quite low for activity reporting on a medium period:
```
# Activity feed max size and max age (eg. 44640 mins = 31 days)

activities.feed.max.size=100 
activities.feed.max.age.mins=44640
```

In order to change default values, simply override those 2 properties in '<'ALFRESCO>\tomcat\shared\classes\alfresco-global.properties
<p>
Note that later Alfresco releases (from 3.5.x branch) will enable the change of these parameters directly from the administrator console.<br>
</p>

# 5 Links #
  * Project home on Alfresco: http://code.google.com/p/alfea
  * Project home on ALFEA website: www.alfea-consulting.be
# 6 Licence #
This project is published under the terms of GPL (GNU Public Licence).

# Legend #
