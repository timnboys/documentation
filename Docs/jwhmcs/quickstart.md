---
title: J!WHMCS Integrator - Quick Start Guide
breadcrumb: /jwhmcs:J!WHMCS Integrator/quickstart:Quick Start Guide
 
---

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
