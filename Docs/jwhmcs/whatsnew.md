---
title: J!WHMCS Integrator - What's New in v2.6
breadcrumb: /jwhmcs:J!WHMCS Integrator/whatsnew:What's New
 
---

J!WHMCS Integrator version 2.6 builds upon the previous J!WHMCS Integrator 2.5 release.  Here is just a quick run down of the major changes that can be found in this version:

### Responsive Handling

WHMCS v6 is introducing a new responsive template to the mix for customers to use.  J!WHMCS Integrator 2.6 attempts to work with this using a javascript resizing mechanism that will permit your responsive WHMCS template to work within any sized Joomla template, but to respond not to the device but instead to the space available from Joomla.  For instance, if you have a Joomla template that allows for only 740 pixels of space, then the new mechanism will adjust the template from WHMCS to expect only 740 pixels of space available to it.  This setting can also be deactivated, to fall back to standard media query responsiveness.

### Bootwhmcs Template Support

J!WHMCS Integrator v2.6 now supports the free Bootwhmcs template.  Like the new `six` template from WHMCS, Bootwhmcs is responsive and is adjusted to be responsive to the Joomla space, not the device.

### Updated Dunamis Debugging

One of the greatest challenges in diagnosing problems is knowing what is going on behind the scenes.  Dunamis Framework 1.4 helps this effort by introducing the use of a debugger toolbar that provides a single location to return debug information to regardless of the page.  In addition, when debug is enabled, errors are logged and API calls to each system are logged to help diagnose any problems that may arise.

### Boostrap replacement

A common issue when blending Joomla with WHMCS is double bootstrap pounding, where Joomla loads a bootstrap, and then WHMCS loads it's own bootstrap.  This causes links and buttons not to work and other unexpected issues.  J!WHMCS Integrator 2.6 now provides for a mechanism to use one or the other.

### Button Fix

Some Joomla templates for some reason hijack button events preventing the cpanel login and other buttons from working properly.  J!WHMCS Integrator 2.6 has a new setting to add a quick script to correct this.
