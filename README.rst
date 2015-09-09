Django SEO Admin
================

Django SEO Admin is the app for apply SEO on your websites with Django.

Installing
----------

Via pip::

	pip install django-seo-admin

Quick start
-----------

1. Include the app 'seo' to INSTALLED_APPS in the settings.py::

	INSTALLED_APPS = (
		'seo',
	)
		
2. Apply migration with migrate for registry the model of django-seo-admin::

	python manage.py migrate

3. Sign in to Admin of Django and load record to the model 'Seo admins'::
	
	Fields are:

	Type: Meta, title, etc.
	Is_property: If tag contains property "property", otherwise contains property "name"
	Field: Value of property. For example, the property name contains value "keywords"
	Content: Contains of property. For example, for keywords contains values "django, web, framework"

Example

.. image:: https://github.com/mapeveri/django-seo-admin/blob/master/img/example.png

4. In the template::
	
	<!DOCTYPE html>
	<html>
		<head>
			<meta charset="UTF-8">
			<meta name="viewport" content="width=device-width, initial-scale=1.0">
			{% load tag_seo_admin %}
			{% get_metadata %}
		</head>
		<body>
			<h1>Django Seo Admin</h1>
		<body>
 	</html>


             

5. Run server
