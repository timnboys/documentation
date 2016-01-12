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

The folder `Integrator` is the core application, and that is what this page will walk you through installing.  For instructions on installing the individual connectors, please see the following:

* [Kayako Fusion](integrator3/installupgrade_guide/newfusion.md)
* [Joomla! 3.x](integrator3/installupgrade_guide/newjoomla3.md)
* [WHMCS v6](integrator3/installupgrade_guide/newwhmcs6.md)
* [Wordpress 4](integrator3/installupgrade_guide/newwordpress4.md)


### Gather Requirements

To complete the installation of the core application, you will need to have the following information:

* **FTP Credentials** - you will need to upload files to your server
* **Database Connection** - you will need to have either a clean database or an existing database with a username and password to access it.
* **Integrator 3 License** - you should have been emailed a copy of your Integrator 3 license, if not you can log into our [Client Portal|https://client.gohigheris.com/clientarea.php] to retrieve it.
* **Folder Location** - you will want to install the core application into a folder that is friendly for your visitors as they may see the folder in the URL when they log in or when they register.

<div class="alert alert-warning"><strong>Recommended Folder Name</strong><br />
We recommend a folder name of `accounts` or `my` or something generic to use.  We do not recommend using `integrator` as your installation folder, particularly if you are installing Integrator 3 as a subfolder of a Joomla! installation - this will cause problems when you install the Joomla! component.
</div>

### Upload Files

Now you are ready to install Integrator 3.

1. Navigate into the Integrator folder you extracted and extract the archive contained within it.  These are the core files.
2. FTP the core files to your server in the Folder Location you determined above.
3. {japopup type="image" content="media/gitdocs/integrator3/installupgrade_guide/assets/install-coreapp-1.png" width="1247" height="1032" title="Terms of Service"}<img src="assets/install-coreapp-1.png" width="100px" align="right" />{/japopup}
In a browser, navigate to the installation folder.  For example, if you uploaded the files to a subfolder called `accounts`, navigate to http://yourdomain.com/accounts.  You should be shown a screen similar to the one to the right.  Once you arive at that screen, accept the Terms of Service to proceed.
4. {japopup type="image" content="media/gitdocs/integrator3/installupgrade_guide/assets/install-coreapp-2.png" width="1247" height="1032" title="Database Credentials"}<img src="assets/install-coreapp-2.png" width="100px" align="right" />{/japopup}
The next step is the database configuration.  Enter the credentials for your database, as you do the system will check the credentials on the fly to let you know if you can proceed or not.  If it checks out, press the Proceed to Requirements Check.


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
