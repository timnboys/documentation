---
title: J!Blesta - New Installations
breadcrumb: /jblesta:J!Blesta/install_upgrade_guide:New Installations/

---

### First Steps

Before proceeding with any portion of the installation of J!Blesta, please be sure to perform the following *First Steps*.

#### Gather Prerequisite Items

The following are required to have on hand prior to installing J!Blesta

* J!Blesta license key (accessed through your [Client Portal|https://client.gohigheris.com/clientarea.php] on our web site)
* Latest release of Dunamis Framework (minimum version 1.3.0)
* Latest release of J!Blesta consisting of the following archive files:
<ul><li>com_jblesta_v{x.y.z}.zip - This is the Joomla! archive for installation into the Joomla! platform.</li>
<li>jblesta_for_blesta_v{x.y.z}.zip - This is the Blesta archive containing the plugin for Blesta</li></ul>

#### Locate Your FTP Credentials

For the Blesta portion of the product installation, you will need to have FTP access to upload files to your Blesta application.  Please consult your hosting provider for more information on locating your FTP credentials.

#### Read Through The Installation Documentation

Be sure to read through the documentation to see how installation is to be done.  J!Blesta is unlike most products and requires an attention to detail

### Upload J!Blesta for Blesta

1. Extract the *jblesta_for_blesta_v{x.y.z}.zip* file to a folder on your local computer.  Contained within this archive are many files within a single folder called _plugins_.
2. Using your favorite FTP program, upload the _plugins_ folder to your Blesta application.  You will notice that you have a _plugins_ folder already in place on your server where Blesta is installed.  This is normal and expected.
3. Once the files have completely uploaded, log into the administrative back end of Blesta using an account with sufficient privileges to activate and configure plugins for your company.
4. From the Blesta Admin Home Screen, click on _Settings_ on the top right side.
5. Next click on _Plugins_ located under the _Company_ tab.
6. Next click on _Available_ beneath the Plugins heading on the left hand navigation bar.
7. Locate the _Dunamis Framework_ plugin in the list that comes up and click the _Install_ button.  *This must be done before installing J!Blesta!*
8. The Dunamis Framework for Blesta should now be installed on your system.
9. Next click on _Available_ beneath the Plugins heading on the left hand navigation bar.
10. Locate the J!Blesta plugin in the list that comes up and click the _Install_ button.

### Install J!Blesta Archive into Joomla!

1. Locate the *com_jblesta_v{x.y.z}.zip* file that you downloaded from our site.  This one file contains the J!Blesta component, the authentication, system and user plugins as well as the Dunamis Library and component required for J!Blesta to operate in Joomla!.
2. Log into your Joomla backend using an account with Super User privileges.
3. Navigate to _Extensions_ > _Extension Manager_.
4. Under the_ Upload Package_ _File_ section click on the _Browse_ button and locate the com_jblesta_v{x.y.z}.zip file you located in step 1.
5. Click on _Upload and Install_.
6. Joomla will now install and activate the Dunamis library, Dunamis component, J!Blesta component, Authentication - J!Blesta, System - J!Blesta and User - J!Blesta plugins.

### Next Steps

After you have installed the product into your site, you are now read to configure the product.  Configuration must be done before your Joomla and Blesta installations will work together.

* [Create An API User in Blesta]
* [Add or Change Your J!Blesta License|Add or Change Your License]
* [API Connection Manager in Joomla](https://support.gohigheris.com/docs/display/J25/API+Connection+Manager+in+Joomla)
