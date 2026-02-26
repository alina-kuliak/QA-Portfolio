# 📝 Project Overview: Conduit (API & Web Testing)

**Conduit** is an open-source social blogging platform (similar to Medium) that allows users to create accounts, publish articles, post comments, follow other authors, and "favorite" content. This project demonstrates a comprehensive testing approach, bridging the gap between UI functional testing and deep REST API verification.

---

## 🎯 Project Goals
* Ensure stable operation of core modules: Authentication, Articles, Profiles, and Comments.
* Validate backend business logic through exhaustive REST API endpoint testing.
* Organize a transparent testing process using Agile methodologies and industry-standard tools (Jira).

---

## 🛠 Tech Stack
* **API Testing:** Postman (Collections, Environment Variables, JavaScript Tests).
* **Test Management:** Jira (Backlog management, Sprint planning, Defect Tracking).
* **Documentation:** TestRail / Google Docs.

---

## 📑 Testing Scope

### 🌐 UI Testing (Manual)
* **Authentication:** User registration, login with valid/invalid credentials, and session persistence.
* **Content Lifecycle:** Creation, editing, and deletion of articles and comments.
* **Interaction:** Testing the tagging system, follow/unfollow logic, and global/user feed filtering.

### 🚀 API Testing (Postman)
Full coverage of key endpoints (`/api/users`, `/api/articles`, `/api/comments`):
* **Status Code Validation:** Verifying $200$ OK, $201$ Created, $401$ Unauthorized, and $422$ Unprocessable Entity responses.
* **Security:** Testing authorization via **JWT Tokens** in request headers.
* **Response Validation:** JavaScript-based test scripts to verify JSON schema structure, mandatory fields, and data types.

---
## 📂 Project Artifacts & Documentation

### 📋 1. Test Planning & Analysis
Foundational documents where the testing strategy and system logic were defined.
* [**Test Plan**](./DocsConduit/Test_Plan_Conduit.pdf) – Overall strategy, scope, and test objectives.
* [**Functional Decomposition**](./DocsConduit/Decomposition_Conduit.md) – Hierarchical breakdown of application features.
* [**Client-Server Architecture**](./DocsConduit/Client_server_architecture_Conduit.pdf) – Technical overview of system interactions.

### 🧪 2. Test Design (Manual & Technical)
Application of various test design techniques to ensure maximum coverage with optimized effort.
* [**Test Cases (Markdown)**](./DocsConduit/Test_Cases.md) – Interactive list of detailed test scenarios.
* [**Test Cases (PDF Version)**](./DocsConduit/Test_Cases_ConduitPDF.pdf) – Portable version of the test suite.
* [**Decision Table Testing**](./DocsConduit/Decision_table_testing_for_Conduit.pdf) – Logic-based testing for complex business rules.
* [**Pairwise Technique**](./DocsConduit/Pairwise_technique_Conduit.pdf) – Combinatorial testing for input parameters.

### 🚀 3. API Testing (Postman)
Automated validation of REST API endpoints to ensure backend stability.
* [**API Endpoints Overview**](./DocsConduit/Conduit_API_endpoints.pdf) – Documentation of tested routes and parameters.
* [**Postman Run Results**](./DocsConduit/Postman_Run_Result_Conduit.png) – Evidence of automated test suite execution and status codes validation.

### 📊 4. Management & Evidence
Screenshots from Jira and Postman proving the practical execution of the project.
* [**Jira_Conduit_Bug_Report**](./DocsConduit/Jira_Conduit_Bug_Reports.png) – Workflow and defect tracking for UI testing.
* [**Manual Testing Jira Board**](./DocsConduit/Jira_Conduit_Manual.png) – Workflow and defect tracking for UI testing.
* [**API Testing Jira Board**](./DocsConduit/Jira_Postman_Practice.png) – Task management for the Postman automation phase.

---

## 🛠 Tools Used
* **Test Management:** Jira (Agile/Scrum).
* **API Testing:** Postman (JavaScript snippets for automated assertions).
* **Documentation:** Markdown, PDF.
* **Techniques:** Boundary Value Analysis, Equivalence Partitioning, Decision Tables, Pairwise.

---
*Prepared by: Alina Kuliak*
