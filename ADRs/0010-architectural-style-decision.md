# 10. Architectural style architecture decision

Date: 2023-09-12

## Status

Accepted
## Context

In response to the requirements presented by a new startup aiming to create a next-generation online trip management dashboard, we are tasked with making architectural decisions to meet the demands of a large user base and complex functionality. Key contextual factors influencing this decision include:

### Users:

Two million active users per week with a total of 15 million user accounts.
The need to support both web and mobile access.
### Functional Requirements:

- Email integration for travel-related emails.
- Real-time travel updates from airline, hotel, and car rental systems.
- Manual reservation management capabilities.
- Dynamic organization of items by trip and automatic removal upon trip completion.
- Social media sharing of trip information.
- Rich user interface across all deployment platforms.
- End-of-year summary reports for users.
- Data analytics for travel trends and preferences.

### Technical Requirements:

- Seamless integration with existing travel systems (SABRE, APOLLO).
- Integration with a preferred travel agency for rapid issue resolution.
- International functionality.
- High availability (max 5 minutes of unplanned downtime per month).
- Real-time updates with a 5-minute generation-to-display constraint.
- Web response time (800ms) and mobile first-contentful paint (under 1.4 seconds).

## Decision

After conducting internal brainstorming sessions and analyzing the outcomes through the [Architecture Characteristics Worksheet](../images/ARCH-KATA-07_Architecture_Characteristics_Worksheet.png), as well as considering various architectural styles (refer to: [Architecture Styles Overview](../images/ARCH-KATA-07_Architecture_Styles_Worksheet.png),  [Architecture Styles Selection](../images/ARCH-KATA-07_Architecture_Styles_Worksheet_Concrete_Comparison.PNG))  and taking into account the defined requirements and context, we've made the decision to embrace a Microservices Architecture combined with a Serverless Computing approach for the creation of the online trip management dashboard. This architectural selection aligns perfectly with our requirements for scalability, high availability, real-time data updates, and international support.

Microservices Architecture will allow us to break down the application into small, independently deployable services. Each microservice can cater to a specific functionality, such as email processing, reservation management, real-time updates, reporting, and analytics. This separation of concerns will facilitate rapid development, scalability, and easier maintenance of individual components.

Serverless Computing complements the Microservices Architecture by enabling automatic scaling, minimizing operational overhead, and ensuring high availability. Serverless functions can handle tasks like email polling, data updates, and real-time notifications without the need for manual server provisioning or maintenance. This approach aligns with the constraint of minimal unplanned downtime and ensures responsiveness.

## Consequences
1. Scalability: The combination of Microservices and Serverless Computing will enable us to scale components independently, ensuring that the system can handle the two million active users per week and support international usage.
2. High Availability: Serverless architecture inherently provides high availability and resilience against failures, aligning with the requirement for minimal unplanned downtime.
3. Real-time Updates: With Microservices managing real-time updates from travel sources, we can ensure that travel details appear in the app within five minutes, surpassing the competition.
4. Complexity: Managing a Microservices ecosystem, especially in an international context, may introduce complexity in terms of service orchestration, data consistency, and monitoring. Robust DevOps practices will be essential to address these challenges.
5. Rapid Development: The modular nature of Microservices allows for efficient development and integration with existing systems like SABRE and APOLLO.
6. Analytics and Reporting: Serverless functions can process and analyze travel data efficiently, providing valuable insights for reporting and end-of-year summaries.
7. Integration: Seamless integration with the preferred travel agency will be achieved through API integration with their systems.
8. Sustainability: Serverless computing will save costs in terms of computation for tasks like Analytics and Reporting or E-Mail polling. Along with that we are able to improve sustainability of the architecture and reduce the footprint of the overall system by not running stand-by/idle instances and saving power.

In conclusion, the adoption of a Microservices Architecture combined with Serverless Computing addresses the startup's requirements for scalability, real-time updates, high availability, and international functionality. However, careful consideration of complexity management and robust DevOps practices will be crucial to successful implementation.

## References
- [Developers Roadmap](https://roadmap.sh/)
- [Fundamentals of Software Architecture](https://learning.oreilly.com/library/view/fundamentals-of-software/9781492043447/)
- [Architectural Patterns in a nutshell](https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013)
- [Pattern: Microservice Architecture](https://microservices.io/patterns/microservices.html)
- [What is Microservices?](https://smartbear.com/solutions/microservices/)
- [Microservices 101](https://thenewstack.io/microservices-101/)
- [Serverless](https://www.ibm.com/cloud/learn/serverless)
- [AWS Services](https://aws.amazon.com/serverless/)
- [Serverless Computing in 100 Seconds](https://www.youtube.com/watch?v=W_VV2Fx32_Y&ab_channel=Fireship)