# Zellij

### What is it?

Zellij is a modern terminal workspace and multiplexer written in Rust. It allows users to split their terminal into multiple panes and tabs, manage persistent sessions, and extend functionality through a powerful webassembly-based plugin system. Unlike traditional multiplexers (like `tmux`), Zellij is designed with a "user-first" philosophy, featuring an intuitive layout system and built-in discovery aids (like a visible status bar with keybindings) that eliminate the steep learning curve typically associated with terminal multiplexing.

In the software development ecosystem, Zellij belongs to the **terminal environment and window management layer**. It serves as a comprehensive workspace where a developer can organize multiple tasks—such as editing code, running a web server, and monitoring logs—within a single terminal window.

### Installation (Optional)

!!! note
    CodeCampus OS includes Zellij by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S zellij
    ```

=== "Ubuntu / Debian"
    ```bash
    # Download the binary from the GitHub releases page
    # and move it to /usr/local/bin
    ```

=== "Fedora"
    ```bash
    sudo dnf install zellij
    ```

### Why this tool matters (In Depth)

As development projects grow in complexity, the "single-session" terminal becomes a significant bottleneck. A typical developer needs to see their code, their test output, and their server logs simultaneously. Constantly switching between terminal tabs or windows leads to cognitive fragmentation. Zellij matters because it providing **persistent, organized spatial context**.

Zellij distinguishes itself through its "Layouts" feature, which allows developers to define complex pane arrangements (e.g., a large editor pane with two smaller panes for logs and tests) in a simple KDL configuration file. When a project is launched with a Zellij layout, the entire environment is created instantly. Furthermore, because Zellij is a multiplexer, sessions can be "detached" and "reattached." This means you can start a long-running process at your workplace, close your laptop, and reconnect to the exact same terminal state later from home.

For students, Zellij represents a massive upgrade in terminal comfort. Its visible keybinding tips and intuitive navigation make "pro-level" terminal productivity accessible without needing to memorize dozens of obscure `Ctrl+b` combinations.

### How students will actually use it

Students will use Zellij to build a high-efficiency command-line cockpit:

*   **Pane Splitting:** Using `Ctrl+h` and `Ctrl+n` (or their configured shortcuts) to split the terminal vertically and horizontally, allowing them to see their source code and its output side-by-side.
*   **Logical Tabs:** Organizing different aspects of a project into tabs—for example, one tab for backend work, another for frontend, and a third for database management.
*   **Session Persistence:** Leaving their development environment "alive" even if the terminal window is accidentally closed or the computer is put to sleep.
*   **Floating Panes:** Using floating windows for quick, non-disruptive tasks like looking up a manual page or running a one-off Git command without disturbing their main layout.
*   **Project Layouts:** Creating a `.kdl` file to automatically restore their preferred pane and tab structure whenever they start working on a specific course project.

### Professional Insight (Top 1% Knowledge)

The "Top 1%" of terminal power users treat Zellij as a **programmable dashboard**. A professional habit is leveraging **Zellij Plugins**. Because Zellij uses WebAssembly (Wasm), professional engineers can write their own UI components—such as a custom project health monitor or a specialized file explorer—that run natively inside the terminal panes.

Another high-level skill is **Cross-Machine Session Sharing**. Senior engineers often use the session management features to pair-program or troubleshoot a remote server, where multiple people can attach to the same Zellij session and see the same panes and outputs in real-time.

The "Top 1%" insight is the use of **Zellij as a replacement for a Tiling Window Manager**. For developers who don't want to switch their entire OS to a tiling manager like i3 or Hyprland, Zellij provides the same high-efficiency spatial management entirely within the terminal. Combined with a "Quake-style" drop-down terminal, it creates a seamless, keyboard-driven environment that is portable across any Linux distribution. Finally, remember that Zellij is designed to stay out of your way. Once you master the "locked" mode (`Ctrl+g`), which passes all keystrokes directly to the underlying application (like Neovim), you get the benefits of multiplexing with zero input interference.
