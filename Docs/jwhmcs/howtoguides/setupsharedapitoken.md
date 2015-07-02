---
title: J!WHMCS Integrator - How To Guide: Setup the Shared API Token
breadcrumb: /jwhmcs:J!WHMCS Integrator/howtoguides:How To Guides/setupsharedapitoken:Setup the Shared API Token/
 
---

J!WHMCS Integrator version 2.5 introduces the concept of a shared API token.  This token is used on both Joomla! and WHMCS to securely pass data back and forth without the need to setup different Joomla users, user groups or provide permissions to users to access API features.

### Setting Up The Shared Token in WHMCS

To setup the shared token in WHMCS, follow these steps:

<div class="alert alert-danger"><strong>BE SURE YOU HAVE A BACKUP</strong><br />
The settings in J!WHMCS Integrator will attempt to update and write to your WHMCS configuration.php file.  If anything interrupts this process, your WHMCS configuration.php file may become corrupted so be sure you have at least a backup of your configuration.php file
</div>

1. Log into the administrative back end of your WHMCS application using an account with access to the J!WHMCS Integrator addon.
2. Navigate to Addons > J!WHMCS Integrator.

<div class="alert alert-info"><strong>Accessing Settings</strong><br />
If you don't see the link for J!WHMCS Integrator under Addons, you will need to go first into WHMCS > Setup > Addon Modules, then click on the 'Configure' button for J!WHMCS Integrator.  Be sure the user group your WHMCS administrator account belongs to has access to J!WHMCS by checking the box next to your corresponding user group and click 'Save'.  You should now see the J!WHMCS Integrator option under Addons.
</div>

3. Click on the Settings link beneath the J!WHMCS Integrator logo.
4. Locate the AutoAuth / API Token field under the General Settings section.
5. Enter a secure, unique token here.

<div class="alert alert-warning"><strong>Important</strong><br />
If you already have configured an AutoAuth token for WHMCS, then this field should already be configured to use that same token.  If you change this token you may break any applications that are setup to utilize AutoAuth through WHMCS.  If you have questions or are unsure about this, please check our forum!
</div>

6. Click Submit

If your configuration.php file is writable, J!WHMCS Integrator will attempt to update your configuration.php file with the new token.  You should receive a confirmation indicating your settings have been saved.

### Setting Up The Shared Token in Joomla!

To setup the shared token in Joomla!, follow these steps:

1. Log into your Joomla backend using an account with Super User privileges.
2. Navigate to Components > J!WHMCS Integrator
3. Click on the Options button.
4. Locate the API Token field under the General parameters section.
5. Enter the same secure, unique token you used in WHMCS into this field.
6. Click Save and Close

You should now have established the API bridge between WHMCS and Joomla!.

### Verifying Connectivity

To verify that you have established the connection properly from WHMCS, follow these steps:

1. Log into the administrative back end of your WHMCS application using an account with access to the J!WHMCS Integrator addon.
2. Navigate to Addons > J!WHMCS Integrator.
3. Click on the System Check link beneath the J!WHMCS Integrator logo.
4. In the top section labelled API Check, see if you have any errors indicated.   If everything is checked you are good to go!
