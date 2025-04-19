# Restaurant Microservice System

## Project Overview
This is a microservice-based restaurant ordering system built with NestJS, RabbitMQ, and MongoDB. The system allows users to fetch a food menu, place orders, and track order status.

## Services
1. **OrderService**: Handles menu retrieval and order placement
2. **KitchenService**: Processes and updates order status
3. **NotificationService**: Sends order confirmation emails

## Technologies
- NodeJS (v16+)
- NestJS Framework
- RabbitMQ (Message Broker)
- MongoDB (Database)
- Docker & Docker Compose

## Prerequisites
- Docker
- Docker Compose
- NodeJS 16+

## Local Deployment
1. Clone the repository
2. Run `docker-compose up --build`
3. Access services at:
   - OrderService: `http://localhost:3001`
   - KitchenService: `http://localhost:3002`
   - NotificationService: `http://localhost:3003`

## API Endpoints

### OrderService
- `GET /menu`: Retrieve food menu
- `POST /order`: Place a new order
- `GET /order/:id`: Track order status

## Testing
Run tests for each service:
```bash
cd order-service && npm test
cd kitchen-service && npm test
cd notification-service && npm test
```

## Architecture
- Microservice architecture
- RabbitMQ fan-out pattern for inter-service communication
- MongoDB for persistent storage

## License
MIT License

