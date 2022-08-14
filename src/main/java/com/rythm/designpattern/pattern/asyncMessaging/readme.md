###The Asynchronous Messaging Pattern

In this type of microservices design pattern, all the services can communicate with each other, but they do not have to communicate with each other sequentially. So, if you consider 3 services: Service A, Service B, and Service C. The request from the client can be directly sent to the Service C and Service B simultaneously. These requests will be in a queue. Apart from this, the request can also be sent to Service A whose response need not have to be sent to the same service through which request has come.

[pattern](docs/img/aggregator.png)

You can find here is AddItem Aggregator Microservice which basically orchestrates the AddItem into Shopping Cart operation. And it aggregates request to several back-end microservices which's are Product, Shopping Cart and Pricing.

So we can say that this pattern isolates the underlying AddItem operation that makes calls to multiple back-end microservices, centralizing its logic into a AddItem Aggregator Microservice.

Also we can apply this pattern into our e-commerce application architecture when querying data from backend systems.