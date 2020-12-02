# [API Gateway Component](../../../README.md)

![API Gateway](../images/api_gateway.svg)


API gateway provides a single entry point to the system and is responsible for initial Authentication and routing requests to the appropriate domain within the system. When needed for scale and latency, the API Gateway will also be responsible for sharding traffic based on location. 

Overall, API gateway component uses a layered modular structure. It has 3 major layers. 

The **Load Balancer** distributes network traffic across services.

The **API Layer** contains the routing to redirect requests to the corresponding FarmacyFood services. 

The **Common Layer** implements the shared functionality including: authentication,authorization,rate limiting, caching, metrics collection and logging.



## Communicates With:
All the rest of the services. One external request may break into several request to different FarmacyFood services. 
