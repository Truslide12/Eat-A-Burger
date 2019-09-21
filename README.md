# Eat-A-Burger

Node Express Handlebars


Eat-Da-Burger! is a restaurant app that lets users input the names of burgers they'd like to eat.
Whenever a user submits a burger's name, your app will display the burger on the left side of the page -- waiting to be devoured.
Each burger in the waiting area also has a Devour it! button. When the user clicks it, the burger will move to the right side of the page.
Your app will store every burger in a database, whether devoured or not.

App Setup:

The following npm packages are required inside of the server.js file:

express

DB Setup:

Inside the burger directory, there is a folder named db.
In the db folder, a file named schema.sql writes SQL queries that do the following:

Create the burgers_db.

Switch to or use the burgers_db.

Create a burgers table with these fields:

id: an auto incrementing int that serves as the primary key.

burger_name: a string.

devoured: a boolean.

The seeds.sql file inserts queries to populate the burgers table with at least three entries for the initial run. Once running the database will keep track of all burgers inputed and devoured utilizing mysql.


Config Setup:

Inside the burger directory is a folder named config.
It creates to the connection.js file inside config directory.

Inside the connection.js file is the setup code to connect Node to MySQL which is exported.



ORM configuration:

Import (require) connection.js into orm.js

In the orm.js file are the methods that will execute the necessary MySQL commands in the controllers. These are the methods you will need to use in order to retrieve and store data in the database.

selectAll()
insertOne()
updateOne()

Export the ORM object in module.exports.


Model setup:

Inside the burger directory is a folder named models.


In models, there is a burger.js file.
Inside burger.js,  orm.js is imported into burger.js and the code that will call the ORM functions using burger specific input for the ORM.
These functions are exported at the end of the file.


Controller setup:

Inside the burger directory is a folder named controllers.
In controllers is the burgers_controller.js file.
Inside the burgers_controller.js file, we import the following:

Express
burger.js

the router is exported at the end of the file.



View setup:

Inside the burger directory is a folder named views.

The index.handlebars file is inside views directory.

The layouts directory is inside views directory.

The main.handlebars file is inside the layouts directory.
The main.handlebars file is setup so it's able to be used by Handlebars.
The index.handlebars is setup to have the template that Handlebars can render onto.
The button in index.handlebars will submit the user input into the database.





Directory structure

All the recommended files and directories from the steps above should look like the following structure:

.
├── config
│   ├── connection.js
│   └── orm.js
│ 
├── controllers
│   └── burgers_controller.js
│
├── db
│   ├── schema.sql
│   └── seeds.sql
│
├── models
│   └── burger.js
│ 
├── node_modules
│ 
├── package.json
│
├── public
│   └── assets
│       ├── css
│       │   └── burger_style.css
│       └── img
│           └── burger.png
│   
│
├── server.js
│
└── views
    ├── index.handlebars
    └── layouts
        └── main.handlebars







