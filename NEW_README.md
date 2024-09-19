
# The Art of Command Line (Simplified for Beginners)

This guide will help you become familiar with commonly used command-line commands for both **Linux** and **Windows**. 
We focus on **Ubuntu** and **Kali Linux** for Linux users, and provide variations when necessary. The goal is to make these 
commands easier to understand and use, and show practical examples.

## Table of Contents
1. [Navigating the File System](#navigating-the-file-system)
2. [File Management](#file-management)
3. [Process Management](#process-management)
4. [Networking](#networking)
5. [System Information and Monitoring](#system-information-and-monitoring)
6. [Other Useful Commands](#other-useful-commands)

---

## Navigating the File System

### Linux (Ubuntu & Kali)

- **`pwd`**: Prints the current working directory.
    ```bash
    pwd
    ```
    Example: If you're in `/home/user/documents`, this command will output `/home/user/documents`.

- **`cd`**: Changes directory.
    ```bash
    cd /path/to/folder
    ```
    Example:
    ```bash
    cd /home/user/documents
    ```
    - To go back to the previous directory:
    ```bash
    cd ..
    ```

### Windows

- **`cd`**: Works similarly in Windows to change the directory.
    ```bash
    cd C:\path\to\folder
    ```

---

## File Management

### Linux

- **`ls`**: Lists files and directories in the current directory.
    ```bash
    ls
    ```
    Example:
    ```bash
    ls -l
    ```
    - `-l` provides a detailed view including file permissions, owner, size, and modification date.
    - To list hidden files, use `-a`:
    ```bash
    ls -a
    ```

- **`rm`**: Removes files.
    ```bash
    rm filename.txt
    ```
    To delete a directory and all its contents (be careful with this):
    ```bash
    rm -r foldername
    ```

    - Use `-f` to force deletion without confirmation:
    ```bash
    rm -rf foldername
    ```

### Windows

- **`dir`**: Lists files and directories in the current directory.
    ```bash
    dir
    ```

- **`del`**: Deletes files.
    ```bash
    del filename.txt
    ```
    - To delete all files in a folder:
    ```bash
    del *.*
    ```
    (Note: Windows doesn’t have a direct `rm -r` equivalent. To remove folders, you generally use `rmdir`.)

---

## Process Management

### Linux

- **`ps`**: Lists running processes.
    ```bash
    ps aux
    ```
    Example: This will list all processes running on the system.

- **`kill`**: Terminates a process using its PID.
    ```bash
    kill PID
    ```

    Example:
    ```bash
    kill 1234
    ```
    (Where `1234` is the Process ID)

    - For forceful termination:
    ```bash
    kill -9 PID
    ```

### Windows

- **`tasklist`**: Lists running processes.
    ```bash
    tasklist
    ```

- **`taskkill`**: Kills a process.
    ```bash
    taskkill /PID 1234
    ```

---

## Networking

### Linux

- **`ifconfig`**: Displays network configuration (replaced by `ip` in modern distributions).
    ```bash
    ifconfig
    ```
    or
    ```bash
    ip addr show
    ```

- **`ping`**: Checks network connectivity.
    ```bash
    ping google.com
    ```

### Windows

- **`ipconfig`**: Displays network configuration.
    ```bash
    ipconfig
    ```

- **`ping`**: Same as in Linux.
    ```bash
    ping google.com
    ```

---

## System Information and Monitoring

### Linux

- **`top`**: Displays system resource usage (CPU, Memory, etc.)
    ```bash
    top
    ```
    - To exit, press `q`.

- **`df`**: Displays disk usage.
    ```bash
    df -h
    ```

    - `-h` makes the output human-readable (e.g., `MB`, `GB` instead of bytes).

### Windows

- **`taskmgr`**: Opens Task Manager.
    ```bash
    taskmgr
    ```

- **`systeminfo`**: Displays detailed system information.
    ```bash
    systeminfo
    ```

---

## Other Useful Commands

### Linux

- **`sudo`**: Runs a command as the superuser (admin).
    ```bash
    sudo apt update
    ```
    - Example: Updates your package list.

- **`chmod`**: Changes file permissions.
    ```bash
    chmod +x filename.sh
    ```
    - Makes the file executable.

### Windows

- **`cls`**: Clears the Command Prompt screen.
    ```bash
    cls
    ```

- **`shutdown`**: Shuts down the system.
    ```bash
    shutdown /s /f /t 0
    ```
