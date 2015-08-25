---
title: J!Blesta - How To Guide: Enable and Access Debug Mode in J!Blesta
breadcrumb: /jblesta:J!Blesta/howtoguides:How To Guides/enabledebugmode:Enable and Access Debug Mode in J!Blesta/
 
---


The debug feature in J!Blesta provides for simple diagnostics for the interface with J!Blesta.  Enabling debug however is not necessarily intuitive, so to do so, please follow these steps.
<!--
### Enable Debug in Blesta

To enable debugging on the Blesta side of things, follow these steps:

1. Log into your Blesta Admin area using an account that has access to the J!Blesta addon module settings.
2. Navigate to Addons > J!Blesta > Settings
3. On the General Settings tab, click on the Debug toggle so that it is enabled<br />
{japopup type="image" content="media/gitdocs/jblesta/howtoguides/assets/debug-01.png" width="1130" height="760" title="Debug Mode in Blesta"}
<img src="assets/debug-01.png" width="100px" />{/japopup}
4. Hit Save

That should enable debug on Blesta for J!Blesta
-->
### Enable Debug in Joomla

Enabling debugging on the Joomla side is also required if you want to troubleshoot any visual integration issues (for example if the site isn't wrapping properly or a module isn't appearing as expected).  To enable it, follow these steps:

1. Log into your Joomla administrator area using an account that has access to the J!Blesta parameters (typically a super user account).
2. Navigate to Components > J!Blesta and click on the Options button on the top navigation bar for the component.
3. Once in there, find the Debug option on the General tab and click on Yes<br />
{japopup type="image" content="media/gitdocs/jblesta/howtoguides/assets/debug-02.png" width="1130" height="780" title="Debug Mode in Joomla!"}
<img src="assets/debug-02.png" width="100px" />{/japopup}
4. Hit Save and Close

Your J!Blesta is now in debug mode on Joomla.

### Important Note

Be sure to disable the debug mode when you are done to prevent the public from accessing it or seeing debug messages on the front end of your site.
