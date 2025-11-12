<img alt="Static Badge" src="https://img.shields.io/badge/Playwright-1.56.1-blue">

<img alt="tests" src="https://img.shields.io/github/actions/workflow/status/khinsushein/Playwright_project/playwright.yml?label=tests">

Project 1 – Automation Testing for Authentication & Shopping Flow
This project demonstrates automated testing of the Demoblaze application using Playwright and the Page Object Model (POM).

It covers both successful and failed login scenarios, and explains how the setup can be extended and scaled across products, browsers, and CI/CD.

### Running the Tests
## Run all tests (headed mode):
  npx playwright test --headed
## Run with UI
  npx playwright test --ui
### Running the Tests

#### Run all tests (headed mode):
```
npx playwright test --headed
```

#### Run with Playwright UI:
```
npx playwright test --ui
```

#### Run all tests (default/headless):
```
npx playwright test
```
### Features Demonstrated

Sign-up: Create a new user
Log in: User login
Log out: User logout
Shopping Flow: Login → Add to cart → Place order → View receipt → Logout
Negative Tests:
Login with non-existent user
Login with wrong password
API Endpoints Test:
GET /entries – fetch all product items
POST /view – verify product details by ID
Category extraction and validation
Schema and data consistency checks

### Architecture

Page Object Model: Centralized selectors in LoginPage.ts for maintainability.
CI/CD Ready: Supports environment-based secrets, artifacts, and selective test runs.

### CI/CD with GitHub Actions

This project uses a [GitHub Actions workflow](.github/workflows/playwright.yml) to automatically run Playwright tests on every push and pull request to the `main` branch.

- Tests run on both Chromium and Firefox browsers.
- JUnit and HTML reports are uploaded as workflow artifacts.
- Test results are published as PR comments and summarized in the job summary.

#### Downloading Reports
After a workflow run, you can download the latest HTML and JUnit reports from the GitHub Actions run artifacts section.

### Playwright API + UI Tests for Demoblaze

<img alt="Playwright CI" src="https://github.com/khinsushein/Playwright_project/actions/workflows/playwright.yml/badge.svg?branch=main">

### HTML & JUnit Reports
You can download the latest HTML and JUnit reports from the "Artifacts" section of each GitHub Actions run.

### Author 

Khin Su Shein — QA Automation Engineer
Based in France, open to Luxembourg/Switzerland roles
