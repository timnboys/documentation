---
title: C!Blesta - How To Guide: Setup the Shared API Token
breadcrumb: /cblesta:C!Blesta/howtoguides:How To Guides/setupsharedapitoken:Setup the Shared API Token/
 
---

C!Blesta introduces the concept of a shared API token.  This token is used on both ModX/Concrete5 and Blesta to securely pass data back and forth without the need to setup different ModX/Concrete5 users, user groups or provide permissions to users to access API features.

### Setting Up The Shared Token in Blesta

To setup the shared token in Blesta, follow these steps:

1. Log into the back end of your Blesta application using an Administrator level account.
2. If you are installing the product at this time, click on Settings > Available Plugins and then click on Install.  If you have already installed the product and need to access the settings, click on to Settings > Available Plugins
3. Click on Manage next to the C!Blesta plugin
4. Click on the Settings link in the navigation row for C!Blesta.
5. Locate the Login Token field under the General Settings section.
7. Enter a secure, unique token here.
8. Click Submit

C!Blesta will update your configuration with the new token.  You should receive a confirmation indicating your settings have been saved.

### Setting Up The Shared Token in ModX/Concrete5

To setup the shared token in ModX/Concrete5, follow these steps:

1. Log into your ModX/Concrete5 backend using an account with Super User privileges.
2. Navigate to Components > C!Blesta
3. Click on the Options button.
4. Locate the API Token field under the General parameters section.
5. Enter the same secure, unique token you used in Blesta into this field.
6. Click Save and Close

You should now have established the API bridge between Blesta and ModX/Concrete5.

### Verifying Connectivity

To verify that you have established the connection properly from Blesta, follow these steps:

1. Log into the back end of your Blesta application using an Administrator level account.
2. If you are installing the product at this time, click on Settings > Available Plugins and then click on Install.  If you have already installed the product and need to access the settings, click on to Settings > Available Plugins
3. Click on Manage next to the C!Blesta plugin
4. Click on the System Check link beneath the C!Blesta logo.
5. In the top section labelled API Check, see if you have any errors indicated.   If everything is checked you are good to go!
