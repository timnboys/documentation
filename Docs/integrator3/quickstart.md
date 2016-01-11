---
title: Integrator 3 - Quick Start Guide
breadcrumb: /integrator3:Integrator 3/quickstart:Quick Start Guide
 
---

## Quick start Guide

### What Integrator 3 Does

Integrator 3 is a robust application that allows you to bridge not just the user accounts between multiple systems but also bridge the visual appearance as well.  Integrator 3 permits any number of applications to be connected subject to licensing, so for example you may want a Joomla site and a Wordpress site to share the same WHMCS installation.  With Integrator 3, all three can be tied together so when a user logs into one, they are logged into all three.  When a user visits WHMCS from Joomla, they will see Joomla wrapping it, but if they visit from Wordpress, they will see Wordpress wrapping it.

### Key Concepts

There are some key concepts to keep in mind in order to understand exactly what the product does.

#### Content Management System (CMS)

A CMS stands for Content Management System.  Integrator 3 currently works with two CMS products: Joomla! and Wordpress.

#### Application

An application is a program that is run that is wrapped.  For example, WHMCS is considered an application because it would be wrapped by a content management system through Integrator 3.  Currently Integrator 3, WHMCS and Kayako Fusion are considered applications and are supported.

#### Visual Integration

The visual integration refers to wrapping your content management system (either Joomla! or Wordpress) around your application (either WHMCS or Kayako Fusion).  This is accomplished by utilizing the built in hook systems within the applications to make requests of Integrator 3 to retrieve the content management site for rendering around the application.  Regular expression matches are performed upon the source from the content management system.  These regular expressions do everything from changing the href links to changing image locations.

#### User Integration

The user integration refers to bridging of user accounts between various systems.  Like visual integration, the user integration is accomplished by utilizing the built in hook system within the applications and well as plugins within the content management system.

### Requirements

The following software requirements must be met for Integrator 3 to operate:

##### Core Application
* PHP 5.3+
* MySQL 5+

##### Joomla Requirements (if used)
* Joomla! 2.5 / 3.4
* Dunamis Framework 1.4+

##### WHCMS Requirements (if used)
* WHMCS 5.3+
* Dunamis Framework 1.4+

##### Wordpress Requirements (if used)
* Wordpress v 4+

##### Kayako Requirements (if used)
* Kayako Fusion v4.50+

Older versions of Joomla!, Wordpress, WHMCS or Kayako may work, however they cannot be supported and should be upgraded to ensure proper functionality (as well as security and other considerations).

#### Considerations

If you are using a server level firewall such as mod_security then you should consider whitelisting your servers IP address. The product will necessarily communicate to your server through CURL and may get blacklisted if your security rules are too stringent. A clear indicator of a firewall issue is a '0' response being received by the API handler. This is unrelated to Integrator 3, but rather is a server configuration issue entirely. Please consult your hosting provider for more information on resolving this issue.

### Installation


### Getting Support

The goal of Integrator 3 is to make managing your web site esaier and for the user experience on your site to be more fluid as they move from your CMS to an application.  We are reworking our  documentation to help in every way we can and we want to encourage our customers to first utilize the Support Forum for your support needs.

<div class="alert alert-info"><strong>Support and Upgrade Pack</strong><br />
You must have a current Support and Upgrade pack for the product you require support for in order to obtain the latest upgrades and premium support services from Go Higher IS.
</div>

* [Documentation](https://www.gohigheris.com/documentation/jwhmcs) 
* [Support Forum](https://www.gohigheris.com/forum/index)
* [Support Ticket](https://support.gohigheris.com/)