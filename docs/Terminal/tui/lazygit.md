# Lazygit

### What is it?

Lazygit is a simple terminal user interface (TUI) for Git commands. It provides a visual dashboard inside the terminal that consolidates repository status, file diffs, commit history, and branch management into a single, interactive view. Written in Go, it is designed to be extremely fast and keyboard-centric, allowing developers to perform complex Git operations without leaving their terminal environment or manually typing out lengthy command-line strings.

In the software development ecosystem, Lazygit belongs to the **version control and developer productivity layer**. It acts as a high-efficiency wrapper around the Git CLI, making it easier to visualize and manage the state of a repository during the development process.

### Installation (Optional)

!!! note
    CodeCampus OS includes Lazygit by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S lazygit
    ```

=== "Ubuntu / Debian"
    ```bash
    LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')
    curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
    tar xf lazygit.tar.gz lazygit
    sudo install lazygit /usr/local/bin
    ```

=== "Fedora"
    ```bash
    sudo dnf copr enable atim/lazygit -y
    sudo dnf install lazygit
    ```

### Why this tool matters (In Depth)

Git is the most powerful and widely used version control system in the world, but its command-line interface is notoriously complex and non-visual. Performing tasks like staging specific lines of a file, managing multiple stashes, or resolving complex merge conflicts can be prone to a high degree of manual error when done purely via text commands. Lazygit matters because it **provides visual clarity to the abstract state of a Git repository**.

By presenting the repository's files, branches, and commits in an organized multi-pane interface, Lazygit allows developers to see precisely what they are about to commit or push. Its split-screen diff view makes code review a seamless part of the workflow rather than a separate, tedious task. Furthermore, Lazygit automates common patterns—such as squashing commits, interactive rebasing, or cherry-picking—into single keystrokes. This reduces the cognitive load of version control, allowing engineers to focus on the logic of their code rather than the mechanics of its management.

For students, Lazygit provides a safe and interactive environment to learn Git best practices. It demystifies the relationship between local and remote states and makes the "commit often, commit early" philosophy easier to adopt through its frictionless interface.

### How students will actually use it

Students will use Lazygit as their main interface for version control:

*   **Interactive Staging:** Using the spacebar to rapidly stage individual files or even specific chunks of code (`v` for visual mode) within a file.
*   **Contextual Committing:** Writing clear commit messages and instantly seeing how they fit into the project's timeline within the "Commits" pane.
*   **Branch Management:** Creating, switching, and merging branches with interactive prompts, reducing the risk of accidental data loss.
*   **Conflict Resolution:** Identifying and resolving merge conflicts using the visual comparison tool built directly into the interface.
*   **Local History Exploration:** Scrolling through the commit log to understand when and why specific changes were made to the codebase.

### Professional Insight (Top 1% Knowledge)

The "Top 1%" of productive engineers use Lazygit to **maintain an immaculate commit history**. A professional habit is the extensive use of **Interactive Rebasing**. While the Git CLI's rebase command is cumbersome, Lazygit allows a developer to reorder, squash, or rename commits with just a few keystrokes (`e` for edit, `s` for squash) before pushing to a shared repository. This ensures that the public history of a project is clean, logical, and easy for other team members to follow.

Another high-level skill is leveraging **custom keybindings and user-defined commands**. Lazygit allows users to extend the TUI with their own shell scripts. A senior engineer might add a shortcut to trigger a specific CI/CD build, run a linter on changed files, or automatically format a commit message following a company-wide template.

The "Top 1%" insight is the use of Lazygit for **surgical code surgery**. By using the "Patch" feature (often bound to `p`), an expert can extract specific changes they've made to their local files and apply them to a different branch without needing to commit the entire file. This level of granular control—managed visually but executed with the speed of a TUI—is what defines a high-velocity developer. Finally, remember that Lazygit is a tool for *your* workflow; its goal is to make version control invisible so that your creativity can remain focused on the code itself.
