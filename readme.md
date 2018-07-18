reSlim
=======
[![Coverage](https://img.shields.io/badge/coverage-100%25-brightgreen.svg)](https://github.com/aalfiann/reSlim)
[![reSlim](https://img.shields.io/badge/stable-1.12.0-brightgreen.svg)](https://github.com/aalfiann/reSlim)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/aalfiann/reSlim/blob/master/license.md)

reSlim is Lightweight, Fast, Secure, Simple, Scalable, Flexible and Powerful rest api framework.<br>
reSlim is based on [Slim Framework version 3](http://www.slimframework.com/).<br>

Features:
---------------

1. User management system
2. File management system
3. Pages management system
4. Backup management system
5. Package management system
6. Token and API Key management system
7. Auto log and trace error message
8. Pagination json response
9. Support Multi Language
10. Server Side Caching to handle high traffic
11. Scalable architecture with modular concept
12. Load Balancer with multiple database server (master to master or master to slave)
13. Etc


Extensions:
---------------
- **Modules**  
Here is the available modules created by reSlim author >> [reSlim-modules](https://github.com/aalfiann/reSlim-modules).

- **UI Boilerplate**  
Here is the basic UI template for production use with reSlim >> [reSlim-ui-boilerplate](https://github.com/aalfiann/reSlim-ui-boilerplate).

System Requirements
---------------

1. PHP 5.5 or newer (last tested on PHP7.3)
2. MySQL 5.6 or MariaDB
3. Web server with URL rewriting
4. Apache Server (Better to use Apache + Reverse Proxy NGINX)

Getting Started
---------------

### I. Installation
1. Get or download the project
2. Extract then rename folder **reSlim-master** to **reslim**
3. Open shell or CMD then go to **src** folder
    ```
    cd reslim/src
    ```
    
4. Install it using Composer  
    ```
    composer install
    ```
5. Done

### II. Connection Database
1. Create Database name reslim in your MySQL/MariaDB
2. Execute or restore **reSlim.sql** which is located at **resources/database/** folder
3. Edit **config.php** which is located at **src/** folder  
    Just only this part,
    ```
    $config['db']['host']   = 'localhost';
    $config['db']['user']   = 'root';
    $config['db']['pass']   = 'root';
    $config['db']['dbname'] = 'reSlim';
    ```
    You can set the rest config later

4. Done

### III. Test
1. Open your browser and visit >> http://localhost:1337/reslim/src/api/

Note: 
    - My apache server is run on port 1337.

### IV. Development
**How to create new app or modules?**  
You can learn from documentation here >> [Tutorial Create Module](https://github.com/aalfiann/reSlim/wiki/Tutorial-Create-Module).  
Or learn directly from this very simple project on [Github.com](https://github.com/aalfiann/reSlim-modules-first_mod).

### V. Deployment
1. Upload all files inside folder src to your server
2. Backup local database and then restore to your server database online
3. Done


  
Learn more deeply
-----------------
### * Documentation
reSlim documentation is available on [Wiki](https://github.com/aalfiann/reslim/wiki).

### * Learn from test router
We created several simple function on the **test.router.php** which is located at **src/router/**.  
You can learn from there 

### * Use Postman for learn or test purpose
I recommend you to use PostMan an add ons in Google Chrome to get Started with test.

1. Import reSlim.sql in your database then config your database connection in config.php inside folder **reSlim/src/**
2. Import file **reSlim User.postman_collection.json** in your PostMan.
3. Edit the path in PostMan. Because the example test is using my path server which is my server is run in http://localhost:1337 
    The path to run reSlim is inside folder api.<br> 
    Example for my case is: http://localhost:1337/reslim/src/api/<br><br>
    In short, It's depend on your server configuration.
4. Then you can do the test by yourself

### * Learn Slim Framework 3
reSlim is based from Slim Framework 3.  
Learning Slim Framework 3 will make you easy to understand about reSlim project.


### * The concept authentication in reSlim
1. Register account first
2. Then You have to login to get the generated new token

The token is always generated new when You relogin and the token is will expired in 7 days as default.<br>
If You logout or change password or delete user, the token will be clear automatically.

  
How to Contribute
-----------------
### Pull Requests

1. Fork the reSlim repository
2. Create a new branch for each feature or improvement
3. Send a pull request from each feature branch to the develop branch