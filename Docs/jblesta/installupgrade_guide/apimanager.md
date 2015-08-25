---
title: J!Blesta - Using the API Connection Manager
breadcrumb: /jblesta:J!Blesta/installupgrade_guide:Install and Upgrade Guide/apimanager:Using the API Connection Manager/

---

### Using the API Connection Manager

The API Connection Manager in Joomla is an easy to use, intuitive feature of J!Blesta allowing you to quickly setup and diagnose your API connection between Joomla and Blesta.

### Accessing the API Connection Manager

To access the API Connection Manager, follow these steps:

1. Log into your Joomla backend using an account with Super User privileges.
2. Navigate to _Components_ > _J!Blesta_.
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

As you enter data into the API Connection Manager in Joomla!, the system will make a call to test the values out.  You will be notified at each step of the way the results of your data entry.  The most common responses are as follows:

<div class="container">
	<div class="row">			
		<div class="col-sm-3 center alert alert-success">
			Successfully Connected
		</div>
		<div class="col-sm-9">
			This indicates that J!Blesta was able to communicate with Blesta as expected with the settings provided
		</div>
	</div>
	<div class="row">			
		<div class="col-sm-3 center alert alert-warning">
			401 Denied
		</div>
		<div class="col-sm-9">
			The API Username and API Key don't match up with your settings in Blesta.  Double check them and try again.
			<div class="alert alert-warning">
				<strong>Running PHP in CGI Mode?</strong><br />
				Update your .htaccess file to pass an environment variable to Blesta so it can capture the basic authentication details as per the following snippet:<br />
				<pre>RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]</pre><br />
				For more information please visit [Blesta API Documentation](http://docs.blesta.com/display/dev/API)
			</div>
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
		<div class="col-sm-3 center alert alert-danger">
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
