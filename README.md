# Spring Boot + GitHub Actions + Docker practice

This is a small learning demo, not a production deployment.

## Prerequisites
- JDK 17, Maven, Docker (Docker only needed for local image build)

## Run locally
```bash
mvn clean verify
mvn spring-boot:run
```
Open http://localhost:8080/api/hello

## Build and run container
```bash
mvn clean package
docker build -t springboot-actions-demo:local .
docker run --rm -p 8080:8080 springboot-actions-demo:local
```

## GitHub Actions
Push the files to a GitHub repository with a `main` branch. Go to **Actions** > **Spring Boot CI**. It runs tests, packages the JAR, and builds a Docker image on GitHub's runner. It does not push or deploy the image.

## Copyright

Copyright © 2026 Srimannarayana Reddi Tadi. All rights reserved.
