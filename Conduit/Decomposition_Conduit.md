# 📂 Functional Decomposition: Conduit App

## 📝 Overview
This document contains a comprehensive functional decomposition of the **Conduit** blogging platform. The goal of this analysis was to break down the application into high-level modules and low-level components to ensure 100% test coverage for both **Guest** and **Authorized** user states.

---

## 👤 1. Guest User State (Logged Out)
*Analysis of features accessible to public users.*

### **1.1 Home Page**
* **Global Feed**
    * Article preview (Title, Description, Tags)
    * Author "User profile" link
    * [Like] button (Interaction check)
* **Popular Tags Section**
    * Individual Tag filtering links

### **1.2 Authentication**
* **Sign In Page**
    * "Sign in" form (Email/Password fields)
    * [Sign in] button
    * Navigation link: "Need an account?"
* **Sign Up Page**
    * "Sign up" form (Username/Email/Password fields)
    * [Sign up] button
    * Navigation link: "Have an account?"

### **1.3 Article View**
* **Header Actions:** Profile link, Follow button, Favorite button.
* **Content:** Full article text and associated tags.
* **Comments:** Display-only view of existing comments and metadata.

### **1.4 Public User Profile**
* **Banner:** User icon and Username display.
* **Feeds:** Tabs for "My posts" and "Favorite posts" previews.

---

## 🔐 2. Authorized User State (Logged In)
*Analysis of features requiring JWT authentication.*

### **2.1 Enhanced Home Page**
* **Your Feed:** Personalized tab for followed authors.
* **Global Feed:** Full interactive article previews.

### **2.2 Content Creation (New Article)**
* **"Create an article" Form**
    * Input fields: Title, About, Content (Markdown textarea).
    * Tag entry system.
    * [Publish Article] submission.

### **2.3 User Settings**
* **Profile Management**
    * Fields: Profile picture URL, Username, Bio, Email, Password.
    * [Update Settings] action.
* **Session Management**
    * [Logout] functionality.

### **2.4 Personal Profile (Owner View)**
* **Header:** Dynamic "Edit profile settings" navigation.
* **Post Management:** Personal post list and saved favorite posts.

### **2.5 Advanced Article Actions**
* **Author Controls:** [Edit Article] and [Delete Article] buttons (Conditional visibility).
* **Interactive Comments**
    * **New Comment Form:** Textarea and [Post Comment] button.
    * **Comment Management:** [Delete] button for user-owned comments.

---

## 🛠 Usage in Testing
This decomposition serves as the foundation for:
1.  **Test Case Design:** Every bullet point above corresponds to at least one functional test case.
2.  **RTM (Requirements Traceability Matrix):** Mapping features to automated Postman API tests.
3.  **Boundary Value Analysis:** Applied to all form fields (Settings, Sign Up, New Article).

---
*Prepared by: Alina Kuliak*
