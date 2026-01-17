# Czkawka

### What is it?

Czkawka (Polish for *hiccup*) is an open-source, multi-functional, and extremely fast application used to find and remove various types of "cruft" from a computer. Written in Rust, it is designed to be safer and significantly faster than traditional system cleaners. It identifies duplicate files, empty directories, large files, similar images, and broken symbolic links.

In the software development ecosystem, Czkawka belongs to the **data management and system performance layer**. It is a specialized utility that helps developers manage the massive amounts of data—such as multiple clones of repositories, duplicate dependency archives, and large temporary build files—that accumulate during intensive development work.

### Installation (Optional)

!!! note
    CodeCampus OS includes Czkawka by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Flatpak"
    ```bash
    flatpak install flathub com.github.qarmin.czkawka
    ```

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S czkawka-gui
    ```

=== "Fedora"
    ```bash
    sudo dnf install czkawka
    ```

=== "AppImage"
    Download the latest `.AppImage` from the [official repository](https://github.com/qarmin/czkawka/releases), make it executable, and run it.

### Why this tool matters (In Depth)

For developers, disk space is not just about storage capacity; it is about system hygiene and search efficiency. Over years of development, it is common to accidentally create duplicate copies of large datasets, project dependencies, or virtual machine images. These duplicates not only waste space but also create "data fragmentation," where a developer might edit one copy of a file while a build tool uses another, leading to confusing and difficult-to-debug errors.

Czkawka matters because it uses **content-aware hashing** (rather than just file names or dates) to identify true duplicates. Because it is written in Rust, it can scan hundreds of thousands of files in seconds, making regular system maintenance a trivial task rather than a time-consuming chore. 

For students, using Czkawka reinforces the importance of knowing "what is on your disk." It encourages a disciplined approach to file management and teaches the value of using specialized, high-performance tools for specific administrative tasks. Identifying and removing empty folders and broken symbolic links is also an excellent way to keep a development environment predictable and clean.

### How students will actually use it

Students will use Czkawka to maintain an organized and efficient filesystem:

*   **Duplicate Detection:** Scanning project directories and download folders to find redundant copies of large files, such as ISO images or database backups.
*   **Similar Image Search:** Finding nearly identical screenshots or assets that differ only in resolution or compression, which is common in web and UI development.
*   **Large File Analysis:** Quickly identifying the "space hogs" on their system to decide which archived projects or old virtual machines can be moved to external storage or deleted.
*   **Cleaning Project Files:** Removing empty directories and broken links that often remain after a project has been restructured or a tool has been uninstalled.
*   **Invalid Extension Check:** Identifying files whose content does not match their extension, which can help in diagnosing corrupted data or malicious files.

### Professional Insight (Top 1% Knowledge)

Experienced engineers value Czkawka not just for its GUI, but for its **Rust-powered CLI**. A professional habit is to use the `czkawka_cli` to automate cleanup tasks. For example, you can write a cron job or a simple script that runs `czkawka_cli dup --directories /path/to/projects` to periodically generate a report of duplicates without ever opening a window.

Another high-level insight is understanding how Czkawka performs its search. It uses the **BLAKE3 hashing algorithm**, which is one of the fastest and most secure hashing functions currently available. A senior engineer knows that "content-based" comparison is the only reliable way to manage data at scale. Using a tool that leverages modern, performance-oriented languages like Rust demonstrates an understanding of how tool choice affects the speed and reliability of administrative workflows. Treat Czkawka as your surgical tool for filesystem hygiene—use it precisely and regularly to ensure your workstation remains a high-performance environment.