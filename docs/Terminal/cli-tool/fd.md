# fd 

### What is it?

fd is an open-source, high-performance command-line tool for finding files and directories in a filesystem. It is designed as a modern, human-centric alternative to the traditional `find` command. Written in Rust, it is optimized for speed through parallelism and provides a more intuitive, concise syntax while defaulting to "smart" behaviors like honoring `.gitignore` rules.

In the software development ecosystem, fd belongs to the **filesystem navigation and automation layer**. It serves as a rapid discovery tool for locating project assets, managing build artifacts, and piping file lists into other developer utilities.

### Installation (Optional)

!!! note
    CodeCampus OS includes fd by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S fd
    ```

=== "Ubuntu / Debian"
    ```bash
    sudo apt install fd-find
    # Note: On Ubuntu/Debian, the binary is 'fdfind'
    # To use 'fd', create an alias or symlink:
    mkdir -p ~/.local/bin
    ln -s $(which fdfind) ~/.local/bin/fd
    ```

=== "Fedora"
    ```bash
    sudo dnf install fd-find
    ```

### Why this tool matters (In Depth)

The traditional `find` command is notoriously difficult to use, with a syntactic structure that is inconsistent with almost every other Unix utility. To perform a basic search, users must often remember complex flags like `-name`, `-type f`, and `-print`, and deal with the frustration of search results being cluttered by untracked directories like `.git` or `node_modules`. fd matters because it **lowers the cognitive burden of filesystem interaction**.

By default, fd is case-insensitive (unless an uppercase letter is used), uses regular expressions for searching, and automatically ignores hidden files and directories specified in your `.gitignore`. This means that in 95% of use cases, fd provides exactly the results a developer expects without any extra configuration. Furthermore, its performance on large storage volumes is significantly higher than `find` due to its multithreaded directory traversal architecture.

For students, fd eliminates the friction of navigating large projects. It allows them to find where a specific file or directory is located using simple keywords, encouraging more efficient project management and reducing the time spent on "administrative" terminal tasks.

### How students will actually use it

Students will use fd to manage their project files and automate repetitive tasks:

*   **Rapid File Discovery:** Finding a file by name without needing to know its exact path (e.g., `fd main.c`).
*   **Extension-Based Filtering:** Listing all files of a specific type across their entire workspace (`fd -e md` for all Markdown files).
*   **Targeted Directory Navigation:** Locating specific subdirectories, such as finding all "tests" folders in a large codebase.
*   **Bulk Command Execution:** Using the `-x` or `-X` flags to perform an action on every found file, such as formatting all `.js` files or deleting all `.log` artifacts.
*   **Regex-Powered Search:** Finding files that match a complex naming pattern (e.g., `fd "v[0-9]+"` to find versioned backups).
