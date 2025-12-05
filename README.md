<p align="center">
  <a href="https://github.com/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App">
    <img src="https://raw.githubusercontent.com/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App/main/.github/assets/logo.svg" alt="TaskPilot Logo" width="150">
  </a>
</p>

<h1 align="center">TaskPilot-CrossPlatform-ToDo-Mobile-App</h1>

<p align="center">
  <a href="https://github.com/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App/ci.yml?branch=main&style=flat-square&label=Build%20Status" alt="Build Status">
  </a>
  <a href="#tech-stack">
    <img src="https://img.shields.io/badge/Stack-React_Native%20%7C%20Expo-61DAFB?style=flat-square&logo=react" alt="Tech Stack">
  </a>
  <a href="#development-standards">
    <img src="https://img.shields.io/badge/Format%20%26%20Lint-Biome-1A908F?style=flat-square&logo=biome" alt="Linting">
  </a>
  <a href="https://codecov.io/gh/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App">
    <img src="https://img.shields.io/codecov/c/github/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App?style=flat-square&token=YOUR_CODECOV_TOKEN" alt="Code Coverage">
  </a>
  <a href="https://github.com/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg?style=flat-square" alt="License">
  </a>
  <a href="https://github.com/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App/stargazers">
    <img src="https://img.shields.io/github/stars/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App?style=flat-square" alt="GitHub Stars">
  </a>
</p>

<p align="center">
  <a href="https://github.com/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App/stargazers">⭐ Star this Repo</a>
</p>

---

## 🚀 Project Overview: TaskPilot

TaskPilot is an ultra-efficient, cross-platform mobile application designed for personal task management. Built atop the robust React Native and Expo framework, it guarantees native performance on both iOS and Android while utilizing persistent storage for reliable, offline-first operation.

This repository serves as a reference implementation for the **Feature-Sliced Design (FSD)** architecture applied to complex mobile applications, ensuring maximum maintainability, separation of concerns, and future scalability.

## 🗺️ Table of Contents

1.  [Project Overview](#-project-overview-taskpilot)
2.  [Architecture & Design](#-architecture--design)
3.  [AI Agent Directives (Meta-Programming)](#-ai-agent-directives-meta-programming)
4.  [Tech Stack](#tech-stack)
5.  [Development Standards](#development-standards)
    *   [Prerequisites](#prerequisites)
    *   [Setup and Installation](#setup-and-installation)
    *   [Available Scripts](#available-scripts)
6.  [License](#-license)

## 📐 Architecture & Design

TaskPilot implements the **Feature-Sliced Design (FSD)** methodology, which is paramount for scalable mobile development. This structure prevents circular dependencies, enforces strict layering, and organizes the codebase around functional slices (features, entities, shared). The app's core persistence layer leverages **AsyncStorage** for fast, reliable data handling.

mermaid
graph TD
    A[TaskPilot App - Entry Point] --> B(App/Providers/Theme);
    B --> C{Pages/Screens};
    C --> D(Features: TaskCreation, TaskList, TaskEditing);
    D --> E(Entities: TaskItem, UserSettings);
    E --> F(Shared: UI/Components, Utils, API);
    F --> G[Persistence Layer: AsyncStorage];


## 🤖 AI Agent Directives (Meta-Programming)

<details>
<summary><strong>SYSTEM VITAL SIGNS & CODING STANDARDS (Click to Expand)</strong></summary>

### APEX ARCHITECTURAL MANDATES

1.  **Architecture:** **Feature-Sliced Design (FSD)**. All new components must adhere to the `app`, `pages`, `features`, `entities`, `shared` structure. Imports must flow top-down (e.g., `features` can import from `entities` or `shared`, but never vice-versa).
2.  **State Management:** State must be isolated within features or use a simple, centralized context/hook pattern for global settings (e.g., Theme).
3.  **UI/UX Standards:** Must strictly adhere to the defined design system (in `shared/ui`). Use atomic component design principles.

### TECHNOLOGY STACK DEFINITION

| Attribute | Value | Target Version |
| :--- | :--- | :--- |
| **Core Platform** | React Native (via Expo) | SDK 51+ |
| **Language Standard** | JavaScript (ESM) | ES2023 |
| **Persistence** | React Native AsyncStorage | Latest |
| **Linting/Formatting** | Biome | Latest |
| **Testing Framework** | Jest/React Native Testing Library | Latest |

### VERIFICATION & QUALITY ASSURANCE PROTOCOL

**Mandate:** All pull requests MUST pass these checks. Agents should use these commands for local validation.

| Command | Description | Purpose |
| :--- | :--- | :--- |
| `npm install` | Installs all dependencies using the lock file. | Dependency Integrity |
| `npm run lint:fix` | Executes Biome for formatting and linting fixes. | Code Quality & Consistency |
| `npm test` | Runs all unit and integration tests (Jest). | Functional Correctness |
| `npm run start` | Launches the Expo development server. | Local Runtime Check |

### CODE PRINCIPLES

*   **SOLID:** Single Responsibility Principle (SRP) is crucial in FSD slices.
*   **DRY:** Do not repeat UI logic or utility functions. Place shared logic in `shared/utils`.
*   **YAGNI:** Implement only the features currently required for the sprint. Prevent scope creep.

</details>

## 🛠️ Tech Stack

TaskPilot leverages modern JavaScript tooling to deliver a performant and maintainable mobile experience.

*   **Framework:** React Native
*   **Toolchain:** Expo (Managed Workflow)
*   **Language:** JavaScript (ESNext)
*   **Styling:** StyleSheet API / React Native Paper (or similar component library)
*   **Persistence:** `AsyncStorage`
*   **Testing:** Jest and React Native Testing Library
*   **Code Quality:** Biome (Linting and Formatting)

## Development Standards

### Prerequisites

Ensure you have the following installed:

*   Node.js (LTS version 18+)
*   npm or yarn/pnpm (npm is used in examples)
*   Expo CLI (`npm install -g expo-cli`)

### Setup and Installation

Clone the repository and install dependencies using the standard workflow:

bash
# 1. Clone the repository
git clone https://github.com/chirag127/TaskPilot-CrossPlatform-ToDo-Mobile-App.git

# 2. Navigate to the project directory
cd TaskPilot-CrossPlatform-ToDo-Mobile-App

# 3. Install dependencies
npm install


### Available Scripts

Use these scripts to manage the development lifecycle, as defined in `package.json`:

| Script | Command | Description |
| :--- | :--- | :--- |
| `start` | `expo start` | Starts the Expo development server locally. |
| `android` | `expo run:android` | Builds and runs the app on an Android emulator/device. |
| `ios` | `expo run:ios` | Builds and runs the app on an iOS simulator/device. |
| `web` | `expo start --web` | Starts the web version (development only). |
| `test` | `jest` | Runs all unit and integration tests. |
| `lint` | `npx biome check .` | Runs the linter against the entire codebase. |
| `lint:fix` | `npx biome check --apply-unsafe .` | Fixes linting and formatting issues automatically. |

## 📝 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** License. See the [LICENSE](LICENSE) file for details.
