# Course-Management-System-Frontend
This is the frontend of Course Management System.

#Commands Description :
ng new Course-Management-System-Frontend :
This command creates a new angular application. It generates a bunch of files and folders and then it uses npm to download third party libraries.

ng serve: Using Angular CLI to load our application in web server. We then get a live deleopment server listening on certain port ( Eg: 4200). And Angular CLI also compiles our application. It generates bundles for javascript and css files.

#My personal Choice of Editor: 
Visual Studio Code : Its a cross-platform lightweight editor. There are other editors too, like Sublime, Atom.

#Structure of Angular Application : 
e2e Folder : We write end to end test for our application in this folder. These are basically
automated test that simulate a real user. So, we can write code to launch our browser, navigate to the homepage of our application, click a few links here and there, fill out a form, click a button and then assert that there is something on the page. This is the example of an e2e test.

node_modules: This is where we store all the third party libraries that our application may depend upon. This folder is purely for development. So, when we compile our application, parts of this third party library are put in a bundle and deployed in the application. So, we dont deploy node_modules folder to server.

src Folder: This is where we have the actual source code of our application. It consists of following files and folders:

app folder : has module and component. Every application has atleast one module and one component.

assets folder: Here, we store static assets of our application like image file,text files, icons...

environments folder: Here we store configuration settings for different environments. So, we have one file for production environment and other file for development environment.

Favicon: It is the icon displayed in the browser.

index.html : It is a very simple html file that contains our angular application. It does not have reference to our scripts or stylesheet, these references will be dynamically inserted into this page.

main.ts : This is basically the starting point of our application. It has the similar concept of main method which is the starting point of the program.
In this typescript file, we bootstrap the main module of our application ( AppModule). So, Angular loads this module and everything else starts from there. 

polyfills.ts : It basically imports some scripts required for running angular. Because angular framework uses feature of Javascript that are not available in the current version of JS supported by most browsers. So, polyfills fills the gap between the features of JS that Angular needs and the features supported by current browser.

styles.css : Here we add the global styles for our application. 

test.ts : It is basically used for setting up our test environment.

Outside source folder, we have : 

.angular-cli.json : This is the configuration file for angular cli. Its a preety standard configuration file, so we dont need to worry about it for the most part.

.editorconfig : If we are working in a team environment, we should make sure that all developers in the team use the same settings in their editors.So, this is where we store such settings.

.gitignore : It is for excluding certain files and folders from git repository.

karma.conf.js : It is a configuration file, for Karma, which is a test runner for JS code.

package.json : This is a standard file that every node project has. Apart from a bunch of basic settings like name and version of application, we have the settings called dependencies which consits of libraries that our application is dependent upon. The third party libraries are listed here.
It also has another key/settings called devDependencies, which consits of libraries that we need in order to develop applications. These are purely for developer machines.

protractor.conf.js : This is basically a tool for running e2e test for angular.

tsconfig.json : It consists of a bunch of settings for typescript compiler. Typescript compiler looks at this settings and based on that, it compiles our code into javascript that browser can understand. 

tslint.json : It includes a number of settings for tslint, which is a static analysis tool for typescript code.It checks our ts code for readability, maintainability and functinality errors.



##Webpack
Angular CLI uses a tool called Webpack which is build automation tool. It gets all our scripts and stylesheets, combines them, puts them in a bundle, and then minifies that bundle and this is for optimisation. Eg: polyfills.bundle.js : Which includes all the scripts to fill the gap between the version of JS that angular needs and the version of JS supported by most browsers out there.
main.bundle.js : It is all the scource code of our application.
styles.bundle.js : Which includes all our stylesheets.
vendor.bundle.js: Which includes all the third part libraries.
Whenver we change a file, whether that is a typescript file, stylesheet or html file, webpack automatically recompiles our application and refreshes the bundle. In the browser, without even refreshing the page, we get our new changes. This is because of the feature of Webpack called Hot Module Replacement/ Reloading (HMR). So, whenever one of the source file is modified, webpack automatically refreshes the browser.


When we do View Page Source in the browser, we can see that all the bundles that webpack generated, it also has injected them in inde.html. In our code, index.html does not have the reference to the scripts, but it is being done by webpack in runtime.

Also, all our stylesheets are compiled into Javascript bundle, i.e. why we have styles.bundle.js.

