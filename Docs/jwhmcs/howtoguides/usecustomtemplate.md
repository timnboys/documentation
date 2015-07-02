---
title: J!WHMCS Integrator - How To Guide: Use A Custom Template Directory
breadcrumb: /jwhmcs:J!WHMCS Integrator/howtoguides:How To Guides/usecustomtemplate:Use A Custom Template Directory/
 
---

In previous releases of J!WHMCS Integrator, templates were replaced on the fly by the J!WHMCS Integrator addon module.  This permitted you to use custom template directories but also limited the ability to utilize other WHMCS addon modules when they needed to include data on the front end.  J!WHMCS Integrator 2.5 changes this by replacing the header.tpl and footer.tpl files in your standard WHMCS template folders upon installation.  In doing so however, custom directories get overlooked.  Here's how to correct that.

### Determine the Original Template

Unless your custom template is completely built from scratch, it will probably have originated from one of the three template styles WHMCS provides:

* Classic
* Default
* Portal

Determine which style your custom template was borne from in order to proceed.  This is really just a matter of either remembering which one you started with originally or looking at the two styles side by side to see which it most resembles.  If you are unable to make a determination, you can use the default template as your original template.

Also be sure to know what your custom template is named.  The template folder for your custom template would be found in

    {WHMCS_ROOT}/templates/nnnnnnnn


Where nnnnnnnn is your custom template folder name

### Extract, Rename and Upload - the WHMCS archive

You will now need to download the WHMCS portion of the J!WHMCS Integrator and extract it to your local computer.  In the extracted contents, you will see:

    {FOLDER_ROOT}/modules/addons/jwhmcs/templates/5.x/nnnnnnnn

Where 5.x is the version of WHMCS you are running and nnnnnnnn is the name of one of the original templates (either classic, default or portal).  Duplicate the folder that matches what you determined to be your original template earlier.  For instance, if you determined you were starting from the default template, then duplicate the `default` template folder.  Name the duplicated folder the same as your custom template folder.

Now upload the folder to your {WHMCS_ROOT} so that the path appears as follows:

    {WHMCS_ROOT}/modules/addons/jwhmcs/templates/5.x/nnnnnnnn

Where 5.x is the version of WHMCS you are CURRENTLY running and nnnnnnnn is the name of your custom template folder.

Copy Files Into Place

The final step is to copy the files over using the J!WHMCS Integrator backend utility.  To do this:

1. Log into your WHMCS backend using an account with permissions to access the J!WHMCS Integrator addon module.
2. Navigate to Addons > JWHMCS Integrator > System Check
3. Part way down you should see the File Check screen and your custom folder will also appear.  It should indicate that there are problems with the file.
4. Click "Correct" next to each of the files that need to be fixed.

That should fix the templates up.

### Future Upgrades

Remember when you do upgrades in the future, you will want to repeat this process to ensure the template files get updated properly.
