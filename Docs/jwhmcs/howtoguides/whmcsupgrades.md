---
title: J!WHMCS Integrator - How To Guide: How to Handle WHMCS Upgrades
breadcrumb: /jwhmcs:J!WHMCS Integrator/howtoguides:How To Guides/whmcsupgrades:How to Handle WHMCS Upgrades/
 
---

The J!WHMCS Integrator product overrides a number of files in the WHMCS template folders in order to accomplish the integration.  To ensure backwards compatibility, the templates are grouped according to the Minor WHMCS release version.  For example, suppose you are using WHMCS version 5.2.16.  The minor version in this case would be 5.2.  For WHMCS version 5.3.5, the minor version would be 5.3.

To know which minor version you are running, log into the backend of WHMCS and look on the left side of the screen in the sidebar.  You should see _Version x.y.z_ indicating your version.  Simply drop the last number so your version is x.y and you have found your minor version.  The dropped version number (the z in this case) is a release number.  So 5.2.16 would be version 5.2 release 16, 5.3.5 is version 5.3 release 5,etc.

### Upgrading WHMCS

When upgrading WHMCS from one release to another, if the minor version number doesn't change (the middle number for example in version `5.3.5`, the `3`), then you usually do not have to worry about upgrading or adjusting J!WHMCS Integrator in any way.  For example, lets say you are running WHMCS version 5.3.4, and you upgrade using their patch to version 5.3.5.  So long as the patch does not contain any template changes (and very few of them do) then you shouldn't have to do anything else with J!WHMCS Integrator.

If however you were running WHMCS version 5.3.3, and you upgraded to version 5.3.5 using the full download instead of the patch, then you WOULD need to do some minor adjustments to the J!WHMCS Integrator system.  This requires *J!WHMCS Template Correction*.

If you are upgrading from say version 5.2 to 5.3, then you WOULD need to do some adjustments to the J!WHMCS Integrator system.

### Handling J!WHMCS Template Corrections

If you have overwritten your templates folder in WHMCS for any reason with the stock templates from WHMCS, say you did an upgrade that changed the template files slightly, then you would need to perform this step.

Each of the template files must be 'corrected' in J!WHMCS Integrator.  To do this, follow these steps:

1. Log into your _WHMCS Administrator_ area.
2. Navigate to _Addons_ > _J!WHMCS Integrator_.  Click on _System Check_ on the top.
3. You will now see a list of templates and any templates that are out of adjustment will have a red "_Correct_ button next to them.
4. Click the _Correct_ button next to each template file until they are all fixed.

### Handling a WHMCS Upgrade

When upgrading WHMCS from one version to the next (say version 5.2 to 5.3) you may need to perform an additional step.  Follow the Handling J!WHMCS Template Corrections procedure above.  Then follow these steps.  For the purposes of this procedure, the old version is your previous minor version (say 5.2) and your new version is your newly upgraded version (say 5.3):

1. Perform the steps above for Handling J!WHMCS Template Corrections
2. Next Log in with FTP to your server.
3. Navigate to the following path:  _WHMCS/modules/addons/jwhmcs/teamplates/(OLDVERSION)/(TEMPLATENAME)/_
4. You may see a file there called _custom.css_.  If you do, continue, if not you are done.
5. Edit the file custom.css and copy all the css adjustments there.
6. Now navigate to the following path:  _WHMCS/modules/addons/jwhmcs/templates/(NEWVERSION)/(TEMPLATENAME)/_
7. You will see a file called _custom.css.new_.
8. Rename this file to _custom.css_.
9. Edit this file and past the CSS adjustments you copied in step 5 into this file.
10. Save and close.

That should be all that is needed to copy your styles over.
