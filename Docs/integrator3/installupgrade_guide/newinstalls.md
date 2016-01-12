---
title: Integrator 3 - New Installs
breadcrumb: /integrator3:Integrator 3/installupgrade_guide:Install and Upgrade Guide/newinstalls:New Installs
 
---

## Integrator 3: <small>New Installs</small>

Before proceeding with any portion of the installation of Integrator 3, please be sure to read the documentation in their entirety.

### Download Integrator 3

1.  Log into our web site using your account credentials.  You may use either your email address and password or your username and password.
2.  Navigate to the *Downloads* link on the main menu and select the latest release of Integrator 3 for download.
3.  Select the file called *Complete Integrator 3 Archive* and save the file to your local computer.
4.  Navigate to the folder the archive was saved into and extract the contents of that folder into a convenient location.
5.  Wherever you extract the archive you should see five folders: Fusion, Integrator, Joomla, WHMCS and Wordpress
6.  Navigate into the Integrator folder you just extracted.  You will see another archive - extract that file - this is the core application.

The core application is what you will be working with for the rest of this page.

For instructions on installing the individual connectors, please see the following:

* [Kayako Fusion](integrator3/installupgrade_guide/newfusion.md)
* [Joomla! 3.x](integrator3/installupgrade_guide/newjoomla3.md)
* [WHMCS v6](integrator3/installupgrade_guide/newwhmcs6.md)
* [Wordpress 4](integrator3/installupgrade_guide/newwordpress4.md)


### Gather Requirements

To complete the installation of the core application, you will need to have the following information:

* FTP Credentials - you will need to upload files to your server
* Database Connection - you will need to have either a clean database or an existing database with a username and password to access it.
* Integrator 3 License - you should have been emailed a copy of your Integrator 3 license, if not you can log into our site and access it there.
* Folder Location - you will want to install the core application into a folder that is friendly for your visitors as they may see the folder in the URL when they log in or when they register.

<div class="alert alert-warning"><strong>Recommended Folder Name</strong><br />
We recommend a folder name of `accounts` or `my` or something generic to use.  We do not recommend using `integrator` as your installation folder, particularly if you are installing Integrator 3 as a subfolder of a Joomla! installation - this will cause problems when you install the Joomla! component.
</div>


The following are required to have on hand prior to installing J!WHMCS Integrator

* J!WHMCS Integrator license key (accessed through your [Client Portal|https://client.gohigheris.com/clientarea.php] on our web site)
* Latest release of Dunamis Framework (minimum version 1.4.0)
* Latest release of J!WHMCS Integrator archive

#### Locate Your FTP Credentials

For the WHMCS portion of the product installation, you will need to have FTP access to upload files to your WHMCS application.  Please consult your hosting provider for more information on locating your FTP credentials.

#### Read Through The Installation Documentation

Before jumping to conclusions on how the product "should" be installed, be sure to read through the documentation to see how it actually is supposed to be done.  Previous versions of J!WHMCS Integrator included an automatic installation procedure that loaded everything into place for you.  The new version has been incredibly simplified and as such, does not have the ability to automatically install the WHMCS portion of the files into place.

### Upload and Activate Dunamis Framework for WHMCS

1. If you have not already done so, download the latest release of the [Dunamis Framework for WHMCS here|https://www.gohigheris.com/customer-downloads/dunamis-framework] (you must be signed in to do so).
2. Extract the *dunamis_whmcs_v{x.y.z}.zip* file to a folder on your local computer.  Contained within this archive are many files within two folders, an includes folder and a modules folder.
3. Using your favorite FTP program, upload the includes and modules folders to your WHMCS application.  You will notice that you have an includes and a modules folder already in place on your server where WHMCS is installed.  This is normal and expected.
4. Once the files have completely uploaded, log into the administrative back end of WHMCS using an account with sufficient privileges to activate and configure addon modules.
5. From the WHMCS Admin Home Screen, navigate to _Setup_ > _Addon Modules_.
6. Locate the _Dunamis Framework_ addon module in the list and click the _Activate_ button.
7. Once activated, click on the _Configure_ button and give your administrative account privileges to access the module.

### Upload J!WHMCS Integrator Addon Module for WHMCS

1. Extract the *jwhmcs_for_whmcs_v{x.y.z}.zip* file to a folder on your local computer.  Contained within this archive are many files within a single folder called modules.
2. Using your favorite FTP program, upload the modules folder to your WHMCS application.  You will notice that you have a modules folder already in place on your server where WHMCS is installed.  This is normal and expected.
3. Once the files have completely uploaded, log into the administrative back end of WHMCS using an account with sufficient privileges to activate and configure addon modules.
4. From the WHMCS Admin Home Screen, navigate to _Setup_ > _Addon Modules_.
5. Locate the _J!WHMCS Integrator_ addon module in the list and click the _Activate_ button.
6. Once activated, click on the _Configure_ button and give your administrative account privileges to access the module.

### Install J!WHMCS Integrator Archive into Joomla!

1. Locate the *com_jwhmcs_v{x.y.z}.zip* file that you downloaded from our site.  This one file contains the J!WHMCS component, the authentication, system and user plugins as well as the Dunamis Library and component required for J!WHMCS Integrator v2.5 to operate in Joomla.
2. Log into your Joomla backend using an account with Super User privileges.
3. Navigate to _Extensions_ > _Extension Manager_.
4. Under the_ Upload Package_ _File_ section click on the _Browse_ button and locate the com_jwhmcs_v{x.y.z}.zip file you located in step 1.
5. Click on _Upload and Install_.
6. Joomla will now install and activate the Dunamis library, Dunamis component, J!WHMCS Integrator component, Authentication - JWHMCS, System - JWHMCS and User - JWHMCS plugins.

### Next Steps

After you have installed the product into your site, you are now read to configure the product.  Configuration must be done before your Joomla and WHMCS installations will work together.

* [Add or Change Your J!WHMCS License](Add or Change Your License)
* [Configuration Walk Through](http://)
* [Setup The Shared API Token](Setup the Shared API Token)
* [API Connection Manager in Joomla](https://support.gohigheris.com/docs/display/J25/API+Connection+Manager+in+Joomla)
