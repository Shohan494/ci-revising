# ci-revising
with codeigniter once again, notes for the updated version

- In the application/config/config.php file with a text editor and set your base URL.
- If you intend to use encryption or sessions, set your encryption key.
- If you intend to use a database, open the application/config/database.php file with a text editor and set your database settings.

#### If you wish to increase security by hiding the location of your CodeIgniter files you can rename the system and application folders to something more private. If you do rename them, you must open your main index.php file and set the $system_path and $application_folder variables at the top of the file with the new name you’ve chosen.

#### For the best security, both the system and any application folders should be placed above web root so that they are not directly accessible via a browser. By default, .htaccess files are included in each folder to help prevent direct access, but it is best to remove them from public access entirely in case the web server configuration changes or doesn’t abide by the .htaccess.

## Application Flow Chart

- The index.php serves as the front controller, initializing the base resources needed to run CodeIgniter.
- The Router examines the HTTP request to determine what should be done with it.
- If a cache file exists, it is sent directly to the browser, bypassing the normal system execution.
- Security. Before the application controller is loaded, the HTTP request and any user submitted data is filtered for security.
- The Controller loads the model, core libraries, helpers, and any other resources needed to process the specific request.
- The finalized View is rendered then sent to the web browser to be seen. If caching is enabled, the view is cached first so that on subsequent requests it can be served.

#### The controller is what will become the center of every request to your web application. In very technical CodeIgniter discussions, it may be referred to as the super object. Like any php class, you refer to it within your controllers as $this. Referring to $this is how you will load libraries, views, and generally command the framework.

## View and Controller

Views are never called directly, they must be loaded by a controller. Remember that in an MVC framework, the Controller acts as the traffic cop, so it is responsible for fetching a particular view. If you have not read the Controllers page you should do so before continuing.

