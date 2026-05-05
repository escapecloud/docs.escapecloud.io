# Deployment Models

EscapeCloud Platform supports multiple deployment approaches depending on the target environment and operational requirements.

## Kubernetes (Helm)

Kubernetes deployment is intended for structured, production-oriented environments where platform workloads are managed within an existing cluster.

This approach is suitable when the target environment already provides core infrastructure services such as database, messaging, ingress, DNS, and certificate management.

Public repository:
[escapecloud_helm_charts](https://github.com/escapecloud/escapecloud_helm_charts)

## Docker Compose

Docker Compose provides a simpler deployment model for evaluation, local installation, or smaller-scale environments.

This approach can be used with external infrastructure services or with selected containerized dependencies included alongside the platform.

Public repository:
[escapecloud_docker_compose](https://github.com/escapecloud/escapecloud_docker_compose)

## Deployment Considerations

The appropriate deployment model depends on:

- target environment maturity
- infrastructure ownership model
- operational requirements
- external dependency strategy
- networking and certificate handling approach
