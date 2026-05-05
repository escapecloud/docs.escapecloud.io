# Security Overview

EscapeCloud Platform is designed to run within customer-controlled infrastructure.

For self-hosted deployments, the platform operates inside environment boundaries defined by the customer, with supporting infrastructure and external access managed according to the target deployment architecture.

## Deployment Boundary

EscapeCloud Platform is deployed within customer-managed infrastructure using either Kubernetes or Docker Compose, depending on the selected deployment approach.

This model allows the customer to define network boundaries, runtime isolation, access controls, and supporting infrastructure according to internal security and operational requirements.

## Infrastructure Separation

The platform services operate together with a small set of supporting infrastructure dependencies, including database, messaging, and outbound email delivery.

These dependencies can be integrated into the customer environment in a way that aligns with existing infrastructure, operational controls, and security policies.

## Operational Control

In self-hosted deployments, the customer retains control over:

- infrastructure boundaries
- network exposure
- access management
- certificate handling
- supporting infrastructure services

## Public Documentation Scope

This page provides a high-level overview of the platform security boundary only.

Detailed hardening guidance, implementation-specific controls, and deployment-specific security configuration are handled separately during onboarding and evaluation.
