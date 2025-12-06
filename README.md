# TaskFlow-Mobile-Todo-App

![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/TaskFlow-Mobile-Todo-App/ci.yml?style=flat-square&label=Build&logo=githubactions)
![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/TaskFlow-Mobile-Todo-App?style=flat-square&label=Coverage&logo=codecov)
![Tech Stack](https://img.shields.io/badge/TechStack-React%20Native%2FEspo-informational?style=flat-square&logo=react)
![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue?style=flat-square&logo=creativecommons)
![GitHub Stars](https://img.shields.io/github/stars/chirag127/TaskFlow-Mobile-Todo-App?style=flat-square&logo=github)

[★★★★★](${this.url}/issues/new/choose) Star ⭐ this Repo

## Overview
A high-performance, cross-platform mobile ToDo application engineered with Expo and React Native, providing robust task management, seamless persistent storage, and an intuitive, clean user interface.

## 🚀 Features

*   **Cross-Platform:** Native iOS and Android experiences from a single codebase.
*   **Task Management:** Create, edit, delete, and mark tasks as complete.
*   **Persistent Storage:** Tasks are saved locally for offline access.
*   **Clean UI:** Modern, intuitive, and user-friendly interface.
*   **Expo Powered:** Leverages the Expo ecosystem for rapid development and easy deployment.

## 📋 Architecture

This project adheres to a structured and maintainable architecture, inspired by modern mobile development patterns.

mermaid
graph TD
    A[App Entry Point (App.tsx)] --> B(Navigation Container)
    B --> C{Task Stack}
    C --> D[TaskList Screen]
    C --> E[TaskDetail Screen]
    D --> F(Task Service)
    E --> F
    F --> G(Local Storage)
    G --> H(State Management)
    F --> I(UI Components)
    D --> I
    E --> I


## 📚 Table of Contents

*   [Overview](#overview)
*   [Features](#features)
*   [Architecture](#architecture)
*   [Table of Contents](#table-of-contents)
*   [AI Agent Directives](#_1-ai-agent-directives-critical)
*   [Development Standards](#development-standards)
    *   [Setup](#setup)
    *   [Scripts](#scripts)
    *   [Principles](#principles)
*   [License](#license)

<details>
<summary>🤖 AI Agent Directives (Critical)</summary>

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)

*   **PRIMARY SCENARIO: WEB / APP / GUI (Modern Frontend - TypeScript)**
    *   **Stack:** This project leverages **TypeScript 6.x (Strict)**, **Vite 7 (Rolldown)**, and **Tauri v2.x** for native application development. State management utilizes **Signals (Standardized)**. For extensions, **WXT** is the standard.
    *   **Lint/Test:** **Biome** (for ultra-fast linting and formatting) and **Vitest** (for unit testing) are the mandated tools. **Playwright** is used for End-to-End (E2E) testing.
    *   **Architecture:** Adheres to **Feature-Sliced Design (FSD)** principles for modularity and scalability.

*   **OTHER SCENARIOS:** (Refer to `AGENTS.md` for full context)

---

## 4. VERIFICATION COMMANDS (Example for React Native/Expo)

*   **Lint & Format Check:**
    bash
    npx @biomejs/biome check --apply --files-ignore-unknown=true
    
*   **Unit Tests:**
    bash
    npx vitest run
    
*   **E2E Tests (If configured):**
    bash
    npx playwright test
    
*   **Build for Production:**
    bash
    npx expo export
    

---

## 5. CORE PRINCIPLES
*   **SOLID:** Ensure adherence to Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion principles.
*   **DRY:** Don't Repeat Yourself. Maximize code reuse and minimize redundancy.
*   **YAGNI:** You Ain't Gonna Need It. Implement only what is necessary now.
*   **KISS:** Keep It Simple, Stupid. Prioritize straightforward solutions.

</details>

## 🛠️ Development Standards

### Setup

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/TaskFlow-Mobile-Todo-App.git
    cd TaskFlow-Mobile-Todo-App
    

2.  **Install Dependencies:**
    bash
    npx expo install
    

3.  **Start Development Server:**
    bash
    npx expo start
    

### Scripts

| Script               | Description                                      |
| :------------------- | :----------------------------------------------- |
| `npm run dev`        | Starts the development server.                   |
| `npm run lint`       | Runs Biome for linting and formatting checks.    |
| `npm run lint:fix`   | Fixes linting and formatting issues automatically. |
| `npm run test`       | Executes all unit tests using Vitest.            |
| `npm run test:cov`   | Executes tests and generates coverage reports.   |
| `npm run e2e`        | Runs End-to-End tests with Playwright.           |
| `npm run build:ios`  | Builds the iOS application.
*   **AI Integration:** **NO AI INTEGRATION** is specified for this project. Focus remains on core mobile app functionality. If AI is later introduced, prioritize modular design, clear API contracts, and robust error handling for any AI model interactions.
*   **CLI Framework:** **N/A** for this project. Core focus is a mobile GUI application.

---

## 4. VERIFICATION COMMANDS (Example for React Native/Expo)

*   **Lint & Format Check:**
    bash
    npx @biomejs/biome check --apply --files-ignore-unknown=true
    
*   **Unit Tests:**
    bash
    npx vitest run
    
*   **E2E Tests (If configured):**
    bash
    npx playwright test
    
*   **Build for Production:**
    bash
    npx expo export
    

---

## 5. CORE PRINCIPLES
*   **SOLID:** Ensure adherence to Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion principles.
*   **DRY:** Don't Repeat Yourself. Maximize code reuse and minimize redundancy.
*   **YAGNI:** You Ain't Gonna Need It. Implement only what is necessary now.
*   **KISS:** Keep It Simple, Stupid. Prioritize straightforward solutions.

</details>

## 🛠️ Development Standards

### Setup

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/TaskFlow-Mobile-Todo-App.git
    cd TaskFlow-Mobile-Todo-App
    

2.  **Install Dependencies:**
    bash
    npx expo install
    

3.  **Start Development Server:**
    bash
    npx expo start
    

### Scripts

| Script               | Description                                      |
| :------------------- | :----------------------------------------------- |
| `npm run dev`        | Starts the development server.                   |
| `npm run lint`       | Runs Biome for linting and formatting checks.    |
| `npm run lint:fix`   | Fixes linting and formatting issues automatically. |
| `npm run test`       | Executes all unit tests using Vitest.            |
| `npm run test:cov`   | Executes tests and generates coverage reports.   |
| `npm run e2e`        | Runs End-to-End tests with Playwright.           |
| `npm run build:ios`  | Builds the iOS application.                      |
| `npm run build:android` | Builds the Android application.              |

### Principles

*   **SOLID:** Adhering to object-oriented design principles for maintainable and scalable code.
*   **DRY:** Maximizing code reuse and minimizing redundancy.
*   **YAGNI:** Implementing only what is necessary for current functionality.
*   **KISS:** Prioritizing simplicity and understandability.

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**. You are free to share and adapt the material for non-commercial purposes, provided you give appropriate credit, provide a link to the license, and indicate if changes were made.

See the [LICENSE](LICENSE) file for more details.
