# [projects](http://ivans-innovation-lab.github.io/projects)/my-company-blog-domain-microservice [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-domain-microservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-domain-microservice)

## Running instructions

Run RabbitMQ
```
$ brew services start rabbitmq
```

Make sure that services are running:

 - [my-company-configuration-backingservice](https://github.com/ivans-innovation-lab/my-company-configuration-backingservice)
 - [my-company-registry-backingservice](https://github.com/ivans-innovation-lab/my-company-registry-backingservice)
 
Make sure that you have this libraries installed in your local maven repository:

 - [my-company-common (transient dependency)](https://github.com/ivans-innovation-lab/my-company-common)
 - [my-company-blog-domain](https://github.com/ivans-innovation-lab/my-company-blog-domain)

```bash
$ cd my-company-blog-domain-microservice
$ ./mvnw spring-boot:run
```

Application will be available on port 8080 (http://localhost:8080)

## Explore

### curl

```
$ curl -H "Content-Type: application/json" -X POST -d '{"title":"xyz","rawContent":"xyz","publicSlug": "publicslug","draft": true,"broadcast": true,"category": "ENGINEERING", "publishAt": "2026-12-23T14:30:00+00:00"}' http://127.0.0.1:8080/blogpostcommands 
```

### rambittmq

Open RabbitMQ management web console at http://localhost:15672/ and explore exchanges, queues and messages.

### registry backing service

Open Registry (Eureka) web console at http://localhost:8761/ and find 'my-company-blog-domain-microservice' registered.

