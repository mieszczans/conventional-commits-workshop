# User Story: Secure Authentication & Dashboard System

---

## 🧩 User Story

**Title:**  
_As a user, I want to create an account, log in, and manage my profile from a secure dashboard, so that I can personalize my experience in the web app._

---

### **Acceptance Criteria**

1. Users can register with email, password, and name.
2. The app validates inputs and provides meaningful errors.
3. Users can log in and receive a JWT token.
4. Users can reset their password via email.
5. Users see a personalized dashboard with profile info.
6. The design matches the app’s theme and is mobile-responsive.
7. The codebase has CI/CD pipelines, unit & integration tests.
8. Documentation is available for developers and users.
9. App follows secure coding and performance best practices.

---

## 🪜 Full Commit Breakdown (Conventional Commits Practice)

Below is a **list of 25 commits** showing how you might implement the above story — all following **Conventional Commits** syntax (and covering _every_ major type used by `@commitlint/config-conventional`).

| #                                                                  | Commit Message                                         | Description |
| ------------------------------------------------------------------ | ------------------------------------------------------ | ----------- |
| 1 `: implement user registration endpoint with email and password` | Adds initial user registration logic on backend.       |
| 2 `: create signup and login pages with form validation`           | Adds front-end forms and client-side validation.       |
| 3 `: add JWT-based login and session handling`                     | Enables secure authentication with JWT tokens.         |
| 4 `: implement password reset via email token`                     | Adds password reset functionality.                     |
| 5 `: display personalized welcome message and profile data`        | Adds user dashboard after login.                       |
| 6 `: handle expired token errors gracefully`                       | Fixes bug when tokens expire mid-session.              |
| 7 `: prevent form submission with empty inputs`                    | Fixes front-end validation issue.                      |
| 8 `: document authentication endpoints in README`                  | Adds API documentation for auth routes.                |
| 9 `: update onboarding guide for new developers`                   | Updates developer setup instructions.                  |
| 10 `: apply consistent spacing and colors across forms`            | Standardizes UI appearance.                            |
| 11 `: reformat codebase with Prettier and ESLint rules`            | Applies formatting and linting rules.                  |
| 12 `: extract token generation logic into helper function`         | Refactors code for better reuse.                       |
| 13 `: split dashboard components into smaller reusable parts`      | Improves component architecture.                       |
| 14 `: cache user profile data for faster dashboard load`           | Improves performance with caching.                     |
| 15 `: optimize query for user lookup by adding index`              | Adds DB index to speed up login.                       |
| 16 `: add unit tests for registration and login endpoints`         | Adds test coverage for backend auth logic.             |
| 17 `: add integration tests for login flow with Cypress`           | Adds end-to-end test for login.                        |
| 18 `: update react and express to latest stable versions`          | Updates main dependencies.                             |
| 19 `: add webpack alias for shared utils`                          | Configures build system for better imports.            |
| 20 `: add workflow for running tests and linting`                  | Adds GitHub Actions CI workflow.                       |
| 21 `: build and push Docker image on main branch`                  | Adds Docker build step in CI pipeline.                 |
| 22 `: add .env.example and update .gitignore`                      | Adds environment template and ignores sensitive files. |
| 23 `: update issue templates and PR guidelines`                    | Adds better contribution setup.                        |
| 24 `: remove caching layer that caused stale profile data`         | Reverts a faulty performance change.                   |
| 25 `: add semantic-release for automatic versioning`               | Sets up automated release versioning.                  |
