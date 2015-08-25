---
title: J!Blesta - Quick Start Guide
breadcrumb: /jblesta:J!Blesta/quickstart:Quick Start Guide
 
---


### Welcome

On behalf of the Go Higher Team, I'd like to say thank you for purchasing J!Blesta, and welcome to the Go Higher product family!

We strive to provide the best possible products, services and support to meet your every integration need, and J!Blesta certainly plays a key role in that effort.  We hope you find the product and this documentation useful and informative, and we hope it makes your integration and site management easier and more professional.

#### Requirements

The following software requirements must be met for J!Blesta to operate:

* PHP 5.3+
* MySQL 5+
* Joomla! 2.5.11+
* Blesta 3.5+
* Dunamis Framework 1.3+

Older versions of Joomla! or Blesta may work, however they cannot be supported and should be upgraded to ensure proper functionality (as well as security and other considerations).  Joomla! version 1.5 is not supported.

#### Considerations

If you are using a server level firewall such as mod_security then you should consider whitelisting your servers IP address. The product will necessarily communicate to your server through CURL and may get blacklisted if your security rules are too stringent. A clear indicator of a firewall issue is a '0' response being received by the API handler. This is unrelated to J!Blesta, but rather is a server configuration issue entirely. Please consult your hosting provider for more information on resolving this issue.

### Key Concepts

When dealing with J!Blesta there are some key concepts to keep in mind in order to understand exactly what the product does.

#### Visual Integration

The visual integration refers to wrapping your Joomla! site around your Blesta content.  This is accomplished by utilizing the event calls built into Blesta to fetch the Joomla! site and perform a number of regular expression matches upon the returned content.  These regular expressions do everything from changing the href links to changing image locations.

#### User Integration

The user integration refers only to the bridging of user accounts between Joomla! and Blesta.  Like visual integration, the user integration is accomplished by utilizing the built the event calls built into Blesta as well as the user level plugin in Joomla!.  The User Plugin also manages the insertion of additional fields into the registration form for Joomla!.

### Installation

Please follow these simple steps in order to install the product into your Joomla! and Blesta sites:

1. Locate your license key and download the latest release of the product from our web site.  For more information on this, please visit *Locating My License*.
2. Download the latest release of the Dunamis Framework (version 1.3 or higher).
3. Extract the Dunamis archive for Blesta to your local machine.
4. Download the latest release of J!Blesta.  You will need the following files:
# ''com_jblesta_v{x.y.z}.zip'' - This is the Joomla portion of the installation
# ''jblesta_for_blesta_v{x.y.z}.zip'' - This is the Blesta portion of the installation
5. Extract the Blesta portion of the archive onto your local machine.
6. Upload both the extracted Dunamis for Blesta plugin and the extracted J!Blesta for Blesta plugin to your Blesta application.
7. Log into your Blesta application and go to Settings, Plugins and select Available beneath the Plugins title on the left side.
8. Click on Install next to Dunamis plugin.  *You must install Dunamis first before installing the J!Blesta plugin!*
9. Now click on install next to the J!Blesta plugin.
10. Install the Joomla! portion of the product into your Joomla installation through the extension manager.

You have now installed the product into your systems.  You should configure the product at this point.

### Accessing Settings

The J!Blesta has settings on both Joomla! and Blesta that permit management of the product for each system.

#### Joomla!

Settings for Joomla! are handled in two different locations.  To access the settings for the component portion of the installation in Joomla!:

1. Log into the back end of your Joomla! CMS with an account that has permission to manage options (for most systems, this will be your Super Admin account)
2. Navigate to Components > J!Blesta.  Then click on the Options button on the top right (for Joomla! 3+ it will be on the top navigation bar on the left).

#### Blesta

Settings for the Blesta portion of the product are handled in the plugin manager in Blesta.  To access the settings:

1. Log into the back end of your Blesta application using an account that has privileges to administer your plugins.
2. Click on Settings on the top right of the admin area.
3. Click on Plugins under the Company tab.  You should now be on the Installed Plugins section of Blesta.
4. Locate the J!Blesta plugin in the list and click on the Manage button.
5. Click on the Settings link beneath the J!Blesta title.

### Getting Support

The goal of J!Blesta in addition to simplifying integration for our customers is to minimize the need for support staff to actually log in and manage your product on your behalf.  We are doing our best to provide documentation to help in every way we can and we want to encourage our customers to first utilize the Support Forum for your support needs.

<div class="alert alert-info"><strong>Support and Upgrade Pack</strong><br />
You must have a current Support and Upgrade pack for the product you require support for in order to obtain both the latest upgrades and premium support services from Go Higher IS.
</div>

* [Documentation](https://www.gohigheris.com/documentation/jwhmcs) 
* [Support Forum](https://www.gohigheris.com/forum/index)
* [Support Ticket](https://support.gohigheris.com/)









### Welcome

On behalf of the Go Higher Team, I'd like to say thank you for purchasing J!WHMCS Integrator, and welcome to the Go Higher product family!

We strive to provide the best possible products, services and support to meet your every integration need, and J!WHMCS Integrator certainly plays a key role in that effort.  We hope you find the product and this documentation useful and informative, and we hope it makes your integration and site management easier and more professional.

#### Requirements

The following software requirements must be met for J!WHMCS Integrator to operate:

* PHP 5.3+
* MySQL 5+
* Joomla! 2.5 / 3.4
* WHMCS 5.3+
* Dunamis Framework 1.4+

Older versions of Joomla! or WHMCS may work, however they cannot be supported and should be upgraded to ensure proper functionality (as well as security and other considerations).  Joomla! version 1.5 is no longer supported.

### Considerations

If you are using a server level firewall such as mod_security then you should consider whitelisting your servers IP address. The product will necessarily communicate to your server through CURL and may get blacklisted if your security rules are too stringent. A clear indicator of a firewall issue is a '0' response being received by the API handler. This is unrelated to J!WHMCS Integrator, but rather is a server configuration issue entirely. Please consult your hosting provider for more information on resolving this issue.

### Key Concepts

When dealing with J!WHMCS Integrator there are some key concepts to keep in mind in order to understand exactly what the product does.

#### Visual Integration

The visual integration refers to wrapping your Joomla! site around your WHMCS content.  This is accomplished by utilizing the built in hook system within WHMCS to fetch the Joomla! site and perform a number of regular expression matches upon the returned content.  These regular expressions do everything from changing the href links to changing image locations.

#### User Integration

The user integration refers only to the bridging of user accounts between Joomla! and WHMCS.  Like visual integration, the user integration is accomplished by utilizing the built in hook system in WHMCS and well as the user level plugins in Joomla!.  The User Plugin also manages the insertion of additional fields into the registration form for Joomla!.

### Installation

The installation procedure for J!WHMCS Integrator has changed greatly in this is version.  Please follow these simple steps in order to install the product into your Joomla! and WHMCS sites:

* Locate your license key and download the latest release of the product from our web site.  For more information on this, please visit *Locating My License*.
* Download the latest release of the Dunamis Framework.
* Extract the primary archive to your local machine.
* Extract the WHMCS portion of the 

### Accessing Settings

The J!WHMCS Integrator has settings on both Joomla! and WHMCS that permit management of the product for each system.

#### Joomla!

Settings for Joomla! are handled in two different locations.  To access the settings for the component portion of the installation in Joomla!:

1. Log into the back end of your Joomla! CMS with an account that has permission to manage options (for most systems, this will be your Super Admin account)
2. Navigate to Components > J!WHMCS Integrator.  Then click on the Options button on the top right (for Joomla! 3+ it will be on the top navigation bar on the left).

The API Token for J!WHMCS Integrator must also be set.  This is handled in the System Plugin and can be found by:

1. Log into the back end of your Joomla! CMS with an account that has permission to manage options (for most systems, this will be your Super Admin account)
2. Navigate to Extensions > Plugin Manager.
3. Select the System as the Plugin Type to filter plugins
4. Locate the System - J!WHMCS Integrator plugin and click on it to edit the API Token

#### WHMCS

Settings for the WHMCS portion of the product are also handled in two different locations.  The first thing to do is check that your WHMCS account has permission to manage the product.  This should only need to be done one time, and is usually done at the time of installation.  This can be done by:

1. Log into the back end of your WHMCS client portal using an account that has privileges to edit the addon modules area.
2. Navigate to Setup > Addon Modules
3. Locate the J!WHMCS Integrator product addon module and click on the Configure button.
4. Ensure your account role is 'ticked' for being permitted to manage the settings and click Save.

The rest of the settings are handled in the product addon.  To manage them:

1. Log into the back end of your WHMCS client portal using an account that has privileges to manage your addon module.
2. Navigate to Addons > JWHMCS Integrator.
3. Click on the Settings link.

### Getting Support

The goal of J!WHMCS Integrator in addition to simplifying the product greatly for our customers is to minimize the need for support staff to actually log in and manage your product on your behalf.  We are doing our best to provide documentation to help in every way we can and we want to encourage our customers to first utilize the Support Forum for your support needs.  With version 2.5 of our product, we don't believe we will need to log in at all to manage your product, the settings have been simplified, the processes used to accomplish the product features have been greatly reduced and streamlined in an effort to minimize interference with other products.

{info:title=Support and Upgrade Pack}

You must have a current Support and Upgrade pack for the product you require support for in order to obtain both the latest upgrades and premium support services from Go Higher IS.

* [Documentation](https://www.gohigheris.com/documentation/jwhmcs) 
* [Support Forum](https://www.gohigheris.com/forum/index)
* [Support Ticket](https://support.gohigheris.com/)
