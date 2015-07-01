---
title: J!WHMCS Integrator - How To Guide: Creating An API User in WHMCS
breadcrumb: /jwhmcs:J!WHMCS Integrator/howtoguides:How To Guides/createapiuser:Creating An API User in WHMCS/
 
---

After following this tutorial you will have setup an API user in WHMCS for connecting with.

### Setting Up An API User Role

If you have never configured an API user in WHMCS, be sure to follow these steps:

1. Log into the administrative back end of your WHMCS application using your highest level admin account.
2. Navigate to Setup > Staff Management > Administrator Roles
3. Click on Add New Role Group
4. Call the new role group `API Administrators` for easy reference in the future and click Continue.
5. On the permissions page (the page with a million little check boxes) locate API Access in the bottom right hand side and click it.  Be sure it is the ONLY box you click and hit Save Changes

You have now setup an API User Role group called API Administrators.

### Setting Up An API User Account

Be sure you have an API User Role setup above and continue with these steps:

1. Log into the administrative back end of your WHMCS application using your highest level admin account.
2. Navigate to Setup > Staff Management > Administrator Users
3. Click on Add New Administrator
4. For the Administrator Role, select the API Administrators group you created earlier.
5. Complete the rest of the form as follows (note that you may use any values, but for this tutorial and reference we will use these values):
* First Name:  API
* Last Name:  Admin (jwhmcs)
* Email Address:  apiadmin@yourdomain.com
* Username:  apiadmin
* Password:  PASSWORD ** Note to use something else... ;)
6. Click Save Changes

You have now setup an API User Account in WHMCS
