---
title: J!WHMCS Integrator - Configuration Walk Through
breadcrumb: /jwhmcs:J!WHMCS Integrator/installupgrade_guide:Install and Upgrade Guide/configwalkthru:Configuration Walk Through/

---

J!WHMCS Integrator has settings located in two different places, those on the Joomla side and those on the WHMCS side.

### Quick Setup on the Joomla Side

After installing the component portion of the J!WHMCS Integrator, you will have installed not just the component but also a series of plugins.  Begin configuration after the installation with the component settings.

#### Access the Component Settings

To access the component settings:

1. Log into the back end of your Joomla! CMS.<br />
{japopup type="image" content="documentation/jwhmcs/installupgrade_guide/assets/1-login.png" width="400" height="300" title="Log Into Joomla"}
<img src="documentation/jwhmcs/installupgrade_guide/assets/1-login.png" width="100px" />
{/japopup}
2. Navigate in the backend of Joomla to Components > J!WHMCS Integrator.<br />
<img src="http://goo.gl/ENV34G" width="100px" />
3. Click on the 'Options' button on the top right side of the page.<br />
<img src="http://goo.gl/QXEvMn" width="100px" />

Now you will be in the component settings

#### Initial Configuration

Assuming you have not configured the API yet to tie into WHMCS, follow these steps:<br />
<img src="http://goo.gl/PmZEdy" width="100px" />

1. *Enable Product*<br />
Set this to 'Yes' to enable the J!WHMCS Integrator product
* *Debug*<br />
Set this to 'Yes' initially to permit debug testing for the visual integration.  Once everything is connecting, be sure to set this to 'No'
* *Download ID*<br />
This is the download ID found on our site after you log into our site.  This permits you to download updates to our product when they become available automatically.
* *API Token*<br />
This is important - you must set a token here.  You will need this for the WHMCS portion of the configuration as well (both sides must have the same token for verification and authentication purposes).

h2. Connect your API from Joomla into WHMCS

There are a number of steps to accomplish this, and they are outlined in the following guides.  Please follow them in order:

# [Create An API User in WHMCS]
# [Granting API Access to WHMCS]
# [API Connection Manager in Joomla]

h2. Create A Menu Item

The last step on the Joomla side is to create a menu item for J!WHMCS Integrator to use.  The purpose of this menu item is two fold:

# Provides a link to your WHMCS app for your customer to click on.
# Provides a menu item to assign modules to in order to have them rendered around your WHMCS app.

This menu item can have modules of any access level assigned to it, and assuming the customer that is logged in on the front end of the WHMCS application has the appropriate access level, will be rendered around the WHMCS content.  To create the menu item, simply go to your Main Menu or any menu you choose, create a New Menu item and select a J!WHMCS Integrator > Link Type of menu item.  Under the options of the menu item, select which page to have the customer land on when they click the link.

You will then select this menu item later in the WHMCS configuration of things.

h1. Walk Through of Settings on WHMCS Side

h2. Accessing the Settings

To access the settings for the J!WHMCS Integrator on the WHMCS side, follow these simple steps.

# Log into the back end of your WHMCS application using an Administrator level account.\\
[!http://goo.gl/Iwe6ta|width=100!|http://goo.gl/Iwe6ta]
# Navigate to Addons > J!WHMCS Integrator.  If you don't have this option in the drop down list:\\
[!http://goo.gl/aZfsTo|width=100!|http://goo.gl/aZfsTo]\\
 
## Navigate to Setup > Addon Module.
## Under Configure for the J!WHMCS Integrator, ensure your access group (ie Administrator) is checked to have access.
## Hit Save
# Click on the Settings link in the navigation row for J!WHMCS Integrator.\\
[!http://goo.gl/smWkja|width=100!|http://goo.gl/smWkja]

h2. Initial Configuration

The first step you want to take is to configure the API connection between WHMCS and Joomla.  In order for this to work you must first do the following in Joomla:

* Ensure that the System - J!WHMCS plugin is activated
* Set and know what the Token is in the J!WHMCS Extension Options
* Be aware of any SSL or language setting requirements in Joomla.

With those requirements set you will need to go through this process:

h3. General Settings

When you go to the settings page, the first screen you will see looks similar to this one:\\
[!http://goo.gl/bQpYpo|width=100!|http://goo.gl/bQpYpo]

To start configuring the application:

# Toggle the Enabled setting to 'Enabled'
# Toggle the Debug setting to 'Enabled'
# In the Joomla URL enter the Fully Qualified URL to your Joomla site.  This would be similar to http://www.yourjoomlasite.com.
{warning:title=Joomla URL Requirement}
If you don't include the scheme (http://) to your site, the API *WILL NOT CONNECT* and you will have issues.
{warning}

# Enter the token you have set in Joomla in the field for Auto Auth / API Token.
# Press the Submit button below to save these settings.\\
\\

{info:title=What if the Auto Auth / API Token won't save?}
If after saving the Auto Auth / API Token field is still blank, you will need to edit your WHMCS configuration file.  Please follow [these directions|Manually Updating the Autoauth Key] to do so.
{info}


To verify that the API is connecting properly, click on the 'System Check' link on the naviation row for J!WHMCS Integrator.  You should see the following display if everything is connecting properly between WHMCS and Joomla:

[!http://goo.gl/4JM0cW|width=100!|http://goo.gl/4JM0cW]

h3. User Integration

For most customers, nothing will need to be modified here.

h3. Visual Integration

There are several common adjustments to make in the Visual Integration section after the API starts connecting.

* *Enable jQuery*<br />
This setting is enabled by default and is included because WHMCS requires the jQuery library to be embedded when the site is rendered.  For most modern Joomla! sites however, jQuery is being included in the template already and embedding it again can cause conflicts and issues.  If your Joomla! site already embeds the jQuery library, you can toggle this to 'Disabled' to avoid potential Javascript conflicts.
* *URL for Images / CSS / JS*<br />
For customers that have WHMCS installed on a subdomain and have an SSL certificate for that subdomain but not for the domain Joomla is installed on, you will want to pay attention to this setting.  This setting permits you to set the images, css and javascript links to another, secured location so your SSL doesn't appear broken.  For more information, please see [Handling Split Server Installations].
* *Menu Item*<br />
After the API starts connecting, this drop down will be populated with active menu items from your Joomla site.  Select a menu item that you have created in Joomla (preferably a menu item of type JWHMCS > Link Type).  This menu item you select can be configured to include modules which will then display around WHMCS.
* *Reset CSS*<br />
J!WHMCS Integrator includes a reset.css file that attempts to reset styles.  For some Joomla! template / WHMCS template combinations this isn't necessary, so if your WHMCS content appears very crunched or out of place after integration, try disabling this setting.
* *Show Navigation Bar*<br />
WHMCS includes a navigation bar on their templates (default and classic have it at the top, portal it appears on the right side).  Enable this to see that navigation bar.
* *Show Footer*<br />
WHMCS includes a copyright at the bottom of their pages but when it's wrapped by your Joomla site, it may appear out of place. You can disable this setting to hide the footer.  Note that this will not remove the WHMCS Branding for a branded WHMCS install.
* *Wrap Invoice*<br />
This feature will allow your invoices to be wrapped by your Joomla site as well.  Many customers prefer this to be disabled.

[!http://goo.gl/wFCXbo|width=100!|http://goo.gl/wFCXbo]

h3. Language Map

If you have a Joomla installation utilizing the Joomla! core multi-language capabilities, you will need to enable the language mapping settings for the visual integration to take place properly.

* *Enable Language Mapping*<br />
This setting is disabled by default, but if you have the multi-language capabilities setup in Joomla, you will want this enabled also.
* *Default Language*<br />
This is the default Joomla! language to use when a language is not specified or mapped on the WHMCS side.

The rest of the settings map the WHMCS language on the left to an appropriate language from Joomla in the drop down box next to it.

[!http://goo.gl/vc19SM|width=100!|http://goo.gl/vc19SM]

h3. Advanced Settings

Most customers won't need to modify anything in here right off the bat.  The only setting you may want to adjust would be:

* *Pass User Agent*<br />
With mod_security and certain firewall solutions, connections can be dropped if there isn't a user agent passed along by the J!WHMCS Integrator when retrieving the site.  You may want to set this to Enabled if you are encountering issues getting the API to connect or are getting a 406 error code when debugging the visual settings.

[!http://goo.gl/MK5c3r|width=100!|http://goo.gl/MK5c3r]
