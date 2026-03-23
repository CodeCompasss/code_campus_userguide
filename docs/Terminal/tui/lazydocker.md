# Lazydocker

### What is it?

Lazydocker is a terminal user interface (TUI) for managing Docker and Docker Compose environments. It provides a visual dashboard inside the terminal that consolidates container statuses, logs, resource usage, image management, and volume tracking into a single, interactive view. Written in Go, it is designed to be lightweight, keyboard-centric, and significantly faster than traditional web-based or heavy graphical Docker managers.

In the software development ecosystem, Lazydocker belongs to the **container orchestration and observability layer**. It serves as an interactive wrapper around the standard Docker CLI, making it easier to manage complex, multi-container applications without needing to remember numerous specialized commands.

### Installation (Optional)

!!! note
    CodeCampus OS includes Lazydocker by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Binary Install"
    ```bash
    curl https://raw.githubusercontent.com/jesseduffield/lazydocker/master/scripts/install_update_linux.sh | bash
    ```

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S lazydocker
    ```

=== "Ubuntu / Debian"
    Download the latest release from the [GitHub releases page](https://github.com/jesseduffield/lazydocker/releases) and move the binary to `/usr/local/bin`.

=== "Fedora"
    ```bash
    sudo dnf install lazydocker
    ```

### Why this tool matters (In Depth)

As developers move from simple single-container apps to complex microservice architectures, the cognitive load of managing Docker increases exponentially. Running commands like `docker ps`, `docker logs -f <id>`, and `docker stats` across a dozen different services is slow and error-prone. Lazydocker matters because it **provides instantaneous visibility and control over the entire container lifecycle**.

It eliminates the "context switching" involved in looking up container IDs and manually typing management commands. With a single keystroke, a developer can restart a service, prune unused images, or attach to a container's shell. Its real-time log streaming and resource monitoring allow for rapid debugging of "leaky" or crashing containers that might otherwise go unnoticed in a busy terminal. For anyone working with Docker Compose, Lazydocker is an essential sanity-preserving tool that transforms an abstract list of services into a tangible, observable system.

### How students will actually use it

Students will use Lazydocker to simplify their interaction with containerized development:

*   **Interactive Dashboard:** Monitoring all active containers, images, and volumes in a single view by simply running `lazydocker`.
*   **Rapid Troubleshooting:** Instantly viewing the logs of a failing container without needing to look up its name or ID.
*   **Resource Auditing:** Identifying which container is consuming excessive CPU or memory through the integrated "Stats" view.
*   **Clean-up Operations:** Safely removing dangling images and stopped containers to reclaim disk space with a single button press.
*   **Compose Management:** Visualizing and controlling "groups" of containers defined in a `docker-compose.yml` file, making it easier to manage full-stack projects.