# E-Commerce Application — Test Scenarios

## 1. Document Information

| Attribute | Details |
|---|---|
| Project | E-Commerce Web Application |
| Application Under Test | SauceDemo |
| Document | Test Scenario Specification |
| Version | 1.0 |
| Status | Draft |
| QA Owner | QA Engineering Team |

---

# 2. Objective

The objective of this document is to identify the functional, negative,
boundary, security-oriented, usability, compatibility and end-to-end test
scenarios required to validate the E-Commerce application.

Scenarios are derived from:

- Business requirements
- Acceptance criteria
- Business rules
- Risk assessment
- User journeys
- Exploratory testing considerations

---

# 3. Scenario Priority

| Priority | Definition |
|---|---|
| P0 | Critical business/security scenario |
| P1 | High-priority business functionality |
| P2 | Medium-priority functionality |
| P3 | Low-priority functionality |

---

# 4. Login Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-LOGIN-001 | Verify login with valid credentials | Positive | FR-001 | P0 |
| TS-LOGIN-002 | Verify login with invalid username | Negative | FR-001 | P0 |
| TS-LOGIN-003 | Verify login with invalid password | Negative | FR-001 | P0 |
| TS-LOGIN-004 | Verify login with invalid username and password | Negative | FR-001 | P0 |
| TS-LOGIN-005 | Verify login with empty username | Negative | FR-001 | P1 |
| TS-LOGIN-006 | Verify login with empty password | Negative | FR-001 | P1 |
| TS-LOGIN-007 | Verify login with both fields empty | Negative | FR-001 | P1 |
| TS-LOGIN-008 | Verify appropriate error message for failed login | Functional | FR-001 | P1 |
| TS-LOGIN-009 | Verify authenticated user can access protected functionality | Security | FR-001 | P0 |
| TS-LOGIN-010 | Verify logged-out user cannot continue accessing protected functionality | Security | FR-010 | P0 |

---

# 5. Product Listing Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-PROD-001 | Verify products are displayed after successful login | Positive | FR-002 | P0 |
| TS-PROD-002 | Verify product names are displayed correctly | Functional | FR-002 | P1 |
| TS-PROD-003 | Verify product prices are displayed correctly | Functional | FR-002 | P1 |
| TS-PROD-004 | Verify product images are displayed | Functional | FR-002 | P2 |
| TS-PROD-005 | Verify user can select a product | Functional | FR-002 | P1 |
| TS-PROD-006 | Verify product list does not contain unexpected duplicates | Functional | FR-002 | P1 |
| TS-PROD-007 | Verify product information is consistent between listing and details | Functional | FR-002, FR-003 | P1 |

---

# 6. Product Details Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-DETAIL-001 | Verify product details can be opened | Positive | FR-003 | P1 |
| TS-DETAIL-002 | Verify selected product name is correct | Functional | FR-003 | P1 |
| TS-DETAIL-003 | Verify selected product price is correct | Functional | FR-003 | P1 |
| TS-DETAIL-004 | Verify selected product image is correct | Functional | FR-003 | P2 |
| TS-DETAIL-005 | Verify navigation back to product listing | Functional | FR-003 | P2 |

---

# 7. Product Sorting Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-SORT-001 | Verify products can be sorted using available options | Functional | FR-004 | P2 |
| TS-SORT-002 | Verify products are sorted correctly by name ascending | Functional | FR-004 | P2 |
| TS-SORT-003 | Verify products are sorted correctly by name descending | Functional | FR-004 | P2 |
| TS-SORT-004 | Verify products are sorted correctly by price ascending | Functional | FR-004 | P2 |
| TS-SORT-005 | Verify products are sorted correctly by price descending | Functional | FR-004 | P2 |
| TS-SORT-006 | Verify sorting does not remove products | Functional | FR-004 | P2 |
| TS-SORT-007 | Verify sorting does not duplicate products | Functional | FR-004 | P2 |

---

# 8. Shopping Cart Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-CART-001 | Verify a product can be added to cart | Positive | FR-005 | P0 |
| TS-CART-002 | Verify cart count is updated after adding a product | Functional | FR-005 | P0 |
| TS-CART-003 | Verify selected product appears in cart | Functional | FR-005, FR-007 | P0 |
| TS-CART-004 | Verify multiple products can be added to cart | Positive | FR-005 | P0 |
| TS-CART-005 | Verify correct products are retained when multiple products are added | Functional | FR-005 | P0 |
| TS-CART-006 | Verify a product can be removed from cart | Positive | FR-006 | P0 |
| TS-CART-007 | Verify cart count is updated after removing a product | Functional | FR-006 | P0 |
| TS-CART-008 | Verify remaining products are unchanged after removing one product | Functional | FR-006 | P1 |
| TS-CART-009 | Verify cart behavior when all products are removed | Boundary | FR-006, FR-007 | P1 |
| TS-CART-010 | Verify empty cart behavior | Boundary | FR-007 | P1 |
| TS-CART-011 | Verify product name in cart matches selected product | Functional | FR-007 | P1 |
| TS-CART-012 | Verify product price in cart matches product listing | Functional | FR-007 | P0 |

---

# 9. Checkout Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-CHECK-001 | Verify user can navigate from cart to checkout | Positive | FR-008 | P0 |
| TS-CHECK-002 | Verify checkout form is displayed correctly | Functional | FR-008 | P1 |
| TS-CHECK-003 | Verify checkout with valid information | Positive | FR-008 | P0 |
| TS-CHECK-004 | Verify checkout with missing first name | Negative | FR-008 | P0 |
| TS-CHECK-005 | Verify checkout with missing last name | Negative | FR-008 | P0 |
| TS-CHECK-006 | Verify checkout with missing postal code | Negative | FR-008 | P0 |
| TS-CHECK-007 | Verify checkout with all mandatory fields empty | Negative | FR-008 | P0 |
| TS-CHECK-008 | Verify checkout validation messages | Functional | FR-008 | P1 |
| TS-CHECK-009 | Verify invalid input is rejected appropriately | Negative | FR-008 | P1 |
| TS-CHECK-010 | Verify user can cancel checkout | Functional | FR-008 | P1 |

---

# 10. Order Completion Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-ORDER-001 | Verify order overview displays selected products | Functional | FR-009 | P0 |
| TS-ORDER-002 | Verify order information is correct before completion | Functional | FR-009 | P0 |
| TS-ORDER-003 | Verify user can complete an order with valid information | Positive | FR-009 | P0 |
| TS-ORDER-004 | Verify order confirmation is displayed after successful order | Functional | FR-009 | P0 |
| TS-ORDER-005 | Verify completed order reflects selected products | Functional | FR-009 | P0 |
| TS-ORDER-006 | Verify order cannot be completed with invalid/incomplete information | Negative | FR-009 | P0 |

---

# 11. Logout and Session Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-LOGOUT-001 | Verify authenticated user can log out | Positive | FR-010 | P0 |
| TS-LOGOUT-002 | Verify user is redirected appropriately after logout | Functional | FR-010 | P1 |
| TS-LOGOUT-003 | Verify protected functionality is not accessible after logout | Security | FR-010 | P0 |
| TS-LOGOUT-004 | Verify browser navigation does not incorrectly restore authenticated access | Security | FR-010 | P0 |

---

# 12. End-to-End Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-E2E-001 | Complete successful purchase journey from login to order completion | E2E | FR-001 to FR-009 | P0 |
| TS-E2E-002 | Login, browse products, add one product, checkout and complete order | E2E | FR-001 to FR-009 | P0 |
| TS-E2E-003 | Login, select multiple products, review cart and complete order | E2E | FR-001 to FR-009 | P0 |
| TS-E2E-004 | Add and remove products before checkout | E2E | FR-005 to FR-008 | P0 |
| TS-E2E-005 | Attempt checkout with incomplete customer information | E2E Negative | FR-008, FR-009 | P0 |
| TS-E2E-006 | Complete order and then log out | E2E | FR-009, FR-010 | P0 |

---

# 13. Usability Scenarios

| ID | Scenario | Type | Priority |
|---|---|---|---|
| TS-USE-001 | Verify primary navigation is understandable | Usability | P2 |
| TS-USE-002 | Verify important actions are clearly visible | Usability | P2 |
| TS-USE-003 | Verify validation/error messages are understandable | Usability | P1 |
| TS-USE-004 | Verify checkout flow is intuitive | Usability | P1 |
| TS-USE-005 | Verify product information is easy to understand | Usability | P2 |

---

# 14. Compatibility Scenarios

| ID | Scenario | Type | Priority |
|---|---|---|---|
| TS-COMP-001 | Verify core customer journey on Chrome | Compatibility | P1 |
| TS-COMP-002 | Verify core customer journey on Edge | Compatibility | P1 |
| TS-COMP-003 | Verify core customer journey on Firefox | Compatibility | P1 |
| TS-COMP-004 | Verify UI layout across supported browsers | Compatibility | P2 |

---

# 15. Security-Oriented Scenarios

| ID | Scenario | Type | Requirement | Priority |
|---|---|---|---|---|
| TS-SEC-001 | Verify unauthenticated user cannot access protected functionality | Security | FR-001 | P0 |
| TS-SEC-002 | Verify invalid credentials cannot authenticate the user | Security | FR-001 | P0 |
| TS-SEC-003 | Verify logout terminates the user session | Security | FR-010 | P0 |
| TS-SEC-004 | Verify protected functionality is not accessible after logout | Security | FR-010 | P0 |
| TS-SEC-005 | Verify authentication errors do not expose sensitive information | Security | FR-001 | P1 |
| TS-SEC-006 | Verify application handles unexpected input safely | Security | FR-001, FR-008 | P1 |

---

# 16. Performance-Oriented Scenarios

| ID | Scenario | Type | Priority |
|---|---|---|---|
| TS-PERF-001 | Measure login response behavior | Performance | P1 |
| TS-PERF-002 | Measure product listing response behavior | Performance | P1 |
| TS-PERF-003 | Measure product navigation response behavior | Performance | P2 |
| TS-PERF-004 | Measure cart operation response behavior | Performance | P2 |
| TS-PERF-005 | Measure checkout navigation response behavior | Performance | P1 |
| TS-PERF-006 | Observe application behavior during repeated user operations | Performance | P2 |

---

# 17. Exploratory Testing Areas

The following areas will be explored beyond predefined scenarios:

### Navigation

- Back/forward navigation
- Repeated navigation
- Unexpected navigation sequences

### Session

- Logout behavior
- Browser refresh
- Browser back button
- Session state

### Cart

- Repeated add/remove operations
- Multiple products
- Empty cart
- Product state consistency

### Checkout

- Missing information
- Invalid information
- Navigation during checkout
- Repeated submission

### Error Handling

- Invalid input
- Unexpected user actions
- Error message consistency

---

# 18. Scenario Coverage Summary

| Functional Area | Number of Scenarios |
|---|---:|
| Login | 10 |
| Product Listing | 7 |
| Product Details | 5 |
| Product Sorting | 7 |
| Shopping Cart | 12 |
| Checkout | 10 |
| Order Completion | 6 |
| Logout/Session | 4 |
| End-to-End | 6 |
| Usability | 5 |
| Compatibility | 4 |
| Security | 6 |
| Performance | 6 |

The scenario inventory will be expanded or refined during detailed test
case design and exploratory testing.

---

# 19. Scenario-to-Requirement Traceability

All functional scenarios will be mapped to the corresponding
requirements.

The traceability relationship will be maintained as:

Requirement
→ Scenario
→ Test Case
→ Execution
→ Defect
→ Retest
→ Regression

This ensures complete visibility from business requirement through final
quality validation.

---

# 20. Scenario Review Criteria

Before test cases are created, scenarios will be reviewed for:

- Requirement coverage
- Business-risk coverage
- Positive coverage
- Negative coverage
- Boundary coverage
- Security coverage
- Compatibility coverage
- End-to-end coverage
- Regression suitability
- Automation suitability

Scenarios may be added, removed or reprioritized based on risk and
application behavior.