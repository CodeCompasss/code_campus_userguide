# CodeCampus OS — Official User Guide Specification

## Purpose

This document defines the writing standards for the CodeCampus OS User Guide.

The guide is designed for:
- Beginner software engineers
- Computer Science & Engineering (CSE) students
- Self-learners who are new to Linux-based development environments

The goal is **not** to simply list tools, but to teach students:
- What each tool is
- Why it exists
- How it is used in real-world software development workflows

CodeCampus differentiates itself from other setups (such as Omakub) by providing:
- Deep, student-focused explanations
- Clear installation instructions for multiple Linux distributions
- Practical guidance instead of surface-level descriptions

---

## Writing Style Rules

- Clear, direct, and professional
- Beginner-friendly, but **never dumbed down**
- No marketing language
- No generic or AI-style filler content
- Prefer explanations over buzzwords
- Assume curiosity and willingness to learn, not prior expertise

---

## Required Structure for Every Tool Section

Every tool **must** follow the structure below exactly.

---

## Tool Name

Use a clear and descriptive main heading.

Example:
```markdown
## Git
````

---

### What is it?

Explain:

* What the tool is
* What problem it solves
* Where it fits in the software development ecosystem

This section must be understandable to a first-year CS student with minimal prior exposure.

---
### Installation (Optional)

!!! note
    CodeCampus OS includes this tool by default.
    Use the commands below only if installing on another distribution.

=== "Ubuntu / Debian"
    ```bash
    sudo apt install git
    ```

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S git
    ```

=== "Fedora"
    ```bash
    sudo dnf install git
    ```

=== "openSUSE"
    ```bash
    sudo zypper install git
    ```

### Why this tool matters (In Depth)

This is the **most important section**.

Explain in detail:

* Why students should care about this tool
* How it improves productivity or understanding
* What problems students will face without it
* Where and how it is used in real-world projects

Write this as a thoughtful explanation, not bullet-point hype.

---

### How students will actually use it

Explain:

* Common real-world usage scenarios
* Typical beginner-level workflows or commands
* How the tool fits into daily development work

If commands are shown, clearly explain **what each command does and why it is used**.

---

### Professional Insight (Top 1% Knowledge)

Provide insight that:

* Beginners usually do not know
* Reflects how experienced engineers think about this tool
* Helps students avoid common mistakes or bad habits

This section should feel like advice from a senior engineer or mentor.

---

## Formatting Rules

* Use Markdown headings only
* Use tables **only** for installation instructions
* Avoid emojis
* Avoid unnecessary bullet lists
* Prefer clear paragraphs and explanations

---

## End Goal

After reading a tool section, a student should:

* Understand **why** the tool exists
* Know **how** to install it on their Linux distribution
* Know **when and how** to use it correctly
* Feel confident exploring the tool further on their own


