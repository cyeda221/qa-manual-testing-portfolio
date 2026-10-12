# Sample Bug Reports

**Project Type:** Practice / Sample  
**Module:** Login and Authentication  
**Document Status:** Illustrative examples — not verified against a live application

This document demonstrates how I report defects with clear reproduction steps, expected results, actual results, severity, and priority.

## BUG-001: Login Form Accepts Empty Fields

**Severity:** Major (proposed)  
**Priority:** High (proposed)  
**Environment:** Sample web application; browser and version not specified  
**Status:** Illustrative example; not executed

### Preconditions
The login page is open.

### Steps to Reproduce
1. Open the login page.
2. Leave the username field empty.
3. Leave the password field empty.
4. Click the Login button.

### Expected Result
The application should prevent submission and display appropriate required-field validation.

### Actual Result (Hypothetical)
The form submits without displaying required-field validation.

### Impact
Users may encounter confusing behavior when required information is missing.

---

## BUG-002: Password Is Displayed as Plain Text by Default

**Severity:** Major (proposed; requires security review)  
**Priority:** High (proposed)  
**Environment:** Sample web application; browser and version not specified  
**Status:** Illustrative example; not executed

### Preconditions
The login page is open.

### Steps to Reproduce
1. Click the password field.
2. Enter a sample password.
3. Observe the characters displayed in the field.

### Expected Result
The password should be masked by default unless the application intentionally provides a controlled visibility feature.

### Actual Result (Hypothetical)
The entered password is visible as plain text without the user enabling a visibility option.

### Impact
Sensitive credentials may be exposed to someone viewing the screen.

---

## BUG-003: Invalid Credentials Produce No Feedback

**Severity:** Medium (proposed)  
**Priority:** Medium (proposed)  
**Environment:** Sample web application; browser and version not specified  
**Status:** Illustrative example; not executed

### Preconditions
The login page is open.

### Steps to Reproduce
1. Enter an invalid username or password.
2. Click Login.
3. Observe the page.

### Expected Result
The application should reject authentication and provide appropriate, non-sensitive feedback.

### Actual Result (Hypothetical)
The application rejects the login but provides no visible feedback to the user.

### Impact
Users may be unsure whether the login attempt was processed.

---

## Reporting Notes

- All three defects are hypothetical examples for portfolio demonstration.
- Severity and priority are proposed classifications and should be confirmed against project standards.
- Actual results must be replaced with observed behavior before reporting any defect as real.
- Evidence such as screenshots, logs, browser details, and reproducible steps should be attached when available.
