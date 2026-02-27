# Cappuccino Cup Test: UI Automation

## 📌 Test Objective
This test validates the core e-commerce flow for the **Coffee Cart** application. It ensures that a user can successfully add a specific product to their cart, navigate to the checkout area, and modify the item quantity.

---

## 📸 Test Execution Results
The following screenshot confirms the successful execution of the automated script:

[Test Execution Screenshot](https://1drv.ms/i/c/6f70d9b489838b4f/IQBDbiHtBf8tTqmbb-2mgr3vAd2BJN-VWZumwiWuQGqtHU4?e=FNBEof)

---

## 🛠 Automation Script Details
This script demonstrates the use of semantic locators and asynchronous navigation handling in Playwright.

### **Test Code:**
```javascript

test('should add cappuccino and increase quantity in cart', async ({ page }) => {
    // Navigate to the application
    await page.goto('[https://coffee-cart.app/](https://coffee-cart.app/)');

    // Select product by Test ID
    await page.getByTestId('Cappuccino').click();

    // Navigate to the Cart page
    await page.getByLabel('Cart page').click();

    // Assert that the URL has changed correctly
    await page.waitForURL('[https://coffee-cart.app/cart](https://coffee-cart.app/cart)');

    // Increase quantity using button role and name
    await page.getByRole('button', { name: 'Add one Cappuccino' }).click();

    // Short pause for UI update (can be replaced with assertion)
    await page.waitForTimeout(1000);
});
```
---
Created by Alina Kuliak
