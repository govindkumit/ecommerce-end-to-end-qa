# E-Commerce Application — Test Plan

## 1. Document Information

| Attribute | Details |
|---|---|
| Project | E-Commerce Web Application |
| Application Under Test | SauceDemo |
| Document | Test Plan |
| Version | 1.0 |
| Status | Draft |
| QA Owner | QA Engineering Team |

---

# 2. Purpose

This Test Plan defines the execution approach for validating the
E-Commerce Web Application.

It translates the approved Test Strategy into an actionable testing plan
covering:

- Test scope
- Test objectives
- Test activities
- Test cycles
- Test resources
- Test environments
- Test data
- Test deliverables
- Defect management
- Test reporting
- Risks and dependencies
- Entry and exit criteria
- Release readiness

---

# 3. Test Objectives

The primary objectives are to:

1. Validate all critical business workflows.
2. Verify that functional requirements are correctly implemented.
3. Identify functional and usability defects.
4. Validate negative and boundary conditions.
5. Validate the complete customer journey.
6. Verify that previously tested functionality remains stable during
   regression.
7. Identify security and performance-related risks within the defined
   scope.
8. Provide objective test evidence for release decisions.

---

# 4. Scope

## 4.1 In Scope

### Functional Areas

- Login
- Product listing
- Product details
- Product sorting
- Add to cart
- Remove from cart
- Shopping cart
- Checkout
- Order completion
- Logout

### Test Types

- Functional testing
- Integration-oriented testing
- System testing
- End-to-end testing
- Positive testing
- Negative testing
- Boundary testing
- Exploratory testing
- Smoke testing
- Sanity testing
- Regression testing
- Usability testing
- Compatibility testing
- Basic security validation
- Basic performance validation

---

## 4.2 Out of Scope

- Real payment processing
- Real financial transactions
- Production infrastructure testing
- Real customer data
- Third-party logistics
- Native mobile application testing
- Full database performance testing
- Full penetration testing
- Production-scale load testing

---

# 5. Test Approach

Testing will follow a risk-based and incremental approach.

The planned sequence is:

1. Requirement analysis
2. Test design
3. Test data preparation
4. Environment validation
5. Smoke testing
6. Functional testing
7. Negative and boundary testing
8. Integration-oriented testing
9. End-to-end testing
10. Exploratory testing
11. Regression testing
12. Defect retesting
13. Final quality assessment
14. Release recommendation

Testing will prioritize critical customer journeys and high-risk
functionality.

---

# 6. Test Cycles

## Cycle 1 — Smoke Testing

### Objective

Determine whether the application is stable enough for detailed testing.

### Key Coverage

- Application availability
- Login
- Product page
- Product selection
- Add to cart
- Checkout navigation

### Exit Condition

Smoke tests pass with no blocking issue preventing further testing.

---

## Cycle 2 — Functional Testing

### Objective

Validate application functionality against defined requirements.

### Coverage

- Authentication
- Product functionality
- Sorting
- Cart
- Checkout
- Order completion
- Logout

Both positive and negative scenarios will be included.

---

## Cycle 3 — Integration / End-to-End Testing

### Objective

Validate interactions between major application functions and complete
customer journeys.

### Primary Journey

Login
→ Products
→ Product Details
→ Add to Cart
→ Cart
→ Checkout
→ Order Completion
→ Logout

Additional combinations will be tested.

---

## Cycle 4 — Exploratory Testing

### Objective

Identify unexpected behavior that may not be detected by predefined
test cases.

### Focus Areas

- Navigation
- Session behavior
- Error handling
- Unusual user actions
- Data consistency
- Boundary conditions
- High-risk functionality

---

## Cycle 5 — Regression Testing

### Objective

Verify that existing functionality remains stable after changes or defect
fixes.

### Priority Coverage

- Login
- Product selection
- Cart
- Checkout
- Order completion
- Logout

Regression testing will be risk-based rather than executing every test
case indiscriminately.

---

## Cycle 6 — Release Validation

### Objective

Perform final validation before making a release recommendation.

### Activities

- Review test execution results
- Verify critical/high defects
- Execute targeted regression
- Review requirement coverage
- Review known risks
- Review test metrics
- Prepare release recommendation

---

# 7. Test Levels

Testing will cover the following levels where applicable:

1. Unit testing — primarily owned by development.
2. Integration testing.
3. System testing.
4. End-to-end testing.
5. Regression testing.

The QA team will focus primarily on integration, system and end-to-end
validation.

---

# 8. Test Design

Test cases will be derived from requirements and business rules.

The following techniques will be used:

- Equivalence Partitioning
- Boundary Value Analysis
- Decision Table Testing
- State Transition Testing
- Use Case Testing
- Error Guessing
- Risk-Based Testing
- Exploratory Testing

Each requirement will have appropriate scenario and test coverage.

---

# 9. Requirement Traceability

Traceability will be maintained using the following relationship:

Requirement
→ Test Scenario
→ Test Case
→ Execution Result
→ Defect
→ Retest
→ Regression

The objective is to ensure that no critical requirement is left without
test coverage.

---

# 10. Test Environment

## Application

SauceDemo

## Operating System

Windows

## Browsers

- Google Chrome
- Microsoft Edge
- Mozilla Firefox

## Environment Characteristics

Testing will be performed against the available demo/test environment.

Environment availability and stability will be validated before formal
execution.

---

# 11. Test Data

Test data will include:

### Authentication Data

- Valid credentials
- Invalid username
- Invalid password
- Empty username
- Empty password
- Invalid credential combinations

### Checkout Data

- Valid customer information
- Missing first name
- Missing last name
- Missing postal code
- Empty required fields
- Boundary and invalid input values

### Product Data

- Single-product selection
- Multiple-product selection
- Product removal
- Empty cart
- Different product combinations

No real customer or financial data will be used.

---

# 12. Resource Plan

The project will use the following responsibilities.

| Role | Responsibilities |
|---|---|
| QA Manager / Lead | Strategy, planning, risk management, governance, reporting, release recommendation |
| QA Engineer | Test design, execution, defect reporting, retesting |
| Automation Engineer | Automation framework and regression automation |
| Developer | Unit testing and defect resolution |
| Product/Business Owner | Requirement clarification and acceptance |
| Release/Project Manager | Release coordination |

For this portfolio project, the activities may be executed by a single
QA engineer while simulating the responsibilities of the complete QA team.

---

# 13. Test Deliverables

The following artifacts will be produced:

| Deliverable | Location |
|---|---|
| Requirements | `01-requirements/` |
| Test Strategy | `02-test-strategy/` |
| Test Plan | `04-test-plan/` |
| Test Scenarios | `04-test-scenarios/` |
| Test Cases | `05-test-cases/` |
| Test Data | `06-test-data/` |
| Test Execution | `07-test-execution/` |
| Defect Reports | `08-defects/` |
| Regression Results | `09-regression/` |
| Test Metrics | `10-test-metrics/` |
| Release Assessment | `11-release-readiness/` |
| Test Summary | `12-test-summary/` |

---

# 14. Defect Management

All defects will be documented using a standardized defect template.

Each defect will contain:

- Defect ID
- Summary
- Description
- Preconditions
- Steps to reproduce
- Expected result
- Actual result
- Severity
- Priority
- Environment
- Evidence
- Status
- Resolution
- Retest result

---

# 15. Defect Workflow

The standard defect workflow is:

New
 ↓
Triaged
 ↓
Assigned
 ↓
In Progress
 ↓
Fixed
 ↓
Ready for Retest
 ↓
Retest
 ↓
Closed

Alternative outcomes may include:

- Reopened
- Deferred
- Duplicate
- Rejected
- Not Reproducible
- Won't Fix

---

# 16. Severity and Priority

Severity represents the technical/business impact of a defect.

Priority represents how urgently the defect should be addressed.

These attributes will be maintained independently.

## Severity

| Severity | Description |
|---|---|
| Critical | Application/business-critical functionality unavailable or severe security/business impact |
| High | Major functionality significantly affected |
| Medium | Functionality affected but workaround may exist |
| Low | Minor functional or cosmetic impact |

## Priority

| Priority | Description |
|---|---|
| P0 | Immediate attention required |
| P1 | Must be addressed before release unless explicitly accepted |
| P2 | Should be addressed in the planned release |
| P3 | Can be addressed later |

---

# 17. Test Execution Process

For each test case:

1. Verify preconditions.
2. Execute test steps.
3. Record actual result.
4. Compare against expected result.
5. Mark Pass / Fail / Blocked.
6. Attach evidence where appropriate.
7. Create defect if required.
8. Link the defect to the test case.
9. Retest after defect resolution.
10. Update final execution status.

---

# 18. Entry Criteria

Testing can begin when:

- Requirements are available.
- Test strategy is defined.
- Test plan is approved.
- Application is accessible.
- Required credentials are available.
- Test environment is operational.
- Test data is prepared.
- Initial build is considered testable.

---

# 19. Exit Criteria

Testing can be considered complete when:

- Planned critical and high-priority test cases are executed.
- Required requirement coverage is achieved.
- No unresolved Critical defects remain.
- High-severity defects are resolved or explicitly accepted.
- Regression testing is completed.
- Defect retesting is completed.
- Test metrics are documented.
- Known risks are documented.
- Release recommendation is prepared.

---

# 20. Test Suspension Criteria

Testing may be suspended when:

- Application is unavailable.
- A blocking defect prevents meaningful testing.
- Test environment becomes unstable.
- Critical functionality is inaccessible.
- Required test data becomes unavailable.

Testing will resume after the blocking condition is resolved and a smoke
test confirms environment stability.

---

# 21. Test Resumption Criteria

Testing can resume when:

- Blocking issue is resolved.
- Environment is available.
- Required data is available.
- A smoke test passes.
- Impact assessment is completed.

---

# 22. Risks

| Risk | Impact | Probability | Mitigation |
|---|---|---|---|
| Environment unavailable | High | Medium | Validate environment before execution |
| Requirement ambiguity | High | Low | Clarify requirements before test design |
| Late defect discovery | High | Medium | Risk-based testing and early execution |
| Insufficient test coverage | High | Medium | Requirement traceability |
| Regression defects | High | Medium | Maintain regression suite |
| Test data issues | Medium | Low | Prepare reusable test data |
| Browser compatibility issues | Medium | Medium | Execute cross-browser validation |

---

# 23. Dependencies

Testing depends on:

- Application availability
- Test environment
- Valid test credentials
- Stable application build
- Test data
- Browser availability
- Requirement clarity

---

# 24. Communication and Reporting

Testing status will be communicated through:

### Daily Test Status

- Tests planned
- Tests executed
- Passed
- Failed
- Blocked
- New defects
- Critical/high defects
- Risks
- Blockers

### Defect Reporting

Defects will be reported as soon as they are identified and validated.

### Final Test Report

A final Test Summary Report will provide:

- Test scope
- Coverage
- Execution results
- Defect summary
- Risks
- Regression results
- Quality assessment
- Release recommendation

---

# 25. Quality Metrics

The following metrics will be tracked:

## Test Execution Metrics

- Total planned tests
- Executed tests
- Passed tests
- Failed tests
- Blocked tests
- Not executed tests

## Coverage Metrics

- Requirement coverage
- Scenario coverage
- Test case coverage

## Defect Metrics

- Total defects
- Critical defects
- High defects
- Medium defects
- Low defects
- Open defects
- Closed defects
- Reopened defects

## Quality Metrics

- Test pass percentage
- Regression pass percentage
- Defect distribution
- Requirement coverage percentage

Metrics will be interpreted in context and will not be used as isolated
targets.

---

# 26. Release Decision Framework

The final release recommendation will consider:

- Test execution results
- Requirement coverage
- Critical-path stability
- Defect severity
- Defect priority
- Regression results
- Known risks
- Business impact

Possible decisions:

### GO

Release criteria are satisfied.

### CONDITIONAL GO

Known risks exist but have been explicitly accepted.

### NO-GO

Release criteria are not satisfied.

---

# 27. Test Completion

At the end of testing, the QA team will:

1. Complete planned execution.
2. Complete defect retesting.
3. Complete regression.
4. Update traceability.
5. Calculate quality metrics.
6. Document known risks.
7. Prepare release-readiness assessment.
8. Prepare the final Test Summary Report.

---

# 28. Continuous Improvement

After completion of the test cycle, the QA team will evaluate:

- Escaped defects
- Test coverage gaps
- Automation opportunities
- Process improvements
- Repeated defect patterns
- Environment issues
- Test-data issues

Lessons learned will be incorporated into future test cycles.