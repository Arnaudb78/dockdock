# DockDock - NestJS with PostgreSQL

A Docker Compose setup for a NestJS application with PostgreSQL and Adminer.

## Prerequisites

-   Docker and Docker Compose installed on your machine
-   Git (optional, for cloning the repository)

## Setup and Run

1. Clone or download this repository
2. Navigate to the project directory
3. Run the following command to start all services:

```bash
docker-compose up
```

To run the services in the background:

```bash
docker-compose up -d
```

## Services

The Docker Compose setup includes the following services:

### NestJS Application

-   Port: 3000
-   Access it at: http://localhost:3000

### PostgreSQL Database

-   Port: 5432
-   Username: postgres
-   Password: postgres
-   Database: dockdock

### Adminer (Database Management)

-   Port: 8080
-   Access it at: http://localhost:8080
-   Server: postgres
-   Username: postgres
-   Password: postgres
-   Database: dockdock

## Development

The NestJS application source code is located in the `nest-app` directory. The application container is set up with hot-reloading, so any changes you make to the source code will be reflected in the running container.

## Stopping the Services

To stop the services, run:

```bash
docker-compose down
```

To stop the services and remove the volumes (this will delete all data in the database):

```bash
docker-compose down -v
```
