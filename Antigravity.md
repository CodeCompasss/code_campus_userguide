

# CodeCampus OS — Official User Guide Specification

## Purpose

This document defines the official writing standards for the **CodeCampus OS User Guide**.

The guide is designed for:

* Beginner software engineers
* Computer Science & Engineering (CSE) students
* Self-learners who are new to Linux-based development environments

The goal is **not** to simply list tools or provide installation instructions. Instead, the guide must teach students:

* What each tool is
* Why the tool exists
* How it is actually used in real-world development workflows, with concrete examples

CodeCampus OS differentiates itself from other setups by emphasizing:

* Deep, student-focused explanations
* Clear installation instructions for multiple Linux distributions
* Practical, hands-on guidance instead of surface-level descriptions

---

## Writing Style Rules

Content must follow these principles:

* Clear, direct, and professional
* Beginner-friendly, but **never dumbed down**
* No marketing language or vague buzzwords
* No generic filler content
* Prefer **explanations over definitions**
* Assume readers are curious and motivated, but may have minimal prior knowledge

The writing should feel like a mentor guiding the student step-by-step, not like a technical reference sheet or promotional page.

---

## Required Structure for Every Tool Section

Every tool section **must** follow the structure below exactly.
The goal is to ensure that beginners can **understand, install, and start using the tool immediately**, with real examples.

---

## Tool Name

Use a clear Markdown heading.

Example:

```markdown
## Git
```

---

### What is it?

Explain in beginner-friendly language:

* What the tool is
* What problem it solves
* Where it fits in the software development ecosystem

This section should provide a **conceptual understanding**, so a first-year CS student can answer:
*"What does this tool do, and why would I need it?"*

---

### Installation

Provide installation instructions for each supported Linux distribution using this format:
it is mkdocs tab (horizontal tabs)

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

Do not include commentary in this section; it is purely for installation commands.

---

### Why this tool matters (In Depth)

This is the **most important section**. Explain thoroughly:

* Why students should care about this tool
* How it improves productivity or understanding
* Common problems students face without it
* Real-world scenarios where professionals use it

**The explanation must go beyond surface-level descriptions**, including examples of typical beginner mistakes and why using the tool correctly matters.

---

### How students will actually use it

This section must include **concrete, beginner-friendly examples**, such as:

* Real-world workflows or tasks a student might perform
* Example commands with detailed explanations of **what they do and why they are used**
* Screenshots or textual descriptions of expected outputs (if applicable)
* Step-by-step mini-tutorials that a student can try immediately

It should answer: *“If I open this tool right now, what should I do first, and how does it fit into my workflow?”*

---

### Professional Insight

Provide guidance that goes beyond beginner usage:

* Explain insights that **experienced engineers know** but beginners often miss
* Warn about common pitfalls or bad habits
* Highlight ways to use the tool **effectively for learning and professional workflows**

This section should feel like advice from a senior engineer or mentor, helping the student build correct habits early.

---

## Formatting Rules

* Use Markdown headings only
* Use tables **only** for installation instructions
* Avoid emojis
* Avoid unnecessary bullet lists (unless they clarify a step-by-step workflow)
* Prefer clear paragraphs with **in-depth explanations**

---

## End Goal

After reading a tool section, a student should be able to:

* Understand **why** the tool exists
* Know **how** to install it on their Linux distribution
* Know **how to start using it immediately**, with practical beginner examples
* Understand common pitfalls and professional usage habits
* Feel confident exploring the tool further independently

