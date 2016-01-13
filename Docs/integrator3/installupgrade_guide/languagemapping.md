---
title: Integrator 3 - Language Mappings
breadcrumb: /integrator3:Integrator 3/installupgrade_guide:Install and Upgrade Guide/languagemapping:Language Mapping
 
---

## Integrator 3: <small>Language Mapping</small>

### What is Language Mapping?

Language mapping is the process of mapping a user's selected language from one application over to another.  It also ensures that a site that is wrapping an application is in the selected (mapped) language when a user is on the application in that language.

For instance, suppose you have a Joomla site that is in English and French, and you have WHMCS that supports English and French.  If a customer views your WHMCS site in French, language mapping ensures that the Joomla site that is retrieved is also in French.

### What connections support language mapping?

These connections support language mapping:
* Integrator 3 core application
* Joomla!
* Kayako Fusion
* WHMCS

<div class="alert alert-warning"><strong>Wordpress Multi-language Not Supported</strong>Currently multi-language capabilities are not supported natively by Wordpress and as such plugins extending this capability are required.  Integrator 3 is not designed to work with those plugins at this time.</div> 

### How To Configure Language Mapping

There are a few settings to get language mapping configured.

#### Joomla Connections

If you are using a Joomla site as one of your connections and it is using multiple languages be sure to:

1. Log into your [Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md).
2. Click on the *Connections* drop down menu and select your Joomla menu item.
3. On the first tab you will see an option called *Multilingual*.  Enable this setting and press *Save Changes*

#### Integrator 3 Core Application

1. Log into your [Integrator 3 Admin Area](integrator3/howtoguides/accessadminarea.md).
2. Click on the *Rendering* drop down menu and select the *Language Mapping* menu item.
3. You will now be presented with a screen containing your applications on the left as tabs and inside each tabbed area are tables with the sites you have configured in Integrator 3 at the top along with the languages from your application on the left side.
4. Select which languages are to be mapped in each application to which language in each site and press *Update Settings*.
