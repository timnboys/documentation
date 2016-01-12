---
title: Integrator 3 - New Installs
breadcrumb: /integrator3:Integrator 3/installupgrade_guide:Install and Upgrade Guide/newinstalls:New Installs

STYLE START
\#gitdox ol > li {
	clear: both;
	margin-bottom: 15px;
}

\#gitdox ol > li img {
	margin-bottom: 10px;
}

STYLE END

---

## Integrator 3: <small>Kayako Fusion Install</small>

### Download Integrator 3 for Kayako Fusion

1.  Log into our web site using your account credentials.  You may use either your email address and password or your username and password.
2.  Navigate to the *Downloads* link on the main menu and select the latest release of Integrator 3 for download.
3.  Select the file called *Complete Integrator 3 Archive* and save the file to your local computer.
4.  Navigate to the folder the archive was saved into and extract the contents of that folder into a convenient location.
5.  Wherever you extract the archive you should see five folders: Fusion, Integrator, Joomla, WHMCS and Wordpress

The folder `Fusion` contains the Integrator 3 for Kayako Fusion module files, and that is what this page will walk you through installing.  For instructions on installing the other connectors or the core app, please see the following:

* [Core Application](integrator3/installupgrade_guide/newinstalls.md)
* [Joomla! 3.x](integrator3/installupgrade_guide/newjoomla3.md)
* [WHMCS v6](integrator3/installupgrade_guide/newwhmcs6.md)
* [Wordpress 4](integrator3/installupgrade_guide/newwordpress4.md)

### Gather Requirements

To complete the installation of the Kayako Fusion plugin, you will need to have the following information:

* **FTP Credentials** - you will need to upload files to your server
* **Integrator 3 Access Details** - you will need an administrator account in Integrator 3 that has API access to the core application.  To find out about setting this up, please see [Creating an API Admin in Integrator 3](integrator3/howtoguides/createi3apiadmin.md).

### Installation Procedure

<div class="alert alert-danger"><strong>Backup Your Fusion Installation</strong><br />
There are a number of file changes that must be made to your core Fusion file because Fusion does not include enough hooks to perform the tasks necessary for integration to take place.  This means there are a few core changes to Kayako Fusion files that must be done in order for Integrator 3 to properly hook into the application.  It is highly recommended that you take a backup of your files prior to proceeding to minimize any downtime in the event of a problem.
</div>

Now you are ready to install Integrator 3 for Kayako Fusion.

#### File Uplaod and Module Activation

1. Navigate into the `Fusion` folder you extracted and extract the archive contained within it.  These are the plugin files, contained within the `__apps` folder.<div class="alert alert-info"><strong>Important Change in Fusion 4.50</strong><br />
As of Kayako Fusion v4.50, the __modules folder was renamed to __apps.  if you are installing into a version of Kayako Fusion earlier than 4.50, then be sure to rename the folder to `__modules` before proceding.
</div>
2. Upload the `__apps` folder to your Kayako Fusion root folder.
3. Log into your Kayako Fusion administration control panel.
4. Navigate to Options > Apps where you will see a list of all addon modules that are available for your Kayako Fusion application.
5. Find the addon module called *Integrator 3* and click on it's name.
6. Click on the Install button.

#### Retrieve Kayako Fusion API Keys

1. Log into your Kayako Fusion administration control panel.
2. Navigate to Options > REST API > Settings
3. Be sure *Enable API* is set to Yes - if not do so and click Update.
4. Navigate to Options > REST API > API Information
5. *COPY* the REST API Key and the Secret Key down into notepad or a text editor for the next step.

#### Create the Connection in Integrator 3

1. Log into your [Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md).
2. Click on the 'Configuration' drop down menu and select 'API Settings'.
3. You will now see a screen containing your API Secret Key.  *COPY* the API Secret Key and store it in a text editor - be sure to label it as not to confuse it with the API Secret Key from your Kayako Fusion application.
4. Click on the Connections drop down menu.  If you are able to add another connection to the Integrator 3 application, you will see 'Add New Connection', else you will need to purchase an additional connection for your license.
5. Select 'Kayako Fusion' from the dropdown menu and click 'Add Connection and Continue'.
6. You will see a form field at the bottom that says 'Connection ID' - *COPY* that Connection ID down as you will need it in the next section.
7. Fill in the fields below and press 'Save Changes' to store the values in place.  The rest of the settings can be left alone for now.

##### Connection Basics

* **Connection Name** - You can name the connection anything you prefer to use.
* **Connection URL** - This must be the URL to your Kayako Fusion help desk root, without any queries or template selections etc.

##### API Settings

* **API URL** - This should be identical to your Connection URL earlier - DO NOT include the `api/index.php?` in the URL, Integrator 3 will take care of that for you.
* **API Secret Value** - This should be what you copied down in 'Retrieve Kayako Fusion API Keys' earlier and is a really long string.
* **API Key** - Again, this is what you copied earlier and isn't quite as long a string as the Secret Value.
  

#### Addon Module Configuration

1. Log into your Kayako Fusion administration control panel.
2. Navigate to Options > Settings then click on Integrator.
3. Fill in the fields below and press 'Update' to connect your Kayako Fusion application to Integrator 3.
  * **Integrator URL** - This should be the fully qualified domain name to your Integrator 3 application.
  * **Integrator API Username** - This is the I3 API username you gathered earlier.
  * **Integrator API Password** - This is the I3 API password that you gathered earlier.
  * **API Secret Key** - This is the API Key that you copied down out of Integrator 3 in the section entitled 'Create the Connection in Integrator 3'.
  * **Integrator Connection ID** - This is the Connection ID you copied out of Integrator 3 in the section entitled 'Create the Connection in Integrator 3'.

### Kayako Fusion Core Modifications

Now you will need to edit some core Kayako Fusion files.  We try to check line numbers regularly as Kayako releases products, but we do miss some of them.  Please know these line numbers are not necessarily exact for your install, and you should gauge the location based on the fuction name the changes are made within as well as the lines before and after we provide.

* **[Kayako Fusion 4.30](integrator3/fusionfilechanges/430.md)**
* **[Kayako Fusion 4.40](integrator3/fusionfilechanges/440.md)**
* **[Kayako Fusion 4.50](integrator3/fusionfilechanges/450.md)**
* **[Kayako Fusion 4.52](integrator3/fusionfilechanges/452.md)**
* **[Kayako Fusion 4.55](integrator3/fusionfilechanges/455.md)**
* **[Kayako Fusion 4.61](integrator3/fusionfilechanges/461.md)**


### Next Steps

After you have installed Integrator 3 for Kayako Fusion into your site, you are now read to configure the product and install additional connectors.

##### Connector Installation

* [Core Application](integrator3/installupgrade_guide/newinstalls.md)
* [Joomla! 3.x](integrator3/installupgrade_guide/newjoomla3.md)
* [WHMCS v6](integrator3/installupgrade_guide/newwhmcs6.md)
* [Wordpress 4](integrator3/installupgrade_guide/newwordpress4.md)

##### Configuration and How-Tos

* [Access Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md)
* [Add or Change Your License](integrator3/howtoguides/licensechange.md)
* [Creating a New Language Translation](integrator3/howtoguides/createnewlanguage.md)
* [Remove index.php File from URL](integrator3/howtoguides/removeindexfile.md)