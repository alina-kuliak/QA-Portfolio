# 🧪 Test Cases: Authentication & Registration (Conduit)

## 📝 Overview
This document contains a detailed list of test cases for the **Sign In** and **Sign Up** modules of the Conduit application. These cases cover functional requirements, UI elements, navigation, and validation logic.

---

## 🛠 Test Case Repository

| ID | Title | Priority | Section | Suite |
| :--- | :--- | :--- | :--- | :--- |
| **C520** | The 'Sign In' page contains a 'Need an account?' link. | Low | Sign In page | Master |
| **C521** | A user is redirected to the 'Sign up' page by clicking on the 'Need an account?' link below the 'Sign In' form. | Medium | Sign In page | Master |
| **C522** | The 'Sign In' page contains a 'Sign In' form. | Critical | Sign In page | Master |
| **C523** | The 'Sign In' page contains a 'Forgot the password?' link. | Medium | Sign In page | Master |
| **C524** | A user is redirected to the 'Forgot password' page by clicking on the 'Forgot the password?' link. | Medium | Sign In page | Master |
| **C525** | User should be redirected to the 'User page' after reaching the 'Sign In' page by direct link. | Medium | Sign In page | Master |
| **C519** | The 'Sign In' page opens after clicking on the 'Sign in' link in the Conduit navigation bar. | High | Sign In page | Master |
| **C526** | The 'Sign in' form should contain a field for entering an email or username. | High | ‘’Sign in’’ form | Master |
| **C527** | The 'Sign in' form should contain the 'Password' field. | Medium | ‘’Sign in’’ form | Master |
| **C528** | The 'Sign in' form should contain the [Sign in] button. | High | ‘’Sign in’’ form | Master |
| **C529** | A user can log in by filling in all fields and clicking on the [Sign in] button. | Critical | ‘’Sign in’’ form | Master |
| **C530** | A user can log in by filling in all fields and clicking on the [Enter] button. | Medium | ‘’Sign in’’ form | Master |
| **C538** | The validation message 'User with such email or username not registered.' is shown when the user enters the 'Email or Username' field, not registered Email. | Medium | ‘'Email or Username’' | Master |
| **C537** | The validation message 'User with such email or username not registered.' is shown when the user enters the 'Email or Username' field with an unregistered username. | Medium | ‘'Email or Username’' | Master |
| **C536** | The validation message 'Email or Username: can’t be blank' should be shown to the user if the 'Email or Username' field isn't filled. | Low | ‘'Email or Username’' | Master |
| **C535** | User should be able to log in by entering the 'Email or Username' field by registered username or email, with or without uppercase. | Medium | ‘'Email or Username’' | Master |
| **C533** | The user should be able to log in by filling in the 'Email or Username' field by registered Email. | Critical | ‘'Email or Username’' | Master |
| **C532** | The user should be able to log in by filling in the 'Email or Username' field by registered Username. | Critical | ‘'Email or Username’' | Master |
| **C531** | User should not be able to log in without filling in the 'Email or Username' field. | Critical | ‘'Email or Username’' | Master |
| **C534** | The 'Email or Username' field should contain the 'Enter your username or email' placeholder. | Medium | ‘'Email or Username’' | Master |
| **C546** | The validation message 'Entered Invalid password! Check your keyboard layout or Caps Lock. Send a one-time password to your email?' is shown if the user enters the 'Password' field with a value not match the password for the user account. | Medium | ‘‘Password’’ field | Master |
| **C545** | User is redirected to the 'Forgot password' page after clicking on the 'Send one-time password' link in the message. | Medium | ‘‘Password’’ field | Master |
| **C544** | The validation message 'Password: can’t be blank' should be shown to the user if the 'Password' field isn't filled. | Medium | ‘‘Password’’ field | Master |
| **C543** | User should be able to paste data into the 'Password' field. | Medium | ‘‘Password’’ field | Master |
| **C542** | User shouldn’t be able to cut values from the 'Password' field. | Medium | ‘‘Password’’ field | Master |
| **C541** | User shouldn’t be able to copy values from the 'Password' field. | Medium | ‘‘Password’’ field | Master |
| **C540** | The 'Password' field should be covered by asterisks. | Medium | ‘‘Password’’ field | Master |
| **C539** | User should not be able to log in without filling in the 'Password' field. | Critical | ‘‘Password’’ field | Master |
| **C547** | The 'Sign Up' page opens after clicking on the 'Sign up' link in the Conduit navigation bar. | High | Sign Up page | Master |
| **C548** | A user can create an account by filling in all fields and clicking on the [Sign Up] button. | Critical | Sign Up page | Master |
| **C549** | Users is able to create an account by filling in all fields and pressing the [Enter] button | High | Sign Up page | Master |
| **C550** | An email to verify the email address is sent after a user is registered. | Critical | Sign Up page | Master |
| **C551** | The 6-digit code is in the email to verify the email address. | Critical | Sign Up page | Master |
| **C552** | A user is redirected to the 'Finish Registration' page after successful registration. | Critical | Sign Up page | Master |
| **C553** | The 'Finish Registration' page should contain a field to enter the 6-digit code sent by email. | Critical | Sign Up page | Master |
| **C554** | A user should be able to enter the 6-digit code and click on the [Confirm] button. | Critical | Sign Up page | Master |
| **C555** | A user is redirected to the 'Sign In' page by clicking on the 'Have an account?' link below the 'Sign Up' form. | Medium | Sign Up page | Master |
| **C556** | The 'Sign up' form should contain the 'Username' field. | Critical | ‘’Sign up’’ form | Master |
| **C559** | The 'Sign up' form should contain the 'Confirm password' field. | Critical | ‘’Sign up’’ form | Master |
| **C557** | The 'Sign up' form should contain the 'Email' field. | Critical | ‘’Sign up’’ form | Master |
| **C558** | The 'Sign up' form should contain the 'Password' field. | Critical | ‘’Sign up’’ form | Master |
| **C568** | 'Username' field should accept digits. | Medium | ‘‘Username’’ field | Master |
| **C573** | User should not be able to sign up with a Username without uppercase letters and create an account with the same value with uppercase letters. | Medium | ‘‘Username’’ field | Master |
| **C572** | The validation message 'Username must start with a letter, have no spaces, and be 3 - 40 characters.' should be shown if the username is invalid. | Medium | ‘‘Username’’ field | Master |
| **C571** | The validation message 'This username is taken.' should be shown if the Username is already taken. | Medium | ‘‘Username’’ field | Master |
| **C570** | The 'Username' field should not accept values with non-printing symbols. | High | ‘‘Username’’ field | Master |
| **C569** | The 'Username' field should not accept values with special characters. | High | ‘‘Username’’ field | Master |
| **C567** | 'Username' field should start from a Latin letter. | High | ‘‘Username’’ field | Master |
| **C566** | 'Username' field should accept Latin letters. | High | ‘‘Username’’ field | Master |
| **C565** | User should not be able to create a Username with 41 symbols. | High | ‘‘Username’’ field | Master |
| **C564** | User should be able to create a Username with 40 symbols. | High | ‘‘Username’’ field | Master |
| **C563** | User should be able to create a Username with 3 symbols. | Critical | ‘‘Username’’ field | Master |
| **C562** | User is not able to create a Username with 2 symbols. | High | ‘‘Username’’ field | Master |
| **C561** | The 'Username' field should not accept an already registered Username. | Critical | ‘‘Username’’ field | Master |
| **C560** | User should not be able to register without filling in the 'Username' field. | High | ‘‘Username’’ field | Master |
| **C576** | The Email field should accept the format [name]@[domain].[top-domain] of Email. | Critical | ‘‘Email’’ field | Master |
| **C581** | The validation message 'This email does not seem valid' should be shown if the email is invalid. | Medium | ‘‘Email’’ field | Master |
| **C580** | The validation message 'This email is taken. Want to log in?' should be shown if the email is taken. | Medium | ‘‘Email’’ field | Master |
| **C579** | The [name] part of the email should accept special characters: plus (+), hyphen (-), underline (_), and dot (.). | Medium | ‘‘Email’’ field | Master |
| **C578** | The [name] part of the email should accept digits. | Medium | ‘‘Email’’ field | Master |
| **C577** | The [name] part of the email should accept Latin letters. | High | ‘‘Email’’ field | Master |
| **C575** | The 'Email' field should not accept already registered Email. | High | ‘‘Email’’ field | Master |
| **C574** | User should not be able to register without filling in the 'Email' field. | Critical | ‘‘Email’’ field | Master |
| **C582** | User should not be able to register without filling in the 'Password' field. | Critical | ‘‘Password’’ field | Master |
| **C583** | User should not be able to create a password with 7 symbols. | High | ‘‘Password’’ field | Master |
| **C584** | User should be able to create a password with 8 symbols. | Critical | ‘‘Password’’ field | Master |
| **C585** | User should be able to create a password with 30 symbols. | Critical | ‘‘Password’’ field | Master |
| **C586** | User should not be able to create a password with 31 symbols. | High | ‘‘Password’’ field | Master |
| **C587** | The 'Password' field should not accept non-printing symbols. | High | ‘‘Password’’ field | Master |
| **C588** | The 'Password' field should not accept a value without a special character. | High | ‘‘Password’’ field | Master |
| **C589** | The 'Password' field should not accept values without digits. | High | ‘‘Password’’ field | Master |
| **C590** | The 'Password' field should not accept a value without capital letters. | High | ‘‘Password’’ field | Master |
| **C591** | The 'Confirm password' field should not accept values different from the New password field. | High | ‘‘Password’’ field | Master |
| **C592** | User should not be able to register without filling in the 'Confirm Password' field. | Critical | ‘‘Password’’ field | Master |
| **C593** | The validation message 'Password should contain at least one capital letter, one number, and one special character.' is shown if the password is non-valid. | Medium | ‘‘Password’’ field | Master |

---

## 🔍 Execution Details
* **Author:** Alina Kuliak
* **Tools Used:** TestRail (Suite S8)
* **Status:** Draft / Active
