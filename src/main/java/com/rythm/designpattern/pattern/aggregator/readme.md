###The Service Aggregator Pattern

In order to minimize service-to-service communications, we can apply Service Aggregator Pattern.

Basically, The Service aggregator design pattern is receives a request from the client or API Gateways, and than dispatches requests of multiple internal backend microservices, and than combines the results and responds back to the initiating request in 1 response structure.

By Service Aggregator Pattern implementation, we can reduces chattiness and communication overhead between the client and microservices.

[pattern](docs/img/aggregator.png)

You can find here is AddItem Aggregator Microservice which basically orchestrates the AddItem into Shopping Cart operation. And it aggregates request to several back-end microservices which's are Product, Shopping Cart and Pricing.

So we can say that this pattern isolates the underlying AddItem operation that makes calls to multiple back-end microservices, centralizing its logic into a AddItem Aggregator Microservice.

Also we can apply this pattern into our e-commerce application architecture when querying data from backend systems.