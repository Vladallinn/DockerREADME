# README: Docker-Compose App

This README file provides instructions for setting up and running a Dockerized application using Docker Compose. The application consists of a Python script (`main.py`), a `Dockerfile`, and a `docker-compose.yml` file.

## Project Structure

```plaintext
docker-compose-app/
├── app/
│   ├── Dockerfile
│   ├── main.py
└── docker-compose.yml
```

- **app/**: Folder containing the application files.
  - **Dockerfile**: Defines the Docker image for the Python application.
  - **main.py**: Python script connecting to MongoDB and listing databases.
- **docker-compose.yml**: Configuration file for Docker Compose, defining services and their settings.

## Prerequisites

Make sure you have Docker and Docker Compose installed on your machine:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Steps to Run the Docker-Compose App

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/docker-compose-app.git
cd docker-compose-app
```

### 2. Build and Run the Application

Run the following command to build and start the application using Docker Compose:

```bash
docker-compose up --build
```

This command will build the Docker image from the `Dockerfile`, start the defined services (`app` and `mongo`), and connect them.

### 3. Access the Application Output

Once the services are up and running, you should see the output of the `main.py` script, which connects to the MongoDB instance and prints the list of databases.

### Additional Information

- The `app` service is built from the `./app` directory, where the `Dockerfile` and `main.py` are located.
- The `mongo` service uses the official MongoDB image from Docker Hub.

### Stopping the Application

To stop the application and remove the containers, use the following command:

```bash
docker-compose down
```

This concludes the setup and execution of the Docker-Compose application. Feel free to explore and modify the files based on your specific requirements. If you encounter any issues, check the Docker Compose documentation or the official images on Docker Hub for additional information.
