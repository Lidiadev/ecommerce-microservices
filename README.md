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
