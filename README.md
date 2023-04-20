
# Hypercrawler Project

Web crawling refers to a program that searches the internet for web pages. The goal
of web crawling is to analyze and persist the examined web pages. 


## Description
This project work should address the mentioned problem. Therefore, it is important
that the problem has been understood and feeds directly into all elements of the software development process.
The objective of the project work is to develop a scalable and high-performance architecture for a web crawler, which enables efficient processing of large data volumes.

The overall architecture should be based on microservices to ensure easy horizontal
and vertical scalability of the system. A resulting architecture concept should be implemented after completion.
The implementation is to be realised using modules of the Spring framework, which
already provide extensive mechanisms as a basis for achieving the goal of a stable and
scalable application

## Status

### config-service

[![Commit Stage](https://github.com/avollmaier/hypercrawler-config-service/actions/workflows/commit-stage.yml/badge.svg)](https://github.com/avollmaier/hypercrawler-config-service/actions/workflows/commit-stage.yml)

### edge-service

[![Commit Stage](https://github.com/avollmaier/hypercrawler-edge-service/actions/workflows/commit-stage.yml/badge.svg)](https://github.com/avollmaier/hypercrawler-edge-service/actions/workflows/commit-stage.yml)

### manager-service

[![Commit Stage](https://github.com/avollmaier/hypercrawler-manager-service/actions/workflows/commit-stage.yml/badge.svg)](https://github.com/avollmaier/hypercrawler-manager-service/actions/workflows/commit-stage.yml)

### discovery-service

[![Commit Stage](https://github.com/avollmaier/hypercrawler-discovery-service/actions/workflows/commit-stage.yml/badge.svg)](https://github.com/avollmaier/hypercrawler-discovery-service/actions/workflows/commit-stage.yml)

## Prerequisites

Chapter after chapter, you'll build, containerize, and deploy cloud native applications. Along the journey, you will
need the following software installed.

* Java 17+
  * OpenJDK: [Eclipse Temurin](https://adoptium.net)
  * GraalVM: [GraalVM](https://www.graalvm.org)
    * JDK Management: [SDKMAN](https://sdkman.io)
* Docker 20.10+
  * [Docker for Linux](https://docs.docker.com/engine/install/ubuntu/)
  * [Docker Desktop for Mac](https://www.docker.com/products/docker-desktop)
  * [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop)
* Kubernetes 1.27+
    * [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
    * [minikube](https://minikube.sigs.k8s.io/docs/)
* Other
    * [HTTPie](https://httpie.org/)

## Run Locally

Clone the project

```bash
  git clone --recursive https://github.com/avollmaier/hypercrawler.git
```

Go to the project directory

```bash
  cd hypercrawler
```

Create a minikube kubernetes cluster (check out the hypercrawler-deployment project)

```bash
  cd hypercrawler-deployment/kubernetes/platform/

  ./create-cluster.sh 
```

Start the tilt server for fast local deployment

```bash
  cd ../development

  tilt up
```