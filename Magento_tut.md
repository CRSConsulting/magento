# Magento Tutorial Summaries

### Create custom theme with tutorial from `https://www.youtube.com/watch?v=BdS2ppmpBxs`;
1. To create front-end customized theme create folder `/app/design/frontend/bmodern/customtheme/`
	a. create `registration.php`
	```
	<?php 

	\Magento\Framework\Component\ComponentRegstrar::register(
		type: \Magento\Framework\Component\ComponentRegistrar::THEME,
		componentName: 'frontend/bmodern/customtheme',
		path: __DIR__
	);
	```
	b. create `theme.xml`
	```
	<theme xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="urn:magento:framework:Config/etc/theme.xsd">
		<title>Custom Theme</title>
		<parent>Magento/luma</parent>
	</theme>
	```
	c. in case you need to sell, create `compose.json`
	```
	{
		"name": "bmodern/custom-theme",
		"description": "N/A",
		"require": {
			"magento/theme-frontend-luma": "100.1.*",
			"magento/framework": "100.1.*"
		},
		"type": "magento2-theme",
		"version": "1.0.0",
		"autoload": {
			"files": [
				"registration.php"
			]
		}
	}
	```
	d. `theme/frontend-luma`
	e.	magenta admin panel - content - design-configuration and apply newly created theme
	```
	hit EDIT -> CUSTOM THEME -> save configuration
	```

2. CUSTOM LOGO
	a. Create under `customtheme/web/images`, put image here
