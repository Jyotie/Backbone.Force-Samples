Backbone.Force Samples
======================

This repository contains a range of single page JavaScript apps that work with Backbone.Force.

The apps use [backbone.force.js](https://github.com/metadaddy-sfdc/Backbone.Force/blob/remotetk/backbone.force.js) from [Pat Patterson's fork of Piotr Walczyszyn's Backbone.Force](https://github.com/metadaddy-sfdc/Backbone.Force/tree/remotetk) (note - the link is to the **remotetk** branch) as it contains fixes necessary for the following samples to work. The backbone.force.js file is included in resources.zip alongside forcetk.js, backbone.js, and other JavaScript, CSS and image files you need to run the samples.

SimpleAccountForceTK.page
-------------------------

Simple Account CRUD from Visualforce with ForceTK. This approach consumes API calls in your org, but is easier to setup than the RemoteTK option.

You will need to upload resources.zip as a static resource.

SimpleAccountRemoteTK.page
--------------------------

Simple Account CRUD from Visualforce with RemoteTK. This approach uses [JavaScript Remoting](http://www.salesforce.com/us/developer/docs/pages/Content/pages_js_remoting.htm) and requires a Visualforce Component and Apex Class as support, but does not consume API calls.

As well as uploading resources.zip as a static resource, you will need to upload [RemoteTKController.cls](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit/blob/master/RemoteTKController.cls) and [RemoteTK.component](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit/blob/master/RemoteTK.component) (from the [Force.com JavaScript REST Toolkit](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit)) to your org as an Apex Class and Visualforce Component respectively.


SimpleAccountWebApp.html
------------------------

Simple Account CRUD from a web page outside Force.com - e.g. Heroku, on-premise system. You will need to unzip resources.zip  and into your web app's directory. To work around the [JavaScript Same-origin policy](https://developer.mozilla.org/en-US/docs/JavaScript/Same_origin_policy_for_JavaScript), you will need to run an HTTP proxy on the same protocol/host/port as SimpleAccountWebApp.html.

You can use [proxy.php](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit/blob/master/proxy.php) (from the [Force.com JavaScript REST Toolkit](https://github.com/developerforce/Force.com-JavaScript-REST-Toolkit)) if you are working in PHP.