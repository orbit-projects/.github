# Orbit

> A modular Python framework and tooling ecosystem focused on modern developer infrastructure, experimental architecture, and clean extensible tooling.

Orbit is an open-source ecosystem under [Undreamt](https://github.com/undreamt-hq) focused on building developer-first tooling and framework utilities in Python.

The ecosystem is designed around a simple idea:

Frameworks should be modular, understandable, type-safe, and easy to extend — without becoming bloated or overly abstract.

---

# Vision

Orbit aims to explore modern framework architecture while keeping the ecosystem lightweight, learnable, and flexible.

Instead of building a single monolithic framework, Orbit focuses on creating independent modules that work well together while remaining usable on their own.

The long-term goal is to build an ecosystem that helps developers experiment, learn framework internals, and create scalable tooling with clean architecture principles.

---

# Philosophy

Orbit is being built with strong focus on:

* Modular design
* Clean architecture
* Strong typing
* Developer experience
* Learnable internals
* Extensibility
* Public experimentation
* Real-world implementation

The project is intentionally being developed in public while continuously evolving through experimentation, iteration, and learning.

---

# Roadmap

## Early Foundation

- [x] Core project structure
- [x] Initial package ecosystem
- [x] CLI foundation
- [x] Type system experiments
- [x] Static site generation experiments
- [x] Modular architecture planning

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

# Current Projects

Orbit currently includes development around:

* `orbit-core`
* `orbit-types`
* `orbit-cli`
* `orbit-kit`
* `orbit-server`
* `orbit-ssg`

Additional modules and tooling may be added as the ecosystem evolves.

---

# Current Status

| Component | Status |
|---|---|
| Core ecosystem structure | ✅ |
| Initial modular architecture | ✅ |
| CLI tooling foundation | ✅ |
| Type utilities | ✅ |
| Static site generation experiments | ✅ |
| Stable APIs | ❌ |
| Full documentation | ❌ |
| Production-ready release | ❌ |
| Complete testing coverage | ❌ |
| SSR infrastructure | ❌ |

---

# Ecosystem Goals

Orbit is currently focused on exploring:

* Framework architecture
* Static site generation
* Backend utilities
* CLI tooling
* Shared typing systems
* Developer infrastructure
* Experimental tooling
* Modular ecosystem design

The ecosystem aims to remain flexible and composable while encouraging developers to understand and experiment with framework internals instead of hiding everything behind abstractions.

---

# Building Applications With Orbit

Orbit is still experimental, but current development is centered around creating modular developer workflows.

A typical workflow currently looks like:

## 1. Create a project structure

```bash
mkdir myapp
cd myapp
```

## 2. Create virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

## 3. Install Orbit modules

```bash
pip install orbit-core orbit-cli orbit-ssg
```

## 4. Initialize project

```bash
orbit init
```

## 5. Start development server

```bash
orbit runserver
```

Orbit development workflows are actively evolving and APIs may change frequently while the ecosystem matures.

---

# Contributing

Orbit is being built publicly and contributions, experiments, discussions, and feedback are always welcome.

## Ways to contribute

* Improve architecture
* Report issues
* Suggest ideas
* Improve documentation
* Create tooling experiments
* Help with testing
* Contribute utilities/modules
* Improve developer workflows

## Contribution Workflow

```bash
# Fork repository

# Clone your fork
git clone https://github.com/your-username/orbit

# Create branch
git checkout -b feature/my-feature

# Commit changes
git commit -m "Add feature"

# Push branch
git push origin feature/my-feature
```

Then open a pull request describing your changes and ideas.

---

# Inspiration & Thanks

Orbit has learned from and experimented around ideas inspired by projects and tools across the Python ecosystem, including:

* [FastAPI](https://fastapi.tiangolo.com)
* [Robyn](https://robyn.tech)
* [Typer](https://typer.tiangolo.com)
* [Click](https://click.palletsprojects.com)
* [Pydantic](https://docs.pydantic.dev)
* [Starlette](https://www.starlette.io)
* [Rich](https://github.com/Textualize/rich)
* [Uvicorn](https://www.uvicorn.org)

Thanks to the open-source community and all the projects that continue to inspire experimentation, learning, and better developer tooling.
