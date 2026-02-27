# Bug Reports: PetStore Project

---

### Category: FieldValue
**ID:** PS-001  
**Summary:** The 'Password' field is pre-populated with 4 characters on the 'Sign In' page upon loading.  

**Bug details** **Preconditions:** The user is not logged in.  
**Steps to reproduce:** 1. Navigate to the Home page.  
2. Click the 'Sign In' link.  
3. Observe the 'Password' field.  

**Actual result:** The 'Password' field is pre-populated with 4 characters.  
**Expected result:** The 'Password' field should be empty.  

**Notes:** This issue is due to the HTML attribute 'value' containing 'j2ee'.  

**Environment** **Operating system:** Windows 10  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Moderate  

---

### Category: FieldValue
**ID:** IDPS-001  
**Summary:** The validation message does not appear on the 'My Account' page when passwords don't match.  

**Bug details** **Preconditions:** The user is logged in.  
**Steps to reproduce:** 1. Navigate to the 'My Account' page on the website: link.  
2. Fill the 'New password' field.  
3. Fill the 'Repeat password' field with another password.  
4. Click on [Save Account Information] button.  
5. Observe the save typo.  

**Actual result:** Account information is saved.  
**Expected result:** Account information is not saved and a user gets an Error message.  

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Moderate  
**Priority:** Medium  

---

### ID:** IDPS-002  
**Summary:** The validation message is not shown on the 'My Account' page when the 'Email' field does not contain '@'.  

**Bug details** **Preconditions:** The user is logged in.  
**Steps to reproduce:** 1. Navigate to the 'My Account' page on the website: link.  
2. Fill the 'Email' field without '@'.  
3. Click on [Save Account Information] button.  
4. Observe the save typo.  

**Actual result:** The validation message is not shown.  
**Expected result:** The validation message is shown.  

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Moderate  
**Priority:** Medium  

---

### ID:** IDPS-003  
**Summary:** The success message does not apear on the account registration page when all fields are filled and clicking the [Save Account Information] button.  

**Bug details** **Preconditions:** The user is not logged in.  
**Steps to reproduce:** 1. The Registration page is opened on the website: link.  
2. Fill in all fields on the Registration page.  
3. Click on [Save Account Information] button.  
4. Observe the save typo.  

**Actual result:** The user is redirected to the 'Main Page.  
**Expected result:** The success message apears.  

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Minor  
**Priority:** Low  

---

### Category: FieldValue
**ID:** IDPS-001  
**Summary:** The navigation bar is not displayed on the 'Help' page after clicking the 'Help' page link.  

**Bug details** **Preconditions:** -  
**Steps to reproduce:** 1. Navigate to the 'Help' page on the website: link.  
2. Observe the navigation bar.  

**Actual result:** The navigation bar is not displayed.  
**Expected result:** The navigation bar is displayed on the 'Help' page.  

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Minor  

---

### Category: FieldValue
**ID:** IDPS-002  
**Summary:** The tooltip ‘Cart’ is not displayed on the Cart icon after navigating the cursor on the Cart icon.  

**Bug details** **Preconditions:** -  
**Steps to reproduce:** 1. Navigate to the 'Main' page on the website: link.  
2. Navigate the cursor to the Cart icon.  
3. Observe the tooltip 'Cart'.  

**Actual result:** The tooltip is not displayed.  
**Expected result:** The tooltip is displayed.    

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Minor  

---

### Category: FieldValue
**ID:** IDPS-003  
**Summary:** The ''Name'' column is not displayed on the table in the Cart after adding a product to the Cart.  

**Bug details** **Preconditions:** The user added at least 1 item to the Cart.  
**Steps to reproduce:** 1. Navigate to the 'Main' page on the website: link.  
2. Navigate to the Cart page.  
3. Observe the 'Name column in the 'Shopping cart' table.  

**Actual result:** The 'Name' column is not displayed on the 'Shopping Cart' table.  
**Expected result:** The 'Name' column is displayed on the 'Shopping Cart' table.  

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Moderate  

---

### Category: FieldValue
**ID:** IDPS-004  
**Summary:** The [Add to Cart] button is not displayed on the the 'List of Products' page.  

**Bug details** **Preconditions:** **Steps to reproduce:** 1. Navigate to the 'Main' page on the website: link.  
2. Navigate to the 'List of Products' page.  
3. Observe the [Add to Cart] button.  

**Actual result:** The [Add to Cart] button is not displayed.  
**Expected result:** The user clicks on the [Add to Cart] button to add products to the Cart.  

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Moderate  

---

### Category: FieldValue
**ID:** IDPS-005  
**Summary:** The badge with a quantity of added-to-the Cart products on the Cart’s icon is not displayed after the user adds a product to the cart.  

**Bug details** **Preconditions:** The user added 4 items to the Cart.  
**Steps to reproduce:** 1. Navigate to the 'Main' page on the website: link.  
2. Navigate to the Cart.  
3. Observe the Cart's icon.  

**Actual result:** The Cart's icon does not change.  
**Expected result:** The badge with a quantity of added-to-the Cart products on the Cart’s icon is displayed.  

**Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Minor  

---

### Category: FieldValue
**ID:** IDPS-006  
**Summary:** The user is allowed to add more than 5 items of the same product to the shopping cart.  

**Bug details** **Preconditions:** The user added 1 item of product to the Cart.  
**Steps to reproduce:** 1. Navigate to the 'Main' page on the website: link.  
2. Navigate to the Cart.  
3. Change the quantity of added item of product to 6.  
4. Click on [Update Cart] button.  
5. Observe resoult after update.  

**Actual result:** The quantity of items is updated.  
**Expected result:** The quantity of items is not updated the validation message “We are sorry, but you can’t buy more than 5 items of the product.” is shown under the table.  

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Major  

---

### Category: FieldValue
**ID:** IDPS-007  
**Summary:** The user is allowed to add not in stock product to the shopping cart.  

**Bug details** **Preconditions:** The user adds 1 not in stock product to the Cart.  
**Steps to reproduce:** 1. Navigate to the 'Main' page on the website: link.  
2. Navigate to the Cart.  
3. Click on [Update Cart] button.  
4. Observe resoult after update.  

**Actual result:** The not-in-stock product is added to the Cart.  
**Expected result:** The not-in-stock product is not added to the Cart the validation message “We are sorry, but we have only N items of this product for now. Would you like to subscribe to notifications when this product will be available?“ is shown.  

**Notes:** **Environment** **Operating system:** Windows 11  
**App version:** Demo  
**Browser:** Chrome (latest)  
**Severity:** Major  

---
*Made by Alina Kuliak*
