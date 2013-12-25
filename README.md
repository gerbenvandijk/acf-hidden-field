acf-hidden-currentdate-field
================

Hidden Current Date field type for Advanced Custom Fields
This adds a field that stores the current date and time every time the field gets saved.

##A use case scenario:

A website of mine uses an option page for each custom post type, that contains settings for the archive page of the custom post type. 
Hence the site relies heavily on caching, I use this hidden date field to detect if the page has changed recently, and therefor clear the cache for the specific archive.

##Usage:

Simply include the file in your functions.php like this:

```
	
	function my_register_fields() {
	
		include_once('acf-hidden-field.php');
	
	}

	add_action('acf/register_fields', 'my_register_fields');
	
```

After this you can use the field like any other field in your templates:
```

	the_field('hidden_date_services_archive', 'options');

```