# E-Commerce Application — Test Data

## 1. Document Information

| Attribute | Details |
|---|---|
| Project | E-Commerce Web Application |
| Application Under Test | SauceDemo |
| Document | Test Data Specification |
| Version | 1.0 |
| Status | Draft |
| QA Owner | QA Engineering Team |

---

# 2. Objective

This document defines the test data required to execute the functional,
negative, security-oriented and end-to-end test scenarios for the
application.

Test data is designed to support:

- Positive testing
- Negative testing
- Boundary testing
- End-to-end testing
- Regression testing
- Security-oriented testing
- Exploratory testing

No real customer or financial information will be used.

---

# 3. Authentication Test Data

> Demo credentials should be validated against the current application
> before execution because demo environments can change.

| Data ID | Username Type | Username | Password | Expected Usage |
|---|---|---|---|---|
| AUTH-001 | Valid | Valid demo user | Valid demo password | Successful login |
| AUTH-002 | Invalid username | Invalid username | Valid demo password | Invalid username |
| AUTH-003 | Invalid password | Valid demo user | Invalid password | Invalid password |
| AUTH-004 | Invalid both | Invalid username | Invalid password | Invalid credentials |
| AUTH-005 | Empty username | Empty | Valid demo password | Required-field validation |
| AUTH-006 | Empty password | Valid demo user | Empty | Required-field validation |
| AUTH-007 | Empty both | Empty | Empty | Required-field validation |

---

# 4. Checkout Test Data

| Data ID | First Name | Last Name | Postal Code | Expected Usage |
|---|---|---|---|---|
| CHECK-001 | ValidFirst | ValidLast | 560001 | Valid checkout |
| CHECK-002 | Empty | ValidLast | 560001 | Missing first name |
| CHECK-003 | ValidFirst | Empty | 560001 | Missing last name |
| CHECK-004 | ValidFirst | ValidLast | Empty | Missing postal code |
| CHECK-005 | Empty | Empty | Empty | All mandatory fields missing |
| CHECK-006 | Test@123 | ValidLast | 560001 | Special-character validation |
| CHECK-007 | ValidFirst | Test@123 | 560001 | Special-character validation |
| CHECK-008 | ValidFirst | ValidLast | ABC123 | Invalid postal-code format |
| CHECK-009 | ValidFirst | ValidLast | 1 | Boundary/short input |
| CHECK-010 | ValidFirst | ValidLast | 999999999999 | Boundary/long input |

---

# 5. Product Test Data

The product data will be captured from the application during execution.

| Data ID | Product Selection | Usage |
|---|---|---|
| PROD-001 | Single product | Single-product purchase |
| PROD-002 | Two different products | Multiple-product purchase |
| PROD-003 | Multiple products | Cart validation |
| PROD-004 | Product added then removed | Remove-product validation |
| PROD-005 | All selected products removed | Empty-cart validation |

---

# 6. Cart Test Data

## Scenario: Single Product

```text
Product A
    ↓
Add to Cart
    ↓
Cart should contain Product A