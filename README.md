# devolvApp

A comprehensive web application designed to optimize recyclable packaging management and streamline collection logistics through an integrated order system. The project is built using a modern, scalable architecture split into microservices/layers, fully containerized for seamless deployment.

## Repository Structure

* **devolvapp_frontend:** The user interface where clients and administrators interact with the platform.
* **devolvapp_backend:** The core Java API handling the business logic, tracking, and database interactions.
* **devolvapp_notification:** A dedicated microservice tasked with handling automated order statuses and system notifications.

## Prerequisites

Make sure you have the following installed on your machine:
* [Docker Desktop](https://docker.com) (which includes Docker Compose)

## Launching the Application

Run the compose file in detached mode to download the required images, build your local containers, and spin up the database and message brokers:

```bash
docker compose up -d
```

## Application Access Points (URLs)

Once the Docker containers are successfully running, you can access the different platform interfaces using your web browser through the following local URLs:

* **Frontend UI:** [http://localhost](http://localhost) (Exposed on the standard web port 80).
* **MailHog Webmail:** [http://localhost:8025](http://localhost:8025) (Use this to view and inspect all outgoing transactional emails sent by the application).
* **RabbitMQ Dashboard:** [http://localhost:15672](http://localhost:15672) (Message broker management panel. User: `demo` / Pass: `demo`).
