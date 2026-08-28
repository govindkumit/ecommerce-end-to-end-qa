# E-Commerce Application — Test Metrics

## 1. Objective

This document defines the quality metrics used to measure test execution,
defect status, coverage and overall product quality.

Metrics are intended to support:

- QA reporting
- Risk assessment
- Defect management
- Regression planning
- Release readiness
- Stakeholder communication
- Quality governance

Only actual execution data will be used in final project metrics.

---

# 2. Test Execution Metrics

## Current Test Cycle

| Metric | Value |
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

### Formula

Execution Progress:

`Executed / Total × 100`

`30 / 30 × 100 = 100%`

Pass Rate:

`Passed / Executed × 100`

`29 / 30 × 100 = 96.67%`

Fail Rate:

`Failed / Executed × 100`

`1 / 30 × 100 = 3.33%`

> These values represent the completed functional test execution
> snapshot for the current test cycle.

---

# 3. Defect Metrics

## Current Defect Status

| Metric | Value |
|---|---:|
| Total Defects | 1 |
| Open | 1 |
| Closed | 0 |
| Critical | 0 |
| High | 0 |
| Medium | 1 |
| Low | 0 |

---

# 4. Defect Distribution

| Severity | Defects | Percentage |
|---|---:|---:|
| Critical | 0 | 0% |
| High | 0 | 0% |
| Medium | 1 | 100% |
| Low | 0 | 0% |

---

# 5. Defect Density

For this portfolio project, defect density can be represented against
executed test cases as an indicative metric.

### Formula

`Defects Detected / Executed Test Cases`

Current value:

`1 / 30 = 0.033 defects per executed test case`

Equivalent representation:

`3.33 defects per 100 executed test cases`

This metric should not be interpreted as a production defect-density
measurement because the project is a controlled demo application.

---

# 6. Test Coverage

Test coverage will be measured against the identified functional areas.

| Functional Area | Planned | Executed | Status |
|---|---:|---:|---|
| Authentication | 5 | 5 | Complete |
| Product | 3 | 3 | Complete |
| Sorting | 4 | 4 | Complete |
| Cart | 6 | 6 | Complete |
| Checkout | 5 | 5 | Complete |
| Order | 3 | 3 | Complete |
| Security | 2 | 2 | Complete |
| End-to-End | 2 | 2 | Complete |
| **Total** | **30** | **30** | **Complete** |

---

# 7. Requirement Coverage

Requirement coverage will be tracked between requirements and test cases.

### Formula

`Requirements with at least one executed test /
Total identified requirements × 100`

All identified functional requirements for the current test cycle have
associated test scenarios and executed test cases.

Therefore:

**Requirement Coverage: 100%**

> Requirement coverage indicates that identified requirements have
> corresponding test coverage. It does not guarantee that every
> requirement has passed validation.

---

# 8. Defect Detection Effectiveness

The project will track the ability of testing to identify defects before
release.

Key indicators:

- Defects detected during functional testing
- Defects detected during regression
- Defects detected during E2E testing
- Defects escaped to later phases
- Defects reopened after retesting

Current status:

```text
Functional Testing → BUG-001 detected

Regression         → Pending

Retesting          → Pending

Production Leakage → Not Applicable