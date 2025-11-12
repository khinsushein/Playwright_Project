<img alt="Static Badge" src="https://img.shields.io/badge/Playwright-1.56.1-blue">

<img alt="tests" src="https://img.shields.io/github/actions/workflow/status/khinsushein/Playwright_project_01/playwright.yml?label=tests">

Project 1 – Automation Testing for Authentication & Shopping Flow
This project demonstrates automated testing of the Demoblaze application using Playwright and the Page Object Model (POM).

It covers both successful and failed login scenarios, and explains how the setup can be extended and scaled across products, browsers, and CI/CD.

### Running the Tests
## Run all tests (headed mode):
  npx playwright test --headed
## Run with UI
  npx playwright test --ui
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

### Playwright API + UI Tests for Demoblaze

<img alt="Playwright CI" src="https://github.com/khinsushein/Playwright_project_01/actions/workflows/playwright.yml/badge.svg?branch=main">

### HTML Report 
Download latest HTML report

### Author 

Khin Su Shein — QA Automation Engineer
Based in France, open to Luxembourg/Switzerland roles
