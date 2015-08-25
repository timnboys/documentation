---
title: Belong - Upgrading from version 1.x
breadcrumb: /belong:Belong/installupgrade_guide:Install and Upgrade Guide/upgrade10:Upgrading from version 1.x/

---


### Upgrading from Belong version 1.x

If you are upgrading from version 1.x, there are some things to keep in mind:

1. All of the configuration settings for Belong have been moved from Joomla! over to WHMCS.  This was done to make the product faster, more reliable and more extensible.
2. Version 2.x of the Joomla! plugin cannot run concurrently with version 1.x.  The component and associated plugins from earlier versions conflict with the system plugin.  If the component is still installed, the system plugin for version 2.x will automatically disable to prevent unwanted errors on the site.

In order to upgrade from Belong 1.x to Belong 2.x:

1. First remove the 1.x component and associated plugins from Joomla.
2. Follow the installation instructions for the 2.x product found here.