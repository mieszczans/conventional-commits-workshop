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
