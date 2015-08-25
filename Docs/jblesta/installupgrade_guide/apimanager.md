---
title: J!Blesta - Using the API Connection Manager
breadcrumb: /jblesta:J!Blesta/installupgrade_guide:Install and Upgrade Guide/apimanager:Using the API Connection Manager/

---

### Using the API Connection Manager

The API Connection Manager in Joomla is an easy to use, intuitive feature of J!Blesta allowing you to quickly setup and diagnose your API connection between Joomla and Blesta.

### Accessing the API Connection Manager

To access the API Connection Manager, follow these steps:

1. Log into your Joomla backend using an account with Super User privileges.
2. Navigate to _Components_ > _J!Blesta_.
3. Click on the _API Connection_ button on the main screen.

### Configuring the API

After the initial installation of the product, all the fields will be blank.  You will want to fill out the form in it's entirety.

||Blesta URL||This is the complete URL to the FRONT END of your Blesta installation.  Note that you should not include the API end point or point to the admin folder.|
||API Username||This is a username for an account in Blesta that has API Access.  Please check [Create An API User in Blesta|Create An API User in Blesta] for more information.|
||API Key||This is the key that is generated for the API user you entered above.|

### API Responses

As you enter data into the API Connection Manager in Joomla!, the system will make a call to test the values out.  You will be notified at each step of the way the results of your data entry.  The most common responses are as follows:

||Successfully Connected||This indicates that J!Blesta was able to communicate with Blesta as expected with the settings provided|
||0 Received||This is always a firewall issue.  If you enter a URL into the field and receive a zero response, then your server has either blacklisted itself or is not permitting access through the firewall for another reason.  Please consult your hosting provider for more information on troubleshooting this issue.|
||401 Denied||The API Username and API Key don't match up with your settings in Blesta.  Double check them and try again.|
||403 Restricted||If this is encountered, you may have restrictions added to your .htaccess file in your Blesta installation folder.|
||404 Not Found||Just as it suggests, the URL you entered isn't found - you may want to double check it|
