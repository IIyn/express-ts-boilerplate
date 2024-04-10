This project helps to create an express API with typescript using hexagonal architecture.

## Pre-requisites :

- Node.js
- NPM
- Typescript

## Installation

To run Typescript in dev mode you will need the following packages:

```bash
npm i -g ts-node-dev concurrently
```

## Project Structure

- **src** : Contains all the source code of the project.
  - **config** : Contains all the configuration files.
    - **example** : env.ts file to load environment variables.
  - **domain** : Contains all the domain logic.
    - **entities** : Contains all the entities.
      - **example** : User.ts file to define the User entity.
    - **services** : Contains all the services.
      - **example** : UserService.ts file to define the UserService.
  - **infrastructure** : Contains all the infrastructure related code.
    - **database** : Contains all the database related code.
    - **repositories** : Contains all the repositories.
      - **example** : UserRepository.ts file to define the UserRepository. (CRUD operations on User entity)
    - **web** : Contains all the web related code.
      - **controllers** : Contains all the controllers.
        - **example** : UserController.ts file to define the UserController. (Routes and request handling)
      - **routes** : Contains all the routes.
        - **example** : user.ts file to define the user routes. (Only define routes and call the controller methods)
  - **middlewares** : Contains all the middlewares.
    - **example** : AuthMiddleware.ts file to define the AuthMiddleware. (use on all routes or specific routes)
  - **types** : Contains all the types.
  - **utils** : Contains all the utility functions.
  - **app.ts** : Entry point of the application.
- **.env.example** : Contains all the environment variables.
