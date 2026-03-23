# Timeshift

### What is it?

Timeshift is an open-source system snapshot and restore utility for Linux. It functions by capturing the current state of the operating system—including system files, configurations, and installed applications—and storing them as bootable snapshots. These snapshots can later be restored to return the system to an identical, previous state.

In the Linux ecosystem, Timeshift belongs to the **system resiliency and recovery layer**. It provides a failure-agnostic way to undo system-level changes such as failed kernel updates, broken drivers, or destructive configuration edits.

### Installation (Optional)

!!! note
    CodeCampus OS includes Timeshift by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Ubuntu / Debian"
    ```bash
    sudo apt install timeshift
    ```

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S timeshift
    ```

=== "Fedora"
    ```bash
    sudo dnf install timeshift
    ```

=== "openSUSE"
    ```bash
    sudo zypper install timeshift
    ```

### Why this tool matters (In Depth)

For a student, the greatest psychological barrier to learning Linux is the fear of an irreversible system failure. Experimentation—installing new toolchains, modifying system paths, or experimenting with different display servers—is essential for growth but carries the risk of rendering the system unbootable. Timeshift matters because it **de-risks experimentation**.

By providing a reliable "undo" button for the entire operating system, Timeshift empowers students to follow complex tutorials and perform aggressive optimizations without fear. It introduces the professional concept of **immutable system states**; rather than viewing an OS as a delicate, one-off installation, students learn to view it as a manageable collection of versioned states. This mental model is foundational for modern DevOps practices, where infrastructure is often treated as code that can be rolled back to a known-good configuration at any time.

### How students will actually use it

Students will use Timeshift to manage their system's stability during major transitions:

*   **Pre-Update Snapshots:** Creating a manual snapshot immediately before performing a system-wide upgrade (`sudo apt upgrade` or `pacman -Syu`) to ensure a quick path back if the new packages cause instability.
*   **Safe Configuration Testing:** Snapshotting before editing critical system files like `/etc/fstab` or X11 configurations, allowing for instant recovery if the changes result in a black screen or boot failure.
*   **Scheduled Maintenance:** Configuring "Daily" or "Weekly" automatic snapshots to maintain a rolling history of stable system states without manual intervention.
*   **External Boot Recovery:** Using a live USB to run Timeshift and restore a local system that is too broken to boot into its own graphical interface.
*   **Environment Comparison:** Reverting to a previous snapshot to verify if a newly introduced bug is caused by a recent system change or by the application code itself.
