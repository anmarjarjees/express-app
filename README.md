# express-application
## A quick introduction to "Express", the minimalist web framework for Node.js
### Up and Running with Express using "Express Generator"

This is a simple demo about how start a new express application by using "Express Generator" package to install the skeleton/boilerplate of express. This quick tutorial is based on Express Guide for building the boilerplate for a full Express application [Express Generator](https://expressjs.com/en/starter/generator.html)

### NOTE:
Please refer to my repo ["express-basics"](https://github.com/anmarjarjees/express-basics) for a full demo about how to create express application from scratch

1. This repo has been created on my GitHub with two initial files:
- README.md
- .gitignore

2. then Cloned to my local machine:
    - README.md
    - .gitignore
    -  And yes, it has the hidden folder ".git"

3. Installing the "express-generator" package:
#### Node Package Manager (npm):
A JavaScript package manager that installed with node.js.
- Adapt packages of code for your apps, or incorporate packages as they are.
- Download standalone tools you can use right away.
Express application generator

#### Node Package eXecute (npx):
It's part of npm to help developers run packages without installing them

We run the Express Application Generator (locally):
- Navigate to your local location where you want to create the main container folder. 
- Create a new folder that will act as the main container to contain the project folder later

This main container folder will be used for:
- Installing the Express project using the npm/npx as explained below
- Creating the actual Express project folder

Notice that:
- My main folder name is "express-application" as the current repo name.
- My actual Express application folder is "auto-gen-express-app" inside the current repo (main) folder


Inside the main folder "express-application" in my case, run the commands:

> npm install express-generator
or you can run the application generator with the npx command (available in Node.js 8.2.0).
> npx install express-generator

I used this command:
> npm install express-generator

NOTES: 
- Running this command will generate the following contents:
  - node_modules folder
  - package-lock.json
  - package.json
- It's unnecessary to commit (push to Github) any folder that included installed packages, as these packages should be installed properly, so we ignore the folder(s) "node_modules" with ".gitignore"

Now after running the command "npm install express-generator", the repo folder will have the following:
- The initial git files:
    - README.md
    - .gitignore
    - the hidden folder ".git"
- The express-generator files:
    - node_modules (folder)
    - package-lock.json
    - package.json 

4. You can run this command:
> express -h 
to see all the options, these options are also called "flags":

  Options:

    -h, --help          output usage information
    -V, --version       output the version number
    -e, --ejs           add ejs engine support (defaults to jade)
        --hbs           add handlebars engine support
    -H, --hogan         add hogan.js engine support
    -c, --css <engine>  add stylesheet <engine> support (less|stylus|compass|sass) (defaults to plain css)
        --git           add .gitignore
    -f, --force         force on non-empty directory

NOTE: [What view engine should I use?](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/skeleton_website#what_view_engine_should_i_use)
The Express Application Generator allows you to configure a number of popular view/templating engines.
The templating engines include:
- EJS
- Hbs
- Pug (Jade)
- Twig
- Vash

The "express-generator" chooses Jade by default if you don't specify a view option. Express itself can also support a large number of other templating languages out of the box.

Generally speaking, you should select a templating engine that delivers all the functionality you need and allows you to be productive sooner — or in other words, in the same way that you choose any other component!

5. Now you are ready to create the "actual project folder" where you will need to deploy later, by running the command express then the option(s) you want to include. Notice that by default, express generator will pick/use "pug" as the templating engine to render our HTML files, or you can specify which one you want to use.

In the example below, we used "--hbs" to install the handlebars engine which reminds us with AngularJS template by using mustache template {{ }}:

> express --git --hbs auto-gen-express-app

the command above has the following 2 flags with the name:
    - --git flag for adding git ignore
    - --hbs flag for adding handlebars engine support [(handlebars template engine)](https://handlebarsjs.com/)
    - auto-gen-express-app is the folder name where we want our application files/folders to be installed. Yes, I know I put a long name "auto-gen-express-app" just for demonstration :-)

Now the content of the repo folder "express-applications" included a new a folder named "auto-gen-express-app":
- auto-gen-express-app
- node_modules
- .gitignore
- package-lock.json
- package.json
- README.md

6. Navigate to your application actual folder "auto-gen-express-app", and you will see these content:
- app.js  
- package.json  
- .gitignore
- bin/ folder 
- public/ folder:
    - images/  
    - javascripts/  
    - stylesheets/
        - style.css
- routes/ folder:
    - index.js  
    - users.js
- views/ folder:
   - error.hbs  
   - index.hbs  
   - layout.hbs

 Notice the content of the json file within the express-generator package folder:
 ```
  {
  "dependencies": {
    "express-generator": "^4.16.1"
  }
}
```

7. Then install dependencies inside the project/application folder "auto-gen-express-app":
> npm install
This command will add the following new contents:
- node_modules/ folder <==> The node modules (packages)
- public/ folder <==> images, javascripts, and stylesheets
    - style.css <==> contains only two basic rules 
- routes/ folder <==> index.js and users.js (the default routes)
- package-lock.json
- app.js <==> the entry point to our application

So the final content of our application folder will be:
- app.js  
- package.json  
- .gitignore
- bin/ folder 
- node_modules/ folder
- public/ folder:
    - images/  
    - javascripts/  
    - stylesheets/
        - style.css
- routes/ folder:
    - index.js  
    - users.js
- views/ folder:
   - error.hbs  
   - index.hbs  
   - layout.hbs

Notice the content of the json file within the actual application folder:
```
{
  "name": "auto-gen-express-app",
  "version": "0.0.0",
  "private": true,
  "scripts": {
    "start": "node ./bin/www"
  },
  "dependencies": {
    "body-parser": "~1.15.1",
    "cookie-parser": "~1.4.3",
    "debug": "~2.2.0",
    "express": "~4.13.4",
    "hbs": "~4.0.0",
    "morgan": "~1.7.0",
    "serve-favicon": "~2.3.0"
  }
}
```
8. Running our application based on the command below from Express Docs (Guide):
NOTE: make sure you are inside the actual project folder
    - On MacOS or Linux, run the app with this command:
        > DEBUG=myapp:* npm start
    
    - On Windows Command Prompt, use this command:
        > set DEBUG=myapp:* & npm start

    - On Windows PowerShell, use this command:
        > $env:DEBUG='myapp:*'; npm start
    
NOTE: Don't forget to change the name "myapp" with your application name like "auto-gen-express-app" for me:
    - I am using powershell, so the command will be:
        > $env:DEBUG='auto-gen-express-app:*'; npm start

You will see this message: auto-gen-express-app:server Listening on port 3000 +0ms

9. Then load http://localhost:3000/ in your browser to access the app.
