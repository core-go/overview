# overview
- GO libraries to develop micro services
### Microservice Architect
![Microservice Architect](https://camo.githubusercontent.com/909373b6f82e8870471feb67d019c52f69c01163b0ce9db0442617f13753ebaf/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a665530785930477077554e566c5a517a354f78504c672e706e67)

### Libraries of core-go
![Collection of libraries of core-go](https://camo.githubusercontent.com/60d52cda67f71d52dd27f42605b1f26cc55be9b34283d53126c761c1d8e11e16/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a434c4e3643377245456555755330714e7937476944672e706e67)

## Databases
![Database](https://camo.githubusercontent.com/4f129f87818ba83ebb04f54ddd7b8339dd44248e120c93ab9d165680351895d3/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6a56423167675250713536424c39332d4830547233512e706e67)
- SQL: Sample is [go-sql-mongo-rest-api](https://github.com/source-code-template/go-sql-mongo-rest-api)
- Mongo: Sample is [go-sql-mongo-rest-api](https://github.com/source-code-template/go-sql-mongo-rest-api)
- Casandra
- Dynamodb
- Firestore
- Elasticsearch

## Storage
![storage](https://camo.githubusercontent.com/2514b228fc47efe0b178dd7bec1c29128b439b232a1025b082928a57250cbd6a/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a724d58443479474e585736724c3448413237587346412e706e67)
- Samples are at [go-storage](https://github.com/project-samples/go-storage)

## Cross-cutting concerns
![cross-cutting concerns](https://camo.githubusercontent.com/0040ccb77dfa3d9cd93f873f35caa2eb2672892f062f87467aede319ddd10bbf/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a56416c555f764b38777642723343703848636b6865512e706e67)
- We provide many libraries to minimize effort for cross-cutting concerns, which can be used by an AOP framework
- We do not implement an AOP framework

#### Evaluate effort for cross-cutting concerns
![Effort for cross-cutting concerns](https://camo.githubusercontent.com/c354215dd62ae32dcf5bd39389c5fff8be0abe2e93fccbb754191ea182d2f768/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6877347538646e75586d6436685649763053767579672e706e67)

### Health Check
![health](https://camo.githubusercontent.com/90474880c142eb8681be645d52c2449c9942d4997fb383f48eca769a9063340a/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6b70533341504345474a51354b7874764341745552512e706e67)


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
![Email](https://camo.githubusercontent.com/b59e219454a863f63a7de1d416abbca40e458d542d4e12ddf0f3d25531b470fd/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a5737344c72354849557168506e58444b497a4a6741772e706e67)
- Build some standard interfaces, which can be shared by multiple providers: SMTP and Sendgrid
- The sample is [go-authentication](https://github.com/project-samples/go-authentication)

#### Message Queue
![Message Queue](https://camo.githubusercontent.com/2092e042898e06a0019cab3fdc78ce996aace45474fb0be2621f992ac6707a89/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a4c436632527437634d6b3953504e4a346758374579512e706e67)
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
![Reusable business components](https://camo.githubusercontent.com/7cb15f5f95d72f2559ad31737384fb7c356e5d2285e0c9930443b32a2e9ecbe4/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a485f58376251623544544d55456749784c44325169772e706e67)
- The sample is [go-authentication](https://github.com/project-samples/go-authentication)

### authentication
![Authentication](https://camo.githubusercontent.com/dd7972afcd6300a4571b3807b3238b08c6bf132133d33a76c498617d4bfd615a/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a6f34784e4553485f4a795f69345046427a52436957772e706e67)
- authenticator
- ldap authenticator
- 2 factor authentication

### oauth2
![oauth2](https://camo.githubusercontent.com/07cb7243c5e9591b86cfc5475d6fad4e0a079926b4c32063bf810def50ba33f6/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a4d4b627257417a482d447630707274684c72537153512e706e67)

### sign up
![sign up](https://camo.githubusercontent.com/15c9751800708b30bd57faf6c7b0aeb002b6c04d598a1230c11d4bb0e6a6055a/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a5375664a696235573549685a6e70682d4668756d56412e706e67)
#### sign up with password
- sign up with password
- verify account (without password)
#### sign up without password
- sign up without password
- verify account (require to input password)
### password
![password](https://camo.githubusercontent.com/766423fa9a3261e77ddbd96a7b38bd5bb1a593f762b2d9f9c9975823192df17d/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a664a513468784559714d43566652706e31716c6370412e706e67)
- forgot password
- change password (also support change password 2 factors)
- reset password
