# Todo App (WORK IN PROGRESS)
Web application to manage a todo list using microservices exposing REST API's and an front end application.

# Services
The backend will have the following services(each of them is a submodule of this project):
- [**todo-user**](https://github.com/Wallace-F-Rosa/todo-user): service responsable to deal with user data and operations (sign up, login)
- [**todo-tasks**](https://github.com/Wallace-F-Rosa/todo-tasks): service responsable to deal with tasks management.

# Interface
The **todo-front** allows use of the features using an web interface.

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
