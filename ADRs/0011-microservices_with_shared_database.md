# 11. Using a Single Database for Microservices Architecture

Date: 2023-09-14

## Status

Accepted

### Context

We decided to use the Microservice Architecture style (refer-to:[0010-architectural-style-decision](../ADRs/0010-architectural-style-decision.md)) for our system. We have identified the need to maintain data consistency and reduce data redundancy while still benefiting from the advantages of a microservices architecture.

### Decision

After careful consideration and evaluation of the system's requirements and constraints, we have decided to use a single database for maintaining trip information for our microservices architecture to ensure data consistency and reduce redundancy. This approach entails the following key points:

1. **Shared Database:** All microservices in our architecture will share a common database instance (except for user management). This single database will store data that is required across multiple services.

2. **Isolated Schemas:** Each microservice will have its own database schema within the shared database. This ensures that data related to a specific service remains logically isolated from other services, preventing data interference.

3. **APIs for Data Access:** Services will communicate with the shared database using well-defined APIs and data access layers. This approach enforces data access boundaries and encapsulation, allowing services to interact with the database without direct access to tables or data structures belonging to other services.

4. **Data Consistency Measures:** We will implement strong data consistency mechanisms within the shared database. This includes transactions, foreign key constraints, and referential integrity checks to maintain the integrity of the data.

### Consequences

The decision to use a single database for our microservices architecture has several implications and consequences:

1. **Data Consistency:** By centralizing data storage, we ensure strong data consistency across services. Updates and transactions involving shared data are atomic and maintain referential integrity.

2. **Reduced Redundancy:** Sharing common data reduces data duplication, leading to a more efficient use of storage resources and easier data maintenance.

3. **Complexity:** While using a single database simplifies some aspects of data management, it also introduces complexity in terms of schema management, versioning, and access control. However, database migration tools like Flyway or Liquibase could reduce this complexity (refer-to: [Solution Strategy](../architecture/04_Solution_Strategy.md))

4. **Dependency:** Services become dependent on the availability and performance of the shared database. Any issues with the database can impact multiple services, potentially causing downtime or degraded performance.

5. **Scalability:** Scalability of the database becomes a concern as it must handle the load of multiple services. Database performance tuning and scaling strategies must be carefully considered.

6. **Security:** Access control and data isolation become critical to ensure that one service cannot access or modify the data of another service inappropriately. Robust authentication and authorization mechanisms must be implemented.

In conclusion, the decision to use a single database in our microservices architecture is made to prioritize data consistency and reduce redundancy. While it offers benefits in terms of data integrity and efficiency, it also introduces complexities that must be managed effectively to ensure the overall success of our microservices-based application. Ongoing monitoring and maintenance of the shared database are essential to address evolving needs and maintain system reliability.

## References
- [Developers Roadmap](https://roadmap.sh/)
- [Fundamentals of Software Architecture](https://learning.oreilly.com/library/view/fundamentals-of-software/9781492043447/)
