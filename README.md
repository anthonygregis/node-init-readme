# Node Learning

### Steps to initialize Node Project

1. Make your directory for the project
2. CD into that directory
3. npm init in that directory and fill out information

#### NPM Init

NPM Init initializes your node project in a directory and asks some starting questions to build your package.json for your project

#### Package.json

This is the brains of your project, it keeps things organized and allows others to easily download your project and install all necessary modules to run this project / server. It also keeps track of current version, project name, description, and author.

#### Import Modules / Packages

To import a module (or package) to your javascript file you can use require() to import the module you installed with npm i or from an exported module in your code. 

#### .gitignore

This file is critical to ensuring that you don't upload any of your companies or your own pesky secret keys or passwords. It's also very useful for ignoring the node_modules folder that gets created when installing modules from a project. The usecase for this file will grow as we learn and use it for other things like .ENV files and others.

# SQL

##### CREATE DATABASE

`CREATE DATABASE databaseName;`

##### CREATE TABLE

```
CREATE TABLE customers (
id SERIAL PRIMARY KEY,
name TEXT,
phone VARCHAR(15),
address TEXT
);
```

##### INSERT INTO TABLE

```
INSERT INTO customers
(name, phone, address)
VALUES
('Anthony', '333-444-4444', '123 Main St.');
```

##### MODIFYING TABLE COLUMNS

Add Column
`ALTER TABLE customers ADD COLUMN date DATE;`

Drop Column
`ALTER TABLE customers DROP date;`

# EXPRESS

##### Declare and Initialize instace of Express

```
const express = require('express')
const app = express()
```

##### Setup Express server and listen on a port

```
app.listen(8000, () => {
  console.log("Server up and listening on port 8000")
})
```

##### Express Router - Serves messages or files went specific path is hit

```
app.get('/', function(req, res) {
  res.send("You are on the home page")
})
```

##### EJS Layouts

Allows for content to be served with javascript mixed HTML files that end in extension .ejs, layouts allows for a template page to be setup with a template placeholders that can be served with dynamic content from different endpoints.

```
var express = require('express');
var app = express();
var ejsLayouts = require('express-ejs-layouts');

app.set('view engine', 'ejs');
app.use(ejsLayouts);

app.get('/', function(req, res) {
    res.render('home');
});
```

##### Express Controllers

Express has the ability for use to use a router to split endpoints up in different files and append those partial url endpoints to a prefixed url segment. An example usage would be for a blog and having the blog prefixed url segment be /blog and have multiple routes inside that part.

```
var express = require('express');
var router = express.Router();

router.get('/animals', function(req, res) {
  res.render('faves/animals', {title: 'Favorite Animals', animals: ['sand crab', 'corny joke dog']})
});

module.exports = router;
});
```
