# devolvApp
A comprehensive web application designed to optimize recyclable packaging management and streamline collection logistics through an integrated order system.
The project is built using a modern, scalable architecture split into microservices/layers, fully containerized for seamless deployment.

The repository is organized into three main services orchestrated together:

*   **`devolvapp_frontend`**: The user interface where clients and administrators interact with the platform.
*   **`devolvapp_backend`**: The core API handling the business logic, recyclable tracking, and database interactions.
*   **`devolvapp_notification`**: A dedicated microservice tasked with handling automated order statuses and system notifications.

Make sure you have the following installed on your machine:
*   [Docker Desktop](https://docker.com) (which includes Docker Compose)

2. **Launch all services**:
   Run the compose file in detached mode to download the required images, build your local containers, and spin up the databases:
   ```bash
   docker compose up -d
   ```
Once the Docker containers are successfully running, you can access the components using your web browser through the following local URLs:

*   **Frontend (User Interface):** [http://localhost:3000](http://localhost:3000) 
    *(or your specific mapped frontend port, e.g., port 5173 if using Vite/React, or port 8080)*
*   **Backend API:** [http://localhost:8000](http://localhost:8000) 
    *(or your specific API port, e.g., 5000, 8080) / Common health check route: [http://localhost:8000/api](http://localhost:8000/api)*
*   **Notification Service:** Running internally or exposed on its designated communication port.
