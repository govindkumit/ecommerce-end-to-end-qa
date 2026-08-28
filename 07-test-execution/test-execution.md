# E-Commerce Application — Test Execution Report

## 1. Execution Information

| Attribute | Details |
|---|---|
| Project | E-Commerce Web Application |
| Application | SauceDemo |
| Test Cycle | Cycle 1 — Functional & E2E |
| Environment | Demo/Test Environment |
| OS | Windows |
| Browser | Microsoft Edge |
| Execution Date | Completed |
| Executed By | QA Engineering Team |
| Status | Completed |

---

# 2. Execution Objective

The objective of this execution cycle was to validate the defined test
cases against the application and record the actual observed results.

All results in this document are based on the completed manual test
execution performed against the application.

---

# 3. Execution Status Definitions

| Status | Meaning |
|---|---|
| PASS | Actual behavior matches expected behavior |
| FAIL | Actual behavior does not match expected behavior |
| BLOCKED | Test cannot be executed because of a blocking condition |
| NOT EXECUTED | Test has not yet been executed |
| N/A | Test is not applicable to the current environment |

---

# 4. Test Execution Results

| Test Case ID | Scenario | Priority | Result | Actual Result | Defect ID |
|---|---|---|---|---|---|
| TC-LOGIN-001 | Login with valid credentials | P0 | PASS | User logged in successfully | |
| TC-LOGIN-002 | Login with invalid username | P0 | PASS | Appropriate error message displayed | |
| TC-LOGIN-003 | Login with invalid password | P0 | PASS | Appropriate error message displayed | |
| TC-LOGIN-004 | Login with empty username | P1 | PASS | Appropriate validation message displayed | |
| TC-LOGIN-005 | Login with empty password | P1 | PASS | Appropriate validation message displayed | |
| TC-PROD-001 | Verify product listing | P0 | PASS | Product listing displayed correctly | |
| TC-PROD-002 | Verify product information | P1 | FAIL | Product image does not match product name for `problem_user` | BUG-001 |
| TC-PROD-003 | Verify product details | P1 | PASS | Product details displayed correctly | |
| TC-SORT-001 | Sort products by name ascending | P2 | PASS | Products sorted by name ascending | |
| TC-SORT-002 | Sort products by name descending | P2 | PASS | Products sorted by name descending | |
| TC-SORT-003 | Sort products by price ascending | P2 | PASS | Products sorted by price ascending | |
| TC-SORT-004 | Sort products by price descending | P2 | PASS | Products sorted by price descending | |
| TC-CART-001 | Add one product to cart | P0 | PASS | Product added successfully | |
| TC-CART-002 | Verify cart count | P0 | PASS | Cart count displayed correctly | |
| TC-CART-003 | Add multiple products | P0 | PASS | Multiple products added successfully | |
| TC-CART-004 | Remove product from cart | P0 | PASS | Product removed successfully | |
| TC-CART-005 | Remove one product while retaining others | P1 | PASS | Selected product removed and remaining products retained | |
| TC-CART-006 | Verify empty cart | P1 | PASS | Empty cart displayed correctly | |
| TC-CHECK-001 | Navigate to checkout | P0 | PASS | Checkout page opened successfully | |
| TC-CHECK-002 | Checkout with valid information | P0 | PASS | Checkout information accepted successfully | |
| TC-CHECK-003 | Missing first name | P0 | PASS | Appropriate validation message displayed | |
| TC-CHECK-004 | Missing last name | P0 | PASS | Appropriate validation message displayed | |
| TC-CHECK-005 | Missing postal code | P0 | PASS | Appropriate validation message displayed | |
| TC-ORDER-001 | Verify order overview | P0 | PASS | Order overview displayed correctly | |
| TC-ORDER-002 | Complete successful order | P0 | PASS | Order completed successfully | |
| TC-ORDER-003 | Verify order contains selected product | P0 | PASS | Selected product displayed in order summary | |
| TC-SEC-001 | Logout authenticated user | P0 | PASS | User logged out successfully | |
| TC-SEC-002 | Verify protected access after logout | P0 | PASS | Protected application access was restricted after logout | |
| TC-E2E-001 | Complete customer purchase journey | P0 | PASS | Complete purchase journey completed successfully | |
| TC-E2E-002 | Multiple-product purchase journey | P0 | PASS | Multiple-product purchase journey completed successfully | |

---

# 5. Execution Summary

| Metric | Count |
|---|---:|
| Total Planned Test Cases | 30 |
| Executed | 30 |
| Passed | 29 |
| Failed | 1 |
| Blocked | 0 |
| Not Executed | 0 |
| Execution Progress | 100% |
| Pass Rate | 96.67% |
| Fail Rate | 3.33% |

### Execution Result

```text
30 Test Cases Executed
        |
        +---- 29 PASS
        |
        +---- 1 FAIL
               |
               +---- TC-PROD-002
                        |
                        +---- BUG-001