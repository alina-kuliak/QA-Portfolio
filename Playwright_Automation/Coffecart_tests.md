# CoffeeCart: Extended Functional Automation

## 📌 Overview
This suite covers advanced functional scenarios for the **CoffeeCart** application using **Playwright**. It validates state persistence, dynamic quantity updates, and promotional offer logic.

---

## 📸 Execution Results
The following screenshot confirms the successful execution of these functional test cases:
[Test Execution Screenshot](https://1drv.ms/i/c/6f70d9b489838b4f/IQDgvtxsKPstSKUiD6TEHvKPAeTZVnAlec9VsFP86oKqnmo?e=96xLRc)

---

## 🧪 Automated Test Cases
## cartCleanedAfterPageRefresh.spec.js code:
```javascript
test('Assert cart cleaned after page refresh', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');  
 await page.waitForURL('https://coffee-cart.app/');  
 await page.getByTestId('Cappuccino').click();  
 await page.getByLabel('Cart page').click();  
 await page.waitForURL('https://coffee-cart.app/cart');  
 await expect(page.locator('div').filter({ hasText: /^Cappuccino$/ })).toBeVisible();  
  await page.reload();  
  await expect(page.locator('div').filter({ hasText: /^Cappuccino$/ })).toBeHidden();  
 await expect(page.getByText('No coffee, go add some.')).toBeVisible();  
});
```

## cartUpdatedAfterClickingMinusButton.spec.js code:
```javascript
test('Assert cart updated correctly after clicking minus for drinks', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');  
 await page.waitForURL('https://coffee-cart.app/');  
 await page.getByTestId('Espresso').click();  
 await page.getByTestId('Cappuccino').click();  
 await page.getByLabel('Cart page').click();  
 await page.waitForURL('https://coffee-cart.app/cart');  
 await expect(page.locator('div').filter({ hasText: /^Espresso$/ })).toBeVisible();  
  await page.getByRole('button', { name: 'Remove one Espresso' }).click();  
  await expect(page.locator('div').filter({ hasText: /^Espresso$/ })).toBeHidden();  
 await expect(page.locator('div').filter({ hasText: /^Cappuccino$/ })).toBeVisible();  
  await page.getByRole('button', { name: 'Remove one Cappuccino' }).click();  
  await expect(page.locator('div').filter({ hasText: /^Cappuccino$/ })).toBeHidden();  
 await expect(page.getByText('No coffee, go add some.')).toBeVisible();  
});
```

## cartUpdatedAfterClickingPlusButton.spec.js code:
```javascript
test('Assert cart updated correctly after clicking plus for drinks', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');  
 await page.getByTestId('Cappuccino').click();  
 await page.getByTestId('Espresso').click();  
 await page.getByLabel('Cart page').click();  
 await page.waitForURL('https://coffee-cart.app/cart');

const cartLocator \= page.getByRole('list').nth(1);  
 const cartFirstItemLocator \= cartLocator.getByRole('listitem').nth(1);  
 const cartFirstItemNameLocator \= cartFirstItemLocator.locator('div').nth(0);  
 const cartFirstItemUnitLocator \= cartFirstItemLocator.locator('div').nth(1);  
 const cartFirstItemTotalLocator \= cartFirstItemLocator.locator('div').nth(3);

const cartSecondItemLocator \= cartLocator.getByRole('listitem').nth(2);  
 const cartSecondItemNameLocator \= cartSecondItemLocator.locator('div').nth(0);  
 const cartSecondItemUnitLocator \= cartSecondItemLocator.locator('div').nth(1);  
 const cartSecondItemTotalLocator \= cartSecondItemLocator.locator('div').nth(3);

await expect(cartFirstItemNameLocator).toContainText('Cappuccino');  
 await expect(cartFirstItemTotalLocator).toContainText('$19.00');

await expect(cartSecondItemNameLocator).toContainText('Espresso');  
 await expect(cartSecondItemTotalLocator).toContainText('$10.00');

await page.getByRole('button', { name: 'Add one Espresso' }).click();  
 await expect(cartSecondItemTotalLocator).toContainText('$20.00');

await page.getByRole('button', { name: 'Add one Cappuccino' }).click();  
 await expect(cartFirstItemTotalLocator).toContainText('$38.00');  
});
```

## mochaAddedToCartOnPromoAccept.spec.js code:
```javascript
test('Assert discounted Mocha added to the Cart after promo accepting', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');  
 await page.getByTestId('Cappuccino').click();  
 await page.getByTestId('Espresso').click();  
 await page.getByTestId('Americano').click();  
 await expect(page.getByText('It\\'s your lucky day\! Get an')).toBeVisible();  
 await page.getByRole('button', { name: 'Yes, of course\!' }).click();  
 await page.getByLabel('Cart page').click();  
 await page.waitForURL('https://coffee-cart.app/cart');

const cartLocator \= page.getByRole('list').nth(1);

const assertCartItem \= async (name, expectedPrice) \=\> {  
 const item \= cartLocator.getByRole('listitem').filter({ hasText: name });  
 await expect(item).toContainText(name);  
 await expect(item).toContainText(expectedPrice);  
 };

await assertCartItem('(Discounted) Mocha', '$4.00');  
 await assertCartItem('Americano', '$7.00');  
 await assertCartItem('Cappuccino', '$19.00');  
 await assertCartItem('Espresso', '$10.00');  
});
```

## mochaAddedToCartOnPromoDecline.spec.js code:
```javascript
test('Assert discounted Mocha added to the Cart after promo accepting', async ({ page }) \=\> {  
 await page.goto('https://coffee-cart.app/');

await page.getByTestId('Cappuccino').click();  
 await page.getByTestId('Espresso').click();  
 await page.getByTestId('Americano').click();

await expect(page.getByText("It's your lucky day\! Get an extra cup of Mocha for $4.")).toBeVisible();

await page.getByRole('button', { name: "Nah, I'll skip." }).click();

await page.getByLabel('Cart page').click();  
 await page.waitForURL('https://coffee-cart.app/cart');

const cartLocator \= page.getByRole('list').nth(1);

await expect(cartLocator.getByRole('listitem').filter({ hasText: 'Espresso' })).toBeVisible();  
 await expect(cartLocator.getByRole('listitem').filter({ hasText: 'Cappuccino' })).toBeVisible();  
 await expect(cartLocator.getByRole('listitem').filter({ hasText: 'Americano' })).toBeVisible();

await expect(cartLocator.getByRole('listitem').filter({ hasText: '(Discounted) Mocha' })).toHaveCount(0);  
});
```
---
Created by Alina Kuliak
