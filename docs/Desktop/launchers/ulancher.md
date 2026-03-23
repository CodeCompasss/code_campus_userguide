# Ulauncher

### What is it?

Ulauncher is a fast, keyboard-driven application launcher for Linux. It is designed to help users find and open applications, search through files, and perform system tasks without ever moving their hands away from the keyboard. For developers, it serves as the central interface for navigating their operating system, analogous to Alfred on macOS.

### Installation (Optional)

!!! note
    CodeCampus OS includes Ulauncher by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Ubuntu / Debian"
    ```bash
    sudo add-apt-repository ppa:agornostal/ulauncher
    sudo apt update
    sudo apt install ulauncher
    ```

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S ulauncher
    ```

=== "Fedora"
    ```bash
    sudo dnf install ulauncher
    ```

### Why this tool matters (In Depth)

In professional software development, maintaining focus and minimizing friction are essential for productivity. Every time a developer lifts their hand from the keyboard to navigate a graphical menu with a mouse, they incur a cognitive "context switch" penalty. While seemingly minor, these interruptions break the "flow state"—the period of deep concentration required for complex problem-solving.

Ulauncher eliminates this friction by providing a unified, keyboard-first command interface. Beyond simple application launching, it reduces the need to navigate through complex file structures or multiple browser tabs for simple tasks. By integrating system commands, file searches, and web shortcuts into a single prompt, Ulauncher allows you to navigate your entire development environment at the speed of thought. Mastering a launcher is a fundamental step in transitioning from a casual user to a high-output software engineer.

### How students will actually use it

Students will primarily use Ulauncher to navigate their daily development environment without distraction:

*   **Launching Applications:** Press `Alt + Space` and type the first few letters of your tool (e.g., `cod` for VS Code, `ter` for Terminal) and hit Enter.
*   **Quick Calculations:** Perform math directly in the search bar (e.g., `2^10` or `150 * 1.05`) to avoid opening a separate calculator application.
*   **File and Folder Search:** Find specific project directories or configuration files instantly without browsing through a file manager.
*   **Web Search Shortcuts:** Use predefined keywords to search the web. For example, typing `g react hooks` will immediately open a Google search in your browser, saving you the steps of opening the browser and navigating to the search bar.
