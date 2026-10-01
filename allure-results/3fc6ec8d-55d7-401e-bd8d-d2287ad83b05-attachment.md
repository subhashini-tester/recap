# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: auto_test_store.spec.ts >> automation_test_store_scenario1 >> s1_tc_004 customize product colour 
- Location: tests/auto_test_store.spec.ts:117:9

# Error details

```
Error: locator.click: Test ended.
Call log:
  - waiting for getByRole('button', { name: ' Confirm Order' })

```

# Test source

```ts
  1 | import{Page}from"@playwright/test";
  2 | import{checkoutConfirmationLocators}from"../locators/checkoutConfirmationLocators.ts";
  3 | export class CheckoutConfirmationPage{
  4 |     constructor(private page:Page){}
  5 |     async verifyOrderConfirmation(){
> 6 |         await this.page.getByRole(checkoutConfirmationLocators.confirmOrderButton.role,{name:checkoutConfirmationLocators.confirmOrderButton.name}).click();
    |                                                                                                                                                     ^ Error: locator.click: Test ended.
  7 |     }
  8 | }
```