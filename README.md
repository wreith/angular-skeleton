angular-skeleton [![Build Status](https://travis-ci.org/wreith/angular-skeleton.svg?branch=master)](https://travis-ci.org/wreith/angular-skeleton)
================

Angular-Skeleton is starter kit for building [AngularJS](https://angularjs.org) application.

## Getting Started

### Prerequisites

You must have [node.js](http://nodejs.org/) and npm installed before going further.

This project uses several node.js tools and has been tested with a version of 1.4.21 of npm.

You will also need [gulp](http://gulpjs.com/) to run tasks

```
npm install -g gulp
```

and [bower](http://bower.io) to manage web dependencies.

```
npm install -g bower
```

### Installation

You can get started by cloning this project

```
git clone https://github.com/wreith/angular-skeleton.git
cd angular-skeleton
```

You can install dependencies by simply run the following command:

```
npm install
```

This command is also configured to:

* Install bower components
* Update protractor webdriver-manager


## How to use this project ?

### Project layout

```
|
+- .tmp                            --> automatically generated
|                                      will contain compiled files (.scss -> .css) 
+- app                 
|   +- index.html                  --> application main template file 
|   +- bower_components            --> web dependencies
|   +- assets
|       +- scss                    --> scss files
|           +- clear.css
|       +- img                     --> images files
|   +- components
|       +- app.js                  --> application declaration and dependencies
|       +- home
|           +- partials
|               +- index.html      --> html partial used by home controller
|           +- src
|               +- home.js         --> home module declaration and dependencies
|               +- homeCtrl.js     --> home controller
|           +- tests               --> unit testing for home module
|               +- home.spec.js
|       +- route
|           +- src
|               +- route.js        --> route module declaration and dependencies
|               +- routeConfig.js  --> route configuration
|           +- tests               --> unit testing for route module
|               +- route.spec.js
|       +- foo                     --> another module
|           +- ...
+- dist                            --> build directory 
+- test                            --> E2E testing
    +- protractor.conf.js          --> Protractor configuration file for E2E tests
    +- scenarios                   --> specifications for E2E
        +- myapp.specs.js

```

### Run the project

Once the installation is done, just run:

```
gulp
```

The default task performs several instructions:

* it creates a server on port 8000. You can access it [here](http://localhost:8000)
* it generates css file
* it executes jshint
* it executes unit testing
* it watches every files and performs a livereload


### End-2-End testing

Before running E2E tests, you need to start the selenium webdriver-manager:

```
gulp webdriver-start
```

This is simply a shortcut to
 
```
node_modules/protractor/bin/webdriver-manager start
```

Open a new shell and then run:

```
gulp e2e
```

E2E tests are executed on a new server on port 8001 with the dist folder as its root directory.
It uses by default Chrome browser.

Enjoy ! =)
