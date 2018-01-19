---
title: C!Blesta - New Installations
breadcrumb: /cblesta:C!Blesta/install_upgrade_guide:New Installations/

---

### First Steps

Before proceeding with any portion of the installation of C!Blesta, please be sure to perform the following *First Steps*.

#### Gather Prerequisite Items

The following are required to have on hand prior to installing C!Blesta

* C!Blesta license key (accessed through your [Client Portal|https://portal.cubedata.net/] on our web site)
* Latest release of Dunamis Framework (minimum version 1.3.0)
* Latest release of C!Blesta consisting of the following archive files:
<ul><li>com_cblesta_v{x.y.z}.zip - This is the CMS! archive for installation into the ModX/Concrete5/Joomla! platform.</li>
<li>cblesta_for_blesta_v{x.y.z}.zip - This is the Blesta archive containing the plugin for Blesta</li></ul>

#### Locate Your FTP Credentials

For the Blesta portion of the product installation, you will need to have FTP access to upload files to your Blesta application.  Please consult your hosting provider for more information on locating your FTP credentials.

#### Read Through The Installation Documentation

Be sure to read through the documentation to see how installation is to be done.  C!Blesta is unlike most products and requires an attention to detail

### Upload C!Blesta for Blesta

1. Extract the *cblesta_for_blesta_v{x.y.z}.zip* file to a folder on your local computer.  Contained within this archive are many files within a single folder called _plugins_.
2. Using your favorite FTP program, upload the _plugins_ folder to your Blesta application.  You will notice that you have a _plugins_ folder already in place on your server where Blesta is installed.  This is normal and expected.
3. Once the files have completely uploaded, log into the administrative back end of Blesta using an account with sufficient privileges to activate and configure plugins for your company.
4. From the Blesta Admin Home Screen, click on _Settings_ on the top right side.
5. Next click on _Plugins_ located under the _Company_ tab.
6. Next click on _Available_ beneath the Plugins heading on the left hand navigation bar.
7. Locate the _Dunamis Framework_ plugin in the list that comes up and click the _Install_ button.  *This must be done before installing C!Blesta!*
8. The Dunamis Framework for Blesta should now be installed on your system.
9. Next click on _Available_ beneath the Plugins heading on the left hand navigation bar.
10. Locate the C!Blesta plugin in the list that comes up and click the _Install_ button.

### Install C!Blesta Archive into ModX/Concrete5/Joomla!

1. Locate the *com_cblesta_v{x.y.z}.zip* file that you downloaded from our site.  This one file contains the C!Blesta component, the authentication, system and user plugins as well as the Dunamis Library and component required for C!Blesta to operate in ModX/Concrete5/Joomla!.
2. Log into your Joomla backend using an account with Super User privileges.
3. Navigate to _Extensions_ > _Extension Manager_.
4. Under the_ Upload Package_ _File_ section click on the _Browse_ button and locate the com_cblesta_v{x.y.z}.zip file you located in step 1.
5. Click on _Upload and Install_.
6. Joomla/ModX/Concrete5 will now install and activate the Dunamis library, Dunamis component, C!Blesta component, Authentication - C!Blesta, System - C!Blesta and User - C!Blesta plugins.

### Next Steps

After you have installed the product into your site, you are now read to configure the product.  Configuration must be done before your ModX/Concrete5/Joomla and Blesta installations will work together.

* [Create An API User in Blesta]
* [Add or Change Your C!Blesta License|Add or Change Your License]
* [API Connection Manager in ModX/Concrete5/Joomla](https://docs.cubedata.net/docs/cblesta/API+Connection+Manager+in+Joomla)
