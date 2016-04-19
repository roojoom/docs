Roojoom player lead genenration form integration
================================================

Installation
-------------

1. paste this code:

	```
	<script type="text/javascript">
   (function() {
      	if(!document.getElementById('rjFormsScript')){ var a = []; var b = document.createElement('script'); b.async = true; b.id = 'rjFormsScript'; b.type = 'text/javascript'; b.charset = 'UTF-8'; b.src = '//sdk.roojoom.com/static/js/rj_lead_gen.js'; document.head.appendChild(b); } 
	   })();
	</script>
	```
2. place your code between ```<head> </head>```
 tags in the code of the page that you want track conversions on

Usage
-----
1. init rjForms:

    ```
    <script>
        window.addEventListener('load', function(){ rjForms.init([{options}]) })
    </script>
    ```

2. Pass options as object in rjForm.init() 
    ex. ```rjForms.init({defaultForm: document.forms['cta_lead_gen_form']})```

API
-------
* rjForms.init([{options}]) - setup form integration - will try to automatically detect the form if not given.  
* rjForms.submit() - send form input fields to the player automation layer and will close the popup if opened.
* rjForms.isValid() - validate form according to HTML5 rules and return boolean result.

Init Options
-------
* defaultForm: (Default: document.forms[0]): a Javascript selector for form (should be used if there's more then one                form in the page)
* isValidateForm (Default: false): if set to true rjSendForm() will validate fields before sending
* requiredError (Default: 'This field is required'): Error message for requeird fields (if validate = true) 
* invalidEmailError (Default: 'Please enter valid Email'): Error message for requeird fields (if validate = true)
* setErrors: function(errors) {
    for (var err = 0; err < errors.length; err++) {
        var field = document.getElementsByName(errors[err].field)[0];
        rjForms.setErrorField(field, errors[err].error)
    }
},
    
        
        