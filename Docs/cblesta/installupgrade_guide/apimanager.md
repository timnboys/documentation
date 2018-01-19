---
title: C!Blesta - Using the API Connection Manager
breadcrumb: /cblesta:C!Blesta/installupgrade_guide:Install and Upgrade Guide/apimanager:Using the API Connection Manager/

---

### Using the API Connection Manager

The API Connection Manager in Modx/Concrete5 is an easy to use, intuitive feature of C!Blesta allowing you to quickly setup and diagnose your API connection between Modx/Concrete5 and Blesta.

### Accessing the API Connection Manager

To access the API Connection Manager, follow these steps:

1. Log into your ModX/Concrete5 backend using an account with Super User privileges.
2. Navigate to _Components_ > _C!Blesta_.
3. Click on the _API Connection_ button on the main screen.

### Configuring the API

After the initial installation of the product, all the fields will be blank.  You will want to fill out the form in it's entirety.

<div class="container">
	<div class="row">			
		<div class="col-sm-3 center bg-info">
			Blesta URL
		</div>
		<div class="col-sm-9">
			This is the complete URL to the FRONT END of your Blesta installation.  Note that you should not include the API end point or point to the admin folder.
		</div>
	</div>
	<div class="row">			
		<div class="col-sm-3 center bg-info">
			API Username
		</div>
		<div class="col-sm-9">
			This is a username for an account in Blesta that has API Access.  Please check [Create An API User in Blesta|Create An API User in Blesta] for more information.
		</div>
	</div>
	<div class="row">			
		<div class="col-sm-3 center bg-info">
			API Key
		</div>
		<div class="col-sm-9">
			This is the key that is generated for the API user you entered above.
		</div>
	</div>
</div>


### API Responses

As you enter data into the API Connection Manager in ModX/Concrete5!, the system will make a call to test the values out.  You will be notified at each step of the way the results of your data entry.  The most common responses are as follows:

<div class="container">
	<div class="row">			
		<div class="col-sm-3 center alert alert-success">
			Successfully Connected
		</div>
		<div class="col-sm-9">
			This indicates that C!Blesta was able to communicate with Blesta as expected with the settings provided
		</div>
	</div>
	<div class="row">			
		<div class="col-sm-3 center alert alert-warning">
			401 Denied
		</div>
		<div class="col-sm-9">
			The API Username and API Key don't match up with your settings in Blesta.  Double check them and try again.
		</div>
	</div>
	<div class="row">			
		<div class="col-sm-3 center alert alert-warning">
			403 Restricted
		</div>
		<div class="col-sm-9">
			If this is encountered, you may have restrictions added to your .htaccess file in your Blesta installation folder.
		</div>
	</div>
	<div class="row">			
		<div class="col-sm-3 center alert alert-warning">
			404 Not Found
		</div>
		<div class="col-sm-9">
			Just as it suggests, the URL you entered isn't found - you may want to double check it
		</div>
	</div>
	<div class="row">			
		<div class="col-sm-3 center alert alert-danger">
			0 Received
		</div>
		<div class="col-sm-9">
			This is always a firewall issue.  If you enter a URL into the field and receive a zero response, then your server has either blacklisted itself or is not permitting access through the firewall for another reason.  Please consult your hosting provider for more information on troubleshooting this issue.
		</div>
	</div>
</div>

<div class="alert alert-warning">
	<strong>Running PHP in CGI Mode?</strong><br />
	Update your .htaccess file to pass an environment variable to Blesta so it can capture the basic authentication details as per the following snippet:<br />
	<pre>RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]</pre>
	For more information please visit <a href="http://docs.blesta.com/display/dev/API" target="_blank">Blesta API Documentation</a>
</div>