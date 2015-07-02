---
title: J!WHMCS Integrator - Troubleshooting: Site is reported as not secure even though I have an SSL certificate installed!
breadcrumb: /jwhmcs:J!WHMCS Integrator/troubleshooting:Troubleshooting/sitenotsecure:Site is reported as not secure even though I have an SSL certificate installed!/
 
---

If you are installing J!WHMCS Integrator on a site with an SSL certificate that applies only to your WHMCS installation and not also to your Joomla installation, you may receive a warning about insecure content when viewing your WHMCS site or content may not render properly.  This is likely caused by the SSL certificate applying to your WHMCS site but not your Joomla site, and in such cases, you will need to perform what is known as a split server installation.

You will know if you need to do a split server if:

* Your Joomla and WHMCS are on two completely different domains and only WHMCS has an SSL certificate
* Your Joomla and WHMCS are on the same domain but your WHMCS is in a subdomain like clients.yourdomain.com, Joomla is not and you have an SSL certificate for the clients subdomain

In either of those cases, you will want to perform the split server installation found at [Handling Split Server Installations](jwhmcs/howtoguides/handlesplitserver.md)