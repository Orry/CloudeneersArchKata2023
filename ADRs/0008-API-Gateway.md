# 8. API Gateway

Date: 2023-09-13
## Status

Accepted

## Context

In the process of designing our microservices-based architecture for our travel management platform, we need to make a decision regarding the selection of an API Gateway. The API Gateway will serve as a central entry point for incoming requests to our microservices, providing various functionalities such as routing, load balancing, authentication, and more. The choice of the API Gateway is critical to the overall success and scalability of our platform.

## Decision

After evaluating several options and considering our specific requirements and constraints, we have decided to select an API Gateway that aligns with the following criteria:

1. **Open Source and Extensible**: We will prioritize an open-source API Gateway that offers flexibility and extensibility. This will allow us to add and customize functionality as needed for our unique use cases.

2. **Scalability**: The chosen API Gateway should be designed to handle high loads and should be horizontally scalable. This is essential to meet our requirements of serving 2 million active users per week and ensuring that the system remains responsive during peak traffic.

3. **Security**: The selected API Gateway should offer robust security features such as rate limiting, authentication mechanisms, and SSL/TLS termination to ensure the security of our API endpoints and data privacy.

4. **Performance**: We will prioritize an API Gateway known for its low-latency performance. This aligns with our technical requirements of achieving an 800ms response time from the web and fast mobile load times.

5. **Integration**: The chosen API Gateway should be capable of seamless integration with various authentication providers, identity management systems, and existing services, including those in the travel industry like SABRE and APOLLO.

## Consequences

By selecting an API Gateway that meets the criteria outlined above, we anticipate the following consequences:

1. **Scalability**: The API Gateway's ability to scale horizontally will ensure that we can handle the expected user load and maintain low latency, meeting our performance goals.

2. **Customization**: The extensibility of the chosen API Gateway will allow us to tailor it to our specific needs, ensuring that it aligns perfectly with our requirements.

3. **Maintenance Overhead**: While flexibility is an advantage, it also means that we will need to manage and maintain the API Gateway's configuration and plugins over time. Proper documentation and training will be necessary for our team.

4. **Cost**: The cost associated with maintaining and scaling the infrastructure to support the selected API Gateway should be considered as part of the decision-making process.

In conclusion, the choice of an API Gateway is pivotal to our platform's success. We will carefully evaluate and select an API Gateway that aligns with our technical and business requirements, keeping in mind the consequences and responsibilities associated with our choice.

## References
- [Developers Roadmap](https://roadmap.sh/)
- [What is an API Gateway?](https://youtu.be/hYgP0cBORVg?si=uqpwNe7fnzScuxvf)
