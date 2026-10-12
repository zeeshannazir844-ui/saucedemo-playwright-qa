# SauceDemo SQA Assessment — Playwright

## Prerequisites
- Node.js and npm
- Internet access to https://www.saucedemo.com/

## Install
```bash
npm install
npx playwright install chromium
```

## Run tests
```bash
npm test
```

Run with a visible browser:
```bash
npm run test:headed
```

Open the HTML report after a run:
```bash
npm run report
```

## Test coverage
- Login as `standard_user`
- Verify inventory page
- Add one product and verify cart badge
- Verify cart item count
- Complete checkout with synthetic details
- Verify order-completion page and heading

## Design notes
The test uses Playwright Test with JavaScript, user-facing locators, assertions on page state, and no fixed sleeps. Screenshots and traces are retained on failure.

## Limitations
This is a single happy-path smoke test, not a complete regression suite. It does not cover invalid credentials, blank required fields, remove-from-cart, sorting, keyboard accessibility, responsive layouts, network interruption or cross-browser behaviour. Verify selectors against the current application and do not report a pass unless the actual test run passes.
