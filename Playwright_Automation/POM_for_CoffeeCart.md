# Page Object Model (POM) Implementation: CoffeeCart

## 📌 Overview
This project demonstrates the transition from flat test scripts to a professional **Page Object Model (POM)** architecture. By encapsulating page-specific elements and methods within dedicated classes, the framework becomes more readable, maintainable, and reusable.

### Key Benefits Demonstrated:
* **Code Reusability:** Methods like `chooseItem` and `assertCartItem` can be reused across multiple test suites.
* **Separation of Concerns:** Test files focus on "What" to test, while Page classes handle "How" to interact with the UI.
* **Maintenance:** UI changes (like a locator update) only need to be fixed in one class file rather than dozens of tests.

---

##CartPage.js class file:  
```javascript
const { expect } \= require('@playwright/test');

export class CartPage {  
 constructor(page) {  
 this.page \= page;  
 this.cartListLocator \= page.getByRole('list').nth(1);  
 this.errorMessage \= page.locator('.list');  
 this.checkoutTotal \= page.getByTestId('checkout');  
 }

async open() {  
 await this.page.goto('https://coffee-cart.app/cart');  
 }

async waitForLoading() {  
 await this.page.waitForURL('https://coffee-cart.app/cart');  
 }

getCartItem(itemName) {  
 const item \= this.cartListLocator.getByRole('listitem').filter({ hasText: itemName });  
 return {  
 itemLocator: item,  
 name: item.locator('div').nth(0),  
 unitPriceAndQty: item.locator('div').nth(1),  
 totalPrice: item.locator('div').nth(3)  
 };  
 }

async expectNameItem(itemName) {  
 const { itemLocator } \= this.getCartItem(itemName);  
 await expect(itemLocator).toContainText(itemName);  
 }

async assertErrorMessageContainsText(messageText) {  
 await expect(this.errorMessage).toContainText(messageText);  
 }

async assertCartItem(name, expectedPrice) {  
 const item \= this.cartListLocator.getByRole('listitem').filter({ hasText: name });  
 await expect(item).toContainText(name);  
 await expect(item).toContainText(expectedPrice);  
 };

async clickRemoveLabel(remove) {  
 const removeLabel \= this.page.getByLabel(remove);  
 await removeLabel.click();  
 }  
 async clickRemoveButton(removeName) {  
 const removeButton \= this.page.getByRole('button', { name: removeName });  
 await removeButton.click();  
 }

async assertHiddenCartItem(name) {  
 const item \= this.page.getByText(name, { exact: true });  
 await expect(item).toBeHidden();  
 }  
 async checkout(total) {  
 await expect(this.checkoutTotal).toContainText(total);  
 }  
}
```

##MenuPage.js class file:  
```javascript
const { expect } \= require('@playwright/test');

export class MenuPage {  
 constructor(page) {  
 this.page \= page;  
 this.cartPageLabel \= page.getByLabel('Cart page');  
 this.checkoutAmount \= page.getByTestId('checkout');  
 this.menuListLocator \= page.getByRole('list').nth(1);  
 this.happyMessage \= page.locator('.promo');  
 this.yesPromoButtom \= page.getByRole('button', { name: 'Yes, of course\!' });  
 this.noPromoButtom \= page.getByRole('button', { name: "Nah, I'll skip." })  
 }

async open() {  
 await this.page.goto('https://coffee-cart.app/')  
 }

async waitForLoading() {  
 await this.page.waitForURL('https://coffee-cart.app/');  
 }

async chooseItem(itemName) {  
 const itemHeading \= this.page.getByTestId(itemName);  
 await itemHeading.click();  
 }

async clickCartPageLabel() {  
 await this.cartPageLabel.click();  
 }

async totalAmountMenu(amount) {  
 await expect(this.checkoutAmount).toContainText(amount);  
 }

async correctItemCost(item) {  
 const itemLocator \= this.menuListLocator.getByRole('heading', { name: item });  
 await expect(itemLocator).toContainText(item);  
 }

async happyMessageVis(messageText) {  
 await expect(this.happyMessage).toContainText(messageText);  
 }  
 async clickYesPromo() {  
 await this.yesPromoButton.click();  
 }  
 async clickNoPromo() {  
 await this.noPromoButton.click();  
 }  
}
```
Created by Alina Kuliak
