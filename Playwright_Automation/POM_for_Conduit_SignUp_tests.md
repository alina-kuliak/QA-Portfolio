# Conduit: POM & Data-Driven Registration Testing

## 📌 Overview
This project demonstrates a scalable automation architecture for the **Conduit (RealWorld)** application. By implementing the **Page Object Model (POM)** and integrating **Faker.js**, the framework supports robust negative validation and dynamic positive registration flows.

### Key Features:
* **Encapsulation:** UI elements and interactions are centralized in the `SignUpPage` class.
* **Dynamic Data:** Use of `@faker-js/faker` to generate unique user credentials for every test run, preventing data collisions.
* **Clean Test Scripts:** Tests use descriptive methods like `fillUserNameField` instead of raw selectors.

---

## SignUpPage.js code:
```javascript
const { expect } \= require('@playwright/test');

export class SignUpPage {  
 constructor(page) {  
 this.page \= page;  
 this.usernameField \= page.getByPlaceholder('Username');  
 this.emailField \= page.getByPlaceholder('Email');  
 this.passwordField \= page.getByPlaceholder('Password');  
 this.signUpButton \= page.getByRole('button', { name: 'Sign up' });  
 this.errorMessage \= page.getByRole('list').nth(1);  
 }

async open() {  
 await this.page.goto('https://conduit.mate.academy/user/register');  
 }

async fillUserNameField(username) {  
 await this.usernameField.fill(username);  
 }

async fillEmailField(email) {  
 await this.emailField.fill(email);  
 }

async fillPasswordField(password) {  
 await this.passwordField.fill(password);  
 }

async clickSignUpButton() {  
 await this.signUpButton.click();  
 }

async assertErrorMessageContainsText(messageText) {  
 await expect(this.errorMessage).toContainText(messageText);  
 }  
}
```

## signUpNegative.spec.js code:
```javascript

import { test, expect } from '@playwright/test';  
import { SignUpPage } from '../../src/pages/SignUpPage';

test.describe('Sign up negative tests', () \=\> {  
 let signUpPage;

test.beforeEach(async ({ page }) \=\> {  
 signUpPage \= new SignUpPage(page);  
 await signUpPage.open();  
 });

test('Assert error message for empty username in Sign up form', async ({ page }) \=\> {  
 await signUpPage.fillPasswordField('kvitka123');  
 await signUpPage.fillEmailField('kvitka123@gmail.com');  
 await signUpPage.clickSignUpButton();  
 await signUpPage.assertErrorMessageContainsText(\`username:Username must start with a letter, have no spaces, and be 2 \- 40 characters.\`);  
 });

test('Assert error message for empty password in Sign up form', async ({ page }) \=\> {  
 await signUpPage.fillUserNameField('kvitka123');  
 await signUpPage.fillEmailField('kvitka123@gmail.com');  
 await signUpPage.clickSignUpButton();  
 await signUpPage.assertErrorMessageContainsText(\`password:can\\'t be blank\`);  
 });

test('Assert error message for empty email in Sign up form', async ({ page }) \=\> {  
 await signUpPage.fillUserNameField('kvitka123');  
 await signUpPage.fillPasswordField('kvitka123');  
 await signUpPage.clickSignUpButton();  
 await signUpPage.assertErrorMessageContainsText(\`email:This email does not\`);  
 });  
});
```

## signUpPositive.spec.js code:
```javascript

import { test } from '@playwright/test';  
import { faker } from '@faker-js/faker';  
import { SignUpPage } from '../../src/pages/SignUpPage';  
import { HomePage } from '../../src/pages/HomePage';

test('Successful \`Sign up\` flow test', async ({ page }) \=\> {  
 const signUpPage \= new SignUpPage(page);  
 const homePage \= new HomePage(page);

await signUpPage.open();  
 await signUpPage.fillUserNameField(faker.internet.username());  
 await signUpPage.fillEmailField(faker.internet.email());  
 await signUpPage.fillPasswordField(faker.internet.password());  
 await signUpPage.clickSignUpButton();

await homePage.assertYourFeedTabIsVisible();

});
```
---
Created by Alina Kuliak
