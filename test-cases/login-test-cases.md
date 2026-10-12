# Login Functionality — Test Cases

**Project Type:** Practice / Sample  
**Module:** Login  
**Test Type:** Functional Testing  
**Priority:** High  
**Status:** Test cases designed; execution pending

## Objective

Validate that users can log in with valid credentials and that invalid inputs, empty fields, and incorrect credentials are handled appropriately.

## Preconditions

- The application is available.
- A valid test account exists.
- The tester can access the login page.

## Test Cases

| Test Case ID | Scenario | Test Steps | Expected Result | Priority |
|---|---|---|---|---|
| LOGIN-001 | Login with valid credentials | Enter valid username and password, then click Login | User is authenticated and redirected to the appropriate page | High |
| LOGIN-002 | Login with an incorrect password | Enter a valid username and incorrect password, then click Login | Login is rejected and an appropriate error message appears | High |
| LOGIN-003 | Login with an unregistered username | Enter an unregistered username and a password, then click Login | Login is rejected without exposing sensitive account information | High |
| LOGIN-004 | Submit empty fields | Leave username and password empty, then click Login | Required-field validation is displayed | High |
| LOGIN-005 | Submit an empty username | Leave username empty, enter a password, then click Login | Username validation is displayed and login is not completed | Medium |
| LOGIN-006 | Submit an empty password | Enter a username, leave password empty, then click Login | Password validation is displayed and login is not completed | High |
| LOGIN-007 | Toggle password visibility | Enter a password and use the visibility control, if available | Password visibility changes correctly without altering the entered value | Low |
| LOGIN-008 | Navigate to password recovery | Click the Forgot Password link, if available | The password recovery flow opens | Medium |
| LOGIN-009 | Verify password masking | Enter a password in the password field | Password characters are masked by default | Medium |
| LOGIN-010 | Verify login after logout | Log in, log out, then attempt to revisit a protected page | Access follows the application's intended session and authorization rules | High |

## Execution Results

Tests have not yet been executed against a real application. Actual results and pass/fail status will be recorded after execution.

## Notes

- Test cases are sample portfolio material.
- Actual behavior should be compared against approved requirements.
- Error messages, password visibility, and recovery behavior may vary by application design.
