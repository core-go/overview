# Overview
## What is a Microservice
A microservice is an architectural style that structures an application as a collection of small, loosely coupled, independently deployable services. Each service typically focuses on a specific business capability and can be developed, deployed, and scaled independently. Microservices communicate with each other through well-defined APIs, often using lightweight protocols such as HTTP/REST, gRPC, or messaging queues.

![Microservice Architect](https://cdn-images-1.medium.com/max/800/1*vKeePO_UC73i7tfymSmYNA.png)
### Comparison: Microservice vs. Monolithic Architecture
#### Monolithic Architecture
- <b>Structure</b>: A single, unified codebase where all components are tightly integrated.
- <b>Deployment</b>: Deployed as a single unit. Any change or update requires redeploying the entire application.
- <b>Development</b>: Usually simpler to develop initially but can become complex and difficult to manage as the application grows.
- <b>Scaling</b>: Scaling requires scaling the entire application, even if only a small part of it requires more resources.
#### Microservice Architecture
- <b>Structure</b>: Composed of multiple, independent services, each responsible for a specific business function.
- <b>Deployment</b>: Each service can be deployed independently, allowing for continuous deployment and updates.
- <b>Development</b>: Enables teams to work on different services simultaneously, often with different technologies and frameworks.
- <b>Scaling</b>: Allows for granular scaling, where individual services can be scaled independently based on their specific resource needs.

### Advantages of Microservices
#### Independent Deployment
- Each service can be deployed, updated, and scaled independently, reducing the risk of deployment failures and allowing for faster release cycles.
#### Technology Diversity
- Teams can choose the best technology stack for each service based on its requirements, enabling the use of the latest and most suitable technologies.
#### Fault Isolation
- Failures in one service do not necessarily affect other services, enhancing the overall resilience and reliability of the application.
#### Scalability
- Services can be scaled independently, allowing for more efficient use of resources and cost-effective scaling.
#### Organizational Alignment
- Microservices align well with agile and DevOps practices, allowing teams to be more autonomous and responsible for specific services.
#### Improved Maintainability
- Smaller codebases are easier to understand, maintain, and refactor, leading to better code quality and reduced technical debt.
### Disadvantages of Microservices
#### Complexity:
- Managing multiple services, including their deployment, monitoring, and communication, introduces significant complexity compared to a monolithic application.
#### Distributed System Challenges
- Issues such as network latency, message serialization, and handling partial failures need to be addressed.
#### Data Consistency
- Maintaining data consistency across services can be challenging and often requires implementing complex patterns like eventual consistency and distributed transactions.
#### Increased Resource Consumption
- Running multiple services often requires more resources, such as CPU, memory, and storage, compared to a monolithic application.
#### DevOps Overhead
- Requires robust DevOps practices, including continuous integration, continuous deployment, containerization, and orchestration tools like Kubernetes.
#### Inter-Service Communication
- Communication between services needs to be carefully managed to ensure efficient and reliable interactions, often requiring additional infrastructure like API gateways and service meshes.

### Use Cases of Microservices
#### E-commerce Platforms
- Individual services for user management, product catalog, inventory, payment processing, and order management.
#### Financial Systems
- Separate services for account management, transaction processing, fraud detection, and reporting.
#### Social Media Applications
- Distinct services for user profiles, posts, comments, likes, notifications, and messaging.
#### Healthcare Systems
- Independent services for patient records, appointment scheduling, billing, and prescription management.
### Conclusion
Microservices offer significant benefits in terms of flexibility, scalability, and maintainability, making them suitable for large, complex applications with high demands for agility and reliability. However, they also introduce considerable complexity and require sophisticated DevOps practices and infrastructure. The choice between monolithic and microservice architecture depends on the specific requirements, scale, and maturity of the development and operations teams within an organization.

## core-go
GO libraries to develop micro services.

### A typical micro service
When you zoom one micro service, the flow is as below
![A typical micro service](https://cdn-images-1.medium.com/max/800/1*d9kyekAbQYBxH-C6w38XZQ.png)

#### In the above image, you can see these libraries you need for a typical micro service

### Database
- Simplify common database operations, such as CRUD (Create, Read, Update, Delete) operations, batch processing and transactions (for [SQL](https://github.com/core-go/sql)), by providing high-level abstractions and utilities.
- Generic CRUD Repository
  - It is like [CrudRepository](https://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/repository/CrudRepository.html) of Spring, which promotes rapid development and consistency across applications.
  - While it provides many advantages, such as reducing boilerplate code and ensuring transactional integrity, it also offers flexibility and control over complex queries.
- My batis for GOLANG, nodejs
  - Project sample is at [go-admin](https://github.com/project-samples/go-admin). Mybatis file is here [query.xml](https://github.com/project-samples/go-admin/blob/main/configs/query.xml)
- Support:
  - [SQL](https://github.com/core-go/sql). The sample is at [go-sql-generic-sample](https://github.com/source-code-template/go-sql-generic-sample).
  - [Mongo](https://github.com/core-go/mongo). The sample is at [go-mongo-generic-sample](https://github.com/source-code-template/go-mongo-generic-sample).
  - [Cassandra](https://github.com/core-go/cassandra). The sample is at [go-cassandra-sample](https://github.com/source-code-template/go-cassandra-sample).
  - [Firestore](https://github.com/core-go/firestore). The sample is at [go-firestore-sample](https://github.com/go-tutorials/go-firestore-sample).
  - [Elastic Search](https://github.com/core-go/elasticsearch). The sample is at [go-elastic-search-generic-sample](https://github.com/source-code-template/go-elastic-search-generic-sample).
  - [Hive](https://github.com/core-go/hive). The sample is at [go-hive-sample](https://github.com/go-tutorials/go-hive-sample).
  - [Dynamodb](https://github.com/core-go/dynamodb). The sample is at [go-dynamodb-tutorial](https://github.com/go-tutorials/go-dynamodb-tutorial).

### Data Processing
Visit [core-go/io](https://github.com/core-go/io), you can see rich data processing:
- Import data from CSV or fix-length format files to [SQL](https://github.com/core-go/sql), [Mongo](https://github.com/core-go/mongo), [Cassandra](https://github.com/core-go/cassandra), [Firestore](https://github.com/core-go/firestore), [Elastic Search](https://github.com/core-go/elasticsearch), [Hive](https://github.com/core-go/hive)
- Export data from [SQL](https://github.com/project-samples/go-sql-export), [Mongo](https://github.com/project-samples/go-mongo-export), [Cassandra](https://github.com/project-samples/go-cassandra-export), [Firestore](https://github.com/project-samples/go-firestore-export), [Hive](https://github.com/project-samples/go-hive-export) to CSV or fix-length format files

### Message Queue
- Please visit [core-go/mq](https://github.com/core-go/mq).
- Because message queues are a crucial component in modern software architecture, we support most of message queues, such as [Kafka](https://github.com/project-samples/go-kafka-sample), [RabbitMQ](https://github.com/project-samples/go-rabbit-mq-sample), [IBMMQ](https://github.com/project-samples/go-ibm-mq-sample), [Active MQ](https://github.com/project-samples/go-active-mq-sample), [NATS](https://github.com/project-samples/go-nats-sample), [Google Pub/Sub](https://github.com/project-samples/go-pubsub-sample), [Amazon SQS](https://github.com/project-samples/go-amazon-sqs-sample).
- Support 2 levels of 7 message queues:
  - Standardize and simplify to use 7 message queues, for 9 libraries [rabbitmq/amqp091-go](https://github.com/rabbitmq/amqp091-go), [aws-sdk-go/service/sqs](https://github.com/aws/aws-sdk-go/tree/main/service/sqs), [go/pubsub](https://pkg.go.dev/cloud.google.com/go/pubsub), [ibmmq](https://github.com/ibm-messaging/mq-golang), [ActiveMQ](https://github.com/go-stomp/stomp), [nats.go](https://github.com/nats-io/nats.go), [segmentio/kafka-go](https://github.com/segmentio/kafka-go), [IBM/sarama](https://github.com/IBM/sarama) and [Confluent](https://github.com/confluentinc/confluent-kafka-go).
  - Support standard level, which share the same interface with all message queues
    - Abstract the consumer flow
    - Support dead letter queue
  - Support SDK or original library level, you can use all advance features of the SDK/libraries

### Health Check
Please visit [core-go/health](https://github.com/core-go/health). We support databases, message queues, redis, http client:
- [http client](https://github.com/core-go/health/blob/main/http/health_checker.go)
- Redis: [go-redis/redis](https://github.com/core-go/health/blob/main/redis/v9/health_checker.go) to support [redis/go-redis](https://github.com/redis/go-redis), [garyburd/redigo](https://github.com/core-go/health/blob/main/redigo/health_checker.go) to support [gomodule/redigo](https://github.com/gomodule/redigo).
- Database: [sql](https://github.com/core-go/health/blob/main/sql/health_checker.go), [mongo](https://github.com/core-go/health/blob/main/mongo/health_checker.go), [dynamodb](https://github.com/core-go/health/blob/main/dynamodb/health_checker.go), [firestore](https://github.com/core-go/health/blob/main/firestore/health_checker.go), [elasticsearch](https://github.com/core-go/health/blob/main/elasticsearch/v8/health_checker.go), [cassandra](https://github.com/core-go/health/blob/main/cassandra/health_checker.go), [hive](https://github.com/core-go/health/blob/main/hive/health_checker.go)
- Message queues: [Kafka](https://github.com/project-samples/go-kafka-sample), [RabbitMQ](https://github.com/project-samples/go-rabbit-mq-sample), [IBMMQ](https://github.com/project-samples/go-ibm-mq-sample), [Active MQ](https://github.com/project-samples/go-active-mq-sample), [NATS](https://github.com/project-samples/go-nats-sample), [Google Pub/Sub](https://github.com/project-samples/go-pubsub-sample), [Amazon SQS](https://github.com/project-samples/go-amazon-sqs-sample).

![health](https://cdn-images-1.medium.com/max/800/1*k-VjYL3UL9Zohwzas4nb8Q.png)

### Logging
#### Providers
Standardize API for logging, support 2 libraries:
- [logrus](https://github.com/sirupsen/logrus)
- [zap](go.uber.org/zap)

#### Middleware Log Tracing
- [middleware](https://github.com/core-go/middleware): Log request and response at http middleware, allow to configure dynamic field names

#### Http Client Log Tracing
- [client](https://github.com/core-go/client): Log request and response at http client, allow to configure dynamic field names

#### Audit Log
- Support for CRUD, search (not required in every application)

### Caching
#### Memory Cache
Refer to [MemoryCacheService](https://github.com/core-go/redis/blob/main/cache/memory_cache_service.go) for more details
- Time To Live: automatically clean up the expired objects in the memory cache
- Maximum size: When the memory exceeds the max size (which is configurable), it automatically remove the oldest object.
#### Redis
The library is here [Redis](https://github.com/core-go/redis). Support 2 libraries:
- [go-redis](https://github.com/go-redis/redis)
- [redigo](https://github.com/garyburd/redigo)

### Validator
Check required, email, url, min, max, country code, phone number, regular expression...
- [validator](https://github.com/core-go/validator)

### Search
Samples are [go-admin](https://github.com/project-samples/go-admin), [go-backoffice](https://github.com/project-samples/go-backoffice) and [go-location](https://github.com/project-samples/go-location)
- Generate the model by URL
- Paging
- Sort
#### Build a dynamic query for these providers
- SQL
- Mongo
- Dynamodb
- Firestore
- Elasticsearch

### Email
- Build some standard interfaces, which can be shared by multiple providers: SMTP and Sendgrid
- [mail](https://github.com/core-go/mail)
  - [smtp](https://github.com/core-go/mail/tree/main/smtp)
  - [sendgrid](https://github.com/core-go/mail/tree/main/sendgrid)
- The sample is [go-authentication](https://github.com/project-samples/go-authentication)

### Storage
- [storage](https://github.com/core-go/storage)
  - [Google](https://github.com/core-go/storage/tree/main/google)
  - [Amazon S3](https://github.com/core-go/storage/tree/main/s3)
- Samples are at [go-storage](https://github.com/project-samples/go-storage)

### Authentication
Please visit [Authentication](https://github.com/core-go/authentication), we support:
- Support to log in by user name/password
- Login by LDAP (both server side and client slide)
- Login by Google, Facebook, Linkedin, Microsoft, Amazon, Dropbox
- Support any database design (SQL, Mongo, Firestore, Cassandra)

### Authorization
Please visit [security](https://github.com/core-go/security):
Sample is [go-admin](https://github.com/project-samples/go-admin)
- Identity and Access Management: Authorization at middleware, support http ([mux](https://github.com/gorilla/mux), [chi](https://github.com/go-chi/chi)), [gin](https://github.com/gin-gonic/gin), [echo](https://github.com/labstack/echo)
  - Support any database design (SQL, Mongo, Firestore, Cassandra)
- Crypto
- JWT

### Others
- [config](https://github.com/core-go/config)

### sign up
![sign up](https://cdn-images-1.medium.com/max/800/1*0sdkqzddyf397NVwkVdRiw.png)
#### sign up with password
- sign up with password
- verify account (without password)
#### sign up without password
- sign up without password
- verify account (require to input password)

### authentication
![Authentication](https://cdn-images-1.medium.com/max/800/1*vR1JU008NUR4wKEgqwfuoA.png)
- authenticator
- ldap authenticator
- 2 factor authentication

### oauth2
![oauth2](https://cdn-images-1.medium.com/max/800/1*aSvPTTDaS-8lgOAdTMnc5A.png)

### password
![password](https://cdn-images-1.medium.com/max/800/1*yhIiALjJQJ70b5HfybefkQ.png)
- forgot password
- change password (also support change password 2 factors)
- reset password

## Summary:
- Libraries of core-go

![Collection of libraries of core-go](https://cdn-images-1.medium.com/max/800/1*bnsHDzTXilvfmI-HbNnK9Q.png)

### Cross-cutting concerns
![cross-cutting concerns](https://cdn-images-1.medium.com/max/800/1*y088T4NoJNrL9sqrKeSyqw.png)

### Hexagonal Architecture
![Hexagonal Architecture](https://cdn-images-1.medium.com/max/800/1*Dmf57O2Fkbx6kteaq5RVUw.png)

## Low code
### Components
![Components](https://cdn-images-1.medium.com/max/800/1*Go1GwfmpBtVdAUntrR2qyQ.png)
#### Commandline
##### export
- input: database, project settings
- output: metadata
##### generate
- input: metadata, project templates
- output: project (working application)
#### GUI
##### generator
- GUI, include "export" and "generate"

### Business View
![Business View](https://cdn-images-1.medium.com/max/800/1*h1yBRlCWPUMAvS5Zw5k4ag.png)
#### Download
- https://github.com/lowcode-tech/windows
- https://github.com/lowcode-tech/mac
- https://github.com/lowcode-tech/linux
#### Output Samples
https://github.com/source-code-template
##### GO Layer Architecture Sample
- https://github.com/source-code-template/go-sql-sample
- https://github.com/source-code-template/go-mongo-sample
##### nodejs Layer Architecture Sample
- https://github.com/source-code-template/mongo-layer-architecture-sample
- https://github.com/source-code-template/sql-layer-architecture-sample
##### nodejs Modular Sample
- https://github.com/source-code-template/mongo-layer-architecture-sample
- https://github.com/source-code-template/sql-layer-architecture-sample
##### nodejs Simple Modular Sample
- https://github.com/source-code-template/mongo-simple-modular-sample
- https://github.com/source-code-template/sql-simple-modular-sample
