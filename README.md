# Vaseegrah Veda Manual Testing

This repository contains manual test cases and recorded execution results for the Vaseegrah Veda website. The test suite covers common customer account and shopping workflows, including login, product search, cart actions, and wishlists.

## Project Objectives

- Check that key customer workflows behave as expected.
- Record test steps, test data, expected results, actual results, and execution status.
- Track defects found during testing.
- Map test cases to coverage areas using a Requirements Traceability Matrix (RTM).

## Coverage

The workbook includes test cases for:

- **Login:** Valid and invalid credentials, blank fields, and password visibility.
- **Registration:** New account setup, password confirmation, invalid email, and duplicate email handling.
- **Logout:** Successful logout and restricted page access after logout.
- **Forgot Password:** Reset requests, email content, reset links, and use of a new password.
- **Search:** Full and partial product names, empty searches, case variations, special characters, numbers, and language input.
- **Cart:** Adding a product, checking cart details and totals, removing a product, and verifying the empty cart.
- **Wishlist:** Adding and removing products and checking the empty wishlist state.
- **Account Details:** Updating profile details and validating password changes.

## Test Results

The workbook currently records **43 test cases**:

| Status | Count |
|---|---:|
| Passed | 41 |
| Failed | 1 |
| Not Run | 1 |

The failed case checks whether the site rejects a password change when the current password is incorrect. The workbook records that the password change succeeded unexpectedly. This case is linked to an open defect in the Bug Report sheet.

The Bug Report sheet also records an open issue for login with a mobile number. Review the defect status in the workbook before treating either issue as resolved.

These totals reflect the statuses recorded in the workbook and may change as testing continues.

## Workbook Contents

- **Test Summary:** Overall counts and results by module.
- **RTM:** Links inferred coverage requirements to test case IDs and execution statuses.
- **Environment Setup:** Fields for the application, environment, URL, operating system, browser, device, role, database, build, tester, and execution date.
- **Module sheets:** Detailed test scenarios, preconditions, steps, test data, expected results, actual results, and statuses.
- **Bug Report:** Defect IDs, related test cases, reproduction steps, expected and actual results, severity, priority, and status.

## RTM Note

The workbook did not include a formal requirements specification. The requirement IDs and descriptions in the RTM were therefore inferred from the test scenarios. Replace or update them when approved requirement IDs become available.

## How to Execute a Test

1. Select the relevant module sheet and review the test case.
2. Confirm that the preconditions are met and use an approved test account and test data.
3. Follow the steps in order.
4. Record what actually happened in **Actual Result**.
5. Set the **Status** based on the observed result.
6. If the actual result differs from the expected result, record the issue in the Bug Report sheet and include the related test case ID.
7. Update the Test Summary and RTM when execution results change.

## Status Definitions

- **Pass:** The observed result matches the expected result.
- **Fail:** The observed result does not match the expected result.
- **Not Run:** The test has not yet been executed.

## Defect Reporting

When recording a defect, include clear reproduction steps and the expected and actual behavior. Assign severity and priority according to the project’s conventions, and update the defect status as it is investigated and fixed.

## Environment and Test Data

Record the environment and execution details in the Environment Setup sheet. Use only approved test accounts and non-production test data. Do not add passwords, access tokens, or other credentials to this repository or workbook.
