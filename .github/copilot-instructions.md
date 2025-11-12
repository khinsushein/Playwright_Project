# Copilot Instructions for Playwright Project

## Project Overview
- **Purpose:** Automated end-to-end and API testing for authentication and shopping flows on Demoblaze.
- **Framework:** Playwright (`@playwright/test`), TypeScript.
- **Architecture:**
  - **Page Object Model:** Centralized selectors/actions in `pages/` (e.g., `LoginPage.ts`).
  - **Test Specs:** Located in `e2e/` and `tests-examples/`. Each spec targets a user flow or API endpoint.
  - **Helpers/Utils:** Shared logic in `helpers/` and `utils/`.
  - **Config:** `playwright.config.ts` sets baseURL, reporters, trace/video/screenshot options, and project matrix (Chromium/Firefox).

## Developer Workflows
- **Run all tests (headed):**
  npx playwright test --headed
- **Run with UI:**
  npx playwright test --ui
- **Show HTML report:**
  npx playwright show-report
- **CI/CD:**
  - GitHub Actions workflow: `.github/workflows/playwright.yml` runs tests for both browsers, uploads JUnit and HTML reports, and publishes results as PR comments.
  - Artifacts: JUnit XML in `results/`, HTML report in `playwright-report/`.

## Conventions & Patterns
- **Test Data:**
  - Environment variables in `env/.env` (e.g., `TEST_USER_EMAIL`, `TEST_USER_PASSWORD`).
  - Use `process.env` for secrets in tests/config.
- **Selectors:**
  - Store selectors in page objects (`pages/`).
  - Prefer data-test attributes for robust selection.
- **Reporting:**
  - JUnit and HTML reporters configured in `playwright.config.ts`.
  - Trace, video, and screenshot capture enabled for all tests.
- **Project Matrix:**
  - Tests run for both Chromium and Firefox via Playwright's `projects` config.
- **API Testing:**
  - API endpoint tests included in specs (GET `/entries`, POST `/view`).
  - Validate schema and data consistency.

## Integration Points
- **External Dependencies:**
  - `glob` for artifact handling in CI.
  - Playwright devices for browser emulation.
- **Artifacts:**
  - Test results: `results/`, `test-results/`, `playwright-report/`.
  - Reports are uploaded as CI artifacts and can be viewed/downloaded from GitHub Actions.

## Examples
- **Page Object Usage:** See `pages/LoginPage.ts` for login selectors/actions.
- **Test Spec:** See `e2e/example.spec.ts` for a sample test structure.
- **Config:** See `playwright.config.ts` for baseURL, reporters, and project matrix.

## Quickstart for AI Agents
- Use page objects for selectors/actions.
- Place new specs in `e2e/` or `tests-examples/`.
- Use environment variables for secrets/test data.
- Validate test results with HTML/JUnit reports.
- Follow Playwright best practices for assertions and error handling.

---
For unclear or missing conventions, ask the user for clarification or examples from their workflow.
