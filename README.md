# Microservices-arch-specialist


## Characteristics of a good microservice Architecture

### Componentization via services 

- Component is a unit of software that is independently repleaceble and upgradeable.
- Services are independently deployable. 

### Organized Around Business Capabilities 

- Split teams based on business capabilities. 
- Teams are cross-functional. 

### Products Not Projects 

- Projects aim just a piece of software, with a closed scope. 
- Products are scalable.
- Team will be the owner of the product over its full lifetime. 
- Products are linked with their on capabilities and their responsabilities, and not just focused and delivery some functionality. 

### Smart endpoints and dumb pipes 

- The communication mechanism must be DUMB. 
- Microservices are decoupled. 
- Own their own domain logic. 

### Decentralized Governance

- Be able to use differents databases, languages and frameworks. 
- Contracts well defined. 
- You build it / you run it 

### Decentralized Data Management

- Duplicate data when necessary. 
- Each system has his own database. 


### Infra Automation 

- Automated test 
- Automated deploy 

### Design for failure 

- Expect dependencies error. 
- Monitoring, Alerts, resilience. 

### Evolutionary Design 

- Be able to change and upgrade my system without impact other MS. 
- Be able to replace one ms without impact archtecture.

#### More details - https://martinfowler.com/articles/microservices.html

## Resilience 

### Intentional Adapt to failure 

### Strategic approach to minimize risk of losing data, losing transactions and avoid impacting infrastructure 

### Response time should not change. 

### Do not make requests to another system that is not healthy. Dont be selfish. 

## Health Check

- Always make sure that your system and their dependencies are healthy.
- Avoid request to systems that are not healthy. 
- Self-healing - an unhealthy system that is not receiving more requests can be healthy after some minutes. 

## Rate limiting 

- Protect the system based on the number of requests is was designed to handle.
- It should be based on each customer, focusing on the most important customers. 

## Circuit Braker 

- Protect the system returning error when the system is not healthy. 
- Circuit closed - requests are processed normally.
- Circuit Open - No requests are processed. Always returns an error. 
- Half open Circuit - Allows a limited amount of requests to be processed focused on verify if system has condition to close the circuit again. 


## Api Gateway 

- Ensures that inappropriate requests do not reach the system.
- implements rate limiting, Health check and etc: 
        - Just necessary to create an endpoint that checks the application status and the api gateway will make requests and make sure to protect the api based on that. 
- Organize microservices in contexts. 

## Service Mesh

- Traffic control.




