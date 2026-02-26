# 🐞 Bug Reports: IMDb Mobile Application

This document contains detailed bug reports identified during the functional testing of the IMDb Native Mobile App.

---

## [CON-23] App opens without content/error message when offline
**Status:** `TO DO` | **Priority:** `Medium` | **Project:** `Conduit`

### 📋 Overview
The application fails to provide user feedback (validation messages) when launched without an active internet connection, leading to a blank UI state.

| Field | Details |
| :--- | :--- |
| **Reporter** | Alina Kuliak |
| **Component** | Functional / Network |
| **Environment** | iPhone 11 Pro Max (iOS 18.1.1) |
| **App Version** | 15.3 |
| **Sprint** | SCRUM Sprint 1 |

### 🛠 Reproduction Steps
1. **Precondition:** Ensure the device's internet connection (Wi-Fi and Mobile Data) is turned **OFF**.
2. Tap the **IMDb app icon** to launch the application.
3. Scroll down the main landing page.
4. Tap through various navigation tabs (Search, Video, Profile).

### 🔍 Analysis
* **Expected Result:** A clear validation message should appear, such as: *“Please check your connection again or connect to Wi-Fi.”*
* **Actual Result:** The app opens to a blank state with no content and no error/validation messages.

### 📎 Attachments
* **Video Evidence:** [Link to Reproduction Video]

---

## [CON-24] UI fails to rotate to landscape after disabling orientation lock
**Status:** `TO DO` | **Priority:** `Medium` | **Project:** `Conduit`

### 📋 Overview
The application page orientation remains stuck in portrait mode even after the system-level portrait orientation lock is disabled and the device is rotated.

| Field | Details |
| :--- | :--- |
| **Reporter** | Alina Kuliak |
| **Component** | UI/UX / Compatibility |
| **Environment** | iPhone 11 Pro Max (iOS 18.1.1) |
| **App Version** | 15.3 |
| **Links** | Relates to CON-22 |

### 🛠 Reproduction Steps
1. **Precondition:** System **Portrait Orientation Lock** is set to **ON**.
2. Launch the IMDb app.
3. Tap on the first recommended video at the top of the home screen.
4. Swipe down to open the **Control Center**.
5. Set **Portrait Orientation Lock** to **OFF**.
6. Flip the phone to a horizontal (landscape) position.
7. Close the video and observe the main page orientation.

### 🔍 Analysis
* **Expected Result:** The application UI should dynamically transition to landscape orientation to match the device positioning.
* **Actual Result:** The app’s page orientation remains fixed in portrait mode and does not respond to device rotation.

### 📎 Attachments
* **Video Evidence:** [Link to Reproduction Video]

---
*Created by Alina Kuliak — Mobile QA Portfolio*
