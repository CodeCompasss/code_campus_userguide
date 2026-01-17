# VS Code

### What is it?

Visual Studio Code (VS Code) is a lightweight but powerful source code editor that runs on your desktop. It comes with built-in support for JavaScript, TypeScript, and Node.js and has a rich ecosystem of extensions for other languages (such as C++, C#, Java, Python, Go, PHP) and runtimes (such as .NET and Unity).

In the software development ecosystem, VS Code sits as the **primary workspace** for the majority of modern developers. It bridge the gap between a simple text editor and a full-featured Integrated Development Environment (IDE), offering the speed of the former with the intelligence of the latter.

### Installation (Optional)

!!! note
    CodeCampus OS includes VS Code by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Ubuntu / Debian"
    ```bash
    sudo apt update
    sudo apt install code
    ```

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S code
    ```

=== "Fedora"
    ```bash
    sudo dnf install code
    ```

### Why this tool matters (In Depth)

VS Code has become the industry standard for a reason: it solves the problem of "tooling fragmentation." Before VS Code, developers often had to switch between multiple heavy IDEs for different languages or settle for simple editors that lacked debugging and version control integration. VS Code provides a unified interface that can be tailored to any tech stack through its extension model.

For students, VS Code matters because it provides a professional-grade environment that grows with their skills. It introduces essential concepts like IntelliSense (smart code completion), integrated terminal usage, and visual debugging in a way that is accessible but not simplified. Mastering VS Code means mastering the workflow of the modern software industry; the same editor a student uses for their first "Hello World" is the one they will likely use in their first professional job at a major tech company.

Furthermore, its integration with Git and GitHub is seamless, teaching students the importance of version control from day one without requiring them to memorize complex command-line flags immediately.

### How students will actually use it

Students will use VS Code as their central hub for almost all programming tasks:

*   **Writing Code:** Utilizing IntelliSense and snippets to write cleaner code faster in languages like Python, C++, or Java.
*   **Debugging:** Setting breakpoints and stepping through code to understand program logic and find errors visually.
*   **Integrated Terminal:** Running commands, scripts, and compilers directly within the editor without switching windows.
*   **Version Control:** Using the built-in Git interface to stage changes, write commit messages, and push code to repositories.
*   **Extensions:** Installing specific tools like the "Live Server" for web development or "Remote - SSH" for working on university servers.

### Professional Insight (Top 1% Knowledge)

The "Top 1%" of VS Code users don't just write code in it; they automate their environment. A senior engineer treats their `settings.json` and `keybindings.json` as part of their professional identity. Specifically, you should learn to use the **Command Palette (Ctrl+Shift+P)** for everything. Reaching for the mouse to navigate menus is a sign of a beginner.

Another high-level skill is the use of **Multi-cursor editing (Alt + Click or Ctrl + Alt + Arrow)**. This allows you to perform repetitive edits across dozens of lines simultaneously, a task that would take minutes manually but takes seconds for an expert. Lastly, learn to use the **Integrated Terminal** for building and testing; developers who rely solely on GUI "Run" buttons often struggle when they eventually have to work on headless servers or CI/CD pipelines where no GUI exists.


