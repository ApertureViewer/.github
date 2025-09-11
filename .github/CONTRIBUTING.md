# How to Contribute

Thank you for your interest in contributing to Aperture Viewer. We are passionate about building the most powerful creative engine for virtual worlds, and we value the feedback and insights of our user community.

This document outlines how you can effectively contribute to the project's success and provides the mandatory technical guidelines for any code contributions.

---

## The "Studio Model" of Development

It is important to understand that Aperture Viewer is developed using a **"Studio Model."** This means that development is an internally directed, high-velocity R&D effort that follows a long-range, mission-oriented roadmap.

While our code is open source, our development process is not a conventional community-driven model. This is a deliberate choice to ensure architectural integrity, maintain a consistent vision, and allow us to focus on solving complex, foundational problems.

---

## Reporting Bugs

The most valuable contribution from our community is the submission of high-quality, well-documented bug reports. Your detailed feedback is critical to the stability and improvement of the Aperture Viewer.

Before submitting a bug report, please adhere to the following protocol:

1.  **Search Existing Issues:** Diligently check our [**GitHub Issues**](https://github.com/ApertureViewer/Aperture-Viewer/issues) to ensure your problem has not already been reported.
2.  **Reproduce the Issue:** Confirm that you can reproduce the bug consistently on the latest release.
3.  **Gather Critical Information:** A report is only useful if it is actionable. Please prepare to provide:
    *   A clear and concise title.
    *   Detailed, step-by-step instructions to reproduce the bug.
    *   Your system specifications (OS, CPU, GPU, RAM).
    *   Any relevant log files (`ApertureViewer.log`).

> **[Click here to Submit a New Bug Report](https://github.com/ApertureViewer/Aperture-Viewer/issues/new?assignees=&labels=bug&template=bug_report.md&title=)**

## Feature Requests

Aperture Viewer is developed using a "Studio Model," meaning its features are planned and executed against a long-range, internally managed architectural roadmap.

> [!NOTE]
> While we appreciate the passion and creativity of our users, **we are not accepting feature requests or suggestions via GitHub Issues at this time.** This allows our development to remain focused on the current mission objectives.

---

## Submitting Code: The Pull Request Protocol

> [!IMPORTANT]
> **We do not accept unsolicited pull requests.**

In rare, pre-approved cases for a critical, self-contained bug fix, a code contribution may be requested by the development team after a thorough discussion in a GitHub Issue.

All development is planned and executed against our long-range, internally managed roadmap. While we deeply value the spirit of open-source collaboration, merging external code that is not aligned with this roadmap can introduce unforeseen complexities and disrupt mission-critical work.

If you have a critical, self-contained bug fix you believe is essential, please **open an issue first** to discuss the problem and your proposed solution with the development team.

### Contributor License Agreement (CLA) - Mandatory

Before any code can be considered for inclusion in the Aperture Viewer project, the contributor must agree to the terms of our CLA. This is a standard and non-negotiable legal requirement that protects both the contributor and the project.

*   **Process:** The CLA will be automatically presented via a GitHub Actions bot upon the creation of your first pull request.
*   **Action Required:** You must read the agreement and follow the bot's instructions to sign it digitally.
*   **Consequence:** We **cannot** review or merge any pull request until the CLA has been signed.

This process ensures that all contributions are properly licensed and that the project remains freely available to all users under the terms of the LGPL v2.1.

## Branching Strategy

*   **ALL development occurs on branches created from `dev`.**
*   Before commencing work, ensure your local `dev` is perfectly synchronized with `upstream/dev`. A rebase is strongly preferred to maintain a clean, linear history.
    ```bash
    git checkout dev
    git fetch upstream
    git rebase upstream/dev
    ```
*   Create a new, descriptively named branch for the specific, authorized task:
    *   `git checkout -b feature/name-of-mission-feature`
    *   `git checkout -b fix/issue-number-or-name-of-fix`
*   **Direct commits to `dev` or `master` are a protocol violation.**

## Core Coding Conventions

1.  **Aperture Commenting Style (Mandatory):**
    *   Multi-line Aperture blocks must use `// <AP:TAG>` and `// </AP:TAG>`. The project lead uses `<AP:WW>`.
    *   Single-line Aperture changes use `// <AP:TAG/>`.
    *   When replacing upstream code, the original code **must** be preserved by commenting it out within an `<FS:TAG>...</FS:TAG>` block.
    *   **Rationale:** This is a non-negotiable requirement for mission-critical code tracking and future maintainability.

2.  **Indentation:**
    *   **Use spaces, not tabs.** Configure your editor to 4 spaces per indent level. This aligns with upstream conventions and is mandatory for code hygiene.

3.  **General Style:**
    *   Adhere to the existing style of the codebase for bracing, spacing, and naming. When in doubt, consistency is the primary directive.

## Commit Message Protocol (Strictly Enforced)

We require a rigorous, three-part commit message format. Non-compliant messages will require a forced rewrite.

**Format:**
```
Type: Concise summary (max ~72 chars)

(Blank Line)

Body:
- A detailed, verbose description of WHAT was changed and WHY.
- Explain the strategic or tactical problem being solved.
- Reference relevant mission directives or issue numbers (e.g., "Fixes #123").

(Blank Line)

Testing:
- A detailed, step-by-step procedure that another engineer can follow to verify the fix or feature.
- Include the testing environment (OS, GPU).
- This section is MANDATORY and must be sufficient to guarantee QA.
```

**Allowed `Type` Prefixes:**
*   `Feature:`, `Fixes:`, `Enhance:`, `Refactor:`, `Perf:`, `Build:`, `Docs:`, `Style:`, `Chore:`, `Test:`

## Pull Request Requirements

Pull Requests will only be accepted from authorized collaborators following a prior discussion in a GitHub Issue.
*   **Local Testing Mandate:** All changes must be thoroughly tested locally *before* a pull request is submitted. This includes a clean recompile, execution of the test plan documented in your commit(s), and verification that no new regressions have been introduced.
*   **Title:** Must be clear and follow the `Type:` convention from the commit protocol.
*   **Description:** Must clearly state the "what" and "why," and explicitly link any fixed Issues (e.g., `Fixes #123`).
*   **Testing Section:** The complete testing procedure from your commit(s) must be copied into the PR description for review.
*   **Checklist:** Acknowledge that your submission adheres to all protocols herein.

## License

By contributing to Aperture Viewer, you agree that your contributions will be licensed under the GNU Lesser General Public License, version 2.1 (LGPL v2.1).

---

> [!NOTE]
> For all other forms of potential contribution or inquiry, please refer to our canonical **[Ways to Contribute](Ways-to-Contribute)** and **[Contact & Support Policy](Contact-&-Support)** documents.
