## Setting up npm and Sequelize models

# Sequelize

- JavaScript library that makes it easy to manage a data base
- Sequelize is an Object-Relational Mapper (ORM ); it maps an object syntax onto DB
- Uses Node.JS and Javascript's object syntax

1.  Install npm package

    ```sh
    npm init -y
    ```

2.  Install express and Sequelize Postgres

    ```sh
    npm i express sequelize pg
    ```

## Dev Dependencies

3.  Install nodemon and Sequelize CLI
    -monitors for changes during node.js app and restarts server
    -CLI is Command Line Interface. This install will allow to run npx to use CLI tools

    ```sh
    npm i --save-dev nodemon sequelize-cli
    ```

    - add dev script to package.json:

    `"dev": :"nodemon index.js"`

4.  Initialize Sequelize
    -Will create folders: config, models, migrations, seeders
    -config file, which tells CLI how to connect with DB

    ```sh
    npx sequelize-cli init
    ```

## Regular Dependencies

5. Install dotenv, express (if haven't already), morgan, express template engine, and librarries to communicate with Postgres

```sh
npm i dotenv
npm i express
npm i morgan
npm i express-es6-template-engine
npm i sequelize
npm i pg-hstore pg
```

## Configure Database

5.  Modify config file

- Create ElephantSQL instance
  -Make a copy of the dist.env file and name the copy .env
  -Copy/paste the credentials into .env
  -Run migrations so that Postres can store Model data:

```sh
npx sequelize-cli db:migrate
```

6. Create data model
   -If creating multiple models, run below command for each model
   -replace modelName and attributes
   -Ensure there are no spaces in attribute listing

```sh
npx sequelize-cli model:generate --name modelName --attributes attribute1:string,attribute2:string,attribute3:string
```

7. Create table, save in DB to use model

- create all models in previous step, then migrate once

```sh
npx sequelize-cli db:migrate
```

- Can revert most recent migration or all to revert back to initial state

```sh
npx sequelize-cli db:migrate:undo

npx sequelize-cli db:migrate:all
```
