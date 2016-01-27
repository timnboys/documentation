---
title: Integrator 3 for WHMCS - New Installation 
breadcrumb: /integrator3:Integrator 3/installupgrade_guide:Install and Upgrade Guide/newwhmcs6:New WHMCS Installation

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

## Integrator 3: <small>WHMCS Install</small>

### Download Integrator 3 for WHMCS

1.  Log into our web site using your account credentials.  You may use either your email address and password or your username and password.
2.  Navigate to the *Downloads* link on the main menu and select the latest release of Integrator 3 for download.
3.  Select the file called *Complete Integrator 3 Archive* and save the file to your local computer.
4.  Navigate to the folder the archive was saved into and extract the contents of that folder into a convenient location.
5.  Wherever you extract the archive you should see five folders: Fusion, Integrator, Joomla, WHMCS and Wordpress

The folder `WHMCs` contains the Integrator 3 for WHMCS plugin files, and that is what this page will walk you through installing.  For instructions on installing the other connectors or the core app, please see the following:

* [Core Application](integrator3/installupgrade_guide/newinstalls.md)
* [Joomla](integrator3/installupgrade_guide/newjoomla3.md)
* [Kayako Fusion](integrator3/installupgrade_guide/newfusion.md)
* [Wordpress](integrator3/installupgrade_guide/newwordpress4.md)

### Gather Requirements

To complete the installation of the Integrator 3 for WHMCS addon, you will need to have the following information:

* **FTP Credentials** - you will need to upload files to your server
* **Integrator 3 Access Details** - you will need an administrator account in Integrator 3 that has API access to the core application.  To find out about setting this up, please see [Creating an API Admin in Integrator 3](integrator3/howtoguides/createi3apiadmin.md).
* **WHMCS Administration Credentials** - you will need to access the backend of WHMCS to install the Integrator 3 for WHMCS.

### Installation Procedure

Now you are ready to install Integrator 3 for WHMCs.

#### WHMCS Addon Installation

1. Navigate into the `WHMCS` folder you extracted earlier and extract the archive file it contains.  There are two folders, `includes` and `modules` which contain WHMCS addon you will need for installation.
2. Upload the two folders to the root directory of your WHMCS application.
3. Log into your WHMCS administration control panel.
4. On the main menu navigate to *WHMCS* and click on *Addon Modules*
5. <span class="label label-danger">Important!</span> Find the *Dunamis Framework* and click on *Activate*.
6. When the Dunamis Framework has been activated, find the *Integrator 3* addon and click on *Activate*.
7. Next click on the *Configure* button for the Integrator 3 addon.  An area will appear below with checkboxes containing different user groups for access control.
8. Find the *Full Administrator* access group and check that box, and click *Save Changes*.
9. Next you will need to create an [API Administrator](common/createapiuser.md) for access into WHMCS.  Be sure to store the the username and password you create for the next section.

The Integrator 3 for WHMCS addon should now be activated and ready to be configured!

#### Create the Connection in Integrator 3

1. Log into your [Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md).
2. Click on the *Configuration* drop down menu and select *API Settings*.
3. You will now see a screen containing your *API Secret Key*.  **COPY** the API Secret Key and store it in a text editor.
4. Click on the *Connections* drop down menu.  If you are able to add another connection to the Integrator 3 application, you will see *Add New Connection*, else you will need to purchase an additional connection for your license.
5. Select *WHMCS* from the dropdown menu and click *Add Connection and Continue*.
6. You will see a form field at the bottom that says *Connection ID* - **COPY** that Connection ID down as you will need it in the next section.
7. Fill in the fields below and press *Save Changes* to store the values in place.  The rest of the settings can be left alone for now.

##### Connection Basics

* **Connection Name** - You can name the connection anything you prefer to use.
* **Connection URL** - This must be the URL to your WHMCS site, without any queries or template selections etc.

##### API Settings

* **API URL** - This should be identical to your Connection URL earlier.
* **API Username** - This should be the username of the API User you created in WHMCS earlier.
* **API Password** - Again, this is what you created earlier for the API User.


#### WHMCS Addon Configuration

1. Log into your WHMCS administration control panel.
2. Navigate to *Addons* > *Integrator 3*.  Click on the *Settings* link at the top center of the page.
3. Fill in the fields below and press 'Save Settings' to connect your WHMCS site to Integrator 3.
  * **Integrator URL** - This should be the fully qualified domain name to your Integrator 3 application.
  * **Secret Token** - This is the API Key that you copied down out of Integrator 3 in the section entitled 'Create the Connection in Integrator 3'.
  * **Connection ID** - This is the Connection ID you copied out of Integrator 3 in the section entitled 'Create the Connection in Integrator 3'.

### Next Steps

After you have installed Integrator 3 for WHMCs into your site, you are now read to configure the product and install additional connectors.

##### Connector Installation

* [Core Application](integrator3/installupgrade_guide/newinstalls.md)
* [Joomla](integrator3/installupgrade_guide/newjoomla3.md)
* [Kayako Fusion](integrator3/installupgrade_guide/newfusion.md)
* [Wordpress](integrator3/installupgrade_guide/newwordpress4.md)

##### Configuration and How-Tos

* [Access Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md)
* [Add or Change Your License](integrator3/howtoguides/licensechange.md)
* [Creating a New Language Translation](integrator3/howtoguides/createnewlanguage.md)
* [Remove index.php File from URL](integrator3/howtoguides/removeindexfile.md)