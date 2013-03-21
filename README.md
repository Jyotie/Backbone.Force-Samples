Backbone.Force Samples
======================

This repository contains a range of single page JavaScript apps that work with Backbone.Force.

The apps use [backbone.force.js](https://github.com/metadaddy-sfdc/Backbone.Force/blob/remotetk/backbone.force.js) from [Pat Patterson's fork of Piotr Walczyszyn's Backbone.Force](https://github.com/metadaddy-sfdc/Backbone.Force/tree/remotetk) (note - the link is to the **remotetk** branch) as it contains fixes necessary for the following samples to work. The backbone.force.js file is included in [resources.zip](https://github.com/developerforce/Backbone.Force-Samples/blob/master/resources.zip) alongside forcetk.js, backbone.js, and other JavaScript, CSS and image files you need to run the samples.

Simple Account Samples
----------------------

Each of these samples implements the same basic app, a simple Account browser that lists all the Account records that you are able to read. You can add a new account, click an existing account to view and modify its Name and Industry fields, and remove Accounts.

### SimpleAccountForceTK.page

Simple Account CRUD from Visualforce with ForceTK. This approach consumes API calls in your org, but is easier to setup than the RemoteTK option.

You can install an [unmanaged package containing both Visualforce Sample apps](https://login.salesforce.com/packaging/installPackage.apexp?p0=04ti0000000UHfa). The package includes two Force.com apps. Selecting either of them from the app menu will take you straight to the sample page.

If you prefer, you can clone this git repository and upload the following files to an org:

* [resources.zip](https://github.com/developerforce/Backbone.Force-Samples/blob/master/resources.zip) - Static Resource
* [SimpleAccountForceTK.page](https://github.com/developerforce/Backbone.Force-Samples/blob/master/SimpleAccountForceTK.page) - Visualforce Page

### SimpleAccountRemoteTK.page

Simple Account CRUD from Visualforce with RemoteTK. This approach uses [JavaScript Remoting](http://www.salesforce.com/us/developer/docs/pages/Content/pages_js_remoting.htm) and requires a Visualforce Component and Apex Class as support, but does not consume API calls.

As mentioned above, you can install an [unmanaged package containing both Visualforce Sample apps](https://login.salesforce.com/packaging/installPackage.apexp?p0=04ti0000000UHfa).page, or, if you prefer, you can clone this git repository and upload the following files to an org:

* [resources.zip](https://github.com/developerforce/Backbone.Force-Samples/blob/master/resources.zip) - Static Resource
* [SimpleAccountRemoteTK.page](https://github.com/developerforce/Backbone.Force-Samples/blob/master/SimpleAccountRemoteTK.page) - Visualforce Page

You will also need the following files from the [Force.com JavaScript REST Toolkit](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit).

* [RemoteTKController.cls](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit/blob/master/RemoteTKController.cls) - Apex Class
* [RemoteTK.component](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit/blob/master/RemoteTK.component) - Visualforce Component

### SimpleAccountWebApp.html

Simple Account CRUD from a web page outside Force.com - e.g. Heroku, or an on-premise system. You can [try it out on Heroku](https://fast-wave-7789.herokuapp.com/); log in with credentials for any org that has access to Accounts (e.g. Developer Edition, Sales or Service Cloud). We strongly recommend you do NOT test this app on production data!

To run the sample yourself, you will need to unzip resources.zip into your web app directory. To work around the [JavaScript Same-origin policy](https://developer.mozilla.org/en-US/docs/JavaScript/Same_origin_policy_for_JavaScript), you will need to run an HTTP proxy on the same protocol/host/port as SimpleAccountWebApp.html. You can use [proxy.php](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit/blob/master/proxy.php) (from the [Force.com JavaScript REST Toolkit](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit)) if you are working in PHP.