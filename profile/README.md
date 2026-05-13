<div align="center">
  
<svg width="512" height="405" viewBox="0 0 512 405" fill="none" xmlns="http://www.w3.org/2000/svg">
<rect width="512" height="405" fill="black"/>
<rect width="512" height="405" fill="white" fill-opacity="0.1"/>
<circle cx="149.655" cy="232.08" r="67.5798" fill="white" stroke="white"/>
<circle cx="334.124" cy="186.72" r="45.2199" fill="white" stroke="white"/>
<path d="M234.371 76.3178C294.804 65.6618 352.285 72.369 396.339 91.6984C440.413 111.036 470.779 142.854 477.742 182.342C484.705 221.831 467.052 262.116 432.251 295.361C397.464 328.592 345.744 354.555 285.311 365.211C224.878 375.867 167.397 369.159 123.342 349.83C79.2689 330.492 48.9036 298.674 41.9407 259.186C34.9778 219.698 52.6296 179.413 87.4311 146.167C122.218 112.936 173.938 86.9738 234.371 76.3178Z" stroke="white" stroke-width="5"/>
<path d="M188.854 59.8318C244.469 33.8977 301.728 25.4992 349.284 32.7678C396.861 40.0397 434.427 62.914 451.373 99.2547C468.319 135.595 461.694 179.076 436.683 220.197C411.683 261.299 368.444 299.763 312.828 325.697C257.213 351.631 199.954 360.029 152.398 352.761C104.822 345.489 67.2557 322.614 50.3098 286.274C33.3639 249.933 39.9877 206.452 64.9987 165.332C89.999 124.23 133.238 85.766 188.854 59.8318Z" stroke="white" stroke-width="5"/>
</svg>

<img width="512" height="405" alt="Orbit" src="https://github.com/user-attachments/assets/a79b4cbc-4643-4a32-a17f-c47181b25642" />


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
