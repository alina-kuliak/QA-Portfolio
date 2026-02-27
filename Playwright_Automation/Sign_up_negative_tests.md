# Conduit: Sign Up Form Negative Validation

## 📌 Test Objective
The goal of this suite is to verify that the **Conduit** registration form correctly handles invalid or incomplete user input. By testing empty fields, we ensure that the front-end displays accurate error messages returned by the back-end API, preventing the creation of invalid user accounts.

---

## 🛠 Automation Script Details
These tests demonstrate the use of strict text assertions to validate specific error messages within list elements.

### **Test Code:**

```javascript
import { test, expect } from '@playwright/test';

test('Assert error message for empty username in Sign up form', async ({ page }) => {  
  await page.goto('[https://conduit.mate.academy/user/register](https://conduit.mate.academy/user/register)');

  await page.getByPlaceholder('Email').fill('kvitka123@gmail.com');  
  await page.getByPlaceholder('Password').fill('kvitka123');  
  await page.getByRole('button', { name: 'Sign up' }).click();

  // Verifying specific username validation message
  await expect(page.getByRole('list').nth(1)).toContainText(
    `username:Username must start with a letter, have no spaces, and be 2 - 40 characters.`
  );
});

test('Assert error message for empty email in Sign up form', async ({ page }) => {  
  await page.goto('[https://conduit.mate.academy/user/register](https://conduit.mate.academy/user/register)');

  await page.getByPlaceholder('Username').fill('kvitka123');  
  await page.getByPlaceholder('Password').fill('kvitka123');  
  await page.getByRole('button', { name: 'Sign up' }).click();

  // Verifying email format validation
  await expect(page.getByRole('list').nth(1)).toContainText(
    `email:This email does not seem valid.`
  );
});

test('Assert error message for empty password in Sign up form', async ({ page }) => {  
  await page.goto('[https://conduit.mate.academy/user/register](https://conduit.mate.academy/user/register)');

  await page.getByPlaceholder('Username').fill('kvitka123');  
  await page.getByPlaceholder('Email').fill('kvitka123@gmail.com');  
  await page.getByRole('button', { name: 'Sign up' }).click();

  // Verifying blank password rejection
  await expect(page.getByRole('list').nth(1)).toContainText(
    `password:can't be blank`
  );
});
```
---
Created by Alina Kuliak
