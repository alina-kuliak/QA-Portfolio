# Wizard Bank: Financial Flow Automation

## 📌 Project Overview
This test suite automates critical banking functionalities for the **GlobalsQA Banking Project**. It demonstrates the ability to validate complex state transitions, such as deposits, withdrawals, and transaction history synchronization.

### Key Skills Demonstrated:
* **State Validation:** Verifying that account balances update accurately after transactions.
* **Negative Financial Logic:** Ensuring users cannot withdraw more than their current balance.
* **Asynchronous Data Handling:** Waiting for table rows to populate after a page reload.
* **Data-Driven Testing:** Using `faker` to simulate varied deposit amounts.

---

## 🧪 Automated Test Cases

### 1. Transactional Integrity (`assertDepositCanBeOpened.spec.js`)
Validates the full lifecycle of a deposit: from initial action to balance update and transaction log verification.

## assertCustomerAccountData.spec.js code:
```javascript

test('Assert customer has correct bank data', async ({ page }) \=\> {  
 await page.goto('https://www.globalsqa.com/angularJs-protractor/BankingProject/\#/customer');  
 await page.locator('select\#userSelect').selectOption({ label: 'Hermoine Granger' });  
 await page.getByRole('button', { name: 'Login' }).click();

    const accountNumberDropdown \= page.locator('select\#accountSelect');
    const accountNumberValue \= await accountNumberDropdown.inputValue();
    await expect(accountNumberValue).not.toBe('');

    const accountNumberText \= await page.locator('.center strong').nth(0).textContent();
    await expect(accountNumberText).not.toBe('');

    const accountBalanceText \= await page.locator('.center strong').nth(1).textContent();
    await expect(accountBalanceText).not.toBe('');

    const accountCurrencyText \= await page.locator('.center strong').nth(2).textContent();
    await expect(accountCurrencyText).not.toBe('');

});
```

## assertCustomerCorrectLogout.spec.js code:
```javascript

test('Assert correct customer Logout ', async ({ page }) \=\> {  
 await page.goto('https://www.globalsqa.com/angularJs-protractor/BankingProject/\#/login ');  
 await page.getByRole('button', { name: 'Customer Login' }).click();  
 await page.locator('select\#userSelect').selectOption({ label: 'Neville Longbottom' });  
 await page.getByRole('button', { name: 'Login' }).click();  
 await page.getByRole('button', { name: 'Logout' }).click();  
 await page.waitForURL('https://www.globalsqa.com/angularJs-protractor/BankingProject/\#/customer');  
 const selectedValue \= await page.getByTestId('userSelect').inputValue();  
 expect(selectedValue).toBe('');  
});
```

## assertDepositCanBeOpened.spec.js code:
```javascript

import { test, expect } from '@playwright/test';  
import { faker } from '@faker-js/faker';

test('Assert the deposit can be opened', async ({ page }) \=\> {  
 // Step 1: Open the customer login page  
 await page.goto('https://www.globalsqa.com/angularJs-protractor/BankingProject/\#/customer');

    // Step 2: Select "Harry Potter"
    await page.locator('select\#userSelect').selectOption({ label: 'Harry Potter' });

    // Step 3: Click \[Login\]
    await page.getByRole('button', { name: 'Login' }).click();

    // Step 4: Click \[Deposit\]
    await page.getByRole('button', { name: 'Deposit' }).click();

    // Step 5: Generate random deposit amount
    const amount \= faker.number.int({ min: 1, max: 100 }).toString();

    // Step 6: Fill deposit value and click \[Deposit\]
    await page.getByPlaceholder('amount').fill(amount);
    await page.getByRole('button', { name: 'Deposit' }).nth(1).click();

    // Step 7: Assert 'Deposit Successful' message is visible
    await expect(page.getByText('Deposit Successful')).toBeVisible();

    // Step 8: Assert balance equals the deposited amount
    const balanceText \= await page.locator('.center strong').nth(1).textContent();
    expect(balanceText?.trim()).toBe(amount);

    // Step 9: Click \[Transactions\]
    await page.getByRole('button', { name: 'Transactions' }).click();

    // Step 10: Assert table header is visible
    await expect(page.locator('thead')).toBeVisible();

    await page.reload();

    // Step 11.5: Wait for at least one row to appear
    await expect(page.locator('tbody tr').first()).toBeVisible();

    // Step 12: Assert amount cell in the first row
    const displayedAmount \= await page.locator('tbody tr').first().locator('td').nth(1).textContent();
    expect(displayedAmount?.trim()).toBe(amount);

    // Step 13: Assert transaction type in the first row
    const transactionType \= await page.locator('tbody tr').first().locator('td').nth(2).textContent();
    expect(transactionType?.trim()).toBe('Credit');

});
```

## assertEmptyTransactionsLIst.spec.js code:
```javascript

import { test, expect } from '@playwright/test';

test('Assert the empty transactions list has correct values', async ({ page }) \=\> {  
 // Step 1: Open the customer login page  
 await page.goto('https://www.globalsqa.com/angularJs-protractor/BankingProject/\#/customer');

// Step 2: Select "Albus Dumbledore"  
 await page.locator('select\#userSelect').selectOption({ label: 'Albus Dumbledore' });

// Step 3: Click \[Login\]  
 await page.getByRole('button', { name: 'Login' }).click();

// Step 4: Click \[Transactions\]  
 await page.getByRole('button', { name: 'Transactions' }).click();

// Step 5: Wait for the table to be visible  
 const table \= page.locator('table.table');  
 await expect(table).toBeVisible();

// Step 6: Assert header columns  
 const headers \= table.locator('td');  
 await expect(headers.nth(0)).toHaveText('Date-Time');  
 await expect(headers.nth(1)).toHaveText('Amount');  
 await expect(headers.nth(2)).toHaveText('Transaction Type');

// Step 7: Assert no transaction rows are visible  
 const transactionRows \= table.locator('tbody tr');  
 await expect(transactionRows).toHaveCount(0);  
});
```

## assertErrorWithdrawWhenEmptyBalance.spec.js code:
```javascript

import { test, expect } from '@playwright/test';  
import { faker } from '@faker-js/faker';

test('Assert the customer cannot withdraw money with empty balance', async ({ page }) \=\> {  
 // Step 1: Open the customer login page  
 await page.goto('https://www.globalsqa.com/angularJs-protractor/BankingProject/\#/customer');

// Step 2: Select "Ron Weasly"  
 await page.locator('select\#userSelect').selectOption({ label: 'Ron Weasly' });

// Step 3: Click \[Login\]  
 await page.getByRole('button', { name: 'Login' }).click();

// Step 4: Assert the "Balance : 0" text is present  
 const balanceText \= await page.locator('.center strong').nth(1).textContent();  
 expect(balanceText?.trim()).toBe('0');

// Step 5: Click \[Withdrawl\]  
 await page.getByRole('button', { name: 'Withdrawl' }).click();

// Step 6: Type amount of money to withdraw  
 await page.getByPlaceholder('amount').fill('50');

// Step 7: Click \[Withdraw\]  
 await page.getByRole('button', { name: 'Withdraw', exact: true }).click();

// Step 8: Assert error message is visible  
 await expect(page.getByText('Transaction Failed. You can not withdraw amount more than the balance.')).toBeVisible();  
});
```
Created by Alina Kuliak
