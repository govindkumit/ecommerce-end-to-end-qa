# Defect Report

## Defect Summary

| Field | Details |
|---|---|
| Defect ID | BUG-001 |
| Title | Product image does not match product name |
| Module | Product / Inventory |
| Test Case | TC-PROD-002 |
| Environment | SauceDemo Web Application |
| Test Account | problem_user |
| Severity | Medium |
| Priority | P1 |
| Status | Open |
| Defect Type | Functional / UI Data Mismatch |

---

# 1. Defect Description

During functional testing of the product inventory page, a mismatch
was identified between the displayed product image and the associated
product name when using the `problem_user` account.

The product information presented to the customer is inconsistent,
which can result in incorrect product identification.

---

# 2. Preconditions

1. SauceDemo application is accessible.
2. User has valid demo credentials.
3. `problem_user` account is used.
4. User is able to successfully log in.

---

# 3. Steps to Reproduce

1. Open the SauceDemo application.
2. Enter username:

```text
problem_user