## 🧪 Deep Dive: Assertions for the Cappuccino Tests

### 📸 Execution Screenshot
[View Test Results](https://1drv.ms/i/c/6f70d9b489838b4f/IQCG_-sYLxlwRY_RxID8LlR3AREywMh0jd1IMhE917ep470?e=Q4aCBK)

### 1. Cart Content Validation (`cappuccinoAddedToCart.spec.js`)
```javascript
test('Check Cappuccino correctly added to the Cart', async ({ page }) => {  
 await page.goto('[https://coffee-cart.app/](https://coffee-cart.app/)');  
 await page.getByTestId('Cappuccino').click();  
 await page.getByLabel('Cart page').click();  
 await page.waitForURL('[https://coffee-cart.app/cart](https://coffee-cart.app/cart)');

// ToDo: Assert that the 'Cappuccino' text is visible in the Item column  
 // ToDo: Assert that the '$19.00 x 1' text is present in the Unit column  
 // ToDo: Assert that the '$19.00' text is present in the Total column  
 // Tip: Use nth locator and locator('div')  
 const cartLocator = page.getByRole('list').nth(1);  
 const cartFirstItemLocator = cartLocator.getByRole('listitem').nth(1);  
 const cartFirstItemNameLocator = cartFirstItemLocator.locator('div').nth(0);  
 const cartFirstItemUnitLocator = cartFirstItemLocator.locator('div').nth(1);  
 const cartFirstItemTotalLocator = cartFirstItemLocator.locator('div').nth(3);

await expect(cartFirstItemNameLocator).toContainText('Cappuccino');  
 await expect(cartFirstItemUnitLocator).toContainText('$19.00 x 1');  
 await expect(cartFirstItemTotalLocator).toContainText('$19.00');  
});
```
---
Created by Alina Kuliak
