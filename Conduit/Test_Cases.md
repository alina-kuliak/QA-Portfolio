# 🧪 Test Cases: Authentication & Registration (Conduit)

## 📝 Overview
This document contains a detailed list of test cases for the **Sign In** and **Sign Up** modules of the Conduit application. These cases cover functional requirements, UI elements, navigation, and negative testing scenarios (validation messages).

---

## 🛠 Test Case Repository

| ID | Title | Priority | Section | Suite |
| :--- | :--- | :--- | :--- | :--- |
| **C520** | The 'Sign In' page contains a 'Need an account?' link | Low | Sign In page | Master |
| **C521** | Redirect to 'Sign up' page via 'Need an account?' link | Medium | Sign In page | Master |
| **C522** | The 'Sign In' page contains a 'Sign In' form | Critical | Sign In page | Master |
| **C523** | The 'Sign In' page contains a 'Forgot password?' link | Medium | Sign In page | Master |
| **C524** | Redirect to 'Forgot password' page via link | Medium | Sign In page | Master |
| **C525** | Redirect to 'User page' after direct link access | Medium | Sign In page | Master |
| **C519** | 'Sign In' page opens via Navigation Bar | High | Sign In page | Master |
| **C526** | Form contains field for Email or Username | High | ‘’Sign in’’ form | Master |
| **C527** | Form contains 'Password' field | Medium | ‘’Sign in’’ form | Master |
| **C528** | Form contains [Sign in] button | High | ‘’Sign in’’ form | Master |
| **C529** | Successful login via [Sign in] button | Critical | ‘’Sign in’’ form | Master |
| **C530** | Successful login via [Enter] key | Medium | ‘’Sign in’’ form | Master |
| **C538** | Validation: Non-registered Email | Medium | ‘'Email or Username’' | Master |
| **C537** | Validation: Non-registered Username | Medium | ‘'Email or Username’' | Master |
| **C536** | Validation: Empty Email/Username field | Low | ‘'Email or Username’' | Master |
| **C535** | Case-insensitivity check for Email/Username | Medium | ‘'Email or Username’' | Master |
| **C533** | Login with registered Email | Critical | ‘'Email or Username’' | Master |
| **C532** | Login with registered Username | Critical | ‘'Email or Username’' | Master |
| **C531** | Login blocked without Email/Username | Critical | ‘'Email or Username’' | Master |
| **C534** | Check 'Enter your username or email' placeholder | Medium | ‘'Email or Username’' | Master |
| **C546** | Validation: Invalid password error message | Medium | ‘‘Password’’ field | Master |
| **C545** | Redirect to 'Forgot password' from error message link | Medium | ‘‘Password’’ field | Master |
| **C544** | Validation: Empty Password field | Medium | ‘‘Password’’ field | Master |
| **C543** | Ability to paste data into Password field | Medium | ‘‘Password’’ field | Master |
| **C542** | Security: Cannot 'Cut' from Password field | Medium | ‘‘Password’’ field | Master |
| **C541** | Security: Cannot 'Copy' from Password field | Medium | ‘‘Password’’ field | Master |
| **C540** | Security: Password field covered by asterisks | Medium | ‘‘Password’’ field | Master |
| **C539** | Login blocked without Password | Critical | ‘‘Password’’ field | Master |
| **C547** | 'Sign Up' page opens via Navigation Bar | High | Sign Up page | Master |
| **C548** | Account creation via [Sign Up] button | Critical | Sign Up page | Master |
| **C549** | Account creation via [Enter] key | High | Sign Up page | Master |
| **C550** | Verification email sent after registration | Critical | Sign Up page | Master |
| **C551** | Email contains 6-digit verification code | Critical | Sign Up page | Master |
| **C552** | Redirect to 'Finish Registration' page | Critical | Sign Up page | Master |
| **C553** | 'Finish Registration' contains 6-digit code field | Critical | Sign Up page | Master |
| **C554** | Ability to enter code and click [Confirm] | Critical | Sign Up page | Master |
| **C555** | Redirect to 'Sign In' via 'Have an account?' link | Medium | Sign Up page | Master |
| **C556** | Sign up form contains 'Username' field | Critical | ‘’Sign up’’ form | Master |
| **C559** | Sign up form contains 'Confirm password' field | Critical | ‘’Sign up’’ form | Master |
| **C557** | Sign up form contains 'Email' field | Critical | ‘’Sign up’’ form | Master |
| **C558** | Sign up form contains 'Password' field | Critical | ‘’Sign up’’ form | Master |
| **C568** | Username accepts digits | Medium | ‘‘Username’’ field | Master |
| **C573** | Username case-sensitivity conflict check | Medium | ‘‘Username’’ field | Master |
| **C572** | Validation: Invalid Username format | Medium | ‘‘Username’’ field | Master |
| **C571** | Validation: Username already taken | Medium | ‘‘Username’’ field | Master |
| **C570** | Security: Username rejects non-printing symbols | High | ‘‘Username’’ field | Master |
| **C569** | Security: Username rejects special characters | High | ‘‘Username’’ field | Master |
| **C567** | Username must start with Latin letter | High | ‘‘Username’’ field | Master |
| **C566** | Username accepts Latin letters | High | ‘‘Username’’ field | Master |
| **C565** | Boundary: Username 41 chars (Invalid) | High | ‘‘Username’’ field | Master |
| **C564** | Boundary: Username 40 chars (Valid) | High | ‘‘Username’’ field | Master |
| **C563** | Boundary: Username 3 chars (Valid) | Critical | ‘‘Username’’ field | Master |
| **C562** | Boundary: Username 2 chars (Invalid) | High | ‘‘Username’’ field | Master |
| **C561** | Prevent duplicate Username registration | Critical | ‘‘Username’’ field | Master |
| **C560** | Registration blocked without Username | High | ‘‘Username’’ field | Master |
| **C576** | Email format validation (name@domain.top) | Critical | ‘‘Email’’ field | Master |
| **C581** | Validation: Non-valid email error | Medium | ‘‘Email’’ field | Master |
| **C580** | Validation: Email already taken | Medium | ‘‘Email’’ field | Master |
| **C579** | Email name accepts: +, -, _, . | Medium | ‘‘Email’’ field | Master |
| **C578** | Email name accepts digits | Medium | ‘‘Email’’ field | Master |
| **C577** | Email name accepts Latin letters | High | ‘‘Email’’ field | Master |
| **C575** | Prevent duplicate Email registration | High | ‘‘Email’’ field | Master |
| **C574** | Registration blocked without Email | Critical | ‘‘Email’’ field | Master |
| **C582** | Registration blocked without Password | Critical | ‘‘Password’’ field | Master |
| **C583** | Boundary: Password 7 chars (Invalid) | High | ‘‘Password’’ field | Master |
| **C584** | Boundary: Password 8 chars (Valid) | Critical | ‘‘Password’’ field | Master |
| **C585** | Boundary: Password 30 chars (Valid) | Critical | ‘‘Password’’ field | Master |
| **C586** | Boundary: Password 31 chars (Invalid) | High | ‘‘Password’’ field | Master |
| **C587** | Security: Password rejects non-printing symbols | High | ‘‘Password’’ field | Master |
| **C588** | Complexity: Password requires special character | High | ‘‘Password’’ field | Master |
| **C589** | Complexity: Password requires digits | High | ‘‘Password’’ field | Master |
| **C590** | Complexity: Password requires capital letters | High | ‘‘Password’’ field | Master |
| **C591** | Validation: Passwords must match | High | ‘‘Password’’ field | Master |
| **C592** | Registration blocked without Password Confirm | Critical | ‘‘Password’’ field | Master |
| **C593** | Validation: Password complexity requirements error | Medium | ‘‘Password’’ field | Master |

---

## 🔍 Execution Details
* **Author:** Alina Kuliak
* **Tools Used:** TestRail (S8 Master Suite)
* **Date Created:** February 25, 2026
