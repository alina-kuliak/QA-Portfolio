# 🛠️ Bug Reports: Handyman App (Technical Debugging)

This document details critical functional defects identified in the Handyman application. These reports include technical evidence captured via **Android Studio Logcat** to assist in Root Cause Analysis.

---

## [CON-31] Registration via Google fails to redirect the user
**Status:** `To Do` | **Priority:** `Medium` | **Project:** `Handyman`

### 📋 Overview
The "Sign up with Google" functionality is non-responsive. Tapping the button does not initiate the OAuth flow or redirect the user, effectively blocking third-party registration.

| Field | Details |
| :--- | :--- |
| **Reporter** | Alina Kuliak |
| **Environment** | Emulator: Pixel 3 API 35 (Android 15.0) |
| **App Version** | Demo (com.call4site.handymanservices) |
| **Technical Evidence** | Logcat (Logs_1.txt) |

### 🛠 Reproduction Steps
1. Launch the **Handyman** app in Android Studio Emulator.
2. Navigate to the **Registration** page.
3. Tap the **[Google]** button.
4. Observe the UI behavior and monitor Logcat output.

### 🔍 Analysis
* **Expected Result:** The app should redirect the user to the Google Account selection screen/OAuth provider.
* **Actual Result:** The user remains on the registration page with no visual feedback or redirection.

### 📎 Technical Attachments
* **Logs:** [Logs_1.txt](https://drive.google.com/file/d/1TzCNxOnsmN7k6Bdc4Fep9nylr7t-MbYQ/view?usp=sharing)
* **Video Evidence:** [Link to Reproduction Video](https://drive.google.com/file/d/1WbjKY5yFObFj0QD8eKJWfK6YEUzLc9MG/view?usp=sharing)

---

## [CON-32] Registration via Facebook fails to redirect the user
**Status:** `To Do` | **Priority:** `Medium` | **Project:** `Handyman`

### 📋 Overview
Similar to the Google integration issue, the Facebook SDK integration appears to be failing or unlinked, preventing users from registering via their Facebook profiles.

| Field | Details |
| :--- | :--- |
| **Reporter** | Alina Kuliak |
| **Environment** | Emulator: Pixel 3 API 35 (Android 15.0) |
| **App Version** | Demo (com.call4site.handymanservices) |
| **Technical Evidence** | Logcat (Logs_2.txt) |

### 🛠 Reproduction Steps
1. Launch the **Handyman** app.
2. Navigate to the **Registration** page.
3. Tap the **[Facebook]** button.
4. Observe the result and check for specific "onClick" errors in Android Studio.

### 🔍 Analysis
* **Expected Result:** The user should be redirected to the Facebook login/authorization page.
* **Actual Result:** The application remains static on the registration screen.

### 📎 Technical Attachments
* **Logs:** [Logs_2.txt](https://drive.google.com/file/d/1dYgCCPxFI_TL-ww4f4rAvqk-FQAOHaJ6/view?usp=sharing)
* **Video Evidence:** [Link to Reproduction Video](https://drive.google.com/file/d/1aYveWixMjBj_LWX0NbLGNjo9L2ldfZRE/view?usp=sharing)

---
*Created by Alina Kuliak — QA Portfolio (Android Studio & Logcat Focus)*
