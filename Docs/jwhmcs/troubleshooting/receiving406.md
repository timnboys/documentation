---
title: J!WHMCS Integrator - Troubleshooting: When rendering, I'm receiving a 406 error from the WHMCS API
breadcrumb: /jwhmcs:J!WHMCS Integrator/troubleshooting:Troubleshooting/receiving406:When rendering, I'm receiving a 406 error from the WHMCS API/
 
---

#### Problem:

When connecting from WHMCS to Joomla, the API is connecting fine in the backend of WHMCS without issues, all looks well.  However when viewing the rendered front end and the debug is enabled, the http code coming back is a 406 response code.

#### Explanation:

It seems that with mod_security enabled, a rule is being triggered that is blocking access to the Joomla site because a browser user-agent isn't passed along by default.

#### Solution:

1. Log into the backend of WHMCS and navigate to _Addons_ > _JWHMCS_ > _Settings_
2. Under the Advanced Settings tab, enable *Pass User Agent*
3. Save and view the front end.
