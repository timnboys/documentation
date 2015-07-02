---
title: J!WHMCS Integrator - Troubleshooting: Manually Updating the AutoAuth Key
breadcrumb: /jwhmcs:J!WHMCS Integrator/troubleshooting:Troubleshooting/manuallyupdatingautoauth:Manually Updating the AutoAuth Key/
 
---

If you receive an error message when saving your configuration settings that reads:

<div class="alert alert-danger"><strong>Warning!</strong><br />
	J!WHMCS Integrator was unable to write the autoauthkey to your configuration file! You will need to manually update your WHMCS configuration file to include the value for the AutoAuth key. For more information, please visit our forum.
</div>

Please follow these steps to properly set the autoauth key in place.

1. Open your WHMCS site in an FTP client such as Filezilla, WinSCP or FireFTP
2. Locate the file called 'configuration.php' located in your WHMCS root directory.
3. Edit the file and towards the end you will see the following code:
    $templates_compiledir = 'templates_c/';
    $mysql_charset = 'utf8';
    ?>

4. Insert the following line into the bottom of the file so that it appears as such:
    $templates_compiledir = 'templates_c/';
    $mysql_charset = 'utf8';
    $autoauthkey = 'abcXYZ123';
    ?>
<br />where the `abcXYZ123` value is what you want to be for your autoauth key.
5. Save the file and upload it back to the server.

That's it!  When you save your settings in the future you may still be given the notification that it was unable to save the autoauthkey, but if you performed the steps above it wont' matter.  The only time you will need to revisit this is if you change your key in the future for any reason.

#### Notes

For more information: [WHMCS Autoauthkey](http://docs.whmcs.com/AutoAuth)
