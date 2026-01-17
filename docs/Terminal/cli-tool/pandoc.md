# Pandoc

### What is it?

Pandoc is a powerful, open-source Haskell library and command-line tool for converting files from one markup format into another. It is widely considered the "Swiss Army knife" of document conversion, supporting a vast array of formats including Markdown, HTML, LaTeX, Docx, PDF, EPUB, and many others.

In the software development ecosystem, Pandoc belongs to the **documentation and publishing layer**. It allows developers to maintain their documentation in a single, simple format (usually Markdown) and programmatically generate output in whatever format is required for publishing, distribution, or submission.

### Installation (Optional)

!!! note
    CodeCampus OS includes Pandoc by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S pandoc
    ```

=== "Ubuntu / Debian"
    ```bash
    sudo apt install pandoc
    ```

=== "Fedora"
    ```bash
    sudo dnf install pandoc
    ```

### Why this tool matters (In Depth)

In professional engineering and academia, information is consumed in many different ways. A technical blog post might need to be HTML, an internal report might need to be a Word document for non-technical stakeholders, and a published research paper might require strict LaTeX-based PDF formatting. Pandoc matters because it **decouples content from presentation**.

Instead of manually reformatting or rewrite information for different audiences, Pandoc allows for a "single source of truth" workflow. A developer can write their project documentation in Markdown—the native language of version control systems like Git—and then use Pandoc to instantly convert that Markdown into a professional-looking PDF or an interactive slide deck. This automation ensures that documentation remains consistent and up-to-date across all distributed formats, significantly reducing the "documentation tax" associated with large-scale projects.

For students, Pandoc is an essential tool for **academic technical writing**. It allows them to write assignments in simple Markdown while generating papers that strictly adhere to academic formatting standards (like IEEE or APA) through the use of citation management and custom templates.

### How students will actually use it

Students will use Pandoc to transform and professionalize their technical writing:

*   **Markdown to PDF:** Converting their class notes or project READMEs into clean, formatted PDFs for submission or sharing.
*   **README to Docx:** Rapidly generating Word documents from GitHub projects for stakeholders who do not use Markdown editors.
*   **Static Site Generation:** Converting documentation into clean HTML for hosting on personal websites or GitHub Pages.
*   **Code Presentation:** Using Pandoc to generate PDF or HTML slide decks (using formats like Reveal.js or Beamer) directly from their technical notes.
*   **Academic Formatting:** Using BibTeX or CSL files with Pandoc to automatically manage citations and bibliographies in their technical reports.

### Professional Insight (Top 1% Knowledge)

The "Top 1%" of technical writers and engineers use Pandoc as a **programmable publishing pipeline**. A professional habit is using **Pandoc Filters** (often written in Lua or Python). Filters allow you to programmatically modify the document's structure during conversion—for example, automatically numbering figures, calculating and inserting mathematical results, or transforming specific tags into custom UI components.

Another high-level skill is the creation of **Custom Templates**. Senior engineers maintain their own LaTeX or HTML templates that define the exact typography, headers, and metadata required for their company or personal brand. This ensures that every document they produce has a consistent, professional, and unique "look and feel" without any manual design work.

The "Top 1%" insight is the integration of Pandoc into **CI/CD pipelines**. Every time code is pushed, a server can automatically run Pandoc to regenerate the project's documentation site, user manual, and PDF specification. This ensures that the documentation is never "out of sync" with the code. Mastering Pandoc means moving beyond simple file conversion to understanding the "Document Object Model" (AST) that underlies all structured text. Finally, always check the **Pandoc User's Guide** for the specific flags related to your output format—fine-tuning the conversion process is what separates a generic document from a polished, professional publication.
