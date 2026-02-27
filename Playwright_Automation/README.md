# Playwright Test Automation Framework | Portfolio

## 📌 Executive Summary
This folder contains a sophisticated E2E (End-to-End) automation framework built with **Playwright (JavaScript)**. It demonstrates the application of modern software testing patterns to validate critical business logic across multiple web platforms, including E-commerce (**CoffeeCart**), FinTech (**Wizard Bank**), and Social Platforms (**Conduit**).

The project highlights the transition from basic scripting to a scalable **Page Object Model (POM)** architecture, incorporating dynamic data generation, cross-browser testing, and advanced assertion strategies.

---

## 🛠 Tech Stack & Tools
* **Core:** Playwright (Node.js)
* **Design Pattern:** Page Object Model (POM)
* **Data Generation:** Faker.js
* **Configuration:** Multi-browser (Chromium, Firefox, WebKit), Parallel Execution
* **Reporting:** Playwright HTML Reporter, Trace Viewer

---

## 📂 Folder Documentation Structure

### 🏗 Architecture & Core Configuration
Detailed documentation regarding the framework's foundation and execution environment:
* **[BaseURL & Browser Configuration](./BaseURL_and_Browsers_configuration_Alina_Kuliak.pdf)** – Environment-specific setups and cross-browser strategies.
* **[Reporters & Parallelization](./Reporters_and_parallel_execution_configuration.pdf)** – Optimization of test execution speed and results visualization.

### 🧩 Page Object Model (POM) Implementations
Showcasing the separation of UI locators from functional test logic:
* **[CoffeeCart POM Implementation](./POM_for_CoffeeCart.md)** – Modular classes for menu navigation and checkout logic.
* **[Conduit Registration POM](./POM_for_Conduit_SignUp_tests.md)** – Encapsulated registration flows using dynamic data.

### 🧪 Specialized Test Suites
Comprehensive validation scenarios covering different testing layers:
* **[Functional: CoffeeCart E2E](./Coffecart_tests.md)** – End-to-end shopping cart lifecycle.
* **[Functional: Cappuccino Assertions](./Assertions_for_the_Cappuccino_tests.md)** – Complex data validation and price calculation logic.
* **[Validation: Negative Registration](./Sign_up_negative_tests.md)** – Boundary testing and server-side error message verification.
* **[Smoke: UI Integrity](./Sign_up_form_elements_presence_test.md)** – Critical element presence and visibility checks.
* **[Organization: Test Orchestration](./Conduit_tests_organization.md)** – Use of hooks (`beforeEach`, `describe`) for clean test lifecycle management.

---

## 🚀 Key Engineering Highlights

1.  **Resilient Locator Strategy:** Utilization of user-centric locators (`getByRole`, `getByLabel`, `getByPlaceholder`) to ensure test stability against DOM changes.
2.  **Dynamic Data Injection:** Implementation of **Faker.js** to generate unique, non-colliding user datasets for registration and financial flows.
3.  **Advanced Web Assertions:** Leveraging Playwright’s auto-retrying assertions to handle asynchronous UI states and promotional pop-ups.
4.  **Financial Logic Validation:** Specialized tests for the **Wizard Bank** project covering deposit integrity, transaction history, and balance reconciliation.

---
**Author:** Alina Kuliak  
**Role:** QA Engineer / Automation Specialist
