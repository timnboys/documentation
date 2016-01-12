---
title: Integrator 3 for Wordpress - New Installation 
breadcrumb: /integrator3:Integrator 3/installupgrade_guide:Install and Upgrade Guide/newwordpress:New Wordpress Installation

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

## Integrator 3: <small>Wordpress Install</small>

### Download Integrator 3 for Wordpress

1.  Log into our web site using your account credentials.  You may use either your email address and password or your username and password.
2.  Navigate to the *Downloads* link on the main menu and select the latest release of Integrator 3 for download.
3.  Select the file called *Complete Integrator 3 Archive* and save the file to your local computer.
4.  Navigate to the folder the archive was saved into and extract the contents of that folder into a convenient location.
5.  Wherever you extract the archive you should see five folders: Fusion, Integrator, Joomla, WHMCS and Wordpress

The folder `Wordpress` contains the Integrator 3 for Wordpress plugin files, and that is what this page will walk you through installing.  For instructions on installing the other connectors or the core app, please see the following:

* [Core Application](integrator3/installupgrade_guide/newinstalls.md)
* [Kayako Fusion](integrator3/installupgrade_guide/newfusion.md)
* [Joomla! 3.x](integrator3/installupgrade_guide/newjoomla3.md)
* [WHMCS v6](integrator3/installupgrade_guide/newwhmcs6.md)

### Gather Requirements

To complete the installation of the Kayako Fusion plugin, you will need to have the following information:

* **FTP Credentials** - you will need to upload files to your server
* **Integrator 3 Access Details** - you will need an administrator account in Integrator 3 that has API access to the core application.  To find out about setting this up, please see [Creating an API Admin in Integrator 3](integrator3/howtoguides/createi3apiadmin.md).

### Installation Procedure

Now you are ready to install Integrator 3 for Wordpress.

#### File Uplaod and Module Activation

1. Navigate into the `Wordpress` folder you extracted earlier and extract the archive contained within it.  These are the plugin files, contained within the `wp-content` folder.
2. Upload the `wp-content` folder to your Wordpress root folder.
3. Log into your Wordpress administration control panel.
4. Click on *Plugins* on the left side where you will be taken to the Plugins page showing you the installed and available plugins for your Wordpress site.
5. Find Integrator 3 in the list of plugins and click on Activate beneath the Integrator 3 plugin name.

The Wordpress plugin for Integrator 3 should now be activated and ready to be configured!

#### Creating an API User in Wordpress

<div class="alert alert-warning"><strong>Protect This Account</strong>
In order to permit the integration to take place between your Wordpress site and Integrator 3, it is necessary to add an administrator to your Wordpress user manager.  This user would have the same level of access to your Wordpress site as you do, so it is important not to lose the password for this account or give it to anyone else.
</div>

1. Log into your Wordpress administration control panel
2. Navigate to *Users* > *Add New* and complete the form as follows:
  * **Username:** apiadmin
  * **Email:** apiadmin@yourdomain.com
  * **First Name:** API
  * **Last Name:** Administrator
  * **Password:** Enter a password
  * **Password 2:** enter the same password
  * **Role:** Administrator
3. Click on *Add New User* to complete the user form.

#### Create the Connection in Integrator 3

1. Log into your [Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md).
2. Click on the *Configuration* drop down menu and select *API Settings*.
3. You will now see a screen containing your API Secret Key.  *COPY* the API Secret Key and store it in a text editor.
4. Click on the Connections drop down menu.  If you are able to add another connection to the Integrator 3 application, you will see *Add New Connection*, else you will need to purchase an additional connection for your license.
5. Select *Wordpress* from the dropdown menu and click *Add Connection and Continue*.
6. You will see a form field at the bottom that says 'Connection ID' - *COPY* that Connection ID down as you will need it in the next section.
7. Fill in the fields below and press *Save Changes* to store the values in place.  The rest of the settings can be left alone for now.

##### Connection Basics

* **Connection Name** - You can name the connection anything you prefer to use.
* **Connection URL** - This must be the URL to your Wordpress site, without any queries or template selections etc.

##### API Settings

* **API URL** - This should be identical to your Connection URL earlier.
* **API Username** - This should be the username of the API User you created in Wordpress earlier (in our example we used *apiadmin*).
* **API Password** - Again, this is what you created earlier for the API User.
  

#### Wordpress Plugin Configuration

1. Log into your Wordpress administration control panel.
2. Navigate to *Settings* > *Integrator*.
3. Fill in the fields below and press 'Save Settings' to connect your Wordpress site to Integrator 3.
  * **Integrator URL** - This should be the fully qualified domain name to your Integrator 3 application.
  * **Integrator API Username** - This is the I3 API username you gathered earlier.
  * **Integrator API Password** - This is the I3 API password that you gathered earlier.
  * **API Secret Key** - This is the API Key that you copied down out of Integrator 3 in the section entitled 'Create the Connection in Integrator 3'.
  * **Integrator Connection ID** - This is the Connection ID you copied out of Integrator 3 in the section entitled 'Create the Connection in Integrator 3'.

### Next Steps

After you have installed Integrator 3 for Wordpress into your site, you are now read to configure the product and install additional connectors.

##### Connector Installation

* [Core Application](integrator3/installupgrade_guide/newinstalls.md)
* [Joomla! 3.x](integrator3/installupgrade_guide/newjoomla3.md)
* [Kayako Fusion](integrator3/installupgrade_guide/newfusion.md)
* [WHMCS v6](integrator3/installupgrade_guide/newwhmcs6.md)

##### Configuration and How-Tos

* [Access Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md)
* [Add or Change Your License](integrator3/howtoguides/licensechange.md)
* [Creating a New Language Translation](integrator3/howtoguides/createnewlanguage.md)
* [Remove index.php File from URL](integrator3/howtoguides/removeindexfile.md)