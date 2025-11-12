# User Story: Secure Authentication & Dashboard System (Updated with Breaking Changes)

**Date:** 2025-11-12

---

## 🧩 User Story - FRON-909012

**Title:**  
_As a user, I want to sign in using my Google or GitHub account and manage my subscription tier from a secure dashboard, so that I can access premium features easily._

---

### **Business Context**

After the MVP launch, **investors requested** a pivot:

- Replace manual registration with **OAuth2 social login (Google & GitHub)**.
- Introduce **subscription tiers (Free / Pro / Enterprise)** to the dashboard.
- Remove password-based authentication entirely.

This decision affects both **frontend and backend** architecture, and it introduces **breaking changes** to existing APIs and user data structures.

---

### **Acceptance Criteria**

1. Users can sign in using Google or GitHub.
2. The previous email/password registration flow is removed.
3. The dashboard shows subscription status and upgrade options.
4. Existing users are migrated or prompted to reauthenticate.
5. OAuth2 tokens are securely stored and refreshed.
6. New “Pro” and “Enterprise” subscription features are displayed.
7. CI/CD and documentation reflect the new flow.
8. Old API endpoints for `/auth/register` and `/auth/login` are deprecated.

---

## 🪜 Full Commit Breakdown (Conventional Commits + Breaking Changes)

Below is the **updated commit list** (total ~30 commits).  
The new commits (26–30) introduce breaking changes and migration steps.

| #   | Type                                                                      | Commit Message                                                          | Description |
| --- | ------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------- |
| 1   | `: implement user registration endpoint with email and password`          | Adds initial user registration logic on backend.                        |
| 2   | `: create signup and login pages with form validation`                    | Adds front-end forms and client-side validation.                        |
| 3   | `: add JWT-based login and session handling`                              | Enables secure authentication with JWT tokens.                          |
| 4   | `: implement password reset via email token`                              | Adds password reset functionality.                                      |
| 5   | `: display personalized welcome message and profile data`                 | Adds user dashboard after login.                                        |
| 6   | `: handle expired token errors gracefully`                                | Fixes bug when tokens expire mid-session.                               |
| 7   | `: prevent form submission with empty inputs`                             | Fixes front-end validation issue.                                       |
| 8   | `: document authentication endpoints in README`                           | Adds API documentation for auth routes.                                 |
| 9   | `: update onboarding guide for new developers`                            | Updates developer setup instructions.                                   |
| 10  | `: apply consistent spacing and colors across forms`                      | Standardizes UI appearance.                                             |
| 11  | `: reformat codebase with Prettier and ESLint rules`                      | Applies formatting and linting rules.                                   |
| 12  | `: extract token generation logic into helper function`                   | Refactors code for better reuse.                                        |
| 13  | `: split dashboard components into smaller reusable parts`                | Improves component architecture.                                        |
| 14  | `: cache user profile data for faster dashboard load`                     | Improves performance with caching.                                      |
| 15  | `: optimize query for user lookup by adding index`                        | Adds DB index to speed up login.                                        |
| 16  | `: add unit tests for registration and login endpoints`                   | Adds test coverage for backend auth logic.                              |
| 17  | `: add integration tests for login flow with Cypress`                     | Adds end-to-end test for login.                                         |
| 18  | `: update react and express to latest stable versions`                    | Updates main dependencies.                                              |
| 19  | `: add webpack alias for shared utils`                                    | Configures build system for better imports.                             |
| 20  | `: add workflow for running tests and linting`                            | Adds GitHub Actions CI workflow.                                        |
| 21  | `: build and push Docker image on main branch`                            | Adds Docker build step in CI pipeline.                                  |
| 22  | `: add .env.example and update .gitignore`                                | Adds environment template and ignores sensitive files.                  |
| 23  | `: update issue templates and PR guidelines`                              | Adds better contribution setup.                                         |
| 24  | `: remove caching layer that caused stale profile data`                   | Reverts a faulty performance change.                                    |
| 25  | `: add semantic-release for automatic versioning`                         | Sets up automated release versioning.                                   |
| 26  | `: migrate authentication from email/password to OAuth2 (Google, GitHub)` | **BREAKING CHANGE:** removes password-based login and adds OAuth2 flow. |
| 27  | `: remove /auth/register and /auth/login endpoints`                       | **BREAKING CHANGE:** deprecated endpoints removed; client must update.  |
| 28  | `: add subscription tiers (Free, Pro, Enterprise)`                        | Introduces tiered user plans and dashboard visibility.                  |
| 29  | `: update README and API docs for OAuth2 migration`                       | **BREAKING CHANGE:** replaces old examples and endpoints.               |
| 30  | `: migrate user schema to support OAuth2 provider IDs`                    | **BREAKING CHANGE:** alters database schema; migration required.        |

---
