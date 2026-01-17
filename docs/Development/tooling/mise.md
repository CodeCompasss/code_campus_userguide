# mise

### What is it?

mise (formerly `rtx`) is a high-performance runtime executor and version manager for many different programming languages and development tools. It functions as a unified interface for installing and switching between multiple versions of tools like Node.js, Python, Ruby, Go, and Java, as well as managing environment variables and task execution.

In the software development ecosystem, mise belongs to the **development infrastructure and environment management layer**. It is designed to replace traditional, language-specific version managers (like `nvm`, `pyenv`, or `rbenv`) with a single, faster, and more feature-rich tool.

### Installation (Optional)

!!! note
    CodeCampus OS includes mise by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Standard Install"
    ```bash
    curl https://mise.jdx.dev/install.sh | sh
    ```

=== "Arch / Manjaro"
    ```bash
    yay -S mise-bin
    ```

=== "Ubuntu / Debian"
    ```bash
    gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys 0x7413A06D
    echo "deb [signed-by=/etc/apt/keyrings/mise-archive-keyring.gpg] https://mise.jdx.dev/deb stable main" | sudo tee /etc/apt/sources.list.d/mise.list
    sudo apt update
    sudo apt install mise
    ```

### Why this tool matters (In Depth)

In professional software engineering, the single most common cause of "broken builds" is version mismatch. A project might require Node.js 18.x to run its build scripts, but the developer has Node.js 20.x installed. Managing these discrepancies manually is error-prone and leads to significant time loss. mise matters because it provides **automated environment consistency**.

Unlike language-specific managers that often require complex shell hooks and slow your terminal startup, mise is written in Rust for near-instant execution. It allows a developer to define the exact versions of all their dependencies in a single `.mise.toml` or `.tool-versions` file within their project directory. When they enter that directory, mise automatically switches the active tool versions. This ensures that every developer on a team and the CI/CD pipeline are using the identical toolchain, eliminating an entire class of "setup-related" bugs.

For students, mise simplifies the transition to multi-language development. Instead of learning the unique syntax and quirks of four different version managers, they learn one unified command set. This reduces cognitive load and allows them to focus on learning the languages themselves rather than the infrastructure surrounding them.

### How students will actually use it

Students will use mise to maintain clean and reliable development environments:

*   **Universal Installation:** Installing runtimes (like `mise install node@20`) without needing sudo or affecting the system-wide packages.
*   **Automatic Version Switching:** Moving between project directories and having mise automatically set the correct Python, Ruby, or Node version based on the project's config file.
*   **Global Defaults:** Setting a "global" version of a tool that is used whenever they are not inside a specific project directory.
*   **Environment Secret Management:** Using mise to manage environment-specific variables (like `DATABASE_URL`) that are automatically loaded when they start their development server.
*   **Task Execution:** Using mise's built-in task runner to define project-specific aliases (like `mise run build`) that wrap complex shell commands into simple, memorable shortcuts.

### Professional Insight (Top 1% Knowledge)

The "Top 1%" of productive engineers value **instantaneous feedback**. Because mise is written in Rust, it performs its version switching and PATH modifications with negligible latency. A senior engineer knows that a slow terminal prompt (caused by slow version managers) is a constant, minor annoyance that accumulate into frustration over a workday.

Another professional trick is leveraging mise for **ephemeral tools**. Instead of globally installing a CLI tool that you only use occasionally (like a linter or a formatter), you can add it to your project's `mise.toml`. This ensures the tool is available only when you need it and in the specified version for that project. 

Finally, top-tier engineers use mise to **standardize team workflows**. By committing a `.mise.toml` file to their Git repository, they ensure that every team member—and the automated build agents—experience the exact same environment. This "infrastructure as code" approach (even for local development) is what separates hobbyist coding from professional engineering at scale. Treat mise as the "operating system for your project's development tools."


