# overview
- GO libraries to develop micro services

## Databases
- SQL
- Mongo
- Casandra
- Dynamodb
- Firestore
- Elasticsearch

## Minimize effort for cross-cutting concerns
### Security
- Identity and Access Management: Authorization at middleware, support http ([mux](https://github.com/gorilla/mux), [chi](https://github.com/go-chi/chi)), [gin](https://github.com/gin-gonic/gin), [echo](https://github.com/labstack/echo)
- Crypto
- JWT

### Validator
Check required, email, url, min, max, country code, phone number, regular expression... 

### Logging
Standardize API for logging, support 2 libraries:
- [logrus](https://github.com/sirupsen/logrus)
- [zap](go.uber.org/zap)

### Request Tracing
- [middleware](https://github.com/core-go/middleware): Log request and response at http middleware, allow to configure dynamic field names
- [client](https://github.com/core-go/client): Log request and response at http client, allow to configure dynamic field names

### Caching
#### Memory Cache
- Time To Live: automatically clean up the expired objects in the memory cache
- Maximum size: When the memory exceeds the max size (which is configurable), it automatically remove the oldest object.
#### Redis
Support 2 libraries
- [go-redis](https://github.com/go-redis/redis)
- [redigo](https://github.com/garyburd/redigo)

### Audit Log
Support for CRUD, search (not required in every application)

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

## Communication
### Email
Build some standard interfaces, which can be shared by multiple providers: SMTP and Sendgrid
### Message Queue
#### Support these providers
- Amazon Simple Queue Service (SQS) at [sqs](https://github.com/core-go/mq/tree/main/sqs)
- Google Cloud Pub/Sub at [pubsub](https://github.com/core-go/mq/tree/main/pubsub)
- Kafka: at [segmentio/kafka-go](https://github.com/core-go/mq/tree/main/kafka), [Shopify/sarama](https://github.com/core-go/mq/tree/main/sarama) and [confluent](https://github.com/confluentinc/confluent-kafka-go)
- NATS at [nats](https://github.com/core-go/mq/tree/main/nats)
- Active MQ at [amq](https://github.com/core-go/mq/tree/main/amq)
- RabbitMQ at [rabbitmq](https://github.com/core-go/mq/tree/main/rabbitmq)
- IBM MQ at [ibm-mq](https://github.com/core-go/mq/tree/main/ibm-mq)

#### Support 2 reusable business flows
- Consume message and handle one by one
- Consume message and handle by batch

## Reusable business components
### authentication
- authenticator
- ldap authenticator
- 2 factor authentication
#### database for authentication
- sql (PosgreSQL, Oracle, MySQL, SQL Server, Sqlite)
- mongo
- casandra
- dynamodb
- firestore
- elasticsearch (as showcase)
### oauth2
- google
- facebook
- linked in
- twitter
- microsoft
- dropbox
- amazon
#### database
This library especially supports repository for these databases: 
- sql (PosgreSQL, Oracle, MySQL, SQL Server, Sqlite)
- mongo
- casandra
- dynamodb
- firestore
### sign up
Support to sign up with 2 rules: sign up with password, or sign up without password
#### sign up with password:
- sign up with password
- verify account (without password)
#### sign up without password:
- sign up without password
- verify account (require to input password)
### password
- forgot password
- change password (also support change password 2 factors)
- reset password
#### database
This library especially supports repository for these databases: 
- sql (PosgreSQL, Oracle, MySQL, SQL Server, Sqlite)
- mongo
- casandra
- dynamodb
- firestore
