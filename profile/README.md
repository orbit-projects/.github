# Orbit

<div align="center">

<img src="assets/orbit.png" width="140" alt="Orbit Logo" />

# Orbit

### A modular Python framework and tooling ecosystem focused on modern developer infrastructure, experimental architecture, and clean extensible tooling.

Open-source project under [Undreamt](https://github.com/undreamt-hq) focused on building developer-first tooling and framework utilities in Python.

</div>

---

## About

Orbit is an open-source ecosystem focused on creating modular tooling and framework utilities with strong emphasis on developer experience, architecture, and experimentation.

The ecosystem is designed around a simple idea:

> Frameworks should be modular, understandable, type-safe, and easy to extend — without becoming bloated or overly abstract.

---

# Vision

Orbit aims to explore modern framework architecture while keeping the ecosystem lightweight, learnable, and flexible.

Instead of building a single monolithic framework, Orbit focuses on creating independent modules that work well together while remaining usable on their own.

The long-term goal is to build an ecosystem that helps developers experiment, learn framework internals, and create scalable tooling with clean architecture principles.

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

The project is intentionally being developed in public while continuously evolving through experimentation, iteration, and learning.

---

# Current Projects

Orbit currently includes development around:

- `orbit-core`
- `orbit-types`
- `orbit-cli`
- `orbit-kit`
- `orbit-server`

Additional modules and tooling may be added as the ecosystem evolves.

---

# Roadmap

## Early Foundation

- [x] Core project structure
- [x] Initial package ecosystem
- [x] CLI foundation
- [x] Type system experiments
- [x] Modular architecture planning

---

## In Progress

- [ ] Stable public APIs
- [ ] Advanced dependency injection system
- [ ] Improved developer tooling
- [ ] Better build pipeline
- [ ] Enhanced typing utilities
- [ ] Documentation system
- [ ] Testing infrastructure
- [ ] Frontend integration utilities
- [ ] Developer workflow improvements

---

## Future Goals

- [ ] Full ecosystem stabilization
- [ ] SSR support exploration
- [ ] Multi-framework frontend support
- [ ] Plugin ecosystem
- [ ] Advanced developer infrastructure
- [ ] Production-ready tooling
- [ ] Extensive documentation
- [ ] Ecosystem-wide integrations

---

# Ecosystem Goals

Orbit is currently focused on exploring:

- Framework architecture
- Backend utilities
- CLI tooling
- Shared typing systems
- Developer infrastructure
- Experimental tooling
- Modular ecosystem design

The ecosystem aims to remain flexible and composable while encouraging developers to understand and experiment with framework internals instead of hiding everything behind abstractions.

---

# Building Applications With Orbit

Orbit is still experimental, but current development is centered around creating modular developer workflows and lightweight application development.

A typical Orbit workflow currently looks like this:

## 1. Create Project

```bash
mkdir testapp
cd testapp
```

## 2. Create Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate
```

## 3. Install Orbit

```bash
pip install orbit-framework-kit
```

## 4. Initialize Orbit Project

```bash
orbit init
```

This generates the initial Orbit project structure and configuration.

## 5. Start Development Server

```bash
orbit runserver
```

The development server watches files and rebuilds automatically during development.

## 6. Build Production Files

```bash
orbit build
```

This generates the production output.

---

Orbit development workflows are actively evolving and APIs may change frequently while the ecosystem matures.

---

# Community

Orbit welcomes:

- Developers
- Open-source contributors
- Students
- Experimenters
- Curious builders

Contributions, feedback, and ideas are always welcome.

---

# Contributing

Orbit is being built publicly and contributions, experiments, discussions, and feedback are always welcome.

## Ways To Contribute

- Improve architecture
- Report issues
- Suggest ideas
- Improve documentation
- Create tooling experiments
- Help with testing
- Contribute utilities/modules
- Improve developer workflows
- Experiment with integrations
- Build reusable tooling

---

# Contribution Workflow

## 1. Fork The Repository

Fork the repository from GitHub.

## 2. Clone Your Fork

```bash
git clone https://github.com/your-username/{project-name}
cd {project-name}
```

## 3. Create Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate
```

## 4. Install Development Dependencies

```bash
pip install -e .
```

## 5. Create A Feature Branch

```bash
git checkout -b feature/my-feature
```

## 6. Make Changes And Test

```bash
orbit runserver
```

## 7. Commit Changes

```bash
git add .
git commit -m "Add feature"
```

## 8. Push Branch

```bash
git push origin feature/my-feature
```

Then open a pull request describing your changes, experiments, or improvements.

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

Thanks to the open-source community and all the projects that continue to inspire experimentation, learning, and better developer tooling.

---

<div align="center">

### Build beyond convention.

</div>

---

# Status

Orbit is currently experimental and under active development.

APIs, tooling, and project structure may evolve frequently as the ecosystem grows.