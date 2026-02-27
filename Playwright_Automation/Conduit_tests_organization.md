### Sign up Negative Tests
This suite ensures that the registration form properly validates user input and displays meaningful error messages.
---

### Test Execution Results
[Test Execution Screenshot](https://1drv.ms/i/c/6f70d9b489838b4f/IQCwn_yFaX7LQ5rerHyqelM0AZUiHe8a-s1fM4Fmwk7uLWU?e=DmzBxh)

###Test files organization screenshot:  
[Test_Files_Organization](https://1drv.ms/i/c/6f70d9b489838b4f/IQCVIirsZHfzSIua6Ybb73KyAZEJnHGgo9PAqRb5RH1Jpb0?e=iVWgHn)

---

## 🧪 Automated Test Cases
```javascript

import { test, expect } from '@playwright/test';

test.describe('Sign up negative tests', () \=\> {

  test.beforeEach(async ({ page }) \=\> {  
    await page.goto('https://conduit.mate.academy/user/login');  
  });

  test('Assert error message for empty username in Sign up form', async ({ page }) \=\> {  
    await page.goto('https://conduit.mate.academy/user/register');

    await page.getByPlaceholder('Email').fill('test@gmail.com');  
    await page.getByPlaceholder('Password').fill('newpass123\!');  
    await page.getByRole('button', { name: 'Sign up' }).click();

    await expect(  
      page.getByRole('list').nth(1)  
    ).toContainText(\`username:Username must start with a letter, have no spaces, and be 2 \- 40 characters.\`);  
  });

  test('Assert error message for empty email in Sign up form', async ({ page }) \=\> {  
    await page.goto('https://conduit.mate.academy/user/register');

    await page.getByPlaceholder('Username').fill('newuser');  
    await page.getByPlaceholder('Password').fill('newpass123\!');  
    await page.getByRole('button', { name: 'Sign up' }).click();

    await expect(page.getByRole('list').nth(1)).toContainText(\`email:This email does not seem valid.\`);  
  });

  test('Assert error message for empty password in Sign up form', async ({ page }) \=\> {  
    await page.goto('https://conduit.mate.academy/user/register');

    await page.getByPlaceholder('Username').fill('newuser');  
    await page.getByPlaceholder('Email').fill('test@gmail.com');  
    await page.getByRole('button', { name: 'Sign up' }).click();

    await expect(page.getByRole('list').nth(1)).toContainText(\`password:can't be blank\`);  
  });  
});
```
---
Created by Alina Kuliak
