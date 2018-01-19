---
title: C!Blesta - Troubleshooting: When rendering, I'm receiving a 406 error from the Blesta API
breadcrumb: /cblesta:C!Blesta/troubleshooting:Troubleshooting/receiving406:When rendering, I'm receiving a 406 error from the Blesta API/
 
---

#### Problem:

When connecting from Blesta to Modx/Concrete5/Joomla, the API is connecting fine in the backend of Blesta without issues, all looks well.  However when viewing the rendered front end and the debug is enabled, the http code coming back is a 406 response code.

#### Explanation:

It seems that with mod_security enabled, a rule is being triggered that is blocking access to the Modx/Concrete5/Joomla site because a browser user-agent isn't passed along by default.

#### Solution:

1. Log into the administrative back end of your Blesta application using an account with access to the C!Blesta plugin.
2. Navigate to Settings > Installed Plugins and select Manage next to C!Blesta
3. Under the Advanced Settings tab, enable *Pass User Agent*
4. Save and view the front end.
