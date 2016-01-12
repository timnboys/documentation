---
title: Integrator 3 for Joomla - New Installation 
breadcrumb: /integrator3:Integrator 3/installupgrade_guide:Install and Upgrade Guide/newwordpress:New Joomla Installation

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

## Integrator 3: <small>Joomla Install</small>

### Download Integrator 3 for Joomla

1.  Log into our web site using your account credentials.  You may use either your email address and password or your username and password.
2.  Navigate to the *Downloads* link on the main menu and select the latest release of Integrator 3 for download.
3.  Select the file called *Complete Integrator 3 Archive* and save the file to your local computer.
4.  Navigate to the folder the archive was saved into and extract the contents of that folder into a convenient location.
5.  Wherever you extract the archive you should see five folders: Fusion, Integrator, Joomla, WHMCS and Wordpress

The folder `Joomla` contains the Integrator 3 for Joomla plugin files, and that is what this page will walk you through installing.  For instructions on installing the other connectors or the core app, please see the following:

* [Core Application](integrator3/installupgrade_guide/newinstalls.md)
* [Kayako Fusion](integrator3/installupgrade_guide/newfusion.md)
* [WHMCS v6](integrator3/installupgrade_guide/newwhmcs6.md)
* [Wordpress](integrator3/installupgrade_guide/newwordpress4.md)

### Gather Requirements

To complete the installation of the Joomla component, you will need to have the following information:

* **Joomla Administration Credentials** - you will need to install the Integrator 3 component into the backend of Joomla!.
* **Integrator 3 Access Details** - you will need an administrator account in Integrator 3 that has API access to the core application.  To find out about setting this up, please see [Creating an API Admin in Integrator 3](integrator3/howtoguides/createi3apiadmin.md).

### Installation Procedure

Now you are ready to install Integrator 3 for Joomla!.

#### Component Installation

<div class="alert alert-warning"><strong>Notice Before Installing</strong>
If you installed your Integrator 3 core application into the same directory as your Joomla site **and** called it *integrator* you will not be able to install the component into Joomla due to checks done by Joomla prior to installation.  To bypass this problem, temporarily rename the *integrator* folder to *_integrator*, install the Integrator 3 component for Joomla component, then rename the *_integrator* folder back to *integrator*.
</div>

1. Navigate into the `Joomla` folder you extracted earlier.  You will find in that folder a file named `integrator_joomla_component_v3xxx.zip`.  This is the component file you will need for installation.
2. Log into your Joomla administration control panel.
3. Navigate to *Extensions* and click on *Manage*.  Click on the *Upload Package File* tab if you are not already on it.
4. Click on *Browse* and find the file named `integrator_joomla_component_v3xxx.zip` that you located in step one.  Then click on *Upload & Install*
5. The Integrator 3 for Joomla archive will be installing the Dunamis framework along with a number of plugins the Integrator 3 for Joomla component require.

The Integrator 3 for Joomla component should now be activated and ready to be configured!

#### Create the Connection in Integrator 3

1. Log into your [Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md).
2. Click on the *Configuration* drop down menu and select *API Settings*.
3. You will now see a screen containing your API Secret Key.  *COPY* the API Secret Key and store it in a text editor.
4. Click on the *Connections* drop down menu.  If you are able to add another connection to the Integrator 3 application, you will see *Add New Connection*, else you will need to purchase an additional connection for your license.
5. Select *Joomla* from the dropdown menu and click *Add Connection and Continue*.
6. You will see a form field at the bottom that says *Connection ID* - **COPY** that Connection ID down as you will need it in the next section.
7. Fill in the fields below and press *Save Changes* to store the values in place.  The rest of the settings can be left alone for now.

##### Connection Basics

* **Connection Name** - You can name the connection anything you prefer to use.
* **Connection URL** - This must be the URL to your Joomla site, without any queries or template selections etc.

##### API Settings

* **API URL** - This should be identical to your Connection URL earlier.
  

#### Joomla Component Configuration

1. Log into your Joomla administration control panel.
2. Navigate to *Components* > *Integrator 3*.  Click on the *Options* button on the top right of the screen.
3. Fill in the fields below and press 'Save Settings' to connect your Joomla site to Integrator 3.
  * **Integrator URL** - This should be the fully qualified domain name to your Integrator 3 application.
  * **API Secret Key** - This is the API Key that you copied down out of Integrator 3 in the section entitled 'Create the Connection in Integrator 3'.
  * **Connection ID** - This is the Connection ID you copied out of Integrator 3 in the section entitled 'Create the Connection in Integrator 3'.

### Next Steps

After you have installed Integrator 3 for Wordpress into your site, you are now read to configure the product and install additional connectors.

##### Connector Installation

* [Core Application](integrator3/installupgrade_guide/newinstalls.md)
* [Kayako Fusion](integrator3/installupgrade_guide/newfusion.md)
* [WHMCS v6](integrator3/installupgrade_guide/newwhmcs6.md)
* [Wordpress](integrator3/installupgrade_guide/newwordpress4.md)

##### Configuration and How-Tos

* [Access Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md)
* [Add or Change Your License](integrator3/howtoguides/licensechange.md)
* [Creating a New Language Translation](integrator3/howtoguides/createnewlanguage.md)
* [Remove index.php File from URL](integrator3/howtoguides/removeindexfile.md)