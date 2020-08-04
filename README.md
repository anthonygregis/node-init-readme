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
