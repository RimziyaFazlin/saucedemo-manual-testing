# Manual Testing of SauceDemo E-commerce Web Application

A manual software quality assurance (SQA) project that tests the main features of [SauceDemo](https://www.saucedemo.com), a demo online shop built for testing practice. It covers planning, test case design, execution, defect reporting, and a final summary report.

**Tester:** Rimziya Fazlin
**Test period:** October 2026
**Type:** Manual functional testing

---

## Project Overview

The goal was to check that the core shopping flow works correctly (login, browsing products, cart, and checkout) and to report any defects found, the way a QA team would on a real project.

## Test Environment

| Item | Details |
|---|---|
| Application | https://www.saucedemo.com |
| Device | ZTE A202ZT |
| OS | Android 12 |
| Browser | Google Chrome [152.0.7977.82] |
| Test users | `standard_user`, `locked_out_user`, `problem_user` |

## Scope

**In scope:** login and logout, product listing and sorting, add to and remove from cart, checkout, access without login, basic UI checks.

**Out of scope:** performance and load testing, security testing, automation.

## Deliverables

| Document | Description |
|---|---|
| [Test Plan](Test_Plan.docx) | Objectives, scope, environment, approach, entry and exit criteria, risks, schedule |
| [Test Cases](Test_Cases.xlsx) | 34 test cases with steps, expected result, actual result, and status |
| Bug Report (tab in the Test Cases file) | 5 defects with steps to reproduce, severity, priority, and screenshot reference |
| [Test Summary Report](Test_Summary_Report.docx) | Execution results, defect summary, findings, and conclusion |
| [Screenshots](screenshots/) | Evidence for each reported bug |

## Test Types Covered

- **Functional:** login, cart, checkout, logout
- **Negative:** wrong password, invalid username, locked-out user, access without login
- **Validation:** empty fields on login and checkout forms
- **UI:** product images, button states, sorting

## Results at a Glance

| Metric | Count |
|---|---|
| Total test cases | 34 |
| Passed | 29 |
| Failed | 5 |
| Pass rate | 85.3% |

| Severity | Bugs |
|---|---|
| Critical | 1 |
| High | 2 |
| Medium | 2 |
| Low | 0 |

## Defects Found

All defects were found with `problem_user`, a SauceDemo account that is intentionally faulty for practice.

| Bug ID | Title | Severity |
|---|---|---|
| BUG01 | All products show the same image | Medium |
| BUG02 | "Add to cart" does not work for some products | High |
| BUG03 | "Remove" does not work for some products on the inventory page | High |
| BUG04 | Sort dropdown does not reorder products | Medium |
| BUG05 | Checkout blocked: text typed in Last Name goes into First Name | Critical |

## Key Findings

- `standard_user` flows (login, cart, checkout, logout) worked as expected.
- Login validation messages and the locked-out user message were correct.
- `problem_user` showed defects in images, cart actions, sorting, and checkout. The checkout defect (BUG05) is the most serious because a purchase cannot be completed.

## Skills Demonstrated

- Writing a test plan, test scenarios, and test cases
- Manual test execution and result recording
- Bug reporting with severity and priority
- Test summary reporting
- Documentation with Google Sheets, Google Docs, and Microsoft Word

## Limitations

- Testing was done on one device and one browser.
- Only three of the available SauceDemo users were tested.
- This is a demo application, so some defects are intentional.

## Repository Structure

```
├── README.md
├── Test_Plan.docx
├── Test_Cases.xlsx          (includes Bug Report sheet)
├── Test_Summary_Report.docx
└── screenshots/
    ├── BUG01
    ├── BUG02
    ├── BUG03
    ├── BUG04
    └── BUG05
```

## Contact

**Rimziya Fazlin**
LinkedIn: https://www.linkedin.com/in/rimziya-fazlin

Email: rimziyafazlin118@gmail.com