# Polymer Starter Kit --Jag Modified

Demo: https://jstarter-73767.firebaseapp.com

The PRPL pattern, in a nutshell:

* **Push** components required for the initial route
* **Render** initial route ASAP
* **Pre-cache** components for remaining routes
* **Lazy-load** and progressively upgrade next routes on-demand

### Setup

##### 1.Prerequisites

Install [polymer-cli](https://github.com/Polymer/polymer-cli):

    npm install -g polymer-cli
    npm install -g firebase-tools

##### 2.Install

    bower install

##### 3.Start the development server

This command serves the app at `http://localhost:8080` and provides basic URL
routing for the app:

    polymer serve --open


##### 4.Build

    polymer build

### Preview the build

Minified Version :

    polymer serve build/bundled
    
For HTTP2 :

    polymer serve build/unbundled



##### 5.Deploy (in Firebase)

    firebase init

What do you want to use as your public directory? `build/bundled`


    firebase deploy


Thats all you are done!!

Open your Hosting URL: https://<firebase-app-name>.firebaseapp.com


---
### Run tests

This command will run
[Web Component Tester](https://github.com/Polymer/web-component-tester) against the
browsers currently installed on your machine.

    polymer test

### Adding a new view

You can extend the app by adding more views that will be demand-loaded
e.g. based on the route, or to progressively render non-critical sections
of the application.  Each new demand-loaded fragment should be added to the
list of `fragments` in the included `polymer.json` file.  This will ensure
those components and their dependencies are added to the list of pre-cached
components (and will have bundles created in the fallback `bundled` build).
