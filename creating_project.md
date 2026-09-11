# we will learn how to create a project in react
---> there are various method of creating a project in react.
we will discuss two of them


# first we will learn it through CRA(Create-react-App)

-->
 1. open the vs terminal and navigate through   your react folder
 2. run :  npx create-react-app 01basicreact

      here,    
           npx → runs a package without you having to install it globally
           create-react-app → tool that creates the React project
           01basicreact → your project name

3. Creating a new React app in
   C:\Users\aditi\Desktop\vs_file\React_learn\01basicreact

   Installing packages...

   we will wait until it shows: Success! Created 01basicreact

4. we will go inside the project : cd 01basicreact
5. To start the application we will write: npm start
   CRA will start the development server.usually your browser will automatically open it.


6. your project structure will look like:

01basicreact/
│
├── node_modules/
├── public/
│
├── src/
│   ├── App.js
│   ├── App.css
│   ├── index.js
│   └── index.css
│
├── .gitignore
├── package.json
├── package-lock.json
└── README.md

src is the most important folder we are gonna work on.


# second we will learn it using Vite

--->
  1. open the new terminal and navigate through project folder

  2. we will create the react project : npm create  vite@latest

   Vite will ask : project name, we will enter 01basicreact
   Then it will ask :Select a framework: we will choose react and then it will ask select a variant: we will select JavaScript

   3. we will go inside a project :cd 01basicreact

   4. install dependencies
      
       npm install

      this creates the node_modules folder and installs the packages your project needs

   5. start the react development server:
       npm run dev
      you will see something like:
      Local: http://localhost:5173/

      after openning the address we will see the react application running


  the project will look like:

01basicreact
│
├── node_modules
├── public
│
├── src
│   ├── assets
│   ├── App.jsx
│   ├── main.jsx
│
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js

the two most important files are App.jsx
and main.jsx---> this is where react starts your application and renders App into the Html page



# what is vite?

---->
Vite is a modern build tool and development server used to create and run frontend applications, including React applications.

Think of it like this:

React = the UI library
Vite = the tool that sets up and runs your React project

So Vite does not replace React.

with simple analogy imagine you are building a house :
 React → the materials and components you use to build the house
 Vite → the modern construction setup/tools that help you build and develop it quickly
 Your React app → the finished house

# why was Vite created?
Before Vite, many React developers used Create React App (CRA).
CRA would set up a lot of things for you.

The problem was that traditional bundlers used by older setups often had to process a large amount of your application before the development server could become ready.

As applications became larger, development could feel slower.

Vite was designed to make the development experience much faster.


# How Vite Works?

---->
  This is the important part 
  with a traditional setup , you can think of it roughly like:
        Your code
        ↓
        Bundler processes lots of files
        ↓
        Development server
        ↓
        Browser

  Vite takes advantage of modern browser support for ES modules (ESM) during development:
        Your code
        ↓
        Vite development server
        ↓
        Browser requests what it needs

 So when you change a file, Vite doesn't need to rebuild the entire application.

  This makes things like:

            Save file
            ↓
            Vite detects change
            ↓
            Browser updates quickly

 This feature is called HMR — Hot Module Replacement.



 # difference between CRA and Vite

                     Create React App	               Vite
Purpose	            Create React apps	       Build/run frontend apps
Developmentspeed	Older/slower approach	        Very fast
Modern choice	      Deprecated	             Common modern choice
Configuration	    More hidden	                 Simple and flexible
Dev server	       Older architecture	            Very fast
React support	        Yes	                           Yes
Build tool	      Webpack-based setup	       Vite/Rollup-based build tooling