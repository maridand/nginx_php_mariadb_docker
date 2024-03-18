
# Dockerized Web Application with Nginx, PHP, and MariaDB

This project sets up a simple web application environment using Docker containers for Nginx, PHP-FPM, and MariaDB. It's designed to provide a straightforward setup for development and production environments.

## Prerequisites

Before you begin, ensure you have Docker and Docker Compose installed on your system. For installation instructions, refer to the [official Docker documentation](https://docs.docker.com/get-docker/) and the [Docker Compose documentation](https://docs.docker.com/compose/install/).

## Structure

- `./configs/nginx`: Contains Nginx configuration files.
- `./configs/php`: Contains PHP configuration files.
- `./docker_images/php`: Contains Dockerfile for building the PHP image.
- `./src`: Your PHP application source code.
- `./db_data`: Directory for MariaDB data persistence.

## Getting Started

To get your environment up and running, follow these steps:

1. **Start the Containers**

   Navigate to the root of this project and run:

   ```bash
   docker-compose up -d
   ```

   This command builds and starts the containers in the background.

2. **Access the Web Application**

   After the containers are up, you can access the web application by navigating to `http://localhost:8080` in your web browser.

3. **Manage the Database**

   MariaDB is accessible on `localhost:3306`. Use the root password specified in the `docker-compose.yml` file to connect to the database.

## Customization

- **Nginx Configuration**: Modify `./configs/nginx/default.conf` to update Nginx settings as per your requirements.
- **PHP Configuration**: Update `./configs/php/php.ini` to change PHP settings.
- **MariaDB Data**: To persist or restore the database, manage files within the `./db_data` directory.

## Stopping the Environment

To stop and remove the containers, networks, and volumes created by `docker-compose up`, run:

```bash
docker-compose down
```

## Note

This setup is configured for development purposes and may need adjustments for production environments, especially regarding security and performance.

## Contributing

Contributions to improve the setup or documentation are welcome. Please submit a pull request or create an issue for any bugs or feature requests.

