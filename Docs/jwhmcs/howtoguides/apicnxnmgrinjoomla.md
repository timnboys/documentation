---
title: J!WHMCS Integrator - How To Guide: Using the API Connection Manager in Joomla!
breadcrumb: /jwhmcs:J!WHMCS Integrator/howtoguides:How To Guides/apicnxnmgrinjoomla:Using the API Connection Manager in Joomla!/

---


The API Connection Manager in Joomla is an easy to use, intuitive feature of J!WHMCS Integrator allowing you to quickly setup and diagnose your API connection between Joomla and WHMCS.

h1. Accessing the API Connection Manager

To access the API Connection Manager, follow these steps:

# Log into your Joomla backend using an account with Super User privileges.
# Navigate to Components > J!WHMCS Integrator.
# Click on the API Connection button on the main screen.

h1. Configuring the API

After the initial installation of the product, all the fields will be blank.  You will want to fill out the form in it's entirety.

||WHMCS URL||This is the complete URL to the FRONT END of your WHMCS installation.  Note that you should not include the API path or point to the admin folder.|
||API Username||This is a username for an account in WHMCS that has API Access.  Please check [Create An API User in WHMCS] for more information.|
||API Password||This is the password for the aforementioned account.|
||API Access Key||The API Access Key is entirely optional and may be setup in WHMCS in place of using the IP Address restriction.  For more information, please check [Granting API Access to WHMCS]|

h1. API Responses

As you enter data into the API Connection Manager in Joomla!, the system will make a call to test the values out.  You will be notified at each step of the way the results of your data entry.  The most common responses are as follows:

||Successfully Connected||This indicates the J!WHMCS Integrator was able to communicate with WHMCS as expected with the settings provided|
||0 Received||This is always a firewall issue.  If you enter a URL into the field and receive a zero response, then your server has either blacklisted itself or is not permitting access through the firewall for another reason.  Please consult your hosting provider for more information on troubleshooting this issue.|
||403 Restricted||If this is encountered, you may have an .htaccess file in place blocking access to your WHMCS installation.|
||404 Not Found||Just as it suggests, the URL you entered isn't found - you may want to double check it|
||Authentication Failed||If you receive this message then you should double check your API Username and Password you have entered.  If you are using unusual characters in either, you may want to try changing them in WHMCS to not rely on symbols as certain symbols have been known to not authenticate in WHMCS properly.  Follow the guide [Create An API User in WHMCS] to correct this.|
||Invalid IP x.y.z.n||This indicates that the IP address listed has not been given API access to the WHMCS system.  Follow the guide [Granting API Access to WHMCS] to correct this.|
||Invalid Access Key||This indicates that the value you entered for the API Access Key does not match what WHMCS has in it's configuration.php file.  Follow the guide [Granting API Access to WHMCS] to correct this.|
