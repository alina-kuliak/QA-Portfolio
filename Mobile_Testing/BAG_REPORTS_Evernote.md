# 🐘 Bug Reports: Evernote Mobile Application

This document outlines UI/UX and layout defects identified during the testing of the Evernote native app, specifically focusing on orientation changes and widget scaling.

---

## [CON-26] Account icon is partially obscured in Landscape mode
**Status:** `RESOLVED` | **Priority:** `Medium` | **Project:** `Evernote`

### 📋 Overview
When the device is rotated to landscape orientation, the account profile icon does not adjust its padding or constraints correctly, resulting in the icon being cut off by the screen edge.

| Field | Details |
| :--- | :--- |
| **Reporter** | Alina Kuliak |
| **Resolution** | Done |
| **Environment** | iPhone 11 Pro Max (iOS 18.1.1) |
| **App Version** | 10.120.1 (1233945) |
| **Links** | Relates to CON-25 (Third Mobile Test) |

### 🛠 Reproduction Steps
1. **Precondition:** Ensure system **Portrait Orientation Lock** is set to **OFF**.
2. Launch the **Evernote** app.
3. Rotate the device to **Landscape** orientation.
4. Observe the account icon located in the top-left corner of the screen.

### 🔍 Analysis
* **Expected Result:** The account icon should be fully visible and correctly positioned within the safe area of the screen.
* **Actual Result:** Only half of the account icon is visible; the rest is cut off by the left screen boundary.

### 📎 Attachments
* **Video Evidence:** [Link to Reproduction Video](https://drive.google.com/file/d/1hFpv2_0fKQl_mE-SJISzHngitlvz05jM/view?usp=sharing)

---

## [CON-27] 'Emails' tab is cut off in 'Recently Captured' widget
**Status:** `RESOLVED` | **Priority:** `Medium` | **Project:** `Evernote`

### 📋 Overview
A UI rendering issue within the "Recently Captured" widget causes the "Emails" tab to be partially invisible when selected, indicating a layout overflow or scaling bug.

| Field | Details |
| :--- | :--- |
| **Reporter** | Alina Kuliak |
| **Resolution** | Done |
| **Environment** | iPhone 11 Pro Max (iOS 18.1.1) |
| **App Version** | 10.120.1 (1233945) |
| **Component** | UI / Widgets |

### 🛠 Reproduction Steps
1. Launch the **Evernote** app.
2. Tap the **[Account Icon]** in the top-left corner.
3. Select **‘My Widgets’** from the top app bar.
4. Scroll to the **‘Recently Captured’** widget.
5. Tap on the **‘Emails’** tab on the internal tab bar.
6. Observe the visibility of the active tab.

### 🔍 Analysis
* **Expected Result:** The ‘Emails’ tab label and container should be 100% visible on the screen.
* **Actual Result:** The ‘Emails’ tab is only half-visible, appearing truncated or shifted off-canvas.

### 📎 Attachments
* **Video Evidence:** [Link to Reproduction Video](https://drive.google.com/file/d/1vTG9mtbnXoQTvTHV-QwaVKdCEWVSZoeS/view?usp=sharing)

---
*Created by Alina Kuliak — Mobile QA Portfolio (Usability & UI Focus)*
