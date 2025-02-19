toy-db-with-docker
==================

# Purpose

This project is used to learn how to create a database and containerize it from scratch. Specifically, it uses a MySQL database using Docker. It includes a `docker-compose.yml` file to define the services and an `init.sql` file to initialize the database schema.

## Project Structure

- `docker-compose.yml`: Defines the MySQL service and its configuration.
- `init.sql`: Contains SQL commands to create a simple MySQL table.

## Getting Started

To build and run the Docker container, follow these steps:

1. Ensure you have Docker and Docker Compose installed on your machine.
2. Clone this repository or download the project files.
3. Navigate to the project directory in your terminal.
4. Run the following command to start the MySQL service:

   ```
   docker-compose up
   ```
5. The MySQL server will be accessible on `localhost:3306`.

## Database Initialization

The `init.sql` file will be executed automatically when the MySQL container starts. It sets up the initial database schema, including the creation of a simple table.

## Stopping the Service

To stop the MySQL service, use the following command:

```
docker-compose down
```

This will stop and remove the containers defined in the `docker-compose.yml` file.

# Check if the Service is Running

You can check if the MySQL database is running by following these steps:

1. **Start the Docker container**:
   Run the following command in the terminal from the directory containing your docker-compose.yml file:

   ```sh
   docker-compose up -d
   ```

2. **Check the status of the container**:
   Run the following command to list all running containers and check the status of your MySQL container:

   ```sh
   docker ps
   ```

   You should see an entry for `mysql_container` in the list of running containers.

3. **Connect to the MySQL database**:
   You can use the MySQL command-line client or any MySQL client tool to connect to the database. For example, using the MySQL command-line client:

   ```sh
   docker exec -it mysql_container mysql -u user -puserpassword mydatabase
   ```

   or if you've like to be asked about the password afterward

   ```sh
   docker exec -it mysql_container mysql -u user -p mydatabase
   ```

   Enter the password when prompted. If you successfully connect, it means your database is running.

4. **Check the logs**:
   You can also check the logs of the MySQL container to ensure it started correctly:

   ```sh
   docker logs mysql_container
   ```

   Look for messages indicating that the MySQL server has started and is ready to accept connections.

# Citation Instructions

If you use this repository in your work, please cite it as follows:

**GitHub Repository**: [toy-db-with-docker](https://github.com/francisco-camargo/toy-db-with-docker.git)

**Suggested Citation**:

Author(s): Francisco Camargo
Title: toy-db-with-docker
Source: https://github.com/francisco-camargo/toy-db-with-docker.git
Date Accessed:

Please ensure proper attribution when using or modifying this work.
