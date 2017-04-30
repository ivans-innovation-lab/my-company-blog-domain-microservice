# my-company-blog-domain-microservice

## Running instructions

Make sure that services are running:

 - my-company-configuration-backingservice
 - my-company-registry-backingservice
 
Make sure that you have this libraries in your local maven repsoitory:

 - [my-company-common](https://github.com/ivans-innovation-lab/my-company-common)
 - [my-company-blog-domain](https://github.com/ivans-innovation-lab/my-company-blog-domain)

```bash
$ cd my-company-blog-domain-microservice
$ ./mvnw spring-boot:run
```

Application will be available on port 8080 (http://localhost:8080)
