---
title: Belong - Configuration Walk Through
breadcrumb: /belong:Belong/installupgrade_guide:Install and Upgrade Guide/configwalkthru:Configuration Walk Through/

---


### License Configuration

Prior to using Belong for the first time, you will need to enter the license associated with your product.

<div class="alert alert-danger">An invalid license will result in the inability to save any settings.</div>

<div class="alert alert-info">Note you cannot upgrade Belong to a release that comes after the expiration date of your Support and Upgrade Pack</div>

To enter your license:

1. Locate your license for Belong.  If you don't have your license available, you can log into our site and locate it under ''My Products''.
2. In the backend of WHMCS go to _Addons_ _ *Belong*_\\
!https://lh3.googleusercontent.com/-V43p_47OCNA/UUN5JNjTJwI/AAAAAAAAAF0/8ai8nBBFqz0/s0/2013-03-15_15-40-13.png!
3. Click on the _License_ link.\\
!https://lh3.googleusercontent.com/-1Ioj9uIP9FM/UUN5ZWvewsI/AAAAAAAAAF8/rlyvCaJm8u0/s0/2013-03-15_15-41-18.png!
4. Enter your license in the _License_ field and click _Save._\\
!https://lh4.googleusercontent.com/-WfM3Z4ZKTFk/UUN4bCxI0SI/AAAAAAAAAFk/-K1kzoGCx4Q/s0/2013-03-15_15-37-09.png!
5. Once you have saved it, you should see a successful save message along with your license in green.\\
!https://lh3.googleusercontent.com/-2Ux9jpNXkO0/UUN4q9F0BxI/AAAAAAAAAFs/k7MzHruItWw/s0/2013-03-15_15-38-12.png!

### Product Configuration

To configure the product for first use:

1. Locate your license for Belong.  If you don't have your license available, you can log into our site and locate it under _My Products_.
2. In the backend of WHMCS go to _Addons_ _Belong\\
_!https://lh3.googleusercontent.com/-V43p_47OCNA/UUN5JNjTJwI/AAAAAAAAAF0/8ai8nBBFqz0/s0/2013-03-15_15-40-13.png!
3. Click on the _Configure_ link.\\
!https://lh4.googleusercontent.com/-5Djji_JFEpo/UUN6LzjR9qI/AAAAAAAAAGE/Gd9WlukrS44/s0/2013-03-15_15-44-30.png!

The configuration settings are defined as follows:

*Enable*\\
This field actually enabled or disables the product globally.

*API User*\\
This field allows you to select which admin user to make system level calls to your local WHMCS. This permits you to audit the system.

*Show Hidden Products*\\
This permits you to display products that you have set as hidden in WHMCS. This is useful to enable if you have products inaccessible to your clients. If once hidden you dont want to see them again, you can simply tick this and the product will not display in the product dropdown selection.

!https://lh3.googleusercontent.com/-wau8OLlLseg/UUN868ZwxbI/AAAAAAAAAGM/WdUAffu3_W0/s0/2013-03-15_15-56-20.png!\\
\\




Belong has settings located in the WHMCS application.

### Walk Through of Settings on WHMCS Side

#### Accessing the Settings

To access the settings for Belong on the WHMCS side, follow these simple steps.

1. Log into the back end of your Blesta application using an Administrator level account.<br />
{japopup type="image" content="media/gitdocs/jblesta/installupgrade_guide/assets/config-blesta-01.png" width="1024" title="Log Into Blesta"}
<img src="assets/config-blesta-01.png" width="100px" />{/japopup}
2. If you are installing the product at this time, click on Settings > Available Plugins and then click on Install.  If you have already installed the product and need to access the settings, click on to Settings > Available Plugins<br />
{japopup type="image" content="media/gitdocs/jblesta/installupgrade_guide/assets/config-blesta-02.png" width="1024" title="Navigate to Plugins"}
<img src="assets/config-blesta-02.png" width="100px" />{/japopup}
3. Click on Manage next to the J!Blesta plugin<br />
{japopup type="image" content="media/gitdocs/jblesta/installupgrade_guide/assets/config-blesta-03.png" width="1024" title="Manage Plugin"}
<img src="assets/config-blesta-03.png" width="100px" />{/japopup}
4. Click on the Settings link in the navigation row for J!Blesta.<br />
{japopup type="image" content="media/gitdocs/jblesta/installupgrade_guide/assets/config-blesta-04.png" width="1024" title="Select Settings"}
<img src="assets/config-blesta-04.png" width="100px" />{/japopup}

#### Initial Configuration

The first step you want to take is to configure the API connection between Blesta and Joomla.  In order for this to work you must first do the following in Joomla:

* Ensure that the System - J!Blesta plugin is activated
* Set and know what the Token is in the J!Blesta Extension Options
* Be aware of any SSL or language setting requirements in Joomla.

With those requirements set you will need to go through this process:

##### General Settings

When you go to the settings page, the first screen you will see looks similar to this one:<br />
{japopup type="image" content="media/gitdocs/jblesta/installupgrade_guide/assets/config-blesta-04.png" width="1024" title="General Settings"}
<img src="assets/config-blesta-04.png" width="100px" />{/japopup}

To start configuring the application:

1. Toggle the Enabled setting to 'Enabled'
2. Toggle the Debug setting to 'Enabled'
3. In the Joomla URL enter the Fully Qualified URL to your Joomla site.  This would be similar to http://www.yourjoomlasite.com.

<div class="alert alert-danger"><strong>Joomla URL Requirement</strong>
<p>If you don't include the scheme (http://) to your site, the API *WILL NOT CONNECT* and you will have issues.</p>
</div>

4. Enter the token you have set in Joomla in the field for Auto Auth / API Token.
5. Press the Submit button below to save these settings.

To verify that the API is connecting properly, click on the 'System Check' link on the naviation row for J!Blesta.  You should see the following display if everything is connecting properly between Blesta and Joomla:

{japopup type="image" content="media/gitdocs/jblesta/installupgrade_guide/assets/config-blesta-05.png" width="1024" title="System Check - All Good"}
<img src="assets/config-blesta-05.png" width="100px" />{/japopup}

##### User Integration

For most customers, nothing will need to be modified here.

##### Visual Integration

There are several common adjustments to make in the Visual Integration section after the API starts connecting.

1. *Enable jQuery*<br />
This setting by default will rely on the Blesta jQuery because Blesta requires the jQuery library to be embedded when the site is rendered.  For most modern Joomla! sites however, jQuery is being included in the template already and embedding it again can cause conflicts and issues.  If your Joomla! site already embeds the jQuery library, you can toggle this to 'Use Joomlas jQuery' to avoid potential Javascript conflicts, or set to Do Nothing if you are unsure if you need it or not.
2. *URL for Images / CSS / JS*<br />
For customers that have Blesta installed on a subdomain and have an SSL certificate for that subdomain but not for the domain Joomla is installed on, you will want to pay attention to this setting.  This setting permits you to set the images, css and javascript links to another, secured location so your SSL doesn't appear broken.
3. *Menu Item*<br />
After the API starts connecting, this drop down will be populated with active menu items from your Joomla site.  Select a menu item that you have created in Joomla (preferably a menu item of type JBlesta > Link Type).  This menu item you select can be configured to include modules which will then display around Blesta.
4. *Reset CSS*<br />
J!Blesta includes a reset.css file that attempts to reset styles.  For some Joomla! template / Blesta template combinations this isn't necessary, so if your Blesta content appears very crunched or out of place after integration, try disabling this setting.
5. *Show Header*<br />
Disable this setting to hide the header of the Blesta page containing the large page title and Return to Portal / Log In links. Note: This will also hide the links that appear directly beneath once logged in - be sure to provide some way for your clients to access their account details.

{japopup type="image" content="media/gitdocs/jblesta/installupgrade_guide/assets/config-blesta-06.png" width="1024" title="Visual Settings"}
<img src="assets/config-blesta-06.png" width="100px" />{/japopup}

##### Advanced Settings

Most customers won't need to modify anything in here right off the bat.  The only setting you may want to adjust would be:

* *Pass User Agent*<br />
With mod_security and certain firewall solutions, connections can be dropped if there isn't a user agent passed along by the J!Blesta when retrieving the site.  You may want to set this to Enabled if you are encountering issues getting the API to connect or are getting a 406 error code when debugging the visual settings.

{japopup type="image" content="media/gitdocs/jblesta/installupgrade_guide/assets/config-blesta-07.png" width="1024" title="Advanced Settings"}
<img src="assets/config-blesta-07.png" width="100px" />{/japopup}