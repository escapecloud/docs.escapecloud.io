# Kubernetes (Helm)

EscapeCloud Platform can be deployed to Kubernetes using the provided Helm chart.

This deployment approach is intended for structured, production-oriented environments where platform workloads run inside an existing Kubernetes cluster and supporting infrastructure is managed separately.

## Deployment Scope

The Helm chart deploys the EscapeCloud Platform workloads and internal Kubernetes services required for application operation.

This includes:

- platform application workloads
- internal Kubernetes Service resources
- one-time bootstrap jobs
- scheduled CronJobs

## External Infrastructure

The Helm chart expects supporting infrastructure to be available outside of the chart itself.

This includes:

- database (PostgreSQL)
- message queue (RabbitMQ)
- container registry access
- DNS
- Gateway or Ingress
- TLS certificates and renewal

## Prerequisites

Before deployment, the target environment should provide:

- Kubernetes cluster access
- Helm
- a target namespace
- access to the EscapeCloud container registry
- a supported database backend
- a supported message queue backend

## Configuration

Deployment is configured through a `values.yaml` file.

Typical configuration areas include:

- hostname
- image tags
- image pull credentials
- database connection settings
- message queue connection settings
- application secrets

## Installation Flow

1. Prepare the target namespace and external infrastructure dependencies.
2. Copy the sample values file and create an environment-specific `values.yaml`.
3. Configure image tags, hostname, secrets, and infrastructure connection details.
4. Install or upgrade the chart with Helm.
5. Verify workload readiness, bootstrap jobs, and service availability.

## Networking

The Helm chart creates internal Kubernetes Services only.

External access is expected to be handled separately through the target Gateway or Ingress layer.

## Public Repository

[escapecloud_helm_charts](https://github.com/escapecloud/escapecloud_helm_charts)
