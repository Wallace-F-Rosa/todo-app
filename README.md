# Todo App
Web application to manage a todo list using an REST API, microservices and an front end application.

# Services
The backend will have the following services(each of them is a submodule of this project):
- (todo-api) An REST API service that exposes all functionalities.
- (todo-service) An Todo Service that allows creation, delition and update of tasks.
- (todo-view) An Todo View Service that allows listing the tasks and getting the details of an specific task.

# Interface
The frontend (todo-front) allows use of the features using an visual interface.

# How to run the application
Using docker compose:

- To build images and run the app
`docker compose up -d --build`

- To run the app when images are already built
`docker compose up -d`

Apply the migrations(didn't found a solution to apply migrations on docker build yet):
```
cd todo-tasks
yarn prisma migrate dev
cd todo-user
yarn prisma migrate dev
```
