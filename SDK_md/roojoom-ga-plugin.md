Roojoom Google analytics plugin
========================
Roojoom GA plugin allows adding Roojoom releted measurements to your own GA 

Installation
-------------

Add the code to your website: 

1. GA plugin requires an [SDK installion](/install)

2. Place the following code between ```<head> </head>``` tags in the HTML source of the page that you want to track conversions on:
	```
	<script type="text/javascript">

	   (function() {
		var site_id = <site_id>;
		var rjgp = document.createElement('script');
		rjgp.async = true;
		rjgp.src = '//sdk.roojoom.com/jssdk/rj-ga-plugin-' + site_id + '.js';
		var script = document.getElementsByTagName('script')[0];
		script.parentNode.insertBefore(rjgp, script);
	   })();
	</script>
	```

3. Replace the ```<site_id>``` with your specific site id provided by roojoom team
	> Contact us at [support@roojoom.com](support@roojoom.com) if you don't have your site ID yet
	

Dimentions
----------

1. User visited a CJ (default to custom dimention 1) 
  
2. User filled lead gen form (default to custom dimention 2) 
  	
> The usage of each dimention is optional and can be set to use any custom dimention	
> Contact us at [support@roojoom.com](support@roojoom.com) for advance setup
