## 🧪 Deep Dive: Assertions for the Cappuccino Tests

### 📸 Execution Screenshot
[View Test Results](https://1drv.ms/i/c/6f70d9b489838b4f/IQCG_-sYLxlwRY_RxID8LlR3AREywMh0jd1IMhE917ep470?e=Q4aCBK)

## cappuccinoAddedToCart.spec.js code:
```
test('Check Cappuccino correctly added to the Cart', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');  
 await page.getByTestId('Cappuccino').click();  
 await page.getByLabel('Cart page').click();  
 await page.waitForURL('https://coffee-cart.app/cart');

// ToDo: Assert that the 'Cappuccino' text is visible in the Item column  
 // ToDo: Assert that the '$19.00 x 1' text is present in the Unit column  
 // ToDo: Assert that the '$19.00' text is present in the Total column  
 // Tip: Use nth locator and locator('div')  
 const cartLocator \= page.getByRole('list').nth(1);  
 const cartFirstItemLocator \= cartLocator.getByRole('listitem').nth(1);  
 const cartFirstItemNameLocator \= cartFirstItemLocator.locator('div').nth(0);  
 const cartFirstItemUnitLocator \= cartFirstItemLocator.locator('div').nth(1);  
 const cartFirstItemTotalLocator \= cartFirstItemLocator.locator('div').nth(3);

await expect(cartFirstItemNameLocator).toContainText('Cappuccino');  
 await expect(cartFirstItemUnitLocator).toContainText('$19.00 x 1');  
 await expect(cartFirstItemTotalLocator).toContainText('$19.00');  
});
```

## cappuccinoAddedToTotal.spec.js code:
```
test('Check Cappuccino cost is added to Total on menu page', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');  
 await page.getByTestId('Cappuccino').click();

// ToDo: Assert "Total" button contains text 'Total: $19.00'  
 await expect(page.getByTestId('checkout')).toContainText('Total: $19.00');  
});
```

## cappuccinoHasCorrectCost.spec.js code:
```
test('Check Cappuccino cup has correct cost', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');

// ToDo: Assert "Cappuccino" cup contains text '$19.00'  
 // Tip: Use the .filter({ has: child })  
 const espressoCup \= page.getByTestId('Cappuccino');  
 const parent \= page.getByRole('listitem').filter({ has: espressoCup })

await expect(parent).toContainText('$19.00');  
});
```

## cappuccinoRemovedFromCart.spec.js code:
```
test('Check Cappuccino removed from Cart after clicking remove button', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');  
 await page.getByTestId('Cappuccino').click();  
 await page.getByLabel('Cart page').click();  
 await page.waitForURL('https://coffee-cart.app/cart');  
 await page.getByLabel('Remove all Cappuccino').click();

// ToDo: Assert the message "No coffee, go add some." is visible on the page.  
 await expect(page.getByText('No coffee, go add some.')).toBeVisible();  
});
```
---
Created by Alina Kuliak
