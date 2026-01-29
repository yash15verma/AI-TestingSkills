# TEST PLAN: StarCare Health Insurance Platform

## 1. Document Control
- **Document ID**: TP-STARECARE-001
- **Owner**: Senior QA Architect
- **Approver**: Product Owner, Compliance Team

## 2. Revision History
| Version | Date | Author | Description |
|---------|------|--------|-------------|
| 1.0     | 2026-01-30 | AI Test Plan Creator | Initial Draft based on BRD/PRD |

## 3. Introduction
This Test Plan outlines the testing strategy for the StarCare Health Insurance Platform, a digital insurance ecosystem designed for online policy purchase, renewal, and real-time claim processing.

## 4. Objectives
- Validate the complete digital insurance lifecycle (Onboarding to Settlement).
- Ensure 100% compliance with security (OWASP) and accessibility (WCAG) standards.
- Verify system scalability to handle 1 million monthly users.
- Achieve a 60% reduction in claim processing turnaround time through automated validation.

## 5. Scope
**Includes**: 
- Customer Onboarding & KYC.
- Policy Selection, Premium Calculation & Purchase.
- Claim Intimation, Document Upload, and Real-time Tracking.
- Admin & Operations Dashboards.
- Integrations: Razorpay, SMS Gateway, Email Service, CRM.

**Excludes**: 
- Agent onboarding and CRM redesign (out of scope for Phase 1).
- Legacy system re-architecture.

## 6. Test Items
- StarCare Web Platform (Build v1.0).
- Razorpay Sandbox Environment.
- AWS S3 for Document Storage.
- Claims Processing Microservices.

## 7. Features to be Tested
- **User Registration**: Email, Phone, and OTP (FR-1).
- **Policy Management**: Plan viewing, Premium calculation (FR-2).
- **Payments**: Razorpay Gateway Integration (FR-3).
- **Claims**: Document upload, form submission, status tracking (FR-4, FR-5).
- **Analytics**: Sales dashboard, settlement metrics.

## 8. Features Not to be Tested
- Post-settlement legacy reconciliation.
- Third-party social media authentication (not in PRD).

## 9. Test Strategy
- **Risk-Based Testing**: Prioritizing Payment and Claims modules.
- **Shift-Left**: Early API testing for Razorpay and SMS integrations.
- **Automation-First**: 70% automation target for regression and smoke tests.

## 10. Test Approach
- **Unit Testing**: Focused on Premium calculation logic.
- **System Testing**: End-to-end flow from registration to policy issuance.
- **Security Testing**: OWASP Top 10 vulnerability scanning.
- **Accessibility Testing**: WCAG 2.1 compliance check.

## 11. Test Environment
- **Web**: Chrome (v100+), Safari, Firefox, Edge.
- **Mobile Web**: iOS Safari, Android Chrome.
- **Servers**: QA Staging (AWS).

## 12. Test Data Strategy
- Synthesized KYC data for customer onboarding.
- Pre-defined premium calculation presets.
- Razorpay test cards for payment validation.

## 13. Test Automation Strategy
- **Tools**: Playwright for UI/E2E, Supertest for API validation.
- **Framework**: Page Object Model (POM) with Data-Driven Testing.

## 14. CI/CD Integration
- GitHub Actions pipeline triggered on every PR.
- Automated Sanity Run on Deployment to QA environment.

## 15. Test Execution Plan
- **Sprint 1-2**: Onboarding & Policy Purchase.
- **Sprint 3-4**: Claims Intimation & Integration Testing.
- **Sprint 5**: Non-Functional (Performance, Security) & UAT.

## 16. Entry Criteria
- Code deployment to QA complete.
- Test data (KYC/Cards) available.
- Requirements (BRD/PRD) signed off.

## 17. Exit Criteria
- 100% Critical/High defects resolved.
- 95% Test case pass rate.
- Sign-off from Compliance and Security teams.

## 18. Deliverables
- Test Plan (this document).
- Bug Reports in Jira.
- Test Execution Summary Report (TESR).
- Automated Test Suite Code.

## 19. Roles & Responsibilities
- **QA Lead**: Strategy and Environment oversight.
- **QA Engineers**: Test design and execution.
- **Security Lead**: OWASP vulnerability assessment.

## 20. Defect Management Process
- Defects logged in Jira.
- Triage meetings: Daily during execution phase.
- Priority levels: P1 (Blocker) to P4 (Minor).

## 21. Risk & Mitigation
| Risk | Probability | Impact | Mitigation Plan |
|------|-------------|--------|-----------------|
| Razorpay Sandbox Downtime | Medium | High | Use mocked payment responses for UI testing. |
| Compliance Delay | Low | High | Weekly sync with Compliance team. |

## 22. Assumptions & Dependencies
- Dependency on Razorpay API stability.
- Assumption: SMS gateway will be provided by 15th of the month.

## 23. Metrics & Reporting
- Defect Density.
- Test Case Pass/Fail % (Monthly).
- Automation coverage percentage.

## 24. Sign-off
- Product Owner: _________________
- Compliance Head: _________________
- Engineering Manager: _________________
