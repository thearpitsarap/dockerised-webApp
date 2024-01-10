# Dockerized Web App

This is a Dockerized web app that you can easily run locally using Docker.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Docker](https://www.docker.com/get-started)

## Running the App

To run this web app locally, follow these steps:

1. Open a terminal and navigate to the project directory.

2. Build the Docker image:

    ```bash
    docker build -t spyder-todo .
    ```

    Replace `your-image-name` with a name you choose for your Docker image.

3. Run the Docker container:

    ```bash
    docker run -p 3000:3000 -d spyder-todo
    ```

    This maps port 3000 on your local machine to port 3000 in the Docker container. Adjust the ports if your app uses a different port.

4. Access the App

    Once the Docker container is running, you can access the web app in your browser at [http://localhost:3000/](http://localhost:3000/).

## Stopping the App

To stop the Docker container, you can use the following command:

```bash
docker stop $(docker ps -q --filter ancestor=spyder-todo)
