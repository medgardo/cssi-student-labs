# Full Webapp - Student Reference
This is a working but simple full application. Use this when you get stuck or are just starting to build your own app. 

Ideally, you can use this reference less an less often as you start to commit some of these pieces to memory - or better yet, get used to reading the documentation about GAE, Jinja and Datastore online. 

## Running the App

* Run this app by typing `dev_appserver.py app.yaml` into the terminal. 
* Then direct your browser to `localhost:8000`.
* You should see the response that is generated by the FoodHandler.
* To stop the server, use <kbd>Ctrl</kbd> + <kbd>C</kbd>.

## Templating

* In order for data to be passed to static HTML pages, the jinja2 library needs to be used.
* Variables get passed to templates as a dictionary of variables. This dictionary is passed in the templates `.render()` method.
* In the `.html` templates, you can use double curly brackets `{{key}}` to access that dictionary. 
* In jinja tempaltes, you can use logic, but Jinja2 has different syntax than Python or Javascript. Be sure to read the (docs)[http://jinja.pocoo.org/docs/2.10/templates/].

## Static Directories
To host static files (images, JavaScript files, stylesheets), place those files in a directory (folder) and then declare that directory as "static" in the `app.yaml` configuration file. 

## Using the Admin Console
* You can go the Admin Console by going to `localhost:8081`.
* The Interactive Console is a good place to interact with the Datastore. Remember that the entities you create in the Interactice Console persist, so you can always delete any test objects by using the Datastore Viewer. Don't forget to flush the memcached data.

## Persisting Data
* Define Model classes in the `models.py` file.
* Model classes need to be imported into `main.py` if they are to be used there.
* To add a Entity to the datastore from `main.py`, use the `.put()` method.

## Getting Data
* To query data that already exists in the datastore, the `query()` method will pull up a Query object, and the `fetch()` method will actually grab the results. 
* You can use `filter()` and `order()` to restrict and sort the data. 

