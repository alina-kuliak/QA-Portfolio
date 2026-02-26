# 🚀 API Testing: Conduit Project

This section documents the functional and automated testing of the Conduit REST API. The goal was to verify the backend logic, security (JWT), and data integrity through comprehensive endpoint validation.

---

## 🛠 Project Setup & Infrastructure
To manage the testing lifecycle, the following infrastructure was established:
* **Postman Workspace:** Created a dedicated team workspace to house the test suite and environment configurations.
* **[Jira Integration:](./DocsConduit/Jira_Postman_Practice.png)** A new project was initialized in Jira to manage test tasks, user stories, and defect tracking.
* **Collection:** Developed the `Postman Practice [Alina Kuliak]` collection containing a complete suite of CRUD operations and edge-case scenarios.

---

## 🔗 Live Postman Workspace
You can view the interactive documentation, environment variables, and automated test scripts here:
👉 **[View My Public Postman Workspace](https://www.postman.com/alinakuliak/workspace/postman-practice-alina-kuliak/collection/40251860-63fa10ca-fa27-4d2f-9287-1152e09b87cf?action=share&source=copy-link&creator=40251860)**

---

## 📑 Testing Scope & Implementation

### 1. Endpoint Verification
I observed and tested the core [Conduit API](./DocsConduit/Conduit_API_endpoints.pdf) endpoints, including:
* **Authentication:** `POST /api/users/login` and `POST /api/users` (Sign up).
* **User Management:** `GET /api/user` and `PUT /api/user`.
* **Articles:** `GET /api/articles`, `POST /api/articles`, `PUT /api/articles/:slug`, `DELETE /api/articles/:slug`.
* **Comments:** `POST /api/articles/:slug/comments` and `DELETE /api/articles/:slug/comments/:id`.

### 2. Advanced Coverage
Beyond the basic requirements, I added tests for:
* **Profile Logic:** `GET /api/profiles/:username` and `POST /api/profiles/:username/follow`.
* **Filtering:** Validation of query parameters for the Global Feed (limit, offset, tag).
* **Negative Scenarios:** Testing for `401 Unauthorized` on protected routes and `422 Unprocessable Entity` for invalid data formats.

### 3. Automated Test Scripts
Every request is covered by JavaScript tests in Postman to verify:
* **Status Codes:** Verification of $200$, $201$, $204$, or error codes.
* **Response Time:** Ensuring API responsiveness is within acceptable limits (e.g., $< 500ms$).
* **JSON Schema:** Validating the structure of the response body and data types.
* **Environment Variables:** Automatically extracting **JWT Tokens** from login responses to authorize subsequent requests.

---

## 🐛 Defect Tracking (Jira)
Bugs identified during API testing were reported in Jira and linked to corresponding User Stories. 

| Bug ID | Summary | Priority | Status |
| :--- | :--- | :--- | :--- |
| **HUN-A-001** | Article creation returns 500 Error when using special characters in tags | High | Closed |
| **HUN-A-002** | JWT Token does not expire after user logout via API | Critical | Open |

---

## ✅ Execution Results
Below is a screenshot of the **Postman Collection Runner** demonstrating the successful execution of the test suite:

![Postman Runner Results](./DocsConduit/Postman_Run_Result_Conduit.png)
