---
title: C!Blesta - How To Guide: How to Handle Blesta Upgrades
breadcrumb: /cblesta:C!Blesta/howtoguides:How To Guides/blestaupgrades:How to Handle Blesta Upgrades/
 
---

The C!Blesta product overrides a number of files in the Blesta template folders in order to accomplish the integration.  To ensure backwards compatibility, the templates are grouped according to the Minor Blesta release version.  For example, suppose you are using Blesta version 4.2.2.  The minor version in this case would be 4.0.

To know which minor version you are running, log into the backend of Blesta and look on the bottom right side of the screen at the very bottom.  You should see _Installed Version x.y.z_ indicating your version.  Simply drop the last number so your version is x.y and you have found your minor version.  The dropped version number (the z in this case) is a release number.  So 3.5.2 would be version 3.5 release 2, 3.3.1 is version 3.3 release 1,etc.

### Upgrading Blesta

When upgrading Blesta from one release to another, if the minor version number doesn't change (the middle number for example in version `3.5.2`, the `5`), then you usually do not have to worry about upgrading or adjusting C!Blesta in any way.  For example, lets say you are running Blesta version 3.5.1, and you upgrade using their patch to version 3.5.2.  So long as the patch does not contain any template changes (and very few of them do) then you shouldn't have to do anything else with C!Blesta.

If however you were running Blesta version 3.0.0, and you upgraded to version 3.5.2 using the full download instead of the patch, then you WOULD need to do some minor adjustments to the C!Blesta system.  This requires *C!Blesta Template Correction*.

If you are upgrading from say version 3.4 to 3.5, then you WOULD need to do some adjustments to the C!Blesta system.

### Handling C!Blesta Template Corrections

If you have overwritten your templates folder in Blesta for any reason with the stock templates from Blesta, say you did an upgrade that changed the template files slightly, then you would need to perform this step.

Each of the template files must be 'corrected' in C!Blesta.  To do this, follow these steps:

1. Log into the administrative back end of your Blesta application using an account with access to the C!Blesta plugin.
2. Navigate to Settings > Installed Plugins and select Manage next to C!Blesta
3. Click on the _System Check_ button located just beneath the C!Blesta logo.
4. You will now see a list of templates and any templates that are out of adjustment will have a red "_Correct_ button next to them.
5. Click the _Correct_ button next to each template file until they are all fixed.

### Handling a Blesta Upgrade

When upgrading Blesta from one version to the next (say version 3.4 to 3.5) you may need to perform an additional step.  Follow the Handling C!Blesta Template Corrections procedure above.  Then follow these steps.  For the purposes of this procedure, the old version is your previous minor version (say 3.4) and your new version is your newly upgraded version (say 3.5):

1. Perform the steps above for Handling C!Blesta Template Corrections
2. Next Log in with FTP to your server.
3. Navigate to the following path:  _BLESTAPATH/plugins/cblesta/teamplates/(OLDVERSION)/(TEMPLATENAME)/_
4. You may see a file there called _custom.css_.  If you do, continue, if not you are done.
5. Edit the file custom.css and copy all the css adjustments there.
6. Now navigate to the following path:  _BLESTAPATH/plugins/cblesta/templates/(NEWVERSION)/(TEMPLATENAME)/_
7. You will see a file called _custom.css.new_.
8. Rename this file to _custom.css_.
9. Edit this file and past the CSS adjustments you copied in step 5 into this file.
10. Save and close.

That should be all that is needed to copy your styles over.
