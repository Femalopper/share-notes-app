[![Actions Status](https://github.com/Femalopper/share-notes-app/workflows/eslint-check/badge.svg?branch=main)](https://github.com/Femalopper/share-notes-app/actions)
[![Maintainability](https://api.codeclimate.com/v1/badges/7a10118d7292a7082434/maintainability)](https://codeclimate.com/github/Femalopper/share-notes-app/maintainability)

## Description
ShareNotes is an app for sharing encrypted messages between users. 

## Implemented features
- [x] create encrypted in URL messages
- [x] open messages with encrypted URL
- [x] search messages by hash, read messages

## Animation

![Functionality](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/ShareNotes.gif)

## Setup

### 1\. Clone project ###
 
  ```sh
   git clone git@github.com:Femalopper/share-notes-app.git

   cd share-notes-app/backend_project

   npm ci

   cd share-notes-app/frontend_project

   npm ci
  ```
***
### 2\. Install SQL database ###

Example of ready and fast solution: 

> Download and install one of the program platforms: 
>  - MAMP(for macOS and Windows): https://www.mamp.info/en/windows/
>  - Open Server(for Windows): https://ospanel.io/

  ### ***MAMP SQL installation*** ###

  **1\.** Click ***Start servers*** button

  >![Mamp start server](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/Mamp%20start.png)


  **2\.** Click ***Open WebStart page*** button -> ***TOOLS*** -> ***PhpMyAdmin***

  >![Mamp start page](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/Mamp%20start%20page.png)

  
  >![Mamp php admin](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/Mamp%20phpmyadmin.png)


  **3\.** Click ***New*** to create Database

  **4\.** Enter database name: ***reactjs***

  **5\.** Enter encoding: ***utf8mb4u_unicode_ci*** -> create

  >![Mamp create database](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/Mamp%20create%20Database.png)

  
  **6\.** Click ***import***: choose ***reactjs.sql***(located in react-app-ShareNotes/backend_project folder) -> ***Go***

  >![Mamp create database2](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/Mamp%20create%20Database2.png)


  **Database is created!**

  **7\.** Open command line:
  ```sh
   cd backend_project/db

   code index.js
  ```
  **8\.** Correct sequelize setting (insert password parameter - ***'root'***):
  ```sh
   const sequelize = new Sequelize('reactjs', 'root', 'root', {
     dialect: 'mysql',
     host: 'localhost',
   });
  ```
***
### ***Open server SQL installation*** ###

  **1\.** Click ***Run server*** button

  >![OS run server](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/OS%20run%20server.png)


  **2\.** Click ***Advanced*** button -> ***PhpMyAdmin***
  

  >![OS phpadmin](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/OS%20phpmyadmin.png)

  ***!!!If PhpMyAdmin is not loaded in the browser, set MySQL-8.0 module:***

  >![Correct modules](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/Correct%20modules.png)

 

  **3\.** Enter login: ***root***

  ***!!!Disable your antivirus and turn off browser extensions in case of authorization problems***

  >![OS login enter](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/OS%20enter.png)


  **4\.** Click create Database

  **5\.** Enter database name: ***reactjs***

  **6\.** Enter encoding: ***utf8mb4u_unicode_ci*** -> create

  >![OS create database](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/OS%20create.png)


  **7\.** Click import: choose ***reactjs.sql*** (located in react-app-ShareNotes/backend_project folder)

  >![OS create database2](https://github.com/Femalopper/raw/blob/main/images/react-app-ShareNotes/OS%20create2.png)


  **Database is created!**

  ### Note: ###
  ```sh
    Open react-app-ShareNotes/frontend_project/src/env.json 
    to change backend server URL("http://localhost:3500")
  ```
***
### 3\. Open two terminals ###
### 4\. Run server (in the first terminal) ###

  ```sh
   cd backend_project

   node index.js
  ```
***
### 5\. Run app (in the second terminal) ###

  ```sh
   cd frontend_project

   npm start
  ```

