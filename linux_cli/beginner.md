# Introduction to Linux CLI - Course Outline

## Course Overview
A 3-hour introductory course on the Linux Command Line Interface (CLI) designed to provide students with a strong foundation in using the Linux shell.

## Introduction to Linux and Basic Commands

### 1. Introduction to Linux
- Brief history and overview of Linux.
- The structure of the Linux operating system (Kernel, Shell, File System).
- Benefits of using the command line.

### 2. Navigating the File System
- Understanding the file system hierarchy (`/`, `/home`, `/etc`, `/var`, etc.).
- Basic navigation commands:
  - `pwd` (print working directory)
    ```bash
    pwd
    ```
  - `ls` (list directory contents)
    ```bash
    ls
    ```
  - `cd` (change directory)
    ```bash
    cd /path/to/directory
    ```
- Viewing file contents:
  - `cat`
    ```bash
    cat filename
    ```
  - `less`
    ```bash
    less filename
    ```
  - `more`
    ```bash
    more filename
    ```


### 1. Package Management (specific to distribution)
- Installing, updating, and removing software packages:
  - `apt` (Debian/Ubuntu based systems)
  - `yum` or `dnf` (RHEL/CentOS based systems)
- Example commands:
  - `sudo apt update` (update package list)
  - `sudo apt install <package>` (install a package)
  - `sudo apt remove <package>` (remove a package)


### 3. Managing Files and Directories
- Creating and deleting files and directories:
  - `touch` (create a file)
    ```bash
    touch filename
    ```
  - `mkdir` (create a directory)
    ```bash
    mkdir directoryname
    ```
  - `rm` (remove a file)
    ```bash
    rm filename
    ```
  - `rmdir` (remove a directory)
    ```bash
    rmdir directoryname
    ```
- Copying and moving files:
  - `cp` (copy files/directories)
    ```bash
    cp sourcefile destinationfile
    cp -r sourcedir destinationdir
    ```
  - `mv` (move/rename files/directories)
    ```bash
    mv sourcefile destinationfile
    mv oldname newname
    ```

### Text Processing and Searching

-  grep (search text using patterns)
```
grep 'pattern' filename
```

```
head filename
tail filename
```
```
wc filename
```

###  File Permissions and Ownership
- Understanding file permissions (read, write, execute):
  - `r` (read): Allows a user to read the contents of the file.
  - `w` (write): Allows a user to modify the file.
  - `x` (execute): Allows a user to execute the file (if it is a script or a program).

- Viewing file permissions:
  ```bash
  ls -l filename
  ```

    ![premmissions](1_l2wRcr87kqZrXZwRBgTxjg.png)

####   Permission Categories
- Permissions are divided into three categories:
  - Owner: The user who owns the file.
  - Group: The group that owns the file.
  - Others: All other users.

#### File Permission Notation
- Permissions are displayed in two ways: symbolic and numeric (octal).

#### Symbolic Notation
- Example: `rwxr-xr--`
  - The first character indicates the file type (`-` for regular files, `d` for directories).
  - The next three characters (`rwx`) represent the owner's permissions.
  - The next three characters (`r-x`) represent the group's permissions.
  - The last three characters (`r--`) represent others' permissions.

#### Numeric (Octal) Notation
- Each permission is represented by a number:
  - Read (`r`) = 4
  - Write (`w`) = 2
  - Execute (`x`) = 1
- Permissions are summed to get a single digit for each category:
  - `rwx` = 4 + 2 + 1 = 7
  - `r-x` = 4 + 0 + 1 = 5
  - `r--` = 4 + 0 + 0 = 4
- Example: `755` (owner has full permissions, group has read and execute, others have read)


- Add or remove specific permissions using symbolic notation

```
chmod u+x filename     # Add execute permission for the owner
chmod g-w filename     # Remove write permission for the group
chmod o+r filename     # Add read permission for others
```

# Basic Network Commands in Linux

## Checking Network Configuration

### ifconfig
- Displays network interfaces and their configurations.
- Commonly used to check IP addresses and interface statuses.
- Example:
  ```bash
  ifconfig
  ```

### ping
- Sends ICMP ECHO_REQUEST packets to network hosts to check connectivity.

```
ping example.com
```

### Curl

- Transfers data from or to a server using supported protocols (HTTP, FTP, etc.).

- Commonly used to test and interact with web servers.

```bash
curl -O https://raw.githubusercontent.com/mdn/content/main/files/en-us/_wikihistory.json

```

### wget
- Downloads files from the web using HTTP, HTTPS, and FTP protocols.

```bash
wget https://raw.githubusercontent.com/mdn/content/main/files/en-us/_wikihistory.json
```

### ssh

- Securely connects to a remote machine over a network.

```
ssh username@hostname
```

### rsync

```
rsync -avz /path/to/source username@hostname:/path/to/destination
```
- -a: Archive mode (preserves permissions, timestamps, etc.).
- -v: Verbose output.
- -z: Compress file data during transfer.