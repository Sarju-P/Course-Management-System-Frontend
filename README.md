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

node_modules: This is where we store all the third party libraries that our application may depend upon. This folder is purely for development. So, when we compile our application, parts of this third party library are put in a bundle and deployed in the application. 