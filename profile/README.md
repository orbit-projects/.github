<div align="center">

<img width="512" height="405" alt="Orbit" src="https://github.com/user-attachments/assets/f1675799-33a8-49ff-b9e0-1c2c32241ad4" />


# Orbit

### A modular Python framework and tooling ecosystem focused on modern developer infrastructure, fullstack orchestration, and experimental architecture.

Open-source project under [Undreamt](https://github.com/undreamt-hq) focused on building developer-first tooling and framework utilities in Python.

</div>

---

## About

Orbit is a modular fullstack framework ecosystem designed for:

- Data-driven applications
- APIs and services
- Backend platforms
- Fullstack orchestration
- Developer tooling
- Experimental infrastructure

The ecosystem is built around a simple idea:

> Frameworks should be modular, understandable, type-safe, and easy to extend — without becoming bloated or overly abstract.

Orbit focuses on orchestration and architecture rather than reinventing every layer of the stack.

---

# Vision

Orbit aims to explore modern framework architecture while keeping the ecosystem lightweight, learnable, and flexible.

Instead of building a single monolithic framework, Orbit focuses on creating independent modules that work well together while remaining usable on their own.

The long-term goal is to create a composable fullstack platform for services and data-driven systems with:

- Modular architecture
- Typed contracts
- Backend/frontend orchestration
- Scalable runtime systems
- Service-oriented workflows

---

# Ecosystem Modules

Current Orbit ecosystem:

| Module | Purpose |
|---|---|
| `orbit-core` | Core framework primitives |
| `orbit-server` | Backend/runtime integrations |
| `orbit-cli` | CLI tooling and project generation |
| `orbit-types` | Typing and shared type utilities |
| `orbit-kit` | Meta-package bundling Orbit ecosystem |

---

# High-Level Architecture

```text
                ┌─────────────────┐
                │   orbit-cli     │
                │ scaffolding/DX  │
                └────────┬────────┘
                         │
                         ▼
              orbit new app
                         │
         ┌───────────────┴────────────────┐
         ▼                                ▼
┌─────────────────┐             ┌─────────────────┐
│     backend     │             │    frontend     │
│ FastAPI/Robyn   │             │ Vue/Nuxt/etc    │
└────────┬────────┘             └────────┬────────┘
         │                               │
         ▼                               ▼
 ┌──────────────┐               ┌────────────────┐
 │ orbit-server │               │ frontend stack │
 │ runtime layer│               │ vite/nuxt/etc  │
 └──────────────┘               └────────────────┘
         │
         ▼
 ┌──────────────┐
 │ orbit-core   │
 │ framework    │
 │ primitives   │
 └──────────────┘
         │
         ▼
 ┌──────────────┐
 │ orbit-types  │
 │ shared types │
 └──────────────┘
```

---

# Philosophy

Orbit is being built with strong focus on:

- Modular design
- Clean architecture
- Strong typing
- Developer experience
- Learnable internals
- Extensibility
- Public experimentation
- Real-world implementation

Orbit intentionally delegates specialized problems to specialized ecosystems instead of replacing everything internally.

Current ecosystem integrations include:

- FastAPI
- Robyn
- Vue
- Nuxt
- Vite
- Quasar

---

# Current Generated Application Structure

```text
app/
├── backend/
│   ├── api/
│   │   ├── routes/
│   │   ├── controllers/
│   │   └── services/
│   │
│   ├── core/
│   ├── models/
│   ├── main.py
│   └── requirements.txt
│
├── frontend/
│   ├── app/
│   ├── package.json
│   ├── vite.config.ts
│   └── ...
│
├── env/
├── orbit.config.py
└── README.md
```

---

# Backend Architecture

Orbit currently structures backend applications into layered components.

## Routes

Responsible for:

- Endpoint definitions
- HTTP mapping
- Request entrypoints

```python
@app.get("/users")
```

---

## Controllers

Responsible for:

- Request handling
- Orchestration
- Calling services

---

## Services

Responsible for:

- Business logic
- Data processing
- Reusable backend logic

---

## Models

Responsible for:

- Data structures
- Schemas
- ORM entities later

---

## Core

Responsible for:

- Config
- Responses
- Shared backend utilities

---

# Supported Backends

| Backend | Purpose |
|---|---|
| FastAPI | Typed APIs/services |
| Robyn | Lightweight high-performance services |

---

# Frontend Ecosystem

Orbit currently supports integration with:

| Frontend | Language Options |
|---|---|
| Vue | JS / TS |
| Nuxt | JS / TS |
| Quasar | JS / TS |

Orbit delegates frontend runtime responsibilities to existing frontend ecosystems instead of reinventing frontend rendering internally.

---

# Runtime Commands

## Backend Only

```bash
orbit start
```

Starts:
- FastAPI server
- or Robyn runtime

---

## Frontend Only

```bash
orbit dev
```

Starts:
- Vite/Nuxt frontend development server

---

## Fullstack Development

```bash
orbit runserver
```

Starts:
- Backend server
- Frontend development server

simultaneously.

---

## Production Build

```bash
orbit build
```

Runs frontend production builds.

---

## Production Preview

```bash
orbit serve
```

Runs frontend preview/runtime commands.

---

# CLI Architecture

Orbit CLI is built using:

- Typer

Current commands:

```bash
orbit new
orbit start
orbit dev
orbit runserver
orbit build
orbit serve
```

---

# Project Generation Flow

```bash
orbit new app
```

Current generation flow:

1. Select backend
2. Select frontend
3. Select JS/TS
4. Create project structure
5. Create environment
6. Install dependencies
7. Generate templates

---

# Environment System

Orbit creates isolated Python environments using:

```bash
python -m venv env
```

Used for:

- Backend dependencies
- Orbit packages
- Isolated development

---

# Orbit Config System

Example config:

```python
CONFIG = {
    "backend": {
        "framework": "fastapi",
        "entry": "main:app"
    },

    "frontend": "vue"
}
```

Acts as:

- Runtime contract
- Framework metadata
- Orchestration configuration

---

# Package Distribution

Orbit modules are published individually to PyPI:

- `orbit-framework-core`
- `orbit-framework-server`
- `orbit-framework-cli`
- `orbit-framework-types`
- `orbit-framework-kit`

---

# Installation

## Meta Package

```bash
pip install orbit-framework-kit
```

---

# Internal Relationships

```text
orbit-kit
    ├── orbit-core
    ├── orbit-server
    ├── orbit-cli
    └── orbit-types
```

---

# Current Architectural Focus

Orbit is currently optimized for:

- APIs
- Services
- Data-driven applications
- SaaS-like systems
- Backend platforms
- Fullstack orchestration

Orbit is not primarily focused on:

- Traditional MVC websites
- CMS-style platforms
- Monolithic rendering systems

---

# Current Development Phase

Orbit is currently in an early framework platform phase.

Current status:

- Foundations exist
- Runtime works
- Architecture direction established
- Ecosystem operational

Still evolving:

- Abstractions
- Service layer
- Middleware systems
- Plugin architecture
- Data layer
- Runtime systems

---

# Contributing

Orbit is being built publicly and contributions, experiments, discussions, and feedback are always welcome.

Ways to contribute:

- Improve architecture
- Report issues
- Suggest ideas
- Improve documentation
- Create tooling experiments
- Help with testing
- Contribute utilities/modules
- Improve developer workflows

---

# Inspiration & Thanks

Orbit has learned from and experimented around ideas inspired by projects and tools across the Python ecosystem and frontend ecosystem, including:

- [FastAPI](https://fastapi.tiangolo.com)
- [Robyn](https://robyn.tech)
- [Typer](https://typer.tiangolo.com)
- [Click](https://click.palletsprojects.com)
- [Pydantic](https://docs.pydantic.dev)
- [Starlette](https://www.starlette.io)
- [Rich](https://github.com/Textualize/rich)
- [Uvicorn](https://www.uvicorn.org)
- [Vue.js](https://vuejs.org)
- [Vite](https://vitejs.dev)
- [Nuxt](https://nuxt.com)
- [Quasar](https://quasar.dev)

Thanks to the open-source community and all the projects that continue to inspire experimentation, learning, and better developer tooling.
