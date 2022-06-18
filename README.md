# overview
- GO libraries to develop micro services
### Microservice Architect
![Microservice Architect](https://camo.githubusercontent.com/cf46a1780520d3612f1d81b219b56a14428fc24bb4ae9f4eede169aa9c58bee8/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a764b6565504f5f5543373369377466796d536d594e412e706e67)

### A typical micro service
When you zoom one micro service, the flow is as below
![A typical micro service](https://camo.githubusercontent.com/581033268b9152e7ea8881904f533a51a29eeb3a63e8d6478540668c6e422ce3/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a64396b79656b416251594278482d4336773338585a512e706e67)
#### Hexagonal Architecture
![Hexagonal Architecture](https://camo.githubusercontent.com/f269cbeebcc31cc4adf5d6080a29d776b0f2e5293a8f1f1e5a73b7b835a5291c/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a446d6635374f32466b6278366b7465617135525655772e706e67)
#### In the above image, you can see these libraries you need for a typical micro service
- [authentication](https://github.com/core-go/auth)
- [security](https://github.com/core-go/security)
- [config](https://github.com/core-go/config)
- [health](https://github.com/core-go/health)
- [log](https://github.com/core-go/log)
- [middleware](https://github.com/core-go/middleware)
- [cache](https://github.com/core-go/cache)
- [redis](https://github.com/core-go/redis)
- [validator](https://github.com/core-go/validator)
- [client](https://github.com/core-go/client)
- [io](https://github.com/core-go/io)
- [mail](https://github.com/core-go/mail)
  - [smtp](https://github.com/core-go/mail/tree/main/smtp)
  - [sendgrid](https://github.com/core-go/mail/tree/main/sendgrid)
- [mq](https://github.com/core-go/mq)
  - [Amazon SQS](https://github.com/core-go/mq/tree/main/sqs)
  - [Google Pub/Sub](https://github.com/core-go/mq/tree/main/pubsub)
  - [kafka](https://github.com/core-go/mq/tree/main/kafka)
  - [NATS](https://github.com/core-go/mq/tree/main/nats)
  - [Active MQ](https://github.com/core-go/mq/tree/main/activemq)
  - [Rabbit MQ](https://github.com/core-go/mq/tree/main/rabbitmq)
  - [IBM MQ](https://github.com/core-go/mq/tree/main/ibmmq)
- [storage](https://github.com/core-go/storage)
  - [Google](https://github.com/core-go/storage/tree/main/google)
  - [Amazon S3](https://github.com/core-go/storage/tree/main/s3)
- [sql](https://github.com/core-go/sql)
- [cassandra](https://github.com/core-go/cassandra)
- [mongo](https://github.com/core-go/mongo)
- [firestore](https://github.com/core-go/firestore)
- [dynamodb](https://github.com/core-go/dynamodb)
- [elasticsearch](https://github.com/core-go/elasticsearch)

### Cross-cutting concerns
![cross-cutting concerns](https://camo.githubusercontent.com/0416e6d9aa090b3b42901b4dd22b19c8962abe6c589988b1e97dea97b63a278d/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a7930383854344e6f4a4e724c397371724b65537971772e706e67)
- We provide many libraries to minimize effort for cross-cutting concerns, which can be used by an AOP framework
- We do not implement an AOP framework

#### Evaluate effort for cross-cutting concerns
![Effort for cross-cutting concerns](https://camo.githubusercontent.com/c354215dd62ae32dcf5bd39389c5fff8be0abe2e93fccbb754191ea182d2f768/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6877347538646e75586d6436685649763053767579672e706e67)

### Summary: Libraries of core-go
![Collection of libraries of core-go](https://camo.githubusercontent.com/c9c636d48e5845439d0ee958a50b655767ce60c7d23152d7c95e0ad93d1ebd59/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a626e7348447a5458696c76666d492d48624e6e4b39512e706e67)

## Databases
![Database](https://camo.githubusercontent.com/afdab5cc52c2d69b5d8bebedd776d9440ac67544b295e6af1e453b7e9b6a26e3/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a656f595865466d6c494f462d63684f4356714a6130412e706e67)

- SQL: Sample is [go-sql-mongo-rest-api](https://github.com/source-code-template/go-sql-mongo-rest-api)
- Mongo: Sample is [go-sql-mongo-rest-api](https://github.com/source-code-template/go-sql-mongo-rest-api)
- Casandra
- Dynamodb
- Firestore
- Elasticsearch

## Storage
![storage](https://camo.githubusercontent.com/8df4819a272d0e1c4cb235ce34448b4b4bb4fc480ced77238deacd98daafea1d/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6a685a79423845364a4d547437714757473963666b412e706e67)
- Samples are at [go-storage](https://github.com/project-samples/go-storage)

### Health Check
![health](https://camo.githubusercontent.com/49287a63a0e1c52818c4321650b3f8cf2348d5f50108aed820cd6441fbb2574d/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6746457a416b7674666e51575665463265644b7767512e706e67)

### Logging
#### Providers
Standardize API for logging, support 2 libraries:
- [logrus](https://github.com/sirupsen/logrus)
- [zap](go.uber.org/zap)

#### Request Tracing
- [middleware](https://github.com/core-go/middleware): Log request and response at http middleware, allow to configure dynamic field names
- [client](https://github.com/core-go/client): Log request and response at http client, allow to configure dynamic field names

#### Audit Log
- Support for CRUD, search (not required in every application)

### Security
Sample is [go-admin](https://github.com/project-samples/go-admin)
- Identity and Access Management: Authorization at middleware, support http ([mux](https://github.com/gorilla/mux), [chi](https://github.com/go-chi/chi)), [gin](https://github.com/gin-gonic/gin), [echo](https://github.com/labstack/echo)
- Crypto
- JWT

- library is here [security](https://github.com/core-go/security)

### Caching
#### Memory Cache
- Time To Live: automatically clean up the expired objects in the memory cache
- Maximum size: When the memory exceeds the max size (which is configurable), it automatically remove the oldest object.
#### Redis
Support 2 libraries
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

### Communication
#### Email
![Email](https://camo.githubusercontent.com/0fcd0826eea9b9883077ac1674e45c4eafa17e7abb02f8d2659fb30bc2b084e5/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a2d6c486a7872355a4d6b4b634c6961746776364731672e706e67)
- Build some standard interfaces, which can be shared by multiple providers: SMTP and Sendgrid
- The sample is [go-authentication](https://github.com/project-samples/go-authentication)

#### Message Queue
![Message Queue](https://camo.githubusercontent.com/31291934a502f50fda6ec65981f77e601efa450f7ef32b3e4bd9041355d68e3e/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a55624b4a753242634159696d385f6f4a67384e7336412e706e67)
##### The samples are [go-subscription](https://github.com/project-samples/go-subscription) and [go-batch-subscription](https://github.com/project-samples/go-batch-subscription)
##### Flow to consume a message from a queue
![Flow to consume a message](https://camo.githubusercontent.com/782bbf69a516401c3918b7e920d8fc25521112d8b04e890f2455768551f6d64e/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a593451554e36516e666d4a67614b6967634e486251412e706e67)
- Consume a message from queue, then write the message to database (SQL, Mongo, Casandra, Dynamodb, Firestore, Elasticsearch)
- Use [core-go/mq](https://github.com/core-go/mq)
- Support these message queues:
  - Amazon Simple Queue Service (SQS) at [sqs](https://github.com/core-go/mq/tree/main/sqs)
  - Google Cloud Pub/Sub at [pubsub](https://github.com/core-go/mq/tree/main/pubsub)
  - Kafka: at [segmentio/kafka-go](https://github.com/core-go/mq/tree/main/kafka), [Shopify/sarama](https://github.com/core-go/mq/tree/main/sarama) and [confluent](https://github.com/core-go/mq/tree/main/confluent)
  - NATS at [nats](https://github.com/core-go/mq/tree/main/nats)
  - Active MQ at [activemq](https://github.com/core-go/mq/tree/main/activemq)
  - RabbitMQ at [rabbitmq](https://github.com/core-go/mq/tree/main/rabbitmq)
  - IBM MQ at [ibmmq](https://github.com/core-go/mq/tree/main/ibmmq)
- Support these databases
  - SQL
  - Mongo
  - Casandra
  - Dynamodb
  - Firestore
  - Elasticsearch

##### Support 2 reusable business flows
- Consume message and handle one by one
- Consume message and handle by batch

### Reusable business components
![Reusable business components](https://camo.githubusercontent.com/d47b277783bd12f7560123878265c9446368a092937cf2d37fcf54c14e872d83/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a4834474a415f53705f73366967396b5f41415a3561672e706e67)
- The sample is [go-authentication](https://github.com/project-samples/go-authentication)

### sign up
![sign up](https://camo.githubusercontent.com/6731bc23c5c74d5a19a860ddc50a9af188434632ecfe5b2dda90397759b7de39/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a3073646b717a646479663339374e56776b56645269772e706e67)
#### sign up with password
- sign up with password
- verify account (without password)
#### sign up without password
- sign up without password
- verify account (require to input password)

### authentication
![Authentication](https://camo.githubusercontent.com/961908454560f4fdcd044a27e1741bc13d8440d794ad69d4fd6bf77023195701/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a7652314a553030384e555234774b4567717766756f412e706e67)
- authenticator
- ldap authenticator
- 2 factor authentication

### oauth2
![oauth2](https://camo.githubusercontent.com/782b650c42e2a73f79e729e77176f3dbd5edf51b683e13ebdae0a6f5e4cdd7b2/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6153765054544461532d386c674f4164544d6e6335412e706e67)

### password
![password](https://camo.githubusercontent.com/d27ddd22c67677cd23a53df92f070d54dce337caa2cf91ee1c36c354112f1551/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a79684969414c6a4a514a373062354866796265666b512e706e67)
- forgot password
- change password (also support change password 2 factors)
- reset password

## Low code
### Components
![Components](https://camo.githubusercontent.com/c95340f3089dc8535b668c08bfa32086d3d7b64998f687284357fd27028eca95/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a476f314777666d704274566441556e747252327179512e706e67)
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
![Business View](https://camo.githubusercontent.com/8a7981234d8731878d566e6da0cd02804b93f4e9cd23c7e1ef33a810c5f66cee/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a68317942526c435750554d417653355a77356b3461672e706e67)
#### Download
- https://github.com/lowcode-tech/windows
- https://github.com/lowcode-tech/mac
- https://github.com/lowcode-tech/linux
#### Output Samples
https://github.com/source-code-template
##### GO Layer Architecture Sample
- https://github.com/source-code-template/mongo-layer-architecture-sample
- https://github.com/source-code-template/go-sql-layer-architecture-sample
##### GO Modular Sample
- https://github.com/source-code-template/go-mongo-modular-sample
- https://github.com/source-code-template/go-sql-modular-sample
##### nodejs Layer Architecture Sample
- https://github.com/source-code-template/mongo-layer-architecture-sample
- https://github.com/source-code-template/sql-layer-architecture-sample
##### nodejs Modular Sample
- https://github.com/source-code-template/mongo-layer-architecture-sample
- https://github.com/source-code-template/sql-layer-architecture-sample
##### nodejs Simple Modular Sample
- https://github.com/source-code-template/mongo-simple-modular-sample
- https://github.com/source-code-template/sql-simple-modular-sample
