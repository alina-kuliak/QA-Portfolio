# 🐞 Bug Reports — Huntd Mobile (iOS)

This document contains a detailed log of defects identified during the testing of the Huntd MVP on iOS.

---

### [HUN-M-001] Password reset email not sent
**Severity:** 🔴 Critical | **Priority:** High

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The email with a link to reset the password is not sent after clicking [Send code]. |
| **Environment** | iOS 18.3.2 | iPhone 11 Pro Max | App MVP |
| **Preconditions** | User is logged out; 'Sign In' screen displayed; Email already exists in system. |
| **Steps** | 1. Tap 'Forgot password?' <br> 2. Enter valid email <br> 3. Tap [Send Code] <br> 4. Check email. |
| **Actual Result** | Confirmation message shows, but no email is ever received (checked Primary/Spam). |
| **Expected Result** | User receives an email containing the password reset link. |
| **Test Case Ref** | TC-M-SI-016 |

</details>

---

### [HUN-M-002] 'Undefined' error on Sign Up with no connection
**Severity:** 🟡 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | 'Undefined' error message displayed instead of network error when internet is disabled. |
| **Environment** | iOS 18.3.2 | iPhone 11 Pro Max |
| **Steps** | 1. Navigate to Sign Up <br> 2. Enter valid details <br> 3. Disable internet <br> 4. Tap [Sign Up]. |
| **Actual Result** | Email field shows "Undefined"; no system network error message appears. |
| **Expected Result** | Process fails gracefully with a clear "No Internet Connection" message. |
| **Test Case Ref** | TC-M-SU-026 |

</details>

---

### [HUN-M-003] Weak password validation (2 characters accepted)
**Severity:** 🟠 Medium | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | User is successfully signed up using only a 2-character password. |
| **Steps** | 1. Enter email <br> 2. Enter "12" in password and repeat password <br> 3. Tap [Create account]. |
| **Actual Result** | User is redirected to 'Chats' screen; account is created. |
| **Expected Result** | System should reject passwords shorter than the required minimum (e.g., 8 chars). |
| **Test Case Ref** | TC-M-SU-034 |

</details>

---

### [HUN-M-004] Autologin via Google without "Existing Account" notice
**Severity:** 🔵 Minor | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | Existing user is signed in via Google without notification that account already exists. |
| **Actual Result** | Redirected directly to Home screen; no clarification provided. |
| **Expected Result** | Notify user: “An account with this Google account already exists. Please log in.” |
| **Test Case Ref** | TC-M-SU-035 |

### [HUN-M-006] No network error when sending chat message offline
**Severity:** 🔵 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | No network error message or retry option displayed when internet is lost while sending a message. |
| **Environment** | iOS 18.3.2 | iPhone 11 Pro Max |
| **Steps** | 1. Type a message <br> 2. Disable internet <br> 3. Tap [Send]. |
| **Actual Result** | The message vanishes (does not appear in chat); no error or retry button is shown. |
| **Expected Result** | Message fails to send; user sees "No internet connection" and a retry option. |
| **Test Case Ref** | TC-M-CH-039 |

</details>

---

### [HUN-M-007] Keyboard overlaps 'Share contact' button
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | Keyboard blocks the [Share contact information] button after clicking on the input field. |
| **Environment** | iOS 18.3.2 | iPhone 11 Pro Max |
| **Steps** | 1. Open a chat <br> 2. Tap input field (keyboard appears) <br> 3. Tap kebab menu. |
| **Actual Result** | The keyboard covers the [Share contact information] button, making it inaccessible. |
| **Expected Result** | The UI should adjust/scroll so the button is visible above or handled properly with the keyboard. |
| **Test Case Ref** | TC-M-CH-040 |

</details>

---

### [HUN-M-008] Missing validation for 'First Name' field (Numeric values)
**Severity:** 🔵 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | System accepts numeric characters in the 'First Name' field without validation error. |
| **Environment** | iOS 18.3.2 | iPhone 11 Pro Max |
| **Steps** | 1. Enter numbers in 'First Name' field <br> 2. Enter valid Last Name <br> 3. Tap [Save and Continue]. |
| **Actual Result** | No validation error; system accepts numeric data and proceeds with registration. |
| **Expected Result** | Error message shown; field highlighted; user prevented from proceeding with invalid name data. |
| **Test Case Ref** | TC-M-PI-069 |

</details>

---
### [HUN-M-009] Local UI reflects saved profile changes during network failure
**Severity:** 🔵 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | Profile changes appear to be saved in the UI even when the network connection fails during the save process. |
| **Environment** | iOS 18.3.2 | iPhone 11 Pro Max |
| **Preconditions** | User is on the "Edit Profile" tab. |
| **Steps** | 1. Edit 'Desired position' <br> 2. Disable internet <br> 3. Tap [Save and Continue]. |
| **Actual Result** | No error message; UI reflects updated value locally, giving a false impression of a successful backend save. |
| **Expected Result** | Error message displayed; UI should not reflect changes that weren't confirmed by the server. |
| **Test Case Ref** | TC-M-PI-077 |

</details>

---

### [HUN-M-010] No network error notification during profile save
**Severity:** 🔵 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | No network error notification displayed when connection is lost during profile save. |
| **Steps** | 1. Edit profile <br> 2. Disable internet <br> 3. Tap [Save]. |
| **Actual Result** | No error message; UI fails to inform the user that the data was not sent. |
| **Expected Result** | Clear message: "No internet connection. Please check your network and try again" with a retry option. |
| **Test Case Ref** | TC-M-PI-082 |

</details>

---

### [HUN-M-011] Maximum Tech Skills limit (15) is not enforced
**Severity:** 🔵 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | User is able to select and save 16 Tech Skills, exceeding the limit of 15. |
| **Steps** | 1. Navigate to Tech Skills <br> 2. Select 16 skills <br> 3. Tap [Save and Continue]. |
| **Actual Result** | System accepts 16 skills; no validation message is shown. |
| **Expected Result** | Selection restricted to 15; additional skills should be greyed out; validation message shown. |
| **Test Case Ref** | TC-M-PC-087 |

</details>

---

### [HUN-M-012] Navigation failure on "Expectation" screen after valid data entry
**Severity:** 🔴 Critical | **Priority:** High

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | User stays on the Expectation screen even after clicking [Save and Continue] with valid data. |
| **Actual Result** | Location field clears itself; user remains on the same screen; no navigation to "Experience" occurs. |
| **Expected Result** | Data is saved and user is redirected to the "Experience" screen. |
| **Test Case Ref** | TC-M-PC-090 |

</details>

---

### [HUN-M-013] Missing [Edit] button on Preview Profile screen
**Severity:** 🔴 Critical | **Priority:** High

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The [Edit] button is missing from the 'Preview profile' screen, preventing user modifications. |
| **Actual Result** | Page is displayed, but there is no way for the user to initiate an edit. |
| **Expected Result** | [Edit] button should be clearly displayed at the bottom of the screen. |
| **Test Case Ref** | TC-M-PR-110 |

</details>
