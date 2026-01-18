

### What is `rsync`?

* **Incremental transfers**: Only transfers the differences between source and destination files, saving time and bandwidth.
* **Supports local and remote synchronization**: Can copy files within the same system or over SSH/remote connections.
* **Preserves file attributes**: Can keep permissions, timestamps, symbolic links, and ownership intact.
* **Efficient**: Uses compression (`-z`) and delta-transfer algorithm to reduce data sent over the network.
* **Versatile**: Can be used for backups, migrations, or mirroring websites and directories.

---

### How to Use `rsync`

#### 1. Basic Local Copy

```bash
rsync -av /source/directory/ /destination/directory/
```

* `-a` = archive mode (preserves permissions, timestamps, symbolic links, etc.)
* `-v` = verbose (shows what’s being transferred)
* Trailing slashes matter: `/source/` means “contents of the source directory.”

#### 2. Remote Copy (via SSH)

```bash
rsync -av /local/dir/ user@remote_host:/remote/dir/
```

* Copies local directory to a remote server via SSH.

#### 3. Remote Copy from Server to Local

```bash
rsync -av user@remote_host:/remote/dir/ /local/dir/
```

#### 4. Compress Data During Transfer

```bash
rsync -avz /local/dir/ user@remote_host:/remote/dir/
```

* `-z` enables compression for faster network transfers.

#### 5. Show Progress

```bash
rsync -av --progress /local/dir/ /destination/dir/
```

* Displays transfer progress and speed.

#### 6. Delete Extra Files in Destination

```bash
rsync -av --delete /local/dir/ /destination/dir/
```

* Deletes files in the destination that no longer exist in the source.

#### 7. Exclude Certain Files

```bash
rsync -av --exclude '*.tmp' /source/ /destination/
```

* Skips all `.tmp` files during transfer.

---

### Installation (Linux Examples)

````markdown
=== "Ubuntu / Debian"

```bash
sudo apt update
sudo apt install rsync
````

=== "Arch / Manjaro"

```bash
sudo pacman -S rsync
```

=== "Fedora"

```bash
sudo dnf install rsync
```

=== "openSUSE"

```bash
sudo zypper install rsync
```

```

