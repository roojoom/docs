Roojoom Conversion pixel
===================
Roojoom conversion pixel enables you to track and enhance your analytics, by combining conversion tracking into the overall data that roojoom uses for its optimization.


Installation
-------------

Add the pixel to your website: 

1. Place the following code between ```<head> </head>``` tags in the HTML source of the page that you want to track conversions on:
	```
	<script type="text/javascript">
	var _rjpxl = window._rjpxl || [];
	_rjpxl.push({'action': 'conversion', 'name': '<goal_name>'[, 'value': <value>]});
	
	   (function() {
	      	var site_id = <site_id>;
	var rjpx = document.createElement('script');
	rjpx.async = true;
	rjpx.src = '//sdk.roojoom.com/jssdk/rjpixel-' + site_id + '.js';
	var script = document.getElementsByTagName('script')[0];
	script.parentNode.insertBefore(rjpx, script);
	   })();
	</script>
	```

2. Replace the ```<site_id>``` with your specific site id provided by roojoom team
	> Contact us at [support@roojoom.com](support@roojoom.com) if you don't have your site ID yet

3. Replace the ```<goal_name>``` with a name you can easily track and distinguish
    > **Note:**  
    > - Goal name must start with a letter
    > - The rest of the name can contain any combination of letters or numbers 
    > - Spaces are not allowed, you can separate words using '_'    
    
4. *optional: set the value for conversion by replacing `<value>` with a number 


