# UI Automation with Playwright

## 📌 Project Overview
This folder contains a collection of automated test suites for various web applications (**Conduit**, **CoffeeCart**, **Wizard Bank**). The project focuses on creating robust, maintainable, and scalable test automation frameworks using modern industry standards.

---

## 🛠 Automation Features & Implementation

### 🏗 Framework Architecture
* **Page Object Model (POM):** Implemented for **Conduit SignUp** and **CoffeeCart** to separate test logic from page-specific elements, ensuring high maintainability.
* **Test Organization:** Structured test suites using `describe` blocks and logical grouping in `Conduit_tests_organization`.
* **Global Configuration:** Advanced setup of `BaseURL`, browser viewports, and multi-browser support (Chromium, Firefox, WebKit).

### 🧪 Test Scenarios & Logic
* **Functional Testing:** End-to-end flows for adding products (Cappuccino) and verifying cart logic.
* **Negative Testing:** Validation of Sign-up forms with invalid data and error message assertions.
* **UI/UX Validation:** Presence and visibility checks for form elements.
* **Complex Assertions:** Using Playwright's `expect` library to validate UI states, counts, and URL transitions.

### ⚙️ Execution & Reporting
* **Parallel Execution:** Configured to run tests in parallel to optimize execution time.
* **Reporting:** Setup of built-in reporters (HTML, List) for clear visibility of test results and debugging.

---

## 📂 File Structure Guide

| File Name | Description |
| :--- | :--- |
| `POM_for_Conduit_SignUp_tests` | Implementation of Page Object Model for the Conduit app. |
| `POM_for_CoffeeCart` | Page objects and action methods for the CoffeeCart app. |
| `Wizard_bank_tests` | Automation of banking flows and transaction logic. |
| `Reporters_and_parallel_execution` | Configuration for performance and result visualization. |
| `BaseURL_and_Browsers_configuration` | Global project settings for environment and cross-browser testing. |
| `Assertions_for_the_Cappuccino_tests`| Deep dive into data-driven assertions and UI state validation. |
| `Sign_up_negative_tests` | Security and validation testing for user registration. |

---

## 🚀 How to Run
1.  **Install dependencies:** `npm install`
2.  **Run all tests:** `npx playwright test`
3.  **Run specific suite:** `npx playwright test Coffecart_tests.spec.js`
4.  **Show report:** `npx playwright show-report`

---
*Created by Alina Kuliak*
