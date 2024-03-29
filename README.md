# Todo App
Web application to manage a todo list using microservices exposing REST API's (with [Swagger](https://swagger.io/) documentation) and an front end application. Communication between services is message based using RabbitMQ.

# Services
The backend will have the following services(each of them is a submodule of this project):
- [**todo-user**](https://github.com/Wallace-F-Rosa/todo-user): service responsable to deal with user data and operations (sign up, login)
- [**todo-tasks**](https://github.com/Wallace-F-Rosa/todo-tasks): service responsable to deal with tasks management.

# How to run the application
Using docker compose:

- Run postgres container first:
`docker compose up -d postgres`

Apply the migrations(didn't found a solution to apply migrations on docker build yet):
```
cd todo-tasks
yarn prisma migrate dev
cd todo-user
yarn prisma migrate dev
```

- Run the app:
`docker compose up -d`

User service API should be running on [localhost:3000](localhost:3000).
Task service API should be running on [localhost:3001](localhost:3001).
Accessing the links should take you to the Swagger documentation of the apis.
