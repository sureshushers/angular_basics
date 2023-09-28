# angular_basics

Bootstaping: Is the processs of initializing the app
app-root: ng serve: Angular CLI saves the compile Angular app in the memory and directly starts it. If we make changes to Angular App, the cli will re-compile the code in memory and update the files and serve the app in the memory. Also, the ng serve injects the bundle js scripts in the index.html file. However, you'll not see the same if you use ng serve.
However, inorder to get the compiled dist folder for the prod ready state of the app, we need to build the app.

-- Webpack is abundler which merges the files and make it as one js file. It is a module bundler.

## Building the Angular App:

-- Run the command ng build
-- Building injects the following script files in index.html

# runtime.\*\*\*.js

-- Webpack runtime file

# polyfill.\*\*\*.js

-- Support for browsers that are old. This is to make old browser compatible.

# main.\*\*\*.js

-- Code of the application.

# vendor.js

-- 3rd party library files.

# styles.\*\*\*.css

# index.html

- This is the loading
  when the index.html file is loaded, Angular core libraries and third oparty libraries are also loaded by that time.

- When you execute the angular app, the entry poiint is main.ts file. The angular compiler knows this thru the entry in angular.json config file.
- platformnBrowserDynamic() method in main.ts file is responsible to load the angular app while loading. The platformbrowserdynamic is responsible to load the angular app in the desktop browser, which in turn loads AppModule which inturn loads the <app-root><app-root>.

## Angular Project --> index.html->angular.json->main.ts ->AppModule->AppCompnent ->View template (app.component.html) 

## App Module: 
declarations []: TSpecify the components, directive and pipes which are required for this module to work.
imports: List all the external modules which is required for the module to work.
providers: Register all the services that are required.
Bootstrap[]: Specify the component that needs to be loaded when the appmodule is loaded.


# What is Component:
- Component is a piece of user interface.
- Every angular app has one component called root component or app component
- The root component has child component.
- 
