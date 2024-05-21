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
RABBITMQ_MANAGEMENT_PORT=15672
RABBITMQ_PORT=5672

# Nginx Configuration
NGINX_PORT=80

# Backend Configuration
PAYMENT_PORT=8001
FLIGHT_PORT=8002
USER_PORT=8003
LIVE_DATA_RECEIVER_PORT=8004
NOTIFICATION_PORT=8005

# Frontend Configuration
FRONTEND_PORT=8083
DISPLAY_PORT=8086

# MySQL Configuration
MYSQL_ROOT_PASSWORD=root123
MYSQL_DATABASE=flights
MYSQL_USER=user
MYSQL_PASSWORD=user123
MYSQL_LOCAL_PORT=33060
MYSQL_DOCKER_PORT=3306

# External API Configuration
API_KEY=???

# JWT Configuration
JWT_SECRET=yoursecret
```
