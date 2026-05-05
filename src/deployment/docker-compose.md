# Docker Compose

EscapeCloud Platform can be deployed with Docker Compose for evaluation, local installation, and simpler runtime environments.

This deployment approach provides a more compact setup model and can be used either with external infrastructure services or with selected containerized dependencies alongside the platform.

## Deployment Scope

The Docker Compose stack runs the main EscapeCloud Platform services required for application operation.

Depending on the deployment approach, supporting services may be provided either externally or through containerized dependencies included with the stack.

## Infrastructure Dependencies

The platform requires supporting infrastructure for persistent storage, messaging, and outbound email delivery.

Depending on the target environment, these may be:

- provided externally by the customer environment
- deployed alongside the platform where supported

## Prerequisites

Before deployment, the target host should provide:

- Docker Engine
- Docker Compose
- access to the EscapeCloud container registry
- reachable network ports for platform access
- DNS pointing to the host when public access is required

For HTTPS deployments, certificate material is also required.

## Configuration

Deployment is configured through a `.env` file derived from the provided environment template.

Typical configuration areas include:

- hostname
- image tags
- database connection settings
- message queue connection settings
- TLS certificate settings

## Installation Flow

1. Copy the provided environment template to a local `.env` file.
2. Configure platform, infrastructure, and certificate values as required.
3. Pull images if needed.
4. Start the platform with Docker Compose.
5. Validate application reachability and service startup.

## HTTP and HTTPS

Docker Compose deployments can be configured for either HTTP-only access or HTTPS access, depending on the provided certificate settings.

Where HTTPS is required, certificate files and related configuration must be available on the deployment host.

## Public Repository

[escapecloud_docker_compose](https://github.com/escapecloud/escapecloud_docker_compose)
