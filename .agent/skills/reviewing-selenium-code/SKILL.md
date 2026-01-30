---
name: reviewing-selenium-code
description: Reviews Selenium + Java automation code for syntax issues, logical bugs, anti-patterns, and framework design flaws. Provides optimized, production-grade code following SDET best practices.
---

# Selenium Code Reviewer

This skill empowers the agent to act as a Senior SDET and Automation Architect to perform deep code reviews of Selenium with Java automation scripts.

## When to use this skill
- When a user provides Selenium + Java code for review.
- When automation scripts are flaky or slow.
- When transitioning from basic scripts to a Page Object Model (POM) or a scalable framework.
- When converting Selenium scripts to Playwright.

## Workflow

1.  **[ ] Phase 1: Input Discovery**
    - Ask the user to provide the Selenium + Java code if not already provided.
    - Identify the context (unit test, integration test, framework component).

2.  **[ ] Phase 2: Line-by-Line Analysis**
    - Check for **Syntax issues** and **Logical bugs**.
    - Identify **Selenium anti-patterns** (e.g., `Thread.sleep()`, using local driver instances).
    - Review **Locator strategies** (prefer ID/CSS over fragile XPaths).
    - Evaluate **Wait strategies** (Hard waits vs Explicit/Fluent waits).
    - Check **Exception handling** and **Java bad practices**.
    - Spot **Code duplication** and naming convention violations.

3.  **[ ] Phase 3: Strategic Optimization**
    - Propose the use of **Explicit Waits (WebDriverWait)**.
    - Suggest **Page Object Model (POM)** structure.
    - Outline **Reusable Utility Methods**.
    - Recommend **Logging (SLF4J/Log4j)** and **Reporting (Extent/Allure)**.
    - Design for **Config-driven** execution.

4.  **[ ] Phase 4: Implementation (Corrected Code)**
    - Generate the refactored, production-grade code.
    - Ensure clean formatting and proper Java documentation.

5.  **[ ] Phase 5: Education & Explanation**
    - Explain "The Why" behind every major change.
    - Highlight the specific best practice applied (e.g., SRP, DRY, Clean Code).

## Advanced Mode (Conditional)
- **Framework Context**: If multiple files are provided, suggest a multi-module architecture (Maven/Gradle).
- **Transformation**: If requested, convert the code to **Playwright** (Java/TypeScript) maintaining the functional intent.

## Instructions
- Always prioritize **Stability over Speed** by using smart waits.
- Ensure **Locators** are resilient (avoid absolute XPaths).
- Use **Self-explanatory naming** (e.g., `clickLoginButton()` instead of `clickBtn()`).
- Encapsulate driver management.

## Resources
- [Example Bad vs Good Code](examples/review-examples.md)
