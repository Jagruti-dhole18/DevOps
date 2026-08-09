# DevOps Examples Repository

This repository contains sample DevOps and application deployment examples for local experimentation and learning.

## Repository Structure

- `docker/`
  - `app1-hello/`
    - `node/`: simple Node.js sample app with Docker configuration
    - `springboot/hello-spring/`: Spring Boot sample app with Maven wrapper and Dockerfile
- `jenkins/`
  - `simple-java-maven-app/`: Java Maven example with Jenkins pipeline and delivery scripts
- `kubernetes/`
  - `app2-tax-calculator/`
    - `spring/service-a/`: Spring Boot service A with Kubernetes manifest and Dockerfile
    - `spring/service-b/`: Spring Boot service B with Kubernetes manifest and Dockerfile
    - `tax-calculator-frontend/`: frontend app with Vite and Docker configuration
  - `demo/`: Kubernetes demo manifests
  - `hello-app/`: sample Kubernetes manifests for a simple app deployment

## Purpose

This repository is intended as a workspace for exploring Docker, Jenkins, and Kubernetes deployment examples. Use it to inspect sample configurations, run local builds, and adapt the examples to your own projects.

## Getting Started

1. Pick a sample project folder from `docker/`, `jenkins/`, or `kubernetes/`.
2. Read the project-specific `Dockerfile`, `pom.xml`, `Jenkinsfile`, or Kubernetes manifest.
3. Build and run locally with Docker, Kubernetes, or your CI tooling of choice.

## Notes

- These examples are for learning and experimentation, not production deployment.
- If you want to keep this repo clean, remove or replace any cloned content that is not relevant.
- Update this README with setup steps and goals for the specific examples you use.

## Example Workflows

- Build the Node.js sample:
  - `cd docker/app1-hello/node`
  - `docker build -t hello-node .`
  - `docker run --rm -p 3000:3000 hello-node`

- Build the Spring Boot sample:
  - `cd docker/app1-hello/springboot/hello-spring`
  - `./mvnw package`
  - `docker build -t hello-spring .`

- Inspect Kubernetes deployments in `kubernetes/` and use `kubectl apply -f <manifest>` to deploy locally.

## Maintainer Guidance

If you add new samples or tools, document them here so the next user can quickly understand the repo layout.
