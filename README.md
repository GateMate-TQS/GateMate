# deployement

## Deployement of the GateMate project

```bash
cd GateMate
git submodule update --recursive --remote
docker-compose up --build -d
```

env file should be created in the root directory of the project with the following content:

```bash
# .env file

# RabbitMQ Configuration
RABBITMQ_USER=admin
RABBITMQ_PASSWORD=admin
RABBITMQ_LOCAL_MANAGEMENT_PORT=15672
RABBITMQ_DOCKER_MANAGEMENT_PORT = 15672
RABBITMQ_LOCAL_PORT=5672
RABBITMQ_DOCKER_PORT=5672

# Nginx Configuration
NGINX_PORT=8080

# Backend Configuration
USER_PORT=8085
PAYMENT_PORT=8081
NOTIFICATION_PORT=8084
FLIGHT_LOCAL_PORT=8082
FLIGHT_DOCKER_PORT=8080
LIVE_DATA_RECEIVER_LOCAL_PORT=8087
LIVE_DATA_RECEIVER_DOCKER_PORT=8087

# Frontend Configuration
FRONTEND_PORT=3000
FRONTEND_PORT=8383

# MySQL Configuration
MYSQL_ROOT_PASSWORD=root123
MYSQL_DATABASE=flights
MYSQL_USER=user
MYSQL_PASSWORD=user123
MYSQL_LOCAL_PORT=33060
MYSQL_DOCKER_PORT=3306

# External API Configuration
API_KEY=???
```
