<div align="center">

![Orbit](https://github.com/user-attachments/assets/a79b4cbc-4643-4a32-a17f-c47181b25642)

# Orbit

### A modular Python framework ecosystem for backend architecture, fullstack orchestration, and developer tooling.

Open-source project under Undreamt focused on building composable infrastructure and tooling for modern Python applications.

</div>

---

# About

Orbit is designed around a simple principle:

> Frameworks should be composable, understandable, and extensible without becoming tightly coupled or overly abstract.

Rather than acting as a monolithic framework that replaces existing ecosystems, Orbit focuses on structured tooling and orchestration around established technologies.

Orbit currently focuses on:

- Backend architecture
- Runtime orchestration
- Project scaffolding
- Shared framework infrastructure
- Developer tooling
- Experimental architecture design

The ecosystem intentionally integrates with specialized frameworks instead of reimplementing every layer internally.

---

# Vision

Orbit aims to explore modern framework design while remaining lightweight, understandable, and modular.

Instead of creating a single tightly coupled framework, Orbit is structured as independent components that can work together or be used individually.

Long-term goals include:

- Composable architecture
- Shared runtime systems
- Typed contracts
- Extensible tooling
- Service-oriented workflows
- Modular ecosystem design

---

# Ecosystem Modules

| Module | Purpose |
|----------|----------|
| `orbit-core` | Core framework primitives and abstractions |
| `orbit-server` | Runtime integrations and backend execution |
| `orbit-cli` | CLI tooling and project generation |
| `orbit-types` | Shared contracts and type definitions |
| `orbit-kit` | Shared utilities and reusable framework infrastructure |

---

# Ecosystem Relationships

```text
orbit-kit
    ↓
orbit-types
    ↓
orbit-core
    ↓
orbit-server
    ↓
orbit-cli
```

---

# High-Level Architecture

```text
                 ┌─────────────────┐
                 │   orbit-cli     │
                 │ scaffolding/DX  │
                 └────────┬────────┘
                          │
                          ▼
                   orbit new
                          │
         ┌────────────────┴────────────────┐
         ▼                                 ▼

┌─────────────────┐             ┌─────────────────┐
│    Backend      │             │    Frontend     │
│ FastAPI/Robyn   │             │ Vue/Nuxt/etc    │
└────────┬────────┘             └────────┬────────┘
         │                               │
         ▼                               ▼

 ┌──────────────┐             ┌──────────────────┐
 │ orbit-server │             │ Existing frontend│
 │ runtime layer│             │ ecosystems       │
 └──────────────┘             └──────────────────┘
         │
         ▼
 ┌──────────────┐
 │ orbit-core   │
 │ abstractions │
 └──────────────┘
         │
         ▼
 ┌──────────────┐
 │ orbit-types  │
 │ contracts    │
 └──────────────┘
```

---

# Philosophy

Orbit is being developed with emphasis on:

- Modular design
- Strong typing
- Clean architecture
- Developer experience
- Extensibility
- Learnable internals
- Public experimentation
- Practical implementation

Orbit intentionally delegates specialized problems to existing ecosystems instead of recreating everything internally.

Current ecosystem integrations include:

- FastAPI
- Robyn
- Vue
- Nuxt
- Vite
- Quasar

---

# Generated Application Structure

Example generated application:

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
│   └── ...
│
├── orbit.config.py
└── README.md
```

---

# Backend Architecture

Orbit structures backend applications into layered components.

### Routes

Responsible for:

- Endpoint definitions
- HTTP mappings
- Request entrypoints

```python
@app.get("/users")
```

---

### Controllers

Responsible for:

- Request orchestration
- Request handling
- Service coordination

---

### Services

Responsible for:

- Business logic
- Data processing
- Reusable application logic

---

### Models

Responsible for:

- Data structures
- Schemas
- Future ORM integrations

---

### Core

Responsible for:

- Configuration
- Shared utilities
- Common responses

---

# Supported Backends

| Backend | Purpose |
|----------|----------|
| FastAPI | Typed APIs and services |
| Robyn | Lightweight high-performance services |

---

# Frontend Ecosystem

Orbit currently integrates with:

| Frontend | Languages |
|----------|------------|
| Vue | JS / TS |
| Nuxt | JS / TS |
| Quasar | JS / TS |

Orbit delegates frontend runtime responsibilities to dedicated frontend ecosystems.

---

# Runtime Commands

## Backend Runtime

```bash
orbit start
```

Starts backend runtime services.

---

## Frontend Development

```bash
orbit dev
```

Starts frontend development runtime.

---

## Fullstack Development

```bash
orbit runserver
```

Starts backend and frontend development environments simultaneously.

---

## Production Build

```bash
orbit build
```

Builds frontend production assets.

---

## Production Preview

```bash
orbit serve
```

Runs frontend production preview.

---

# CLI Architecture

Orbit CLI currently uses:

- Typer

Available commands:

```bash
orbit new
orbit start
orbit dev
orbit runserver
orbit build
orbit serve
```

---

# Project Generation Workflow

```bash
orbit new
```

Current generation workflow:

1. Select backend framework
2. Select frontend framework
3. Generate project structure
4. Copy templates
5. Generate `orbit.config.py`
6. Create starter application files

---

# Orbit Configuration

Example:

```python
CONFIG = {
    "backend": {
        "framework": "fastapi",
        "entry": "main:app"
    },

    "frontend": "vue"
}
```

Used as:

- Runtime configuration
- Framework metadata
- Application orchestration

---

# Installation

## CLI

```bash
pip install orbit-framework-cli
```

---

## Individual Packages

```bash
pip install orbit-framework-core
pip install orbit-framework-server
pip install orbit-framework-types
pip install orbit-framework-kit
```

---

# Current Focus Areas

Orbit currently focuses on:

- APIs
- Services
- Backend platforms
- Fullstack orchestration
- Tooling infrastructure

---

# Development Status

Orbit is currently in an early ecosystem development phase.

Current state:

- Core architecture established
- CLI tooling operational
- Runtime orchestration functional
- Project generation available
- Ecosystem structure defined

Areas still evolving:

- Service abstractions
- Middleware systems
- Plugin architecture
- Runtime features
- Tooling improvements
- Data integrations

---

# Contributing

Orbit is being built publicly and contributions are welcome.

Ways to contribute:

- Improve architecture
- Report issues
- Improve documentation
- Create tooling experiments
- Help testing
- Suggest ideas
- Contribute utilities/modules

---

# Inspiration

Orbit experiments around ideas and concepts influenced by:

- FastAPI
- Robyn
- Typer
- Pydantic
- Starlette
- Rich
- Uvicorn
- Vue
- Vite
- Nuxt
- Quasar

Thanks to the open-source community and the projects that continue to inspire learning and experimentation.
