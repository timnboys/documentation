---
title: Common Tasks: Granting API Access to WHMCS 
breadcrumb: /common:Common Tasks/grantapiaccess:Granting API Access to WHMCS/
 
---


Be default, WHMCS is installed without the ability to access the WHMCS API, even if you have a user account that has API Access granted to it.  To open up access, you have two options, please follow the easiest option for you.

### IP Address Access (simplest)

If you receive an error message when connecting to the API interface indicating that WHMCS is reporting an Invalid IP Address, then you should look at this section to correct it.  The IP address in question is not your IP address, but rather it is the IP Address the SERVER is using.  This may also be complicated if you have an SSL certificate using one IP address and another IP address for non-SSL usage.  Be sure if you are using SSL and non-SSL to add both IP addresses in place just in case.  To add an IP Address to the Access List, follow these steps:

1. Log into the administrative back end of your WHMCS application using your highest level admin account.
2. Navigate to Setup > General Settings.
3. Click on the Security Tab.
4. Locate the API IP Access Restriction Field towards the bottom of the page.<br />
Version 5.2 and above:  Click on Add IP and enter the IP address you wish to add along with a quick note like 'Server' or 'Joomla' for future reference<br />
Version 5.1 and below:  Enter the IP address into the text box on it's own line.
5. Click on Save Changes

You now have added your IP Address(es) to the API Access list to permit J!WHMCS Integrator to communicate with WHMCS properly.  For more information on API Access, please consult [http://docs.whmcs.com/API](http://docs.whmcs.com/API)

### API Access Key

If your site is cloud based (ie the IP floats) or you change your IP address alot (for some other reason) then you will want to setup the API Access Key.  To do this, follow these steps:

1. Using an FTP program, download your WHMCS configuration.php file.  This file is located in the root of your WHMCS application.
2. Edit the configuration.php file using notepad, notepad++, TextPad, etc.
3. Towards the bottom you will see a closing PHP tag, it looks like a question mark and a greater than sign:

    ?>


4. On the line above this closing tag, add a new line by hitting return.
5. On the blank line, enter the following:

    $api_access_key = 'YoUrS3Cure';

** Note to please use some other access key than the above - it is used for demonstration purposes ;)
6. Save the configuration.php file
7. Upload the file back to your WHMCS root folder on your server.

You have now added an Access Key to your WHMCS configuration file.  For more information on adding an access key, please consult [http://docs.whmcs.com/API:Access_Keys](http://docs.whmcs.com/API:Access_Keys)
