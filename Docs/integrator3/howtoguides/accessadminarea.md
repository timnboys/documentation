---
title: Integrator 3 - How To:  Accessing the Integrator 3 Administration Area 
breadcrumb: /integrator3:Integrator 3/howtoguides:How To Guides/accessadminarea:Accessing the Integrator 3 Administration Area
 
---

## How To Access the Integrator 3 Administration Area

Your Integrator 3 application has two sides to it, much like other applications: a front, client facing side and an admin area that is accessible by you and your staff for configuring the application.

Your Integrator 3 Administration Area is always accessible by appending `index.php/admin` to your Integrator 3 URL, so for example:

`http://yourdomain.com/integrator3/index.php/admin`

This will always result in bringing you to the admin log in screen, regardless of whether you later enable the .htaccess file to remove the index.php filename from the URL.

#### Examples

##### Subfolder

If you installed your Integrator 3 application into a subfolder of yourdomain.com, it would look like this:
 
`http://yourdomain.com/integrator3/index.php/admin`

##### Subdomain

If you installed your Integrator 3 application into a subdomain of yourdomain.com, it would look like this:
 
`http://integrator3.yourdomain.com/index.php/admin`