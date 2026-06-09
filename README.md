# Unity Project Architecture Template

A scalable and extensible Unity project template built around **VContainer**, **State Machines**, and a modular **Service-Oriented Architecture**.

The goal of this template is to provide a clean and maintainable foundation for game development by separating application flow, gameplay logic, UI, infrastructure, and data into independent modules.

## Key Features

* Dependency Injection with VContainer
* Modular architecture with isolated scopes
* Hierarchical State Machines
* Window-based UI framework
* Input abstraction layer
* Save/Load system
* Scene management
* Asset management
* Settings system
* Audio and vibration services
* Addressables support
* UniRx integration
* DOTween integration
* Centralized update services (Tickable, FixedTickable, LateTickable)

## Architecture Overview

### Dependency Injection

The project uses **VContainer** as the primary Dependency Injection framework.

Dependencies are registered through dedicated scopes:

* **ProjectScope** — global application services and systems
* **MenuScope** — menu-specific dependencies
* **GameplayScope** — gameplay-specific dependencies

This approach keeps systems decoupled and allows each module to manage its own lifecycle independently.

### State Machines

Application flow is driven by dedicated state machines.

The template contains separate state machines for:

* Game Flow
* Menu Flow
* Gameplay Flow

Typical execution flow:

```text
Bootstrap → Setup → Loading → Loop
```

This structure makes it easy to add new states and features without introducing tight coupling between systems.

### Service Layer

Core functionality is implemented through injectable services.

Included services:

* Input Service
* Window Service
* Scene Service
* Save/Load Service
* Asset Service
* Settings Service
* Time Scale Service
* Vibration Service
* Logging Service
* Tickable Services

Additional services can be added without modifying existing modules.

### UI Framework

The UI is built around a window management system.

Features include:

* Window factories
* Centralized window lifecycle management
* Dependency injection support
* Easy creation of new screens and popups

### Data Management

The template separates runtime and persistent data.

Main data models:

* Static Data
* Persistent Data
* ScriptableObject Configurations

This allows game data to remain organized and easily extendable.

## Project Goals

This template is designed to help developers:

* Build scalable Unity projects
* Reduce coupling between systems
* Improve maintainability
* Accelerate prototyping
* Create production-ready architecture from the start

## Tech Stack

* Unity
* C#
* VContainer
* Addressables
* UniRx
* DOTween
* Odin Inspector

## Getting Started

1. Clone the repository.
2. Open the project in Unity.
3. Configure project-specific services and game states.
4. Start building gameplay features on top of the provided architecture.

## License

MIT License.
