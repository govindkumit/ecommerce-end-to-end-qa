# E-Commerce Application — Regression Test Suite

## 1. Regression Testing Objective

The objective of regression testing is to verify that application changes,
bug fixes, or enhancements have not introduced unintended impact to
existing functionality.

Regression testing will cover:

- Authentication
- Product listing
- Product details
- Product sorting
- Shopping cart
- Checkout
- Order completion
- Logout
- End-to-end customer journey

---

# 2. Regression Entry Criteria

Regression testing can begin when:

- Required build is available.
- Developer fixes are deployed.
- Environment is available.
- Critical blockers are resolved.
- Test data is available.
- Required test accounts are available.
- Defect fixes are ready for QA verification.

---

# 3. Regression Strategy

Regression testing will be performed using a risk-based approach.

### Priority 0 — Critical Business Flow

- Login
- Product selection
- Add to cart
- Checkout
- Order completion
- Logout

### Priority 1 — Important Functional Areas

- Product information
- Cart operations
- Checkout validation
- Product sorting
- Navigation

### Priority 2 — Secondary Coverage

- Additional sorting combinations
- Negative scenarios
- Boundary scenarios
- UI consistency checks

---

# 4. Defect-Focused Regression

## BUG-001

### Defect

Product image does not match product name for `problem_user`.

### Original Expected Behavior

The product named "Sauce Labs Backpack" should display the
corresponding Backpack image.

### Original Actual Behavior

The product named "Sauce Labs Backpack" displayed the Bike Light image.

### Retest Objective

Verify that the defect is resolved and that the correct product image
is displayed for the corresponding product.

### Retest Status

PENDING FIX / RETEST

---

# 5. Regression Test Cases

| Regression ID | Test Case | Priority | Status |
|---|---|---|---|
| REG-001 | Valid user login | P0 | NOT EXECUTED |
| REG-002 | Invalid username | P0 | NOT EXECUTED |
| REG-003 | Invalid password | P0 | NOT EXECUTED |
| REG-004 | Product listing | P0 | NOT EXECUTED |
| REG-005 | Product information | P1 | NOT EXECUTED |
| REG-006 | Product details | P1 | NOT EXECUTED |
| REG-007 | Product sorting A-Z | P2 | NOT EXECUTED |
| REG-008 | Product sorting Z-A | P2 | NOT EXECUTED |
| REG-009 | Product sorting price low-high | P2 | NOT EXECUTED |
| REG-010 | Product sorting price high-low | P2 | NOT EXECUTED |
| REG-011 | Add product to cart | P0 | NOT EXECUTED |
| REG-012 | Multiple products in cart | P0 | NOT EXECUTED |
| REG-013 | Remove product from cart | P0 | NOT EXECUTED |
| REG-014 | Checkout with valid data | P0 | NOT EXECUTED |
| REG-015 | Checkout mandatory-field validation | P0 | NOT EXECUTED |
| REG-016 | Order overview validation | P0 | NOT EXECUTED |
| REG-017 | Complete order | P0 | NOT EXECUTED |
| REG-018 | Logout | P0 | NOT EXECUTED |
| REG-019 | Protected navigation after logout | P1 | NOT EXECUTED |
| REG-020 | End-to-end purchase journey | P0 | NOT EXECUTED |
| REG-021 | BUG-001 product image verification | P0 | PENDING FIX |

---

# 6. Regression Execution

Regression results will be recorded using:

| Status | Definition |
|---|---|
| PASS | Expected behavior confirmed |
| FAIL | Regression defect identified |
| BLOCKED | Execution prevented by environment or dependency |
| NOT EXECUTED | Test has not yet been executed |

---

# 7. Defect Retest Process

For each fixed defect:

```text
Defect Fixed
     ↓
Build Deployed
     ↓
QA Retest
     ↓
PASS?
 ┌───┴────┐
YES       NO
 ↓         ↓
Close     Reopen
 ↓
Regression