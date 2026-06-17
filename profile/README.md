<div align="center">

![Orbit](https://github.com/user-attachments/assets/a79b4cbc-4643-4a32-a17f-c47181b25642)

# Orbit

### Enterprise-grade application platform built on FastAPI.

Building modern Python applications through a unified architecture, official batteries, and developer-first tooling.

</div>

---

# About

Orbit is an open-source ecosystem for building scalable Python applications.

Rather than acting as a thin wrapper around existing frameworks, Orbit provides a structured platform that combines architecture, tooling, batteries, and conventions into a cohesive developer experience.

Orbit is built around a carefully chosen stack:

* FastAPI
* Starlette
* Pydantic
* Vue
* Nuxt
* PrimeVue
* Oruga
* Point

The goal is simple:

> Provide a stable foundation for startups while offering the architecture and tooling required by enterprise teams.

---

# Philosophy

We believe application platforms should be:

* Learnable
* Modular
* Extensible
* Type-safe
* Developer-first
* Built for the long term

Orbit emphasizes:

* Clean architecture
* Strong foundations
* Convention over configuration
* Batteries included
* Excellent developer experience
* Long-term maintainability

Rather than supporting every possible technology stack, Orbit focuses on providing one well-integrated ecosystem.

---

# Ecosystem

## Core

The Orbit foundation.

| Package      | Purpose                                                     |
| ------------ | ----------------------------------------------------------- |
| orbit-core   | Application architecture, modules, lifecycle, configuration |
| orbit-server | FastAPI runtime integration                                 |
| orbit-types  | Shared contracts and type definitions                       |
| orbit-cli    | Scaffolding and developer tooling                           |
| orbit-kit    | Meta package and ecosystem distribution                     |

---

## Batteries

Official packages maintained as part of the Orbit platform.

| Package             | Purpose                          |
| ------------------- | -------------------------------- |
| orbit-auth          | Authentication and authorization |
| orbit-db            | Database integration             |
| orbit-admin         | Administrative dashboard         |
| orbit-cache         | Caching and Redis integration    |
| orbit-storage       | File and object storage          |
| orbit-mail          | Email delivery and notifications |
| orbit-queue         | Background jobs and scheduling   |
| orbit-observability | Logging, metrics, and tracing    |

---

## Performance Extensions

Optional acceleration layers.

| Package     | Purpose                                    |
| ----------- | ------------------------------------------ |
| orbit-robyn | High-performance integrations and services |

Performance extensions enhance Orbit but are never required for applications to function.

---

# Frontend Ecosystem

Orbit officially supports a Vue-centric frontend stack.

## Applications

* Vue
* Nuxt

## UI

* PrimeVue
* Oruga

## Documentation

* Point
* VitePress

This allows Orbit applications, documentation, and administrative tooling to share a consistent ecosystem.

---

# Architecture

Orbit follows a layered architecture.

```text
Orbit

Core
├── orbit-core
├── orbit-server
├── orbit-types
├── orbit-cli
└── orbit-kit

Batteries
├── orbit-auth
├── orbit-db
├── orbit-admin
├── orbit-cache
├── orbit-storage
├── orbit-mail
├── orbit-queue
└── orbit-observability

Performance
└── orbit-robyn
```

Applications are composed of modules rather than large collections of unrelated folders.

```text
modules/

├── users/
├── auth/
├── billing/
└── inventory/
```

Each module owns its routes, services, schemas, repositories, tests, and configuration.

---

# Vision

Orbit is being built as a long-term platform for application development.

Current focus areas include:

* Application architecture
* Developer tooling
* Authentication
* Database integration
* Administrative tooling
* Background processing
* Observability
* Performance extensions

Future capabilities will continue to build upon the same core principles of modularity, maintainability, and developer experience.

---

# Status

Orbit is currently under active development.

The ecosystem architecture has been established and the platform is evolving toward its first generation of official batteries.

APIs and implementations may evolve as the ecosystem matures.

We build in public, iterate continuously, and share what we learn along the way.

---

# Contributing

Orbit welcomes contributions from developers, students, researchers, and builders.

Ways to contribute:

* Improve architecture
* Report issues
* Improve documentation
* Help testing
* Suggest ideas
* Contribute tooling and integrations

You do not need to be an expert to contribute.

Curiosity, experimentation, and a willingness to learn are enough.

---

# ![Undreamt](https://github.com/undreamt-hq)

Orbit is developed as part of the Undreamt ecosystem.

Focused on building open-source infrastructure, developer tooling, educational platforms, and software systems designed for long-term growth.
