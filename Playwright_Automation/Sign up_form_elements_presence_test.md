# Conduit: Sign Up Form Elements Presence Test

## 📌 Test Objective
This test performs a **UI Integrity Check** (Smoke Test) for the registration page of the **Conduit** application. It ensures that all critical entry points, input fields, and call-to-action buttons are correctly rendered and visible to the user.

---

## 🛠 Automation Script Details
The script utilizes Playwright's built-in assertions (`toBeVisible`) to validate the presence of key UI components.

### **Test Code:**

```javascript
import { test, expect } from '@playwright/test';

test('Verify presence of all Sign up form elements', async ({ page }) => {
  // Navigate to the Registration page
  await page.goto('[https://conduit.mate.academy/user/register](https://conduit.mate.academy/user/register)');

  // Assert visibility of headers and links
  await expect(page.getByRole('heading', { name: 'Sign up' })).toBeVisible();  
  await expect(page.getByRole('link', { name: 'Have an account?' })).toBeVisible();  

  // Assert visibility of input fields
  await expect(page.getByPlaceholder('Username')).toBeVisible();  
  await expect(page.getByPlaceholder('Email')).toBeVisible();  
  await expect(page.getByPlaceholder('Password')).toBeVisible();  

  // Assert visibility of the primary action button
  await expect(page.getByRole('button', { name: 'Sign up' })).toBeVisible();  
});
```
---
Created by Alina Kuliak
