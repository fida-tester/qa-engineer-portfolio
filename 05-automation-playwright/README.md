# Playwright Automation (Sample Framework)

## Overview
This folder contains sample Playwright UI automation tests for demonstration purposes.

## Prerequisites
- Node.js (LTS)
- npm

## Setup
```bash
npm install
npm run install:pw

npm test

npm run test:headed

npm run report

```js
const { test, expect } = require("@playwright/test");

test.describe("Login - demo site", () => {
  test("Successful login redirects to inventory", async ({ page }) => {
    await page.goto("https://www.saucedemo.com/");

    await page.fill("#user-name", "standard_user");
    await page.fill("#password", "secret_sauce");
    await page.click("#login-button");

    await expect(page).toHaveURL(/inventory/);
    await expect(page.locator(".inventory_list")).toBeVisible();
  });

  test("Invalid login shows error message", async ({ page }) => {
    await page.goto("https://www.saucedemo.com/");

    await page.fill("#user-name", "standard_user");
    await page.fill("#password", "wrong_password");
    await page.click("#login-button");

    await expect(page.locator("[data-test='error']")).toBeVisible();
  });
});
