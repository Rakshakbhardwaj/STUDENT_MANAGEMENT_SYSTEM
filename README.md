# Software Testing Techniques: An Online Shopping Application Case Study

A comprehensive case study analyzing software defects in a launched e-commerce platform and providing a structured testing framework to ensure transaction accuracy, security, and scalability under heavy loads[cite: 2, 3].

---

## Document Details

| Field | Information |
| :--- | :--- |
| **Institution** | Chandigarh University — University Institute of Computing[cite: 2] |
| **Course** | Software Engineering[cite: 2] |
| **Author** | Rakshak (UID: 25BCD10102)[cite: 2] |
| **Program / Section** | BCA (Data Science), Semester 3, Section 25BCD2(A)[cite: 2] |
| **Faculty Mentor** | Mrs. Shilpa Mahajan (Assistant Professor)[cite: 2] |
| **Submission Date** | 31/11/2026[cite: 2] |

---

## Executive Summary

After launching a web and mobile shopping platform, the business suffered customer complaints, abandoned carts, and financial discrepancies due to inadequate pre-release testing[cite: 3]. Critical problems included:

* **Price Discrepancies:** Mismatched amounts between catalog listings and the checkout cart[cite: 3].
* **Payment Failures:** Money deducted from accounts without order confirmation, and risks of double charging[cite: 3].
* **Performance Degradation:** Timeouts and system freezes during high-traffic sale events[cite: 3].
* **Security & Cart Flaws:** Flawed quantity calculations and weak access controls exposing user data[cite: 3].

The case study presents a full remediation roadmap using multi-tier software testing techniques[cite: 3, 4].

---

## Key Testing Techniques Covered

* **Black-Box Testing:** Evaluates inputs vs. expected outputs without source code access (e.g., verifying subtotal calculations, form field validations)[cite: 4].
* **White-Box Testing:** Analyzes source code logic, branches, and calculation routines (e.g., pricing formulas with delivery fees and taxes)[cite: 4].
* **Unit Testing:** Tests individual functions in isolation (e.g., checking zero-item totals, discount deduction logic)[cite: 4].
* **Integration Testing:** Assesses data transfer across connected modules (e.g., catalog, cart, payment gateway, inventory, order processing)[cite: 3, 5].
* **System Testing:** Validates end-to-end user workflows from authentication through delivery tracking[cite: 5].
* **Regression Testing:** Re-runs core test suites after code changes to ensure existing features remain stable[cite: 5].
* **Performance Testing:** Load-tests the platform under high traffic (e.g., 1,000+ concurrent shoppers) to detect bottlenecks[cite: 5].
* **Security Testing:** Audits authorization, input sanitization, and session safety to prevent data leaks and ID tampering[cite: 5].

---

## Proposed Solution & Implementation Roadmap

1. **Requirement Analysis:** Map out explicit expected behaviors for all functional flows (search, checkout, refunds, tracking)[cite: 5].
2. **Test Planning:** Prioritize critical high-risk modules (payments, user credentials, real-time inventory updates)[cite: 6].
3. **Formal Test Case Execution:** Run structured test matrices covering positive, negative, and edge-case inputs[cite: 6].
4. **Idempotent Payment Handling:** Implement strict transaction IDs and duplicate-request protection to prevent double billing on connection drops[cite: 6].
5. **Pre-Sale Load & Security Audits:** Conduct synthetic stress testing and OWASP-guided vulnerability checks before festival sales[cite: 6].
6. **Continuous Regression & Defect Tracking:** Maintain automated checks for core workflows and log defects with reproduction steps, severity, and resolution verification[cite: 6].

---

## Standards & References

* R. S. Pressman & B. R. Maxim — *Software Engineering: A Practitioner's Approach*
* I. Sommerville — *Software Engineering*
* ISO/IEC/IEEE 29119 Series — *Software Testing*
* ISTQB — *Certified Tester Foundation Level (CTFL)*
* OWASP Foundation — *Web Security Testing Guide (WSTG)*
