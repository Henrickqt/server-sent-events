# Application

This is a simple web application created especially to demonstrate how to work with real-time communication between server and client. In this project, I'm implementing the "Server Sent Events", using the GO language, Docker Compose and RabbitMQ

# How to run

## Prerequisites

Tools that you need to install on the machine:

- WSL2
- Docker Desktop
- Go

## Running the RabbitMQ with Docker Compose

On terminal, inside the project folder, input the following command:

```bash
docker-compose up -d
```

After that, you can navigate to `http://localhost:15672/` and access the RabbitMQ page with the credentials set in the `docker-compose.yaml`.
Remember navigating to the tab `Queues` and create your first queue with the name `msgs`.

## Running the project

On terminal, inside the project folder, input the following command:

```bash
go run cmd/main.go
```

After that, you can navigate to `http://localhost:8080/` and start receiving the messages that you are publishing in the queue above.
