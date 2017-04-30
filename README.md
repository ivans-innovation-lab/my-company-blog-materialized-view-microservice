# my-company-blog-materialized-view-microservice

## Running instructions

Run RabbitMQ
```
$ brew services start rabbitmq
```

Make sure that services are running:

 - my-company-configuration-backingservice
 - my-company-registry-backingservice
 
Make sure that you have this libraries installed in your local maven repsoitory:

 - [my-company-common (transient dependency)](https://github.com/ivans-innovation-lab/my-company-common)
 - [my-company-blog-materialized-view](https://github.com/ivans-innovation-lab/my-company-blog-materialized-view)

```bash
$ cd my-company-blog-materialized-view-microservice
$ ./mvnw spring-boot:run
```

Application will be available on port 8081 (http://localhost:8081)

## Explore

### curl

```
$ curl http://localhost:8081/blogposts 
```

### rambittmq

Open RabbitMQ management web console at http://localhost:15672/ and explore exchanges, queues and messages.

### registry backing service

Open Registry (Eureka) web console at http://localhost:8761/ and find 'my-company-blog-materialized-view-microservice' registered.

