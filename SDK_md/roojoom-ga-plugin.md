Roojoom Google analytics plugin
========================
Roojoom GA plugin allows adding Roojoom releted measurements to your own GA 

Installation - HTML
-----------------------

Add the code to your website: 

1. GA plugin requires an [SDK installion](/install)

2. Add ```ga('require', 'roojgaplugin');``` after your google analyics code the code should be used after initializing the tracker ```ga('create', 'UA-XXXXXXX-X', 'auto';``` and before your first event - usually ```ga('send', 'pageview');``` <br/> 
example: 

	```
	(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

  ga('create', 'UA-11111111-1', 'auto');
  ga('require', 'roojgaplugin');
  ga('send', 'pageview');
	```


3. Place the following code between ```<head> </head>``` tags in the HTML source of the page that you want to track conversions on:
	```
	<script type="text/javascript">

	   (function() {
		var site_id = '<site_id>';
		var rjgp = document.createElement('script');
		rjgp.async = true;
		rjgp.src = '//sdk.roojoom.com/jssdk/rj-ga-plugin-' + site_id + '.js';
		var script = document.getElementsByTagName('script')[0];
		script.parentNode.insertBefore(rjgp, script);
	   })();
	</script>
	```

4. Replace the ```<site_id>``` with your specific site id provided by roojoom team
	> Contact us at [support@roojoom.com](support@roojoom.com) if you don't have your site ID yet


Installation - Google tag manager
---------------------------------------

1. Select "Tags" on your right menu bar and then select "New"

	![enter image description here](http://roojoommedia.s3.amazonaws.com/docs/gtm_side_bar_small.png)

2. Select "Custom HTML tag"

	![enter image description here](http://cdn.roojoom.com/docs/gtm_custom.png)

3. Copy the following code and paste it in Configure Tag's HTML textarea:
```
	<script type="text/javascript">
	(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
	  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
	  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
	  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
	
	  ga('create', 'UA-xxxxxxxx-x', 'auto');
	  ga('require', 'roojgaplugin');
	  ga('send', 'pageview');
	
	   (function() {
	    var site_id = '<side_id>';
	    var rjgp = document.createElement('script');
	    rjgp.async = true;
	     rjgp.src = '//sdk.roojoom.com/jssdk/rj-ga-plugin-' + site_id + '.js';
	    var script = document.getElementsByTagName('script')[0];
	    script.parentNode.insertBefore(rjgp, script);
	   })();
	</script>
```
	

	- In ```ga('create', 'UA-xxxxxxxx-x', 'auto');```  replace UA-xxxxxxx-x with your Google analytics Tracking ID
	
	- Replace the ```<site_id>``` with your specific site id provided by roojoom team
	> Contact us at [support@roojoom.com](support@roojoom.com) if you don't have your site ID yet
	
![enter image description here](http://cdn.roojoom.com/docs/gtm_paste_code.png)

5. Select your trigger on "Fire On"

Dimensions
--------------

1. User visited a CJ (default to custom dimension 1) 
  
2. User filled lead gen form (default to custom dimension 2) 
  	
> The usage of each dimention is optional and can be set to use any custom dimention	
> Contact us at [support@roojoom.com](support@roojoom.com) for advance setup
