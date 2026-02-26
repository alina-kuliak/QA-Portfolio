# 🐞 Bug Reports — Huntd Web Platform

This document logs defects identified during the web application testing cycle. Testing was conducted on **Windows 11** using **Google Chrome**.

---

### [HUN-W-001] Broken Google Play Store link on Main page
**Severity:** 🔴 Major | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Not found' page opens after clicking the 'Get it on Google Play' button on the 'Main' page. |
| **Environment** | Windows 11 | Chrome v144 | Stage |
| **Preconditions** | User is logged in. |
| **Steps** | 1. Open the main page URL. <br> 2. Click the [Get it on Google Play] button. |
| **Actual Result** | A 'Not found' 404 error page is displayed. |
| **Expected Result** | Redirect to the official Google Play store page showing app icon and details. |
| **Ref** | TC-MP-027 |

</details>

---

### [HUN-W-002] Candidates list not displayed for unauthorized users
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The candidates list is not displayed for unauthorized users on the 'Candidates' page. |
| **Environment** | Windows 11 | Chrome v144 |
| **Preconditions** | User is logged out. |
| **Steps** | 1. Open the main page URL. <br> 2. Click the 'Candidates' tab on the navigation menu. |
| **Actual Result** | The page is entirely empty; no candidate list is shown. |
| **Expected Result** | A list of candidate cards with relevant professional information should be visible. |
| **Ref** | TC-CP-029 |

</details>

---

### [HUN-W-004] Weak password validation (3 characters accepted)
**Severity:** 🔴 Major | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | User is successfully signed up using only a 3-character password. |
| **Environment** | Windows 11 | Chrome v144 |
| **Steps** | 1. Navigate to Sign Up. <br> 2. Enter valid email and a 3-char password (e.g., 's12'). <br> 3. Click [Create account]. |
| **Actual Result** | Registration proceeds; no validation error is triggered. |
| **Expected Result** | System rejects the password; validation error is displayed; user remains on Sign Up page. |
| **Ref** | TC-SU-101 |

</details>

---

### [HUN-W-005] Numeric values accepted in 'My role' field (Recruiter)
**Severity:** 🔴 Major | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | System accepts numeric input in the 'My role' field during recruiter registration. |
| **Environment** | Windows 11 | Chrome v144 |
| **Steps** | 1. Enter numbers in 'My role' (e.g., '12'). <br> 2. Enter valid company name. <br> 3. Click [Save and continue]. |
| **Actual Result** | No error shown; user proceeds to 'Contact information' page. |
| **Expected Result** | Validation error displayed for the 'My role' field; navigation prevented. |
| **Ref** | TC-SR-115 |

</details>

---

### [HUN-W-006] Mixed alphabet validation failure (Cyrillic/Latin)
**Severity:** 🔴 Major | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | System allows registration when 'First Name' and 'Last Name' use different alphabets. |
| **Environment** | Windows 11 | Chrome v144 |
| **Steps** | 1. Enter First Name in Cyrillic (e.g., Іван). <br> 2. Enter Last Name in Latin (e.g., Ivanenko). <br> 3. Click [Save and continue]. |
| **Actual Result** | User proceeds to the next page without a validation error. |
| **Expected Result** | System should flag inconsistent alphabet use or enforce specific character sets; validation message shown. |
| **Ref** | TC-SR-123 |

</details>

---

### [HUN-W-007] Numeric values accepted in 'First Name' field
**Severity:** 🔴 Major | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | User is continuing recruiter registration after entering numeric values in the 'First Name' field on the 'Contact information' page. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | 1. User is on 'Contact Information' form. <br> 2. **Test Data:** First Name: `007`, Last Name: `Ivanenko`. |
| **Steps** | 1. Enter numeric values in the 'First Name' field. <br> 2. Enter a valid last name. <br> 3. Click the [Save and continue] button. |
| **Actual Result** | The 'Let's find your first engineers!' page is displayed. <br> User proceeds without a validation error. |
| **Expected Result** | User is not able to continue. <br> The validation message is shown. <br> The 'Contact Information' form is displayed. |
| **Ref / Video** | **Test Case:** TC-SR-124 <br> **Link:** [Video Evidence](https://www.veed.io/view/edbd8102-a5c7-403d-82ad-db060085213d?source=editor&panel=share) |

</details>

---

### [HUN-W-008] Numeric values accepted in 'Last Name' field
**Severity:** 🔴 Major | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | User is continuing recruiter registration after entering numeric values in the 'Last Name' field on the 'Contact information' page. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | 1. User is on 'Contact Information' form. <br> 2. **Test Data:** First Name: `Ivan`, Last Name: `007`. |
| **Steps** | 1. Enter a valid first name. <br> 2. Enter numeric values in the 'Last Name' field. <br> 3. Click the [Save and continue] button. |
| **Actual Result** | The 'Let's find your first engineers!' page is displayed. <br> User proceeds without a validation error. |
| **Expected Result** | User is not able to continue. <br> The validation message is shown. <br> The 'Contact Information' form is displayed. |
| **Ref / Video** | **Test Case:** TC-SR-125 <br> **Link:** [Video Evidence](https://www.veed.io/view/f1feef4b-f1c7-49b7-abba-36e4ecce8896?source=editor&panel=share) |

</details>

---

### [HUN-W-009] Missing validation for invalid 'Wallet Address'
**Severity:** 🟡 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The error message is not displayed after entering an invalid wallet address in the 'Wallet Address' field. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | **Test Data:** First Name: `Ivan`, Last Name: `Ivaniuk`, Wallet address: `123`. |
| **Steps** | 1. Fill valid First/Last names. <br> 2. Enter an invalid Wallet format (`123`). <br> 3. Click the [Save and continue] button. |
| **Actual Result** | The validation message is not displayed for the 'Wallet Address' field. <br> The 'Contact information' page is displayed. |
| **Expected Result** | The validation error message is displayed for the 'Wallet Address' field. <br> The 'Contact Information' form remains displayed. |
| **Attachments** | **Screenshot:** [View Link](https://1drv.ms/i/c/6f70d9b489838b4f/IQC2z-8UFmtNQaukP086KYD4AfsQNDQjafzajgSAYqD0zPU?e=ZVRfKT) <br> **Video:** [View Link](https://www.veed.io/view/47c56d18-4620-4207-9d52-e5dbb7389f13?source=editor&panel=share) |
| **Ref** | TC-SR-128 |

</details>

---

### [HUN-W-010] 'Role' field is not mandatory
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Reach out to matching engineers' form is displayed after leaving the 'Role' field empty on the 'Perfect candidate' page. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Steps** | 1. Leave the 'Role' field empty. <br> 2. Fill all other required fields. <br> 3. Click [Next]. |
| **Actual Result** | The [Next] button is active. <br> The 'Reach out to matching engineers' form is displayed. |
| **Expected Result** | The [Next] button is inactive. <br> The 'Perfect candidate' page is displayed. |
| **Ref / Video** | **Test Case:** TC-PC-134 <br> **Link:** [Video Evidence](https://www.veed.io/view/c38cbe79-1fc9-4171-afc8-f84c9b2045be?source=editor&panel=share) |

</details>

---

### [HUN-W-011] 'Technologies' field is not mandatory
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Reach out to matching engineers' form is displayed after leaving the 'Technologies' field empty on the 'Perfect candidate' page. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Steps** | 1. Leave the 'Technologies' field empty. <br> 2. Fill all other required fields. <br> 3. Click [Next]. |
| **Actual Result** | The [Next] button is active. <br> The 'Reach out to matching engineers' form is displayed. |
| **Expected Result** | The [Next] button is inactive. <br> The 'Perfect candidate' page is displayed. |
| **Ref / Video** | **Test Case:** TC-PC-135 <br> **Link:** [Video Evidence](https://www.veed.io/view/0daed419-b687-481d-8dc9-bc47d82c0189?source=editor&panel=share) | 

</details> 

--- 

### [HUN-W-012] 'Salary period' field is not mandatory 
**Severity:** 🟠 Moderate | **Priority:** Medium 

<details> 
<summary>View Full Report Details</summary> 

| Field | Description | 
| :--- | :--- | 
| **Summary** | The 'Reach out to matching engineers' form is displayed after leaving the 'Salary period' field empty on the 'Perfect candidate' page. | 
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage | 
| **Steps** | 1. Leave the 'Salary period' field empty. <br> 2. Fill all other required fields. <br> 3. Click [Next]. | 
| **Actual Result** | The [Next] button is active. <br> The 'Reach out to matching engineers' form is displayed. | 
| **Expected Result** | The [Next] button is inactive. <br> The 'Perfect candidate' page is displayed. | 
| **Ref / Video** | **Test Case:** TC-PC-136 <br> **Link:** [Video Evidence](https://www.veed.io/view/fd67df24-3778-4899-aed9-8d8ad49ca140?source=editor&panel=share) | 

</details>

---

### [HUN-W-013] 'Job experience' field is not mandatory
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Reach out to matching engineers' form is displayed after leaving the 'Job experience' field empty on the 'Perfect candidate' page. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | User continues registration as a recruiter. The 'Perfect candidate' page is displayed. |
| **Steps** | 1. Leave the 'Job experience' field empty. <br> 2. Fill all other required fields. <br> 3. Click [Next]. |
| **Actual Result** | The [Next] button is active. <br> The 'Reach out to matching engineers' form is displayed. |
| **Expected Result** | The [Next] button is inactive. <br> The 'Perfect candidate' page is displayed. |
| **Ref / Video** | **Test Case:** TC-PC-137 <br> **Link:** [Video Evidence](Video_HUN_W_013) |

</details>

---

### [HUN-W-014] 'English Level' field is not mandatory
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Reach out to matching engineers' form is displayed after leaving the 'English Level' field empty on the 'Perfect candidate' page. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Steps** | 1. Leave the 'English Level' field empty. <br> 2. Fill all other required fields. <br> 3. Click [Next]. |
| **Actual Result** | The [Next] button is active. <br> The 'Reach out to matching engineers' form is displayed. |
| **Expected Result** | The [Next] button is inactive. <br> The 'Perfect candidate' page is displayed. |
| **Ref / Video** | **Test Case:** TC-PC-138 <br> **Link:** [Video Evidence](Video_HUN_W_014) |

</details>

---

### [HUN-W-015] 'Location type' field is not mandatory
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Reach out to matching engineers' form is displayed after leaving the 'Location type' field empty on the 'Perfect candidate' page. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Steps** | 1. Leave the 'Location type' field empty. <br> 2. Fill all other required fields. <br> 3. Click [Next]. |
| **Actual Result** | The [Next] button is active. <br> The 'Reach out to matching engineers' form is displayed. |
| **Expected Result** | The [Next] button is inactive. <br> The 'Perfect candidate' page is displayed. |
| **Ref / Video** | **Test Case:** TC-PC-139 <br> **Link:** [Video Evidence](Video_HUN_W_015) |

</details>

---

### [HUN-W-016] 'Role' field is not fully clickable
**Severity:** 🟡 Minor | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Role' field is not clickable in the whole field area in the 'Add manually' form. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | User continues registration as a candidate. The 'Experience' form is displayed. |
| **Steps** | 1. Click on the [Add manually] button. <br> 2. Click on the 'Role' field area (not just the edge). |
| **Actual Result** | The 'Role' field is clickable only at the end (edge) of the field. |
| **Expected Result** | The whole 'Role' field is clickable. <br> The field changes to an entry mode upon clicking anywhere inside. |
| **Ref / Video** | **Test Case:** TC-SC-180 <br> **Link:** [Video Evidence](Video_HUN_W_016) |

</details>

---

### [HUN-W-017] Experience saved with empty 'End Date' month
**Severity:** 🟡 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The experience is saved with an empty End Date month in the 'Add manually' form after activating the 'End date' experience toggle. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Steps** | 1. Click [Add manually]. <br> 2. Fill Role, Company, Start Month, Start Year. <br> 3. Activate 'End date' toggle. <br> 4. Leave 'Month' empty but enter 'End Year'. <br> 5. Fill Achievements and click [Save]. |
| **Actual Result** | The experience form is saved with the 'current time' as End date month. |
| **Expected Result** | The validation message 'End date is required' is displayed. <br> The form is not saved until the month is selected. |
| **Ref / Video** | **Test Case:** TC-SC-185 <br> **Link:** [Video Evidence](Video_HUN_W_017) |

</details>

---

### [HUN-W-018] Start year field allows future year data
**Severity:** 🔴 Major | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The start year field allows entering and saving future year data in the 'Add manual' experience form. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Steps** | 1. Click [Add manually]. <br> 2. Enter Role, Company, and Start month. <br> 3. Enter a **future year** (e.g., 2030) in the 'Start year' field. <br> 4. Click the [Save] button. |
| **Actual Result** | The experience form was saved without validation. <br> The [Save and Continue] button becomes active. |
| **Expected Result** | The 'Add manually' form is not saved. <br> A validation message (e.g., "Year cannot be in the future") is displayed. |
| **Attachments** | **Screenshot:** [View Link](Screenshot_HUN_W_018) <br> **Video:** [View Link](Video_HUN_W_018) |
| **Ref** | TC-SC-186 |

</details>

---

### [HUN-W-019] Missing validation for 'Wallet Address' (Candidate)
**Severity:** 🟡 Minor | **Priority:** Low

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The error message is not displayed after entering an invalid wallet address in the 'Wallet Address' field for candidates. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | User continues registration as a candidate. <br> **Test Data:** First Name: `Ivan`, Last Name: `Ivaniuk`, Wallet: `123`. |
| **Steps** | 1. Enter First and Last names. <br> 2. Enter invalid Wallet format (`123`). <br> 3. Click the [Activate profile] button. |
| **Actual Result** | Validation message is not displayed. The 'Contact information' page remains active without feedback. |
| **Expected Result** | The 'Contact Information' form displays a validation error message for the 'Wallet Address' field. |
| **Attachments** | **Screenshot:** [View Link](Screenshot_HUN_W_019) <br> **Video:** [View Link](Video_HUN_W_019) |
| **Ref** | TC-SC-199 |

</details>

---

### [HUN-W-020] Reset password link not sent to email
**Severity:** 🔴 Critical | **Priority:** High

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The reset password link is not sent to the registered email after clicking the [Send] button on the 'Forgot password' page. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | User is logged out and is on the 'Forgot password' page. |
| **Steps** | 1. Enter an existing email in the 'Email' field. <br> 2. Click on the [Send code] button. <br> 3. Check 'Primary' and 'Spam' folders in the inbox. |
| **Actual Result** | No reset email received, although the confirmation message is displayed on the UI. |
| **Expected Result** | The reset link/code is successfully delivered to the user's inbox. |
| **Attachments** | **Video:** [View Link](Video_HUN_W_020) |
| **Ref** | TC-SN-208 |

</details>

---

### [HUN-W-021] 'Favourite' option missing in Chat (Recruiter)
**Severity:** 🔴 Major | **Priority:** High

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Mark as Favourite' option is not displayed for the recruiter in the chat kebab menu. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | Recruiter is logged in, has an active chat, and is on the 'Chats' page. |
| **Steps** | 1. Click on the kebab menu (three dots) on the chat. <br> 2. Look for the [Favourite] button. |
| **Actual Result** | The 'Favourite' option is not displayed in the menu. |
| **Expected Result** | The 'Favourite' option is available and marks the chat accordingly. |
| **Attachments** | **Screenshot:** [View Link](Screenshot_HUN_W_021) <br> **Video:** [View Link](Video_HUN_W_021) |
| **Ref** | TC-CH-242 |

</details>

---

### [HUN-W-022] Vacancies list opens in the same tab (Logo click)
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The vacancies list of the company opens in the same tab instead of a new one after clicking on the company logo. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | User is on the 'Web3-companies' page. |
| **Steps** | 1. Click on a company logo. |
| **Actual Result** | The specific vacancy list for that company is opened on the same browser tab. |
| **Expected Result** | A new browser tab opens leading to the specific vacancy list for that company. |
| **Attachments** | **Video:** [View Link](Video_HUN_W_022) |
| **Ref** | TC-WP-273 |

</details>

---

### [HUN-W-023] Vacancies list not opened via Company Name
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The vacancies list of the company does not open at all after clicking on the company name. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Steps** | 1. Navigate to 'Web3-companies' page. <br> 2. Click on a company name. |
| **Actual Result** | Nothing happens; the 'Web3-companies' list remains displayed. |
| **Expected Result** | A new browser tab opens leading to the specific vacancy list for that company. |
| **Attachments** | **Video:** [View Link](Video_HUN_W_023) |
| **Ref** | TC-WP-274 |

</details>

---

### [HUN-W-024] Job listing opens in the same tab (Icon click)
**Severity:** 🟠 Moderate | **Priority:** Medium

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | User stays on the same tab after clicking the company icon, which replaces the current page with job listings. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Steps** | 1. Click on a company icon/logo on the 'Web3-companies' page. |
| **Actual Result** | The company's job listing opens in the current tab. |
| **Expected Result** | The job listing opens in a new browser tab to keep the main list accessible. |
| **Attachments** | **Video:** [View Link](Video_HUN_W_024) |
| **Ref** | TC-WP-278 |

</details>

---

### [HUN-W-025] 'Favourite' option missing in Chat (Candidate)
**Severity:** 🔴 Major | **Priority:** High

<details>
  <summary>View Full Report Details</summary>

| Field | Description |
| :--- | :--- |
| **Summary** | The 'Mark as Favourite' option is not displayed for the candidate in the chat kebab menu. |
| **Environment** | **OS:** Windows 11 Home <br> **Browser:** Chrome v144.0.7559.133 <br> **Version:** Stage |
| **Preconditions** | Candidate is logged in, has an active chat, and is on the 'Chats' page. |
| **Steps** | 1. Click on the kebab menu on the chat. <br> 2. Look for the [Favourite] option. |
| **Actual Result** | The Favourite option is not displayed. |
| **Expected Result** | Chat can be marked as Favourite via the menu. |
| **Attachments** | **Screenshot:** [View Link](Screenshot_HUN_W_025) <br> **Video:** [View Link](Video_HUN_W_025) |
| **Ref** | TC-CH-242 |

</details>
