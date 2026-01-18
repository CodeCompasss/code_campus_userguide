

### What is Aria2?

```markdown
Aria2 is a lightweight, multi-protocol, and multi-source command-line download utility.  
It supports downloading files from:

- HTTP/HTTPS
- FTP
- SFTP
- BitTorrent
- Metalink  

Key features include:

- Multi-connection downloads to speed up file transfers.
- Support for resuming interrupted downloads.
- Parallel downloads from multiple sources.
- Integration with scripts and automation tools.
- Minimal system resource usage compared to GUI download managers.
````

---
### Installation

````markdown
=== "Ubuntu / Debian"

```bash
sudo apt update
sudo apt install aria2
````

=== "Arch / Manjaro"

```bash
sudo pacman -S aria2
```

=== "Fedora"

```bash
sudo dnf install aria2
```

=== "openSUSE"

```bash
sudo zypper install aria2
```

````
### How to Use Aria2

````markdown
#### Basic Usage

To download a single file:

```bash
aria2c https://example.com/file.zip
````

This will download `file.zip` to the current directory.

#### Download with Multiple Connections

```bash
aria2c -x 16 https://example.com/file.zip
```

* `-x 16` specifies 16 simultaneous connections to speed up the download.

#### Download Multiple Files from a List

Create a file called `urls.txt`:

```
https://example.com/file1.zip
https://example.com/file2.zip
```

Then run:

```bash
aria2c -i urls.txt
```

#### BitTorrent Downloads

```bash
aria2c --bt-max-peers=55 https://example.com/file.torrent
```

* Supports magnet links as well:

```bash
aria2c "magnet:?xt=urn:btih:..."
```

#### Resuming Downloads

```bash
aria2c -c https://example.com/largefile.zip
```

* `-c` allows resuming interrupted downloads.

#### Downloading from Metalink

```bash
aria2c https://example.com/file.metalink
```

* Metalink provides multiple mirrors, hashes, and file info for reliable downloads.

#### Advanced Options

* **Speed limit**: `--max-download-limit=500K`
* **Save to specific directory**: `-d /path/to/dir`
* **File renaming**: `-o newname.zip`
* **Enable RPC mode**: `aria2c --enable-rpc` (useful for web-based frontends)

Aria2 can be fully automated and scripted, making it ideal for batch downloads, server environments, or situations where GUI-based download managers are inefficient.

```

