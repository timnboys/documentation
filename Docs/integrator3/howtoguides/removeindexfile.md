---
title: Integrator 3 - How To Guide:  Remove The index.php File 
breadcrumb: /integrator3:Integrator 3/howtoguides:How To Guides/removeindexfile:Remove The index.php File
 
---

## How To Remove The Filename From The URL

For usability and SEO purposes, you may want to remove the `index.php` file from the URL when on an Integrator 3 page.  Normally your URL will look something like this:

`http://yourdomain.com/integrator3/index.php/register/index`

You can change this to read:

`http://yourdomain.com/integrator3/register/index`

To do so, follow these steps:

1. Using an FTP client, download the configuration.php file from your Integrator 3 application to a local drive. This file is located on your web server in the directory you installed Integrator 3 into.
2. Open the local configuration.php file in your favorite text editor.
3. At about line 40 you will see a line that reads:<pre>$rewrite = false;</pre>Change this line to read:<pre>$rewrite = true;</pre>
4. Next upload the changed file back to your server.
5. Find the file in the same directory called htaccess.txt.
6. Rename this file to `.htaccess`

That should do it. Now you don't need to include the index.php file in the URL to access any portion of the Integrator 3 application including the front end as well as the administrative backend.

<div class="alert alert-warning"><strong>Important</strong><br/>
You can always access the Integrator 3 application by including the index.php in the URL.
</div>
