
## What is Samba?

* **SMB/CIFS Protocol**: Samba implements the Server Message Block (SMB) and Common Internet File System (CIFS) protocols used by Windows for file/printer sharing.
* **Cross-Platform**: Allows Linux, Unix, and macOS systems to share files and printers with Windows clients.
* **Authentication**: Supports Windows-style user authentication and access control.
* **Integration**: Can integrate with Windows domains, Active Directory, and NT4-style domains.
* **Server and Client Roles**:

  * **Samba Server**: Shares files and printers for Windows/Linux clients.
  * **Samba Client**: Accesses shared resources from Windows or other Samba servers.
* **Additional Tools**:

  * `smbclient`: Command-line client to access SMB shares.
  * `smbd`: The main daemon for sharing files and printers.
  * `nmbd`: Handles NetBIOS name service for discovery on networks.
  * `winbind`: Integrates Linux accounts with Windows accounts.

---

## Installation

````markdown
=== "Ubuntu / Debian"

```bash
sudo apt update
sudo apt install samba
````

=== "Arch / Manjaro"

```bash
sudo pacman -S samba
```

=== "Fedora"

```bash
sudo dnf install samba
```

=== "openSUSE"

```bash
sudo zypper install samba
```

````

---

## How to Use Samba

### 1. Check Samba Version

```bash
smbd --version
````

### 2. Basic Configuration

The main configuration file is:

```text
/etc/samba/smb.conf
```

* Global settings: Define workgroup, server name, logging, security.
* Share definitions: Specify directories to share and access permissions.

Example:

```ini
[global]
   workgroup = WORKGROUP
   server string = My Samba Server
   security = user

[SharedDocs]
   path = /srv/samba/shared
   browseable = yes
   read only = no
   guest ok = yes
```

### 3. Create Samba User

```bash
sudo smbpasswd -a username
sudo smbpasswd -e username
```

* Adds and enables a Samba user. The username must exist on the Linux system.

### 4. Start and Enable Samba Services

```bash
sudo systemctl start smbd nmbd
sudo systemctl enable smbd nmbd
```

* `smbd`: File/printer sharing.
* `nmbd`: Network browsing (NetBIOS).

### 5. Accessing Samba Shares (Client)

* Using Linux:

```bash
smbclient //server_ip/SharedDocs -U username
```

* Mount a Samba share locally:

```bash
sudo mount -t cifs -o username=username,password=password //server_ip/SharedDocs /mnt/samba
```

* Access from Windows: Open `\\server_ip\SharedDocs` in File Explorer.

### 6. Common Commands

* List available shares on a server:

```bash
smbclient -L //server_ip -U username
```

* Test configuration:

```bash
testparm
```

* Monitor connections:

```bash
smbstatus
```

---

### Practical Use Cases

1. **File Sharing Across OSes**: Share documents, media, or backups between Linux and Windows.
2. **Printer Sharing**: Make Linux printers available to Windows clients.
3. **Home Networks**: Central file repository for multiple devices.
4. **Enterprise**: Integrate Linux servers into Active Directory environments.

