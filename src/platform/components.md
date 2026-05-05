# Components

EscapeCloud Platform consists of platform services deployed within customer-controlled infrastructure together with a small set of supporting infrastructure dependencies.

## Platform Services

### Web Application

The web application provides the primary user interface for interacting with EscapeCloud Platform.

### Assessment Engine

The assessment engine provides the platform’s processing and service execution layer, including background processing and internal platform operations.

## Infrastructure Dependencies

### Database

The platform requires a relational database for persistent storage. PostgreSQL is currently the supported database backend.

### Message Queue

The platform requires a messaging component for asynchronous communication and task coordination. RabbitMQ is currently the supported messaging backend.

### SMTP

SMTP is used for outbound email delivery and notification-related messaging. This is typically provided by the customer environment, although managed SMTP support can be arranged for specific deployment requirements.
