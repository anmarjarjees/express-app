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
- It's unnecessary to commit any folder that included installed packages, as these packages should be installed properly, so we ignore the folder(s) "node_modules"

Now after running the command "npm install express-generator", the repo folder will have the following:
- The initial git files:
    - README.md
    - .gitignore
    - the hidden folder ".git"
- The express-generator files:
    - node_modules folder
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

5. Now you are ready to create the actual project folder where you will need to deploy later, by running the command express then the option(s) you want to include:
> express --git --hbs auto-gen-express-app
the command above has the following:
    - --git flag for adding git ignore
    - --hbs flag for adding handlebars engine support [(handlebars template engine)](https://handlebarsjs.com/)
    - auto-gen-express-app is the folder name where we want our application files/folders to be installed. Yes, I know I put a long name "auto-gen-express-app" just for demonstration

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
- node_modules/ folder <==> The node modules 
- package-lock.json

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
    - On MacOS or Linux, run the app with this command:
        > DEBUG=myapp:* npm start
    
    - On Windows Command Prompt, use this command:
        > set DEBUG=myapp:* & npm start

    - On Windows PowerShell, use this command:
        > $env:DEBUG='myapp:*'; npm start
    
NOTE: Don't forget to change the name "myapp" with your application name like "auto-gen-express-app"
    - I am using powershell, so the command will be:
        > $env:DEBUG='auto-gen-express-app:*'; npm start

You will see this message: auto-gen-express-app:server Listening on port 3000 +0ms

9. Then load http://localhost:3000/ in your browser to access the app.
