# GitHub CLI (gh)

### What is it?

GitHub CLI, known by its command name `gh`, is an open-source tool that brings GitHub's core functionality—including issues, pull requests, releases, and repository management—directly to the terminal. It serves as a command-line interface for GitHub, allowing developers to manage their collaborative workflows without switching context between their terminal and a web browser.

In the software development ecosystem, GitHub CLI belongs to the **developer productivity and collaboration layer**. It complements the standard `git` command-line tool by providing access to the "social" and "administrative" features that GitHub layers on top of the Git version control system.

### Installation (Optional)

!!! note
    CodeCampus OS includes GitHub CLI by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Ubuntu / Debian"
    ```bash
    type -p curl >/dev/null || (sudo apt update && sudo apt install curl -y)
    curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
    sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
    sudo apt update
    sudo apt install gh -y
    ```

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S github-cli
    ```

=== "Fedora"
    ```bash
    sudo dnf install gh
    ```

### Why this tool matters (In Depth)

The greatest enemy of developer productivity is "context switching." Every time an engineer leaves their terminal to navigate a complex web interface, they break their concentration and lose the "flow state" required for complex problem-solving. GitHub CLI matters because it **consolidates the entire engineering lifecycle into the terminal**.

By enabling actions like creating pull requests, checking CI/CD status, and reviewing issues through a typed interface, `gh` allows developers to maintain focus on their code. Furthermore, GitHub CLI is built for **scripting and automation**. Tasks that would require multiple manual clicks in a browser can be condensed into a single shell command or integrated into a larger automation script.

For students, mastering `gh` marks the transition from being a "user" of GitHub to an "engineer" on GitHub. It encourages a more disciplined, keyboard-centric approach to collaboration, significantly reducing the "overhead" of managing open-source contributions or team projects.

### How students will actually use it

Students will use GitHub CLI to streamline their collaborative development:

*   **Repository Initialization:** Rapidly creating a new GitHub repository (`gh repo create`) and linking it to their local code without manual URL copying.
*   **Pull Request Management:** Creating, listing, and tracking the status of pull requests (`gh pr create`, `gh pr list`, `gh pr status`) directly from the branch they are working on.
*   **CI/CD Visibility:** Checking the outcome of automated tests and build actions (`gh run watch`) without waiting for browser notifications.
*   **Issue Tracking:** Creating and reviewing bug reports or task lists (`gh issue create`, `gh issue list`) as they identify them in their code.
*   **Secure Authentication:** Managing OAuth tokens and SSH keys (`gh auth login`) through a guided, secure terminal interface that eliminates the danger of manual token handling.

### Professional Insight (Top 1% Knowledge)

The "Top 1%" of productive engineers use GitHub CLI to **automate the mundane**. A professional habit is to use aliases and scripts to perform multi-step operations. For example, a senior engineer might have a script that creates a branch, pushes code, opens a pull request, and assigns a reviewer—all with a single custom command like `gh pr-ready`.

Another high-level skill is using **GitHub CLI Extensions**. Since `gh` is extensible, professional developers often install community-built plugins for managing GitHub Projects, analyzing repository statistics, or integrating with specialized cloud services. This allows them to customize their CLI to fit their specific team's workflow perfectly.

Finally, a senior developer knows how to use the **`--json` and `--jq` flags** to filter and process GitHub data. Instead of just reading text, they can extract specific information—like the names of all open PRs with a specific label—and pipe that data into other terminal tools. This ability to treat GitHub as a queryable data source is what enables the high-level automation and reporting that defines enterprise-grade engineering. Adopting `gh` isn't just about speed; it's about gaining programmatic control over your collaborative ecosystem.
