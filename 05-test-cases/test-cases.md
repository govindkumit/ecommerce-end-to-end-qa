# E-Commerce Application — Test Cases

## 1. Document Information

| Attribute | Details |
|---|---|
| Project | E-Commerce Web Application |
| Application Under Test | SauceDemo |
| Document | Detailed Test Cases |
| Version | 1.0 |
| Status | Draft |
| QA Owner | QA Engineering Team |

---

# 2. Test Case Fields

| Field | Description |
|---|---|
| Test Case ID | Unique test identifier |
| Requirement | Related requirement |
| Scenario | Related test scenario |
| Test Type | Functional / Negative / Security / E2E etc. |
| Priority | P0 / P1 / P2 / P3 |
| Preconditions | Conditions required before execution |
| Test Data | Data required |
| Steps | Detailed execution steps |
| Expected Result | Expected application behavior |
| Automation Candidate | Whether suitable for automation |

---

# 3. Authentication Test Cases

## TC-LOGIN-001 — Login with valid credentials

| Field | Details |
|---|---|
| Requirement | FR-001 |
| Scenario | TS-LOGIN-001 |
| Test Type | Functional / Positive |
| Priority | P0 |
| Preconditions | Application is accessible |
| Test Data | Valid username and password |
| Automation Candidate | Yes |

### Steps

1. Open the application.
2. Enter a valid username.
3. Enter a valid password.
4. Click Login.

### Expected Result

User is successfully authenticated and redirected to the product
listing page.

---

## TC-LOGIN-002 — Login with invalid username

| Field | Details |
|---|---|
| Requirement | FR-001 |
| Scenario | TS-LOGIN-002 |
| Test Type | Functional / Negative |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Open the application.
2. Enter an invalid username.
3. Enter a valid password.
4. Click Login.

### Expected Result

Login fails and an appropriate error message is displayed.

---

## TC-LOGIN-003 — Login with invalid password

| Field | Details |
|---|---|
| Requirement | FR-001 |
| Scenario | TS-LOGIN-003 |
| Test Type | Functional / Negative |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Open the application.
2. Enter a valid username.
3. Enter an invalid password.
4. Click Login.

### Expected Result

Login fails and an appropriate error message is displayed.

---

## TC-LOGIN-004 — Login with empty username

| Field | Details |
|---|---|
| Requirement | FR-001 |
| Scenario | TS-LOGIN-005 |
| Test Type | Negative |
| Priority | P1 |
| Automation Candidate | Yes |

### Steps

1. Open the application.
2. Leave username empty.
3. Enter a valid password.
4. Click Login.

### Expected Result

Login is rejected and validation information is displayed.

---

## TC-LOGIN-005 — Login with empty password

| Field | Details |
|---|---|
| Requirement | FR-001 |
| Scenario | TS-LOGIN-006 |
| Test Type | Negative |
| Priority | P1 |
| Automation Candidate | Yes |

### Steps

1. Open the application.
2. Enter a valid username.
3. Leave password empty.
4. Click Login.

### Expected Result

Login is rejected and validation information is displayed.

---

# 4. Product Test Cases

## TC-PROD-001 — Verify product listing after login

| Field | Details |
|---|---|
| Requirement | FR-002 |
| Scenario | TS-PROD-001 |
| Test Type | Functional |
| Priority | P0 |
| Preconditions | User is successfully logged in |
| Automation Candidate | Yes |

### Steps

1. Log in using valid credentials.
2. Observe the product listing page.

### Expected Result

Available products are displayed correctly.

---

## TC-PROD-002 — Verify product information

| Field | Details |
|---|---|
| Requirement | FR-002 |
| Scenario | TS-PROD-002 / TS-PROD-003 |
| Test Type | Functional |
| Priority | P1 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Select a product.
3. Observe product name, price and image.

### Expected Result

Product name, price and image are displayed correctly.

---

## TC-PROD-003 — Verify product details

| Field | Details |
|---|---|
| Requirement | FR-003 |
| Scenario | TS-DETAIL-001 |
| Test Type | Functional |
| Priority | P1 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Select a product from the product listing.
3. Open the product details.

### Expected Result

The product details correspond to the selected product.

---

# 5. Product Sorting Test Cases

## TC-SORT-001 — Sort products by name ascending

| Field | Details |
|---|---|
| Requirement | FR-004 |
| Scenario | TS-SORT-002 |
| Test Type | Functional |
| Priority | P2 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Open the product sorting control.
3. Select name ascending.
4. Observe the product order.

### Expected Result

Products are displayed in alphabetical ascending order.

---

## TC-SORT-002 — Sort products by name descending

| Field | Details |
|---|---|
| Requirement | FR-004 |
| Scenario | TS-SORT-003 |
| Test Type | Functional |
| Priority | P2 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Select name descending.
3. Observe the product order.

### Expected Result

Products are displayed in alphabetical descending order.

---

## TC-SORT-003 — Sort products by price ascending

| Field | Details |
|---|---|
| Requirement | FR-004 |
| Scenario | TS-SORT-004 |
| Test Type | Functional |
| Priority | P2 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Select price low-to-high.
3. Observe product prices.

### Expected Result

Products are displayed from lowest price to highest price.

---

## TC-SORT-004 — Sort products by price descending

| Field | Details |
|---|---|
| Requirement | FR-004 |
| Scenario | TS-SORT-005 |
| Test Type | Functional |
| Priority | P2 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Select price high-to-low.
3. Observe product prices.

### Expected Result

Products are displayed from highest price to lowest price.

---

# 6. Shopping Cart Test Cases

## TC-CART-001 — Add one product to cart

| Field | Details |
|---|---|
| Requirement | FR-005 |
| Scenario | TS-CART-001 |
| Test Type | Functional |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Select a product.
3. Click Add to Cart.
4. Open the cart.

### Expected Result

The selected product appears in the cart.

---

## TC-CART-002 — Verify cart count after adding product

| Field | Details |
|---|---|
| Requirement | FR-005 |
| Scenario | TS-CART-002 |
| Test Type | Functional |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Add one product to the cart.
3. Observe the cart indicator.

### Expected Result

Cart count reflects the number of selected products.

---

## TC-CART-003 — Add multiple products

| Field | Details |
|---|---|
| Requirement | FR-005 |
| Scenario | TS-CART-004 |
| Test Type | Functional |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Add multiple different products.
3. Open the cart.

### Expected Result

All selected products are displayed in the cart.

---

## TC-CART-004 — Remove product from cart

| Field | Details |
|---|---|
| Requirement | FR-006 |
| Scenario | TS-CART-006 |
| Test Type | Functional |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Add a product to the cart.
2. Open the cart.
3. Remove the product.

### Expected Result

The selected product is removed from the cart.

---

## TC-CART-005 — Remove one product while retaining others

| Field | Details |
|---|---|
| Requirement | FR-006 |
| Scenario | TS-CART-008 |
| Test Type | Functional |
| Priority | P1 |
| Automation Candidate | Yes |

### Steps

1. Add multiple products.
2. Open the cart.
3. Remove one product.
4. Observe remaining products.

### Expected Result

Only the selected product is removed. Other products remain unchanged.

---

## TC-CART-006 — Verify empty cart

| Field | Details |
|---|---|
| Requirement | FR-007 |
| Scenario | TS-CART-010 |
| Test Type | Boundary |
| Priority | P1 |
| Automation Candidate | Yes |

### Steps

1. Add a product.
2. Open the cart.
3. Remove the product.

### Expected Result

The cart contains no products and displays the appropriate empty-cart
state.

---

# 7. Checkout Test Cases

## TC-CHECK-001 — Navigate from cart to checkout

| Field | Details |
|---|---|
| Requirement | FR-008 |
| Scenario | TS-CHECK-001 |
| Test Type | Functional |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Add a product.
3. Open the cart.
4. Select checkout.

### Expected Result

The checkout information page is displayed.

---

## TC-CHECK-002 — Checkout with valid information

| Field | Details |
|---|---|
| Requirement | FR-008 |
| Scenario | TS-CHECK-003 |
| Test Type | Positive |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Add a product to the cart.
2. Navigate to checkout.
3. Enter valid first name.
4. Enter valid last name.
5. Enter valid postal code.
6. Continue.

### Expected Result

User proceeds successfully to the order overview page.

---

## TC-CHECK-003 — Checkout with missing first name

| Field | Details |
|---|---|
| Requirement | FR-008 |
| Scenario | TS-CHECK-004 |
| Test Type | Negative |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Navigate to checkout.
2. Leave first name empty.
3. Enter valid last name.
4. Enter valid postal code.
5. Continue.

### Expected Result

Checkout is rejected and appropriate validation information is displayed.

---

## TC-CHECK-004 — Checkout with missing last name

| Field | Details |
|---|---|
| Requirement | FR-008 |
| Scenario | TS-CHECK-005 |
| Test Type | Negative |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Navigate to checkout.
2. Enter valid first name.
3. Leave last name empty.
4. Enter valid postal code.
5. Continue.

### Expected Result

Checkout is rejected and appropriate validation information is displayed.

---

## TC-CHECK-005 — Checkout with missing postal code

| Field | Details |
|---|---|
| Requirement | FR-008 |
| Scenario | TS-CHECK-006 |
| Test Type | Negative |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Navigate to checkout.
2. Enter valid first name.
3. Enter valid last name.
4. Leave postal code empty.
5. Continue.

### Expected Result

Checkout is rejected and appropriate validation information is displayed.

---

# 8. Order Test Cases

## TC-ORDER-001 — Verify order overview

| Field | Details |
|---|---|
| Requirement | FR-009 |
| Scenario | TS-ORDER-001 |
| Test Type | Functional |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Add one or more products.
2. Navigate through checkout.
3. Observe the order overview.

### Expected Result

Selected products and relevant order information are displayed correctly.

---

## TC-ORDER-002 — Complete successful order

| Field | Details |
|---|---|
| Requirement | FR-009 |
| Scenario | TS-ORDER-003 |
| Test Type | E2E / Positive |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Select a product.
3. Add the product to the cart.
4. Open the cart.
5. Proceed to checkout.
6. Enter valid customer information.
7. Continue to order overview.
8. Complete the order.

### Expected Result

The order is successfully completed and confirmation is displayed.

---

## TC-ORDER-003 — Verify order contains selected product

| Field | Details |
|---|---|
| Requirement | FR-009 |
| Scenario | TS-ORDER-005 |
| Test Type | E2E |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Select a specific product.
2. Add it to the cart.
3. Proceed through checkout.
4. Review order information.

### Expected Result

The order contains the product selected by the customer.

---

# 9. Logout and Security Test Cases

## TC-SEC-001 — Logout authenticated user

| Field | Details |
|---|---|
| Requirement | FR-010 |
| Scenario | TS-LOGOUT-001 |
| Test Type | Functional / Security |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Open the application menu.
3. Select logout.

### Expected Result

User is logged out and returned to the login page.

---

## TC-SEC-002 — Verify protected access after logout

| Field | Details |
|---|---|
| Requirement | FR-010 |
| Scenario | TS-LOGOUT-003 |
| Test Type | Security |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Log out.
3. Attempt to access protected application functionality.

### Expected Result

Unauthenticated user should not retain authorized access to protected
functionality.

---

# 10. End-to-End Test Cases

## TC-E2E-001 — Complete customer purchase journey

| Field | Details |
|---|---|
| Requirement | FR-001 to FR-010 |
| Scenario | TS-E2E-001 |
| Test Type | End-to-End |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Open the application.
2. Log in using valid credentials.
3. Browse products.
4. Open a product.
5. Add the product to the cart.
6. Open the shopping cart.
7. Verify selected product.
8. Proceed to checkout.
9. Enter valid customer information.
10. Review order information.
11. Complete the order.
12. Verify order confirmation.
13. Log out.

### Expected Result

The complete customer journey executes successfully from login through
order completion and logout without unexpected failures.

---

## TC-E2E-002 — Multiple-product purchase journey

| Field | Details |
|---|---|
| Requirement | FR-001 to FR-010 |
| Scenario | TS-E2E-003 |
| Test Type | End-to-End |
| Priority | P0 |
| Automation Candidate | Yes |

### Steps

1. Log in.
2. Select multiple products.
3. Add all selected products to the cart.
4. Open the cart.
5. Verify all selected products.
6. Proceed to checkout.
7. Enter valid information.
8. Complete the order.

### Expected Result

All selected products are correctly retained throughout the purchase
journey and the order completes successfully.

---

# 11. Test Case Summary

| Area | Test Cases |
|---|---:|
| Authentication | 5 |
| Product | 3 |
| Sorting | 4 |
| Shopping Cart | 6 |
| Checkout | 5 |
| Order | 3 |
| Security / Logout | 2 |
| End-to-End | 2 |
| **Total** | **30** |

---

# 12. Automation Candidates

The majority of stable, repeatable regression scenarios are suitable for
automation.

Priority automation candidates:

- Login
- Product navigation
- Product selection
- Sorting
- Add/remove cart
- Checkout validation
- Successful order
- Logout
- Critical end-to-end flows

Automation implementation will be developed separately using Python and
an appropriate browser automation framework.

---

# 13. Test Case Review Checklist

Before execution, test cases should be reviewed for:

- Requirement traceability
- Clear preconditions
- Correct test data
- Unambiguous steps
- Measurable expected results
- Positive coverage
- Negative coverage
- Boundary coverage
- Security coverage
- End-to-end coverage
- Regression suitability
- Automation suitability