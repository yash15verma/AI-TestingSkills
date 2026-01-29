---
name: creating-test-plans
description: Generates professional, enterprise-grade Test Plan documents based on project inputs, BRDs, PRDs, or JIRA stories (including PDF formats). Use when the user needs a comprehensive QA strategy or a structured test plan following IEEE 829 / ISTQB standards.
---

# AI Test Plan Creator

## When to use this skill
- When starting a new project or sprint and a formal Test Plan is required.
- When the user provides project details and needs a structured QA strategy.
- When documentation like BRD, PRD, or JIRA stories is available to derive testing scope (supports PDF, Markdown, or text formats).

## Workflow
1. **[ ] Phase 1: Input Discovery** - Collect project metadata, scope, and strategy inputs using structured questions.
2. **[ ] Phase 2: Strategy Design** - Analyze inputs to derive approach, regression, automation, and environment strategies.
3. **[ ] Phase 3: Test Plan Generation** - Generate the document using the enterprise template in `resources/test_plan_template.md`.
4. **[ ] Phase 4: Review & Refinement** - Iterate based on user feedback.

## Instructions

### Phase 1: Input Discovery
If the user hasn't provided details, ask for:
- **Project Details**: Name, Client, Domain, App Type (Web/Mobile/API/Desktop), Version, Methodology (Agile/Waterfall), Environments.
- **Functional Scope**: Modules, Features, Integrations, APIs, Third-party dependencies.
- **Testing Scope**: Functional, Automation, API, Performance, Security, Accessibility, Compatibility.
- **Test Strategy Inputs**: Manual vs Auto %, Tools, CI/CD, Browsers, Devices, Test Data.
- **Team & Timeline**: Size, Roles, Dates, Sprint duration.
- **Risks & Constraints**: Risks, Dependencies, Assumptions.

### Phase 2: Strategy Design
Derive the following based on collected inputs:
- **Test Approach**: Testing levels (Unit, Integration, System, UAT).
- **Regression Strategy**: Selection criteria, frequency, automation level.
- **Automation Strategy**: Tool selection, framework type, scope for automation.
- **Environment & Data Strategy**: Requirements for test beds and data provisioning.

### Phase 3: Test Plan Generation
Use the template located at `resources/test_plan_template.md`. Ensure the document maintains professional, audit-friendly language and clear structure.

### Advanced Mode
- **BRD/PRD (including PDF formats)**: If provided, skip Phase 1 questions and auto-derive the plan.
- **JIRA stories (including PDF exports)**: Generate a sprint-specific test plan based on the story descriptions and acceptance criteria.

## Resources
- [Test Plan Template](resources/test_plan_template.md)
