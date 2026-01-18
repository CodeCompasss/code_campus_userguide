

## What is `jdupes`?

* **Duplicate Finder**: Scans directories to detect files that are **byte-for-byte identical**.
* **High Performance**: Optimized for speed and low memory usage; can handle millions of files.
* **Flexible**: Supports options for listing, deleting, or replacing duplicates with hard links.
* **Safe**: Provides interactive and batch modes to prevent accidental deletion.
* **Cross-platform**: Works on Linux, Windows, and macOS.

---

## Installation

````markdown
=== "Ubuntu / Debian"

```bash
sudo apt update
sudo apt install jdupes
````

=== "Arch / Manjaro"

```bash
sudo pacman -S jdupes
```

=== "Fedora"

```bash
sudo dnf install jdupes
```

=== "openSUSE"

```bash
sudo zypper install jdupes
```

````

> On some distributions, `jdupes` might need to be installed from source or a repository if not available in the default package manager.

---

## How to Use `jdupes`

### 1. Basic Duplicate Scan

```bash
jdupes /path/to/directory
````

* Lists all duplicate files in the directory and subdirectories.

### 2. Scan Multiple Directories

```bash
jdupes /dir1 /dir2 /dir3
```

* Finds duplicates across multiple paths.

### 3. Recursively Scan

```bash
jdupes -r /path/to/directory
```

* `-r` enables recursive scanning of all subdirectories.

### 4. Show Only Duplicates

```bash
jdupes -1 /path/to/directory
```

* `-1` prints only files that have duplicates, one per line.

### 5. Delete Duplicates Interactively

```bash
jdupes -d /path/to/directory
```

* Prompts you to select which duplicates to keep or delete.
* **Use with caution**; it will delete files permanently if confirmed.

### 6. Replace Duplicates with Hard Links

```bash
jdupes -L /path/to/directory
```

* Deletes duplicates and replaces them with hard links, saving disk space without losing file access.

### 7. Save Output to a File

```bash
jdupes -r /path/to/directory > duplicates.txt
```

* Useful for reviewing duplicates before taking action.

### 8. Advanced Options

* `-S` → Show size of duplicate sets.
* `-A` → Ignore empty files.
* `-Q` → Quiet mode, minimal output.
* `--nohidden` → Skip hidden files and directories.

---

### Practical Use Cases

1. **Disk Cleanup**: Identify and remove duplicate media, documents, or backups.
2. **Backup Optimization**: Avoid storing multiple copies of the same file.
3. **Automated Scripts**: Integrate into cron jobs to maintain clean directories.
4. **File System Analysis**: Quickly assess how much space duplicates occupy.

