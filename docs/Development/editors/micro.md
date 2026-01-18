

## What is `micro`?

* **Terminal-Based Editor**: Runs inside the terminal, similar to `nano` or `vim`.
* **Modern Features**:

  * Syntax highlighting for many programming languages.
  * Mouse support in the terminal.
  * Undo/redo system.
  * Plugin support for extending functionality.
  * True Unicode support.
  * Multiple cursors and selection.
* **No Configuration Required**: Works out-of-the-box with sensible defaults, unlike `vim` which requires configuration.
* **Cross-Platform**: Linux, macOS, Windows.

---

## How Micro Differs from Nano

| Feature                 | `micro`                       | `nano`                         |
| ----------------------- | ----------------------------- | ------------------------------ |
| **User Interface**      | Modern, clean, supports mouse | Simple, minimal, keyboard only |
| **Syntax Highlighting** | Yes, supports many languages  | Limited or none by default     |
| **Plugins**             | Yes, supports extensions      | No                             |
| **Undo/Redo**           | Multiple undo/redo            | Basic, limited undo only       |
| **Unicode Support**     | Full                          | Limited                        |
| **Multiple Cursors**    | Yes                           | No                             |
| **Mouse Support**       | Yes                           | Limited                        |
| **Configuration**       | Optional JSON config file     | Minimal, through `.nanorc`     |
| **Installation Size**   | Slightly larger than nano     | Very lightweight               |

**In short:**

* `nano` is extremely lightweight, very simple, and ideal for quick edits.
* `micro` adds **modern conveniences** (syntax highlighting, plugins, better undo/redo, mouse support) while keeping the simplicity of `nano`. It’s a good choice for users who want a **“nano but smarter”** editor without jumping to `vim` or `emacs`.

---

## Installation

````markdown
=== "Ubuntu / Debian"

```bash
sudo apt update
sudo apt install micro
````

=== "Arch / Manjaro"

```bash
sudo pacman -S micro
```

=== "Fedora"

```bash
sudo dnf install micro
```

=== "openSUSE"

```bash
sudo zypper install micro
```

````

---

## Basic Usage

- Open a file:

```bash
micro filename.txt
````

* **Common shortcuts** (displayed at the bottom of the screen):

  * `Ctrl+S` → Save
  * `Ctrl+Q` → Quit
  * `Ctrl+C` → Copy
  * `Ctrl+V` → Paste
  * `Ctrl+Z` → Undo
  * `Ctrl+Shift+Z` → Redo
  * `Alt+Arrow` → Move cursor by words
* Plugins and configurations are stored in:

```text
~/.config/micro
```

* Install plugins via:

```bash
micro -plugin install <plugin-name>
```

