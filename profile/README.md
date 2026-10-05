<div align="center">

![Orbit](https://github.com/user-attachments/assets/a79b4cbc-4643-4a32-a17f-c47181b25642)

# Orbit

### Building an enterprise-grade, cloud native web framework.

A Python framework and modular package ecosystem for building, deploying, and operating modern web applications.

</div>

---

## About

Orbit is an open source web framework project. Its goal is to provide a stable foundation for application teams—from startups to enterprises—with the architecture, integrations, and developer tools needed to build cloud native web applications.

The framework has a Python core and a modular ecosystem of separately installable packages. Core owns application orchestration, lifecycle, dependency injection, configuration, state, events, health, ASGI and routing, CLI, and stable extension contracts. Database, authentication, storage, messaging, observability, and provider integrations live in their respective packages.

Orbit is designed for containerized and distributed environments while remaining practical to develop and run locally. Teams can adopt capabilities as needed without making every infrastructure choice a requirement of the core framework.

## Philosophy

Orbit aims to be:

- Learnable and productive for application developers
- Modular, with clear boundaries between Core and optional packages
- Extensible through stable, documented contracts
- Secure by default, with explicit operational behavior
- Cloud native and portable across deployment environments
- Open source, with package level documentation and contribution practices
- Sustainable to maintain as the framework and ecosystem grow

The goal is a cohesive framework, not a collection of unrelated integrations. Packages should work well together while remaining independently useful.

## Architecture

Orbit separates the web framework runtime, capability contracts, and provider implementations:

Web application
└── orbit-core
    ├── capability package
    │   └── provider integration
    └── optional language-specific implementation

- **`orbit-core`** provides the Python application runtime and stable extension contracts.
- **Capability packages** define focused interfaces, such as data access, storage, messaging, or security.
- **Provider integrations** implement those interfaces and own vendor SDKs, credentials, transport, and provider-specific behavior.
- **Language-specific implementations** are separate packages when another language suits the workload. Cross-language boundaries are defined by the relevant package contract; gRPC and Protobuf are used where a typed service boundary is appropriate.

For example, object storage uses a shared capability with provider-specific integrations:

orbit-storage
├── orbit-s3
├── orbit-gcs
└── orbit-azure-storage

Applications can use the storage contract without tying application code to one provider.

## Ecosystem

### Core and application development

| Repository | Purpose |
|---|---|
| [orbit-core](<https://github.com/orbit-projects/orbit-core>) | Python web application runtime and stable extension contracts |
| [orbit-admin](<https://github.com/orbit-projects/orbit-admin>) | Administrative application capabilities |
| [orbit-gateway](<https://github.com/orbit-projects/orbit-gateway>) | API gateway utilities |
| [orbit-graphql](<https://github.com/orbit-projects/orbit-graphql>) | GraphQL support |
| [orbit-realtime](<https://github.com/orbit-projects/orbit-realtime>) | WebSockets and server-sent events |
| [orbit-devtools](<https://github.com/orbit-projects/orbit-devtools>) | Development tooling |
| [orbit-testing](<https://github.com/orbit-projects/orbit-testing>) | Testing utilities |

### Data and storage

| Repository | Purpose |
|---|---|
| [orbit-data](<https://github.com/orbit-projects/orbit-data>) | Shared data access contracts |
| [orbit-sql](<https://github.com/orbit-projects/orbit-sql>) | SQL capability |
| [orbit-nosql](<https://github.com/orbit-projects/orbit-nosql>) | NoSQL capability |
| [orbit-sql-sqlite](<https://github.com/orbit-projects/orbit-sql-sqlite>) | SQLite integration |
| [orbit-sql-postgres](<https://github.com/orbit-projects/orbit-sql-postgres>) | PostgreSQL integration |
| [orbit-sql-mysql](<https://github.com/orbit-projects/orbit-sql-mysql>) | MySQL integration |
| [orbit-mongo](<https://github.com/orbit-projects/orbit-mongo>) | MongoDB integration |
| [orbit-redis](<https://github.com/orbit-projects/orbit-redis>) | Redis integration |
| [orbit-vector](<https://github.com/orbit-projects/orbit-vector>) | Vector database capability |
| [orbit-migrations](<https://github.com/orbit-projects/orbit-migrations>) | Database migrations |
| [orbit-storage](<https://github.com/orbit-projects/orbit-storage>) | Object storage capability |
| [orbit-s3](<https://github.com/orbit-projects/orbit-s3>) | S3-compatible object storage |
| [orbit-gcs](<https://github.com/orbit-projects/orbit-gcs>) | Google Cloud Storage |
| [orbit-azure-storage](<https://github.com/orbit-projects/orbit-azure-storage>) | Azure Blob Storage |

### Messaging and background work

| Repository | Purpose |
|---|---|
| [orbit-events](<https://github.com/orbit-projects/orbit-events>) | Event-driven application contracts |
| [orbit-kafka](<https://github.com/orbit-projects/orbit-kafka>) | Apache Kafka integration |
| [orbit-rabbitmq](<https://github.com/orbit-projects/orbit-rabbitmq>) | RabbitMQ integration |
| [orbit-nats](<https://github.com/orbit-projects/orbit-nats>) | NATS integration |
| [orbit-streams](<https://github.com/orbit-projects/orbit-streams>) | Stream processing |
| [orbit-streams-rust](<https://github.com/orbit-projects/orbit-streams-rust>) | Rust stream-processing implementation |
| [orbit-workers](<https://github.com/orbit-projects/orbit-workers>) | Background workers |
| [orbit-scheduler](<https://github.com/orbit-projects/orbit-scheduler>) | Scheduled jobs |

### Security

| Repository | Purpose |
|---|---|
| [orbit-security](<https://github.com/orbit-projects/orbit-security>) | Authentication and authorization capabilities |
| [orbit-oauth2](<https://github.com/orbit-projects/orbit-oauth2>) | OAuth2 and OpenID Connect |
| [orbit-jwt](<https://github.com/orbit-projects/orbit-jwt>) | JWT authentication |
| [orbit-rbac](<https://github.com/orbit-projects/orbit-rbac>) | Role-based access control |

### Observability and operations

| Repository | Purpose |
|---|---|
| [orbit-observability](<https://github.com/orbit-projects/orbit-observability>) | Shared observability capabilities |
| [orbit-logging](<https://github.com/orbit-projects/orbit-logging>) | Structured logging |
| [orbit-metrics](<https://github.com/orbit-projects/orbit-metrics>) | Metrics collection |
| [orbit-prometheus](<https://github.com/orbit-projects/orbit-prometheus>) | Prometheus integration |
| [orbit-tracing](<https://github.com/orbit-projects/orbit-tracing>) | Distributed tracing |
| [orbit-cache](<https://github.com/orbit-projects/orbit-cache>) | Caching |
| [orbit-lock](<https://github.com/orbit-projects/orbit-lock>) | Distributed locking |
| [orbit-resilience](<https://github.com/orbit-projects/orbit-resilience>) | Retry, circuit breaker, and rate limiting |

Health checks and application readiness are part of the Core runtime.

### Cloud native integrations and services

| Repository | Purpose |
|---|---|
| [orbit-cloud](<https://github.com/orbit-projects/orbit-cloud>) | Cloud control-plane capability contracts |
| [orbit-kubernetes](<https://github.com/orbit-projects/orbit-kubernetes>) | Kubernetes integration |
| [orbit-kubernetes-go](<https://github.com/orbit-projects/orbit-kubernetes-go>) | Go Kubernetes implementation |
| [orbit-discovery](<https://github.com/orbit-projects/orbit-discovery>) | Service discovery capability |
| [orbit-discovery-go](<https://github.com/orbit-projects/orbit-discovery-go>) | Go service discovery implementation |
| [orbit-config-server](<https://github.com/orbit-projects/orbit-config-server>) | Centralized configuration |
| [orbit-search](<https://github.com/orbit-projects/orbit-search>) | Search capability |
| [orbit-search-elasticsearch](<https://github.com/orbit-projects/orbit-search-elasticsearch>) | Elasticsearch integration |
| [orbit-search-opensearch](<https://github.com/orbit-projects/orbit-search-opensearch>) | OpenSearch integration |
| [orbit-email](<https://github.com/orbit-projects/orbit-email>) | Email integration |
| [orbit-notifications](<https://github.com/orbit-projects/orbit-notifications>) | Email, SMS, and push notification capabilities |

Planned cloud control-plane adapters include `orbit-aws`, `orbit-gcp`, and `orbit-azure`. They will implement `orbit-cloud` and remain separate from service-specific integrations such as `orbit-s3`, `orbit-gcs`, and `orbit-azure-storage`.

## Cloud native applications

Orbit is intended for applications that run across local development, containers, and cloud native infrastructure.

- Develop and run applications locally without requiring a cluster.
- Package services as containers and use Kubernetes integrations when needed.
- Keep provider SDKs and credentials inside provider integrations.
- Compose only the capabilities an application uses.
- Preserve provider-specific options when a common abstraction would hide meaningful differences.

## Production direction

Orbit’s goal is to become an enterprise-grade framework. That requires more than a broad package catalog: each capability must have clear contracts, safe defaults, tested lifecycle and failure behavior, useful documentation, and a dependable release process.

The ecosystem is actively developing toward that goal. Readiness varies by repository and release; a repository’s presence does not imply feature completeness, production certification, or support for every deployment. Check each project’s README, release notes, compatibility information, and security policy before adopting it.

## Open source and contributing

Orbit is built in the open. Contributions, bug reports, documentation improvements, and focused design discussions are welcome.

Start with the contributing guide and code of conduct in the repository you want to work on. Each repository owns its documentation, support boundaries, and release history.

- Browse the [Orbit repositories](<https://github.com/orgs/orbit-projects/repositories>).
- Read the [Core architecture documentation](<https://github.com/orbit-projects/orbit-core/tree/main/docs/architecture>).
- Report issues in the repository responsible for the behavior.

***

Orbit is developed as part of the [Undreamt](<https://github.com/undreamt-hq>) ecosystem, focused on open source infrastructure, developer tooling, and software designed for long-term growth.

