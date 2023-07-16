# Docker Compose

## What is Docker Compose?

Docker Compose is a tool for defining and managing multi-container applications. It allows you to describe the services, networks, and volumes required for a complete application stack in a simple YAML file.

## Docker Compose Commands

To manage your application with Docker Compose, you can use the following commands:

- **`docker-compose up`**: Creates and starts the containers defined in the Docker Compose file. It also builds images if necessary.

- **`docker-compose down`**: Stops and removes the containers defined in the Docker Compose file.

- **`docker-compose start`**: Starts the containers defined in the Docker Compose file.

- **`docker-compose stop`**: Stops the containers defined in the Docker Compose file.

- **`docker-compose restart`**: Restarts the containers defined in the Docker Compose file.

## Volumes and Networks in Docker Compose

When working with Docker Compose, you can define volumes and networks to manage data persistence and communication between containers:

### Volumes

Volumes in Docker Compose allow you to persist and share data between containers and the host machine. By using volumes, you can separate your data from the container's lifecycle, making it easier to update or replace containers without losing important data. Volumes can be used for databases, file uploads, or any other data that needs to persist across container restarts.

To define a volume in Docker Compose, you can use the `volumes` key under a service. Here's an example:

````
services:
  db:
    image: mysql
    volumes:
      - db_data:/var/lib/mysql

volumes:
  db_data:
````

In this example, a volume named `db_data` is created, and it is mounted to the `/var/lib/mysql` directory inside the db service container.

### Networks

Networks in Docker Compose enable communication between containers within the same application stack. By default, Docker Compose creates a default network for your application, allowing services to communicate with each other using their service names as hostnames. This makes it easy to establish connections between containers without exposing unnecessary ports to the host machine.

To define a network in Docker Compose, you can use the `networks` key under a service. Here's an example:

````
services:
  web:
    image: nginx
    networks:
      - frontend

  api:
    image: myapi
    networks:
      - frontend
      - backend

networks:
  frontend:
  backend:
````

In this example, two networks are defined: `frontend` and `backend`. The `web` service is connected to the `frontend` network, while the `api` service is connected to both the `frontend` and `backend` networks.


## How to Use Docker Compose

To use Docker Compose, follow these steps:

1. Define your application's services, networks, and volumes in a Docker Compose YAML file.

2. Save the YAML file with a `.yml` or `.yaml` extension (e.g., `docker-compose.yml`).

3. Open a terminal or command prompt and navigate to the directory where the Docker Compose file is located.

4. Run the desired Docker Compose command, such as `docker-compose up`, to start your application.

5. Monitor the logs to ensure everything is running correctly.

6. When you're done, use `Ctrl + C` to stop the Docker Compose command, or run `docker-compose down` to stop and remove the containers.

Docker Compose simplifies the process of running multi-container applications and enables easy management of complex application stacks.


## Example
To get you started, let's consider running a multi-container application using a `docker-compose.yml` file. Here are the steps:

To start:

1. Ensure Docker Compose is installed on your machine. If not, follow the official Docker Compose installation guide for your operating system.

2. Create a directory for your application and navigate to it using the command line:

```bash
   mkdir my-app
   cd my-app

Next:

1. Create a `docker-compose.yml` file in the project directory (`my-app`) using a text editor:

````
version: '3'
services:
  web:
    image: nginx:latest
    ports:
      - 8080:80
    volumes:
      - ./html:/usr/share/nginx/html
  db:
    image: mysql:latest
    environment:
      - MYSQL_ROOT_PASSWORD=secretpassword
      - MYSQL_DATABASE=mydatabase
      - MYSQL_USER=myuser
      - MYSQL_PASSWORD=mypassword
````

In this example, we define two services: web and db. The web service uses the official nginx image, maps port 8080 on the host to port 80 in the container, and mounts the html directory from the host to the /usr/share/nginx/html directory inside the container. The db service uses the official mysql image and sets environment variables for the root password, database, user, and password.

2. Create an `html` directory in the project directory (`my-app`) and place your HTML files inside it.

3. Open a terminal or command prompt, navigate to the project directory (`my-app`), and run the following command to start the application:

````
docker-compose up -d
````

This command starts the services defined in the docker-compose.yml file in detached mode (-d), creating and running the containers.

4. Open a web browser and navigate to **`http://localhost:8080`** to access your web applicatio

In this example, we demonstrate a basic use case where we use Docker Compose to define and run a multi-container application. The `docker-compose.yml` file specifies two services: `web` and `db`. The `web` service uses the official `nginx` image, mounts the `html` directory from the host, and exposes port 8080. The `db` service uses the official `mysql` image and sets environment variables. Running `docker-compose up -d` starts the application, and you can access the web application by navigating to `http://localhost:8080` in a web browser.

That's it! You've successfully run a multi-container application using Docker Compose.

## Additional Information

If you would like any additionalk information, please refer to this [documentation](https://docs.docker.com/compose/).

