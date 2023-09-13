# 3. RDBMS for user data management
Date: 2023-09-13

## Status

Accepted
## Context

For the solution strategy of the Online Trip Management Dashboard, we are faced with a critical decision regarding the storage and management of user data, particularly user accounts, reservations, and related information. The choice of an appropriate data storage solution is essential for the reliability, scalability, and security of the application.

## Decision

After careful consideration and evaluation of our requirements, we have decided to use a Relational Database Management System (RDBMS) for storing and managing user data.

### Reasons for Choosing RDBMS:

1. **Data Structure Consistency:** RDBMS enforces a structured schema, ensuring data consistency and integrity. This is crucial for user account information, where data correctness is paramount.

2. **Query Flexibility:** RDBMS systems offer robust querying capabilities, enabling complex searches and reporting, which is essential for generating user reports and analytics.

3. **Maturity and Reliability:** RDBMS technologies like PostgreSQL, MySQL, or Microsoft SQL Server have a proven track record of reliability and stability, making them suitable for production environments.

4. **Scalability Options:** RDBMS systems offer horizontal and vertical scaling options, allowing us to scale as our user base grows. Techniques like sharding and replication can be employed for high availability and scalability.

5. **Security Features:** RDBMS platforms provide robust security features such as access controls, authentication, and encryption, which are crucial for protecting user data.

6. **Data Backup and Recovery:** RDBMS systems typically include mechanisms for data backup and recovery, ensuring data resilience in case of unexpected failures.

## Consequences

While the decision to use an RDBMS for user data offers several advantages, it also comes with some potential consequences:

1. **Complexity:** Proper schema design and maintenance are required.

2. **Scalability Challenges:** Although RDBMS systems offer scalability options, there may be limitations in handling extremely large datasets and high-throughput workloads. This may necessitate advanced scaling strategies.

3. **Development Overhead:** RDBMS requires developers to adhere to a structured schema, which may involve additional development effort compared to schema-less databases.

4. **Query Performance:** Complex queries may require careful indexing and optimization to maintain high query performance.

In summary, the decision to use an RDBMS for user data is driven by the need for data consistency, query flexibility, and reliability. However, it is essential to carefully manage complexities, scalability, and costs associated with this choice throughout the development and operation of the Online Trip Management Dashboard.


