# API Testing Portfolio: Postman Automation & Scripting

## 📌 Project Overview
This project contains a series of API testing collections for **Conduit (RealWorld App)**, **Weather API**, and **Student API**. It demonstrates a transition from basic REST functional testing to advanced automation using JavaScript-based scripting, dynamic variables, and request orchestration.
**Main Project Collection** [🔗View Full Conduit API Collection](https://www.postman.com/alinakuliak/workspace/postman-practice-alina-kuliak)

---

## 🛠 Technical Skills & Tools
* **Testing:** Functional API Testing, Regression, Negative Testing (422 Unprocessable Entity).
* **Scripting:** Pre-request and Post-response (Tests) scripts in JavaScript.
* **Automation:** API Chaining, Automated Auth Token handling, Dynamic data generation.
* **Variable Management:** Global, Collection, and Environment scopes.
* **Debugging:** Advanced use of Postman Console for script execution tracking.

---

## 📑 Detailed Project Modules

### 1. Postman Basics & Data Retrieval
Focus on working with existing documentation and retrieving specific data sets.
* **Student API:** Created requests to fetch all goods, specific items by ID, and filtered "todos" (completed/uncompleted) for specific users.
* **Status Validations:** Implemented status code tests (200 OK) for all requests in the suite.
* [🔗 View Collection Link](https://www.postman.com/alinakuliak/workspace/postman-practice-alina-kuliak/collection/40251860-a1885968-04f3-458c-8f1a-8edb5d399fe4?action=share&creator=40251860)

### 2. Functional API Testing (Sign In / Sign Up)
Validation of user authentication flows and error handling.
* **Conduit API (Sign In/Up):** Verified successful authentication and handled negative scenarios (already taken email/username).
* **Variable Injection:** Integrated `BASE_URL` and `passwordConduit` variables to maintain clean and reusable collections.
* **Advanced Validations:** Fixed complex scripts to ensure 4/4 passed tests for dynamic responses.
* [🔗 View Collection Link](#)

### 3. Scripting Order & Execution Logic
Deep dive into the Postman hierarchy (Collection -> Folder -> Request).
* **Logic Validation:** Used Postman Console logging to verify the sequence of script execution across different levels.
* **Debugging:** Demonstrated proficiency in using the console to track script propagation and debug failures.
* [🔗 View Collection Link](https://www.postman.com/alinakuliak/workspace/postman-practice-alina-kuliak/collection/40251860-ec0faf23-4be9-4e97-9abb-9c0d5d1aa91b?action=share&creator=40251860)
* [🔗 View Collection Link](https://www.postman.com/alinakuliak/workspace/postman-practice-alina-kuliak/collection/40251860-e3369d23-e75d-49e6-8c96-a0551a1fb429?action=share&source=copy-link&creator=40251860)

### 4. Advanced Pre-Request Scripts & Data Generation
Using JavaScript to prepare the environment before the request is fired.
* **Introduction to Pre-Requests:** Automated the creation of unique `emailConduit` and `username` variables for registration.
* **Weather API:** Implemented a script to dynamically generate current dates in the required format for real-time weather requests.
* [🔗 View Collection Link](https://www.postman.com/alinakuliak/workspace/postman-practice-alina-kuliak/collection/40251860-7282257b-7ea9-437a-94d6-6f6528043c79?action=share&source=copy-link&creator=40251860)

### 5. Advanced Postman: Orchestration & Independent Requests
The most complex part of the suite, involving background request execution.
* **Request Chaining:** Implemented `pm.sendRequest` in the Pre-request tab to automatically register a new user before creating an article.
* **Cleanup Automation:** Added logic to the Post-response tab to automatically delete created articles, ensuring a clean test environment.
* **Dynamic Bodies:** Generated random data for article bodies using JavaScript.
* [🔗 View Collection Link](https://www.postman.com/alinakuliak/workspace/postman-practice-alina-kuliak/collection/40251860-623bf942-22d2-4522-8fc3-1f3674fb623f?action=share&source=copy-link&creator=40251860)

### 6. Postman Extended: End-to-End Automation
Full-stack manual collection creation from scratch with complex dependencies.
* **Workflow:** `Registration` ➔ `Login` ➔ `Create Article` ➔ `Post Comment` ➔ `Delete Comment` ➔ `Delete Article`.
* **Token Management:** Extracted `tokenConduit` and `slugConduit` to automate the entire user lifecycle without manual data entry.
* [🔗 View Collection Link](https://www.postman.com/alinakuliak/workspace/postman-practice-alina-kuliak/collection/40251860-63fa10ca-fa27-4d2f-9287-1152e09b87cf?action=share&creator=40251860)

---

## 📊 Summary of Results
* **Functional Coverage:** 100% of core business flows for the Conduit application.
* **Test Automation:** All collections include automated assertions with a 100% pass rate in the Postman runner.
* **Dynamic Logic:** Zero hardcoded data in registration and authentication flows.

---
*Created by Alina Kuliak*
