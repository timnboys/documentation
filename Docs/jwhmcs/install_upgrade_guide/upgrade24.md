---
title: J!WHMCS Integrator - Upgrading from J!WHMCS Integrator 2.4
breadcrumb: /jwhmcs:J!WHMCS Integrator/install_upgrade_guide:Install and Upgrade Guide/upgrade24:Upgrading from version 2.4/

---

{toc}

J!WHMCS Integrator version 2.6 is a radical departure from versions 2.4 or earlier, and as such, requires special consideration when upgrading an existing installation.

### Changes to Consider

Before upgrading to version 2.6, you need to be aware of some significant changes in the product.

* *Joomla! 1.5 No Longer Supported*
Unfortunately, the time to discontinue actively developing and maintaining new releases for Joomla! 1.5 has come for J!WHMCS Integrator.  If you are using Joomla! 1.5, you will not be able to upgrade to version 2.6 without first migrating your CMS over to at least Joomla! 2.5.
* *Integrated Registration Dropped*
With Joomla! 2.5 and 3.x, the standard registration form from Joomla can be expanded to include any fields desired.  J!WHMCS Integrator takes advantage of this by including the fields required for WHMCS client registration into the default registration form (both front and back ends).  In addition, it is now possible to create a Username field in WHMCS and specify it as storing your Username for Joomla, so now you can use either the Joomla! or WHMCS registration solutions by default, making the Integrated Registration form obsolete and unnecessary.
* *Logging In and Logging Out Changes*
Previous versions of J!WHMCS Integrator included a "Logging In" screen with a blue bar - this has been done away with as the log in and log out process has been completely rewritten.
* *User Management*
Previous versions utilized a user manager and matched up the users and stored these matches in the database.  Version 2.6 now matches users up solely on their email address, eliminating any database write errors or incorrect matches and changes.
* *Visual Rendering Changes*
Previously, J!WHMCS Integrator required two pages, one for logged in users and one for logged out users.  This has been done away with entirely.  Now you can select ANY menu item as the page to be wrapped around WHMCS, and when J!WHMCS retrieves that page it will show the user as logged in and any Registered or Special level elements will be rendered appropriately.  This also means all login modules will display correctly and render the user as expected (even if the user hasn't already logged into Joomla!)
* *Log In Module Dropped*
With the changes in the way the visual rendering is accomplished, there is no longer a need to manage the log in form through J!WHMCS Integrator.  The log in module has been dropped, although it may be reworked in the future as an additional, independent extension.
* *Automatic Installation Discontinued*
While a benefit for some, too often this resulted in breaking J!WHMCS when upgrading due to permission issues.

### Improvements in Version 2.6

* *Faster Performance*
Not only is the visual rendering vastly improved over previous versions, but the log in and log out performance is incredible as well.
* *More Intuitive and Flexible*
By relying on the Joomla core when possible, J!WHMCS Integrator permits you to style your site exactly as you like, even using the styles from template designers for their registration and log in fields (on the Joomla! side)
* *Simpler Configuration*
Gone are the array of complex and confusing options - in it's place is a flatter, simpler set of options.

### Upgrade Procedure

To upgrade from any version of J!WHMCS Integrator prior to 2.5, you will need to perform the following tasks:

1. Disable the J!WHMCS Integrator product in WHMCS
1. 1. Version 2.4: This can be done by going into WHMCS and navigating to Setup > Addon Modules and clicking on the Deactivate button next to J!WHMCS Integrator.
1. 2. Version 2.3:  Using an FTP client, log into your server and navigate to the WHMCS directory /includes/hooks and delete the two files with jwhmcs in their name.
2. Uninstall the Joomla! portion of the product entirely.  Start first with the plugins (there are 4, sometimes 5 plugins), then uninstall the log in module and the component as well.

* Ensure you have both the Authentication - Joomla and the User - Joomla plugins enabled before logging out! *

3. Using FTP, delete the WHMCS portion of the product.  To do this (files referenced are based in the WHMCS root folder):
3. 1. Version 2.4:  Remove the jwhmcs.php and jconfig.php files in the root directory.  Then remove the jwhmcs api files located in WHMCS/includes/api.  Next remove the jwhmcs folder in WHMCS/modules/addons directory.
3. 2. Version 2.3:  Remove the jwhmcs.php and jconfig.php files in the root directory.   Be sure you are using a regular template from WHMCS by going into WHMCS > Setup > General Settings and change your template from any jwhmcs-* templates to their corresponding WHMCS standard template.  Then remove the jwhmcs-classic, jwhmcs-portal and jwhmcs-default directories from the WHMCS/templates folder (unless you are using them or have customized them – this step simply cleans up after JWHMCS).

At this point your site applications should be not integrated, and should be working independent of one another.

### Final Step

Follow the steps outlined on [New Installations](documentation/jwhmcs/install_upgrade_guide/newinstalls.md) guide and install the new product.
