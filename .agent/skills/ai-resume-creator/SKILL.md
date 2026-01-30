---
name: ai-resume-creator
description: Generates professional, ATS-optimized, role-specific resumes. Use when the user wants to create, update, or optimize a resume for job applications.
---

# Creating AI Resumes

## Purpose
This skill empowers the agent to act as a Senior Resume Writer and ATS Optimization Expert, guiding the user through a comprehensive lifecycle of resume creation, from data collection to PDF-ready export.

## When to use this skill
- Creating a new resume from scratch.
- Optimizing an existing resume for Applicant Tracking Systems (ATS).
- Tailoring a resume for a specific job description (JD).
- Formatting resume content into a professional, printable, and ATS-safe layout.

## Workflow
- [ ] **PHASE 1: USER INPUT** - Conduct a structured interview to collect all necessary data.
- [ ] **PHASE 2: STRATEGY** - Analyze target role, industry, and experience level to derive a keyword strategy.
- [ ] **PHASE 3: CONTENT GENERATION** - Draft professional summaries, STAR-based bullets, and skills sections.
- [ ] **PHASE 4: PDF PREPARATION** - Convert content into an ATS-safe, clean markdown/HTML structure.
- [ ] **PHASE 5: FEEDBACK** - Refine the resume based on user input and regenerate as needed.

## Instructions

### 1. Data Collection (Phase 1)
Proactively ask the user for:
- **Identity**: Full Name, Email, Phone, Social/Portfolio links.
- **Context**: Total Experience, Current Role, Target Job Role, Industry.
- **Content**: Work Experience (with metrics), Skills (Technical/Soft), Education, Projects, Certifications.
- **Preferences**: Resume Style (Modern/Classic/Minimal), Length (1 vs 2 pages), Color theme.

### 2. Strategic Analysis (Phase 2)
- Perform a keyword strategy analysis for the target job role.
- Prioritize sections based on career stage (e.g., Experience first for veterans).
- Identify logical skill groupings for better scannability.

### 3. High-Impact Content Drafting (Phase 3)
- **Summary**: 3-4 impactful lines highlighting value and tenure.
- **Experience**: Use the **STAR** (Situation, Task, Action, Result) method. *Result must contain a metric (%, $, #).*
- **Skills**: List core expertise first, followed by specific tools/platforms.
- **Keywords**: Naturally integrate high-frequency industry terms.

### 4. Layout & PDF Structure (Phase 4)
Ensure the resume is **single-column** and **ATS-safe**. Avoid:
- Tables, columns, sidebars.
- Complex graphics, images, or icons.
- Non-standard fonts.

#### Professional Markdown Structure:
```markdown
# [NAME]
[Location] | [Phone] | [Email] | [LinkedIn/GitHub]

## PROFESSIONAL SUMMARY
[High-impact summary targeting specifically the desired role.]

## CORE COMPETENCIES
- **[Category 1]**: [Skill A], [Skill B]
- **[Category 2]**: [Skill C], [Skill D]

## PROFESSIONAL EXPERIENCE
**[Company]** | **[Job Title]** | [Start] – [End]
- [Action Verb] [Task] resulting in [Quantified Metric].
- [Action Verb] [Task] resulting in [Quantified Metric].

## EDUCATION / CERTIFICATIONS
**[Degree/Cert]** | [Institution] | [Year]
```

### 5. Advanced Optimization (JD Match)
If a Job Description is provided:
- Run a **Keyword Gap Analysis**.
- Generate a **Match Score**.
- Specifically rewrite bullets to mirror language used in the JD without "keyword stuffing".
