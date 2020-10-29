### Event-Driven Microservice Architecture
Microservices implemented using:
- ASP.NET Core Web API
- RabbitMQ
- Ocelot API Gateway
- SQL Server
- MangoDB
- Redis
- Docker

### Architecture overview 

The ECommerce system is using a microservice oriented architecture with autonomous microservices (each one owning its own data/db) and implementing different approaches within each microservice (simple CRUD vs. DDD/CQRS patterns) using HTTP as the communication protocol between the client apps and the microservices and supports asynchronous communication for data updates propagation across multiple services based on Integration Events and an Event Bus (RabbitMQ). 

### Components overview 

#### Catalog microservice:
- ASP.NET Core Web API application
- REST API principles, CRUD operations
- Mongo DB NoSQL database connection on docker

#### Basket microservice:
- ASP.NET Core Web API application
- REST API principles, CRUD operations
- Redis connection as a Database on docker

#### RabbitMQ messaging library:
- Base EventBus implementation

### Prerequirements
- Visual Studio 2019
- .NET Core 3.0.1 SDK
- Docker Desktop

### How to run the solution
1. Clone the repository
2. At the root directory which include docker-compose.yml files, run the command:
``` 
docker-compose -f docker-compose.yml -f docker-compose.override.yml up –d
``` 
4. Launch microservices:
- RabbitMQ: http://localhost:15672/
- Catalog API: http://localhost:8000/swagger/index.html
- Basket API: http://localhost:8001/swagger/index.html
