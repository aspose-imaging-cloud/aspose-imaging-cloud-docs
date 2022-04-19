---
title: "How to Run Docker Container"
second_title: "Aspose Imaging Cloud Docs"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "How to run Docker container"
weight: 100
---

The **Docker** technology is designed to automate the deployment of the applications by using lightweight containers. Developers can use a **Docker Container** to wrap up an application with all of its libraries and dependencies and deploy everything as a single package.

Aspose.Imaging Cloud team has published the Docker Container on [Docker Hub](https://hub.docker.com/r/aspose/imaging-cloud) to facilitate the Docker users. The following sections will guide you that how to run a Docker commands or write configuration in a Yaml file for Docker compose tool.

## Container configuration

### Required volumes

|Mount path in container|Description|
| :- | :- |
|/data|File storage folder|

### Parameters

|Name|Description|
| :- | :- |
|LicensePublicKey|Public key of the license|
|LicensePrivateKey|Private key of the license|



### Run a Docker container using command line

You can simply run the following docker command after pulling the container from [Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/imaging-cloud).

```JAVA
docker run  -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v "/fonts:/fonts" -v "/data:/data" aspose/imaging-cloud
```

### Configurations for Docker-Compose Tool

You can write the following configurations in your yaml file for Docker-Compose tool:

```JAVA
AsposeImagingCloud:
      image: aspose/imaging-cloud
      ports: ["8082:80"]
      volumes: [
        "./storage:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```
