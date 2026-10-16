<div align="center">

![Orbit](https://github.com/user-attachments/assets/a79b4cbc-4643-4a32-a17f-c47181b25642)

# Orbit

### An open-source framework ecosystem for cloud-native web applications

Orbit is being built toward an enterprise-grade Python web framework, with modular capabilities and optional integrations for the systems applications depend on.

</div>

---

## About

Orbit brings together an application runtime, developer tools, capability packages, and provider integrations. The goal is to help teams build web applications that work well in local development and can be operated across containerized and cloud-native environments.

The ecosystem is modular. Applications install the capabilities they need, while provider-specific packages own their vendor SDKs, credentials, and transport details. This keeps infrastructure choices out of application code where a stable shared contract is useful, while still allowing providers to expose meaningful differences.

Orbit is in active development. Its goal is enterprise-grade operation; the current package maturity and release status vary. Check each repository's documentation and release information before relying on a capability in production.

## Architecture

Orbit separates the application runtime, capability contracts, and provider implementations:

```text
Application
└── orbit-core
    ├── capability package
    │   └── provider integration
    └── optional language-specific implementation
```

- **`orbit-core`** provides the Python application runtime: orchestration, lifecycle, dependency injection, configuration, state, events, health, ASGI and routing, and stable extension contracts.
- **`orbit-cli`** provides an interactive control interface for common development and operations workflows, with conventional commands for automation and fallback use.
- **Capability packages** define focused user-facing contracts, such as data access, authentication, storage, messaging, or observability.
- **Provider integrations** implement those contracts and own provider configuration, credentials, SDKs, transport, and provider-specific errors.
- **Language-specific implementations** are optional packages for workloads where another language is a suitable fit. Packages use a defined service boundary, such as gRPC and Protobuf, when cross-process communication is appropriate.

For example, applications can use the object-storage capability while selecting a provider adapter:

```text
orbit-storage
├── orbit-storage-s3
├── orbit-storage-gcs
└── orbit-storage-azure
```

## Ecosystem

Orbit packages are maintained as separate repositories. These are examples of the current package families; use the [organization repository list](https://github.com/orgs/orbit-projects/repositories) for the up-to-date inventory.

| Area | Capability and integration examples |
|---|---|
| Application foundation | `orbit-core`, `orbit-cli`, `orbit-admin`, `orbit-gateway`, `orbit-graphql` |
| Data | `orbit-data`, `orbit-sql`, `orbit-nosql`, `orbit-migrations`, `orbit-cache`, `orbit-vector` |
| SQL providers | `orbit-sql-sqlite`, `orbit-sql-postgres`, `orbit-sql-mysql` |
| NoSQL and cache providers | `orbit-nosql-mongo`, `orbit-cache-redis` |
| Object storage | `orbit-storage`, `orbit-storage-s3`, `orbit-storage-gcs`, `orbit-storage-azure` |
| Identity and security | `orbit-auth`, `orbit-auth-jwt`, `orbit-auth-oauth2`, `orbit-auth-rbac`, `orbit-security`, `orbit-secrets` |
| Messaging and work | `orbit-events`, `orbit-events-kafka`, `orbit-events-rabbitmq`, `orbit-events-nats`, `orbit-workers`, `orbit-scheduler`, `orbit-streams`, `orbit-saga` |
| Observability | `orbit-observability`, `orbit-logging`, `orbit-metrics`, `orbit-tracing`, `orbit-metrics-prometheus`, `orbit-metrics-grafana` |
| Cloud and operations | `orbit-cloud`, `orbit-cloud-aws`, `orbit-cloud-gcp`, `orbit-cloud-azure`, `orbit-discovery`, `orbit-kubernetes`, `orbit-config-server`, `orbit-resilience` |
| Realtime and transport | `orbit-sockets`, `orbit-realtime`, `orbit-webrtc`, with selected Go and Rust implementations |
| External services | `orbit-search` and provider adapters, `orbit-email`, `orbit-notifications`, `orbit-payments` and payment-provider adapters |
| Developer experience | `orbit-testing`, `orbit-devtools` |

Package availability, supported providers, and maturity vary. A package name in this catalog does not imply a published release, complete feature set, or verified production compatibility.

## Cloud-native direction

Orbit is designed to support applications running from a developer's machine through containers and cloud-native infrastructure. The ecosystem is working toward:

- Explicit startup, shutdown, resource cleanup, timeout, and failure behavior.
- Portable capability contracts with provider-specific behavior kept visible where it matters.
- Optional integrations for databases, brokers, object storage, identity, and cloud platforms.
- Clear security boundaries for credentials, authentication, authorization, and secret handling.
- Operational visibility through logs, metrics, traces, health checks, and resilience tools.
- Optional Go and Rust implementations where a package has a well-defined workload and a useful conformance boundary.

Cloud-native does not mean requiring a cluster for local development. Applications should be able to adopt infrastructure integrations when their deployment needs call for them.

## Development status

Orbit is an early-stage open-source project working toward a `v0.1.0-alpha` milestone. Interfaces and implementations may change as the ecosystem is reviewed and validated. Local checks, hosted CI, live-provider compatibility, publication, provenance, and deployment are separate forms of evidence; check the relevant repository for current results.

## Open source and contributing

Orbit is developed in the open. Contributions can improve code, tests, documentation, examples, accessibility, security, and developer experience.

Before contributing, read the contributing guide, security policy, and development instructions in the repository you plan to work on. Keep changes focused, include tests for behavior changes, and document operational constraints. Report issues in the repository responsible for the capability or integration.

- Browse [Orbit repositories](https://github.com/orgs/orbit-projects/repositories).
- Read the [Core architecture documentation](https://github.com/orbit-projects/orbit-core/tree/main/docs/architecture).
- Review the [organization contribution guidance](https://github.com/orbit-projects/.github).

---

Orbit is developed as part of the [Undreamt](https://github.com/undreamt-hq) open-source community.
