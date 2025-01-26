- [README for Linux Commands and Their Uses](#readme-for-linux-commands-and-their-uses)
  - [Overview](#overview)
- [Key Linux Commands](#key-linux-commands)
  - [File and Directory Management](#file-and-directory-management)
    - [1. **Creating and Editing Files**](#1-creating-and-editing-files)
    - [2. **Creating Empty Files**](#2-creating-empty-files)
    - [3. **Renaming or Moving Files**](#3-renaming-or-moving-files)
    - [4. **Copying Files**](#4-copying-files)
    - [5. **Deleting Files and Directories**](#5-deleting-files-and-directories)
    - [6. **Viewing Directory Structure**](#6-viewing-directory-structure)
    - [7. **Creating Directories**](#7-creating-directories)
  - [Bash Scripts](#bash-scripts)
    - [Writing a Simple Bash Script in Nano](#writing-a-simple-bash-script-in-nano)
  - [Viewing and Searching Files](#viewing-and-searching-files)
    - [1. **Viewing File Contents**](#1-viewing-file-contents)
    - [2. **Viewing First/Last Lines**](#2-viewing-firstlast-lines)
    - [3. **Searching for Text in Files**](#3-searching-for-text-in-files)
    - [4. **Checking File Types**](#4-checking-file-types)
  - [File Permissions and Ownership](#file-permissions-and-ownership)
    - [1. **Changing Permissions**](#1-changing-permissions)
    - [2. **Checking File Permissions**](#2-checking-file-permissions)
  - [SSH and Key Management](#ssh-and-key-management)
    - [1. **Generating SSH Keys**](#1-generating-ssh-keys)
    - [2. **Connecting to Remote Servers**](#2-connecting-to-remote-servers)
    - [3. **Transferring Files Securely**](#3-transferring-files-securely)
  - [System Utilities](#system-utilities)
    - [1. **Checking Disk Usage**](#1-checking-disk-usage)
    - [2. **Monitoring System Processes**](#2-monitoring-system-processes)
    - [3. **Installing Software**](#3-installing-software)
    - [4. **Updating System Packages**](#4-updating-system-packages)
    - [5. **Renaming and Moving Files Simultaneously**](#5-renaming-and-moving-files-simultaneously)
- [Best Practices](#best-practices)
  - [Command Safety](#command-safety)
  - [Efficient Navigation](#efficient-navigation)
  - [Documentation](#documentation)
- [Additional Resources](#additional-resources)

# README for Linux Commands and Their Uses

## Overview

This document provides a comprehensive list of essential Linux commands, their purposes, and examples. The goal is to aid developers and system administrators in efficiently navigating and managing Linux systems using the terminal, particularly in conjunction with Visual Studio Code.

---

# Key Linux Commands

## File and Directory Management

### 1. **Creating and Editing Files**

- **Command**: `nano`
  - Use Nano to edit or create text files directly in the terminal.
  - Example:
    ```bash
    nano filename.txt
    ```
- Save changes: `Ctrl + O`, Exit Nano: `Ctrl + X`.

### 2. **Creating Empty Files**

- **Command**: `touch`
  - Creates an empty file.
  - Example:
    ```bash
    touch filename.txt
    ```

### 3. **Renaming or Moving Files**

- **Command**: `mv`
  - Moves or renames files and directories.
  - Example:
    ```bash
    mv oldname.txt newname.txt
    ```

### 4. **Copying Files**

- **Command**: `cp`
  - Copies files and directories.
  - Example:
    ```bash
    cp source.txt destination.txt
    ```
- Recursive copy (for directories):
  ```bash
  cp -r source_dir/ destination_dir/
  ```

### 5. **Deleting Files and Directories**

- **Command**: `rm`
  - Removes files and directories.
  - Example:
    ```bash
    rm filename.txt
    ```
- Recursive delete (use with caution):
  ```bash
  rm -r directory_name
  ```

### 6. **Viewing Directory Structure**

- **Command**: `tree`
  - Displays directory structure in a tree-like format.
  - Example:
    ```bash
    tree
    ```
- Install Tree (if not available):
  ```bash
  sudo apt install tree
  ```

### 7. **Creating Directories**

- **Command**: `mkdir`
  - Creates a new directory.
  - Example:
    ```bash
    mkdir new_directory
    ```

## Bash Scripts

### Writing a Simple Bash Script in Nano

1. Open a file in Nano:

   ```bash
   nano script_name.sh
   ```

2. Add the shebang line at the top to specify the interpreter:

   ```bash
   #!/bin/bash
   ```

3. Write your script commands. Example:

   ```bash
   #!/bin/bash
   echo "Hello, World!"
   sudo apt update
   sudo apt install nginx -y
   sudo systemctl enable nginx
   sudo systemctl restart nginx
   ```

4. Save and exit Nano (`Ctrl + O`, then `Ctrl + X`).

5. Make the script executable:

   ```bash
   chmod +x script_name.sh
   ```

6. Run the script:
   ```bash
   ./script_name.sh
   ```

---

## Viewing and Searching Files

### 1. **Viewing File Contents**

- **Command**: `cat`
  - Outputs the contents of a file.
  - Example:
    ```bash
    cat filename.txt
    ```

### 2. **Viewing First/Last Lines**

- **Command**: `head` / `tail`
  - View the first or last lines of a file.
  - Example:
    ```bash
    head -n 10 filename.txt
    tail -n 10 filename.txt
    ```

### 3. **Searching for Text in Files**

- **Command**: `grep`
  - Searches for patterns in files.
  - Example:
    ```bash
    grep 'search_term' filename.txt
    ```

### 4. **Checking File Types**

- **Command**: `file`
  - Determines the type of a file.
  - Example:
    ```bash
    file filename.txt
    ```

## File Permissions and Ownership

### 1. **Changing Permissions**

- **Command**: `chmod`
  - Modifies file permissions.
  - Example:
    ```bash
    chmod 600 filename.txt
    ```

### 2. **Checking File Permissions**

- **Command**: `ls -l`
  - Lists files with permissions.
  - Example:
    ```bash
    ls -l
    ```

## SSH and Key Management

### 1. **Generating SSH Keys**

- **Command**: `ssh-keygen`
  - Generates SSH key pairs for secure access.
  - Example:
    ```bash
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```

### 2. **Connecting to Remote Servers**

- **Command**: `ssh`
  - Connects to a remote server using SSH.
  - Example:
    ```bash
    ssh -i private_key.pem user@server_address
    ```

### 3. **Transferring Files Securely**

- **Command**: `scp`
  - Copies files to/from a remote server.
  - Example:
    ```bash
    scp file.txt user@server_address:/remote/directory/
    ```

## System Utilities

### 1. **Checking Disk Usage**

- **Command**: `df` / `du`
  - `df`: Displays disk space usage.
    ```bash
    df -h
    ```
  - `du`: Displays directory space usage.
    ```bash
    du -sh /path/to/directory
    ```

### 2. **Monitoring System Processes**

- **Command**: `top`
  - Monitors real-time system processes.
  - Example:
    ```bash
    top
    ```

### 3. **Installing Software**

- **Command**: `apt install`
  - Installs software packages.
  - Example:
    ```bash
    sudo apt install package_name
    ```

### 4. **Updating System Packages**

- **Command**: `sudo apt update && sudo apt upgrade`
  - Updates package lists and upgrades installed packages.
  - Example:
    ```bash
    sudo apt update && sudo apt upgrade
    ```

### 5. **Renaming and Moving Files Simultaneously**

- **Command**: `mv`
  - Renames and moves files in one step.
  - Example:
    ```bash
    mv oldfile.txt /new/path/newname.txt
    ```

---

# Best Practices

## Command Safety

- Always double-check destructive commands (`rm`, `mv`, `cp -r`).
- Avoid using `sudo` unless absolutely necessary.

## Efficient Navigation

- Use tab completion to save time and reduce errors.
- Avoid spaces in file and folder names; use underscores `_` or hyphens `-` instead.

## Documentation

- Maintain clear and concise documentation for commands and workflows.
- Use comments (`#`) to annotate scripts and commands.

---

# Additional Resources

- [Linux Documentation](https://linux.die.net/)
- [GNU Bash Reference](https://www.gnu.org/software/bash/manual/bash.html)
- [SSH Key Management](https://www.ssh.com/academy/ssh/keygen)
