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

## 📁 Project Artifacts

### 📋 Documentation
* [Test_Plan_Conduit_[Alina Kuliak].pdf](./Docs/Test_Plan_Conduit_%5BAlina%20Kuliak%5D.pdf) — Strategy, scope, and risk assessment.
* [Decomposition_Conduit_[Alina Kuliak].pdf](./Docs/Decomposition_Conduit_%5BAlina%20Kuliak%5D.pdf) — Feature decomposition and hierarchy.
* [Test_Cases_Conduit.pdf](./Docs/Test_Cases_Conduit.pdf) — Detailed test scenarios and execution steps.
* [Bug_Reports_Conduit.pdf](./Docs/Bug_Reports_Conduit.pdf) — Comprehensive log of identified defects.

### 🧪 API Assets (Postman)
* [Postman_Collection_Conduit.json](./Postman-Collections/Conduit_Collection.json) — Exported test collection for easy import.
* [Postman_Environment_Conduit.json](./Postman-Collections/Conduit_Environment.json) — Global variables and environment settings.

### 🖼 Evidence
* [Jira_Dashboard_Conduit.png](./Docs/Jira%20Dashboard%20Conduit.png) — Screenshot of the development and testing workflow in Jira.

---

## 📊 Key Results
* Developed a full **RTM (Requirements Traceability Matrix)** to link business requirements with test coverage.
* Created a Postman collection automating the verification of core API endpoints.
* Successfully identified and documented critical integration issues between the Frontend and Backend, specifically regarding $422$ error handling.

---

### 💡 How to run API tests locally?
1. Clone the repository.
2. Import `Conduit_Collection.json` into Postman.
3. Select `Conduit_Environment.json` in the Environment dropdown.
4. Run the collection via the **Postman Collection Runner** to view automated test results.
