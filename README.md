# overview
- GO libraries to develop micro services
### Microservice Architect
![Microservice Architect](https://camo.githubusercontent.com/368cfac1508618ab027885ebfb3df1d4eee4d93445352de354162b7806892aa5/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a3045744f716c524b69456836544f536a6764636766772e706e67)
### Libraries of core-go
![Collection of libraries of core-go](https://camo.githubusercontent.com/a7ef78cfca52e23f9484a56432be01a37fb7744995f05a5910b5554b1838e208/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a78684574357079776e6c67747348594b4b76635f64512e706e67)

## Databases
![Database](https://camo.githubusercontent.com/01c9e6dda6af2e00cc011d137927a03fc038d64668ea4a2b436f0f899a4652c2/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6c31675a584649355175537831782d4b2d51433776512e706e67)
- SQL: Sample is [go-sql-mongo-rest-api](https://github.com/source-code-template/go-sql-mongo-rest-api)
- Mongo: Sample is [go-sql-mongo-rest-api](https://github.com/source-code-template/go-sql-mongo-rest-api)
- Casandra
- Dynamodb
- Firestore
- Elasticsearch

## Storage
![storage](https://camo.githubusercontent.com/5f7b19bd0bc82451fa2a3c8b696715560d67f091b1597aaf3a3c644e82bd6e19/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a68657750665f4f61646b766f31674454696d6a5949512e706e67)
- Samples are at [go-storage](https://github.com/project-samples/go-storage)

## Cross-cutting concerns
![cross-cutting concerns](https://camo.githubusercontent.com/f18c275b941d7c2554549b906c1173daf3eb26b28192a893e799e0133192eead/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a526f352d47437572486756526c746a36746c555032772e706e67)
- We provide many libraries to minimize effort for cross-cutting concerns, which can be used by an AOP framework
- We do not implement an AOP framework

#### Evaluate effort for cross-cutting concerns
![Effort for cross-cutting concerns](https://camo.githubusercontent.com/49bd125a8efd5afd6a5aeb861a9aacddd1d9ed04048df04522446ef771d8aae1/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a584f633061764b42625f6c7366314d3966557a445a412e706e67)

### Health Check
![health](https://camo.githubusercontent.com/563b71e07ce74a6457066dc41260addf5e131db81b0903a0250a59cbd7634ae5/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a316b4645637876714d445a665457476d4a54454537672e706e67)


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
- Identity and Access Management: Authorization at middleware, support http ([mux](https://github.com/gorilla/mux), [chi](https://github.com/go-chi/chi)), [gin](https://github.com/gin-gonic/gin), [echo](https://github.com/labstack/echo)
- Crypto
- JWT

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

### Search
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
![Email](https://camo.githubusercontent.com/1a239ae784d3f8c33517b2b4b0860f6e438432c6589191072ae773204918fc39/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a374a46344f47397a427973754a71724f4958324a76672e706e67)
- Build some standard interfaces, which can be shared by multiple providers: SMTP and Sendgrid
- The sample is [go-authentication](https://github.com/project-samples/go-authentication)

#### Message Queue
![Message Queue](https://camo.githubusercontent.com/25ff46695aa80731f9814cff5036e38f65597cf76fd0cb93a1425745184a807a/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a355049763841616a34673031585050466169433059412e706e67)
##### The samples are [go-subscription](https://github.com/project-samples/go-subscription) and [go-batch-subscription](https://github.com/project-samples/go-batch-subscription)
##### Support these providers
- Amazon Simple Queue Service (SQS) at [sqs](https://github.com/core-go/mq/tree/main/sqs)
- Google Cloud Pub/Sub at [pubsub](https://github.com/core-go/mq/tree/main/pubsub)
- Kafka: at [segmentio/kafka-go](https://github.com/core-go/mq/tree/main/kafka), [Shopify/sarama](https://github.com/core-go/mq/tree/main/sarama) and [confluent](https://github.com/confluentinc/confluent-kafka-go)
- NATS at [nats](https://github.com/core-go/mq/tree/main/nats)
- Active MQ at [amq](https://github.com/core-go/mq/tree/main/amq)
- RabbitMQ at [rabbitmq](https://github.com/core-go/mq/tree/main/rabbitmq)
- IBM MQ at [ibm-mq](https://github.com/core-go/mq/tree/main/ibm-mq)

##### Support 2 reusable business flows
- Consume message and handle one by one
- Consume message and handle by batch

### Reusable business components
![Reusable business components](https://camo.githubusercontent.com/ea532f30062f85ea549d50ba4da256c99d4a978a1c5e4152a23dd6544b6fc4ab/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a484d41343065666c5f3431386f7950667541423751672e706e67)
- The sample is [go-authentication](https://github.com/project-samples/go-authentication)

### authentication
![Authentication](https://camo.githubusercontent.com/a394ea3c13f690ecb9cf4a1747973cce1bdc8558e659040995003e96e486f88a/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a56504f343261596a736c6d524937424c6369796a77412e706e67)
- authenticator
- ldap authenticator
- 2 factor authentication

### oauth2
![oauth2](https://camo.githubusercontent.com/a6cd5e06400bce64e704cae6bca2de6726d8c8fa0968baec74f0c5aa018594c6/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a4b615a64434239675a6745356c646543597a763834412e706e67)

### sign up
![sign up](https://camo.githubusercontent.com/3202736e57f5c785f1a1cf13b3a26876502547f49502358c239bd4006362b1fc/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a73586a4f4362654339796a586e684e32676c706950672e706e67)
#### sign up with password:
- sign up with password
- verify account (without password)
#### sign up without password:
- sign up without password
- verify account (require to input password)
### password
![password](https://camo.githubusercontent.com/c1aa4eeae3a5056cfc9d0cf59583e2d9555a25dfea538bfcfa2249ef08a7fe40/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a514a344a33506b6b734d69586f6751396546414142412e706e67)
- forgot password
- change password (also support change password 2 factors)
- reset password
