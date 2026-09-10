# 🧪 SauceDemo QA Testing Project

A manual software testing project conducted on the **SauceDemo** web application as part of my QA learning and portfolio development.

The project covers functional testing, negative testing, input validation, business logic, usability, basic security testing, and exploratory testing — from designing and executing test cases to identifying, documenting, and tracing defects.

---

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Highlights](#-highlights)
- [Testing Objectives](#-testing-objectives)
- [Testing Scope](#-testing-scope)
- [Testing Approach](#-testing-approach)
- [Testing Techniques](#️-testing-techniques)
- [Test Accounts](#-test-accounts)
- [Test Artifacts](#-test-artifacts)
- [Defect Summary](#-defect-summary)
- [Repository Structure](#-repository-structure)
- [Test Case → Bug Traceability](#-test-case--bug-traceability)
- [Application Under Test](#-application-under-test)
- [Disclaimer](#️-disclaimer)
- [Author](#-author)

---

## 📌 Project Overview

The purpose of this project is to practice the complete manual testing workflow: exploring application behavior, designing test cases, executing tests, identifying defects, and documenting them with supporting evidence.

Testing is performed using different SauceDemo test accounts to explore both expected and abnormal application behavior.

---

## 📊 Highlights

- **37** structured test cases documented for the `standard_user` account across 6 functional areas
- **3** defects logged with full reproduction steps, severity/priority reasoning, and evidence
- Full **test-case-to-defect traceability** between failed scenarios and their bug reports
- Additional test accounts (`locked_out_user`, `problem_user`, `performance_glitch_user`, `error_user`, `visual_user`) in progress

---

## 🎯 Testing Objectives

- Verify core application functionality
- Validate positive and negative user scenarios
- Test input validation and boundary conditions
- Verify cart and checkout business logic
- Test authentication and access-control behavior
- Identify functional and usability issues
- Perform exploratory testing to discover unexpected behavior
- Document defects using structured bug reports
- Maintain traceability between test cases and identified defects

---

## 🔍 Testing Scope

The following areas of the application were tested:

- 🔐 Login / Authentication
- 🛍️ Products
- 📦 Product Details
- 🛒 Shopping Cart
- 💳 Checkout
- 📝 Customer Information Validation
- 💰 Order Calculation
- ✅ Order Placement
- 🧭 Navigation
- 🚪 Logout
- 🔄 Application State / Reset
- 🔒 Basic Authorization / Access-Control Checks
- 🖥️ UI Behavior

---

## 🧪 Testing Approach

### Exploratory Testing

Exploratory testing was used first to understand the application's behavior and surface potential issues without relying solely on predefined test cases.

Particular attention was given to:

- Unexpected workflows
- Empty and invalid states
- Boundary and edge cases
- Input validation
- Business logic
- Navigation and access behavior
- Error handling

### Structured Testing

After exploring the application, structured test cases were documented based on the functionality and behaviors covered during the assessment.

Test execution results are recorded as **Passed**, **Failed**, **Blocked**, or **Not Run**, with failed test cases linked to their corresponding bug reports.

---

## 🛠️ Testing Techniques

- Functional Testing
- Negative Testing
- Exploratory Testing
- Equivalence Partitioning
- Boundary Value Analysis
- Input Validation Testing
- Business Logic Testing
- Usability Testing
- Basic Security Testing
- Authentication Testing
- Authorization / Access-Control Testing
- UI Testing

---

## 👤 Test Accounts

Different SauceDemo test accounts were used for different testing purposes.

| Test Account | Testing Focus |
|---|---|
| `standard_user` | Baseline functional testing |
| `locked_out_user` | Authentication and access behavior |
| `problem_user` | Exploratory and abnormal behavior |
| `performance_glitch_user` | Performance-related behavior |
| `error_user` | Error handling |
| `visual_user` | Visual and UI behavior |

> **Note:** Test account credentials are intentionally not included in this repository.

---

## 📊 Test Artifacts

This repository contains:

### 📋 Test Cases

Structured test cases covering the application's main functionality, including positive, negative, validation, and edge-case scenarios.

### 🐞 Bug Reports

Documented defects containing:

- Bug ID
- Title
- Environment
- Severity
- Priority
- Preconditions
- Steps to Reproduce
- Expected Result
- Actual Result
- Evidence
- Status
- Notes

### 📸 Evidence

Screenshots supporting reported defects and demonstrating the observed application behavior.

---

## 🐞 Defect Summary

| Bug ID | Summary | Severity | Priority | Status |
|---|---|---|---|---|
| BUG-001 | Order can be completed with an empty cart | High | High | Open |
| BUG-002 | Zip Code field accepts malformed input without validation | High (Critical if XSS executes) | High | Open |
| BUG-003 | Checkout validation reports only the first missing required field | Low | Low | New |

> Severity and priority were assigned based on the observed impact and urgency from the perspective of the tested application.

---

## 📁 Repository Structure

```
QA-Portfolio-Saucedemo/
│
├── README.md
│
├── Standard-User/
│   ├── Test-Cases/
│   │   └── Standard_User_Test_Cases.xlsx
│   │
│   └── Bug-Reports/
│       ├── Standard_User_Bug_Report.xlsx
│       └── Attachments/
│
├── Locked-Out-User/
│   ├── Test-Cases/
│   └── Bug-Reports/
│
├── Problem-User/
│   ├── Test-Cases/
│   └── Bug-Reports/
│
├── Performance-Glitch-User/
│   ├── Test-Cases/
│   └── Bug-Reports/
│
├── Error-User/
│   ├── Test-Cases/
│   └── Bug-Reports/
│
└── Visual-User/
    ├── Test-Cases/
    └── Bug-Reports/
```

---

## 🔗 Test Case → Bug Traceability

Failed test cases are linked to their corresponding defects to provide traceability between test execution and defect reporting.

| Test Case | Scenario | Related Defect |
|---|---|---|
| TC_019 | Cart becomes empty after removing the only item | BUG-001 |
| TC_027 | Cart is empty from the start | BUG-001 |
| TC_024 | Only the first missing required field is reported | BUG-003 |
| TC_025 | Zip Code field accepts invalid/malformed input | BUG-002 |

---

## 🌐 Application Under Test

- **Application:** SauceDemo
- **Purpose:** Practice / Educational Testing
- Testing was performed against the publicly available SauceDemo practice application.

---

## ⚠️ Disclaimer

This repository is an educational and portfolio project created to demonstrate manual QA testing skills. All testing was performed for learning and portfolio purposes on the SauceDemo practice application.

---

## 👩‍💻 Author

**Deema Salah**
QA Intern | Manual & API Testing
[LinkedIn] https://www.linkedin.com/in/deema-salah-2056412a6/ · 
[GitHub] https://github.com/DeemaSalah

