# The Terminal Playbook 🚀

### Overclock Your Productivity 💻✨

This repository is your ultimate guide to mastering the command line, with a special focus on **Linux** and **Windows** systems. Whether you're a beginner looking to enhance your command line knowledge or a seasoned pro aiming to sharpen your skills, this guide has you covered. It’s packed with practical tips, powerful commands, and advanced techniques to streamline your workflow, save time, and boost productivity.

Mastering the command line is a **game-changer** for developers. This guide empowers you to:
- Navigate your system efficiently 🔍
- Automate repetitive tasks ⚙️
- Optimize your development workflow 🛠️
- Master essential tools like **Git**, **Bash**, and **grep** 🧠

Unlock the power of the terminal and take full control of your development environment. Your productivity is about to skyrocket! 🚀

---

## Meta

**Scope**  
- This guide is perfect for **beginners** and **advanced users** alike, offering essential commands without the fluff. Each tip is curated to provide maximum value and real-world applications.  
- While the primary focus is on **Linux** (Bash), most commands and tips also apply to **Windows** (especially if using WSL or Git Bash). We’ll point out specific OS differences when necessary.

**Notes**  
- This is a **reference guide**, so if you need detailed explanations, make use of tools like `man` or online resources such as [Explainshell](http://explainshell.com/).  
- Install necessary programs using package managers like `apt` for Linux or [Chocolatey](https://chocolatey.org/) for Windows.  
- Contributions are always welcome! If you spot an area for improvement or have any questions.

---

## 🛠️ Command Line Basics

### Learn Basic Bash
- **Bash** is the default shell on most Linux systems and is essential to learn. You can start by typing `man bash` to read its manual. 
- For Windows users, consider using [Git Bash](https://gitforwindows.org/) or WSL for a similar experience.

### Use a Command Line Text Editor 📝
- **Nano**: Beginner-friendly text editor. It's simple and shows all commands at the bottom.
- **Vim**: Advanced text editor with a steeper learning curve but great for speed and efficiency.
- Windows users can also install [Notepad++](https://notepad-plus-plus.org/) or [Visual Studio Code](https://code.visualstudio.com/), but having a command-line text editor like Vim or Nano can be useful when working in terminal environments.

### Overview
### File and Directory Operations

This section covers commands for working with files and directories in Linux.

## Listing Files
- `ls` – List directory contents
- `ls -a` – List all files, including hidden files
- `ls -l` – List files in long format

## Changing Directories
- `cd` – Change to the home directory
- `cd [directory]` – Change to a specific directory
- `cd ..` – Move up one directory level

## Creating Files and Directories
- `touch [filename]` – Create a new file
- `mkdir [directory]` – Create a new directory
- `mkdir -p [parent-dir]/[sub-dir]` – Create nested directories

## Removing Files and Directories
- `rm [file]` – Remove a file
- `rm -r [directory]` – Remove a directory and its contents
- `rmdir [directory]` – Remove an empty directory

## Copying and Moving Files
- `cp [source] [destination]` – Copy a file
- `cp -r [source-dir] [destination-dir]` – Copy a directory and its contents
- `mv [source] [destination]` – Move or rename a file or directory

## Viewing and Editing Files
- `cat [file]` – View the contents of a file
- `less [file]` – View file content page by page
- `nano [file]` – Edit a file using the nano text editor
- `vim [file]` – Edit a file using the vim editor

### Process Management

This section provides commands for managing processes in Linux.

## Listing Processes
- `ps` – List currently running processes
- `top` – Display dynamic real-time system statistics and processes
- `htop` – Interactive process viewer (if installed)

## Killing Processes
- `kill [PID]` – Terminate a process by its PID
- `killall [process-name]` – Terminate all processes with a given name
- `pkill [pattern]` – Terminate processes that match a pattern

## Background and Foreground Processes
- `&` – Run a command in the background
- `fg` – Bring a background process to the foreground
- `bg` – Resume a suspended job in the background
- `jobs` – List all background jobs

## Process Priorities
- `nice [command]` – Start a command with a specified priority
- `renice [priority] [PID]` – Change the priority of a running process



### File Management 📂




# File and Directory Commands 

This section provides the most commonly used commands for managing files and directories in Windows.

## dir
Description:
Lists the contents of a directory.

**Usage:**
```bash
dir [<path>] [options]
```
Examples:

- `dir` – Lists contents of the current directory.
- `dir C:\Users` – Lists contents of the specified directory.
- `dir /w` – Lists directory contents in wide format.
- `dir /p` – Lists the directory contents page by page.

## cd
Description:
Changes the current directory.

**Usage:**

```bash
cd [<path>]
```
Examples:

- `cd Documents` – Changes to the Documents directory.
- `cd ..` – Moves up one directory level.
- `cd C:\` – Changes to the root of the C drive.
- `cd /d D:\Projects` – Changes to the specified directory on a different drive.

## touch
Description:
Create new file in current directory.

**Usage**

```bash
touch [filename]
```
Example:

- `touch [filename]` – Create a new file

## mkdir
Description:
Creates a new directory.

**Usage:**

```bash
mkdir [<directory-name>]
```
Examples:

- `mkdir Projects` – Creates a new directory named "Projects" in the current location.
- `mkdir C:\NewFolder` – Creates a new folder called "NewFolder" in the root of the C drive.

## rmdir
Description:
Removes a directory.

**Usage:**

```bash
rmdir [<directory-name>] [options]
```
Examples:

- `rmdir NewFolder` – Removes an empty directory called "NewFolder."
- `rmdir /s /q C:\Projects` – Removes the directory "Projects" and all of its contents without confirmation.

## copy
Description:
Copies files from one location to another.

**Usage:**

```bash
copy [<source>] [<destination>]
```
Examples:

- `copy file.txt D:\Backup\` – Copies "file.txt" to the "Backup" directory on the D drive.
- `copy C:\Data\*.txt D:\Backup\` – Copies all text files from the "Data" folder to the "Backup" folder.

## move
Description:
Moves or renames files or directories.

**Usage:**

```bash
move [<source>] [<destination>]
```
Examples:

- `move file.txt D:\Documents\` – Moves "file.txt" to the "Documents" folder on the D drive.
- `move C:\OldFolder C:\NewFolder` – Renames "OldFolder" to "NewFolder."

## del
Description:
Deletes one or more files.

**Usage:**

```bash
del [<file>] [options]
```
Examples:

- `del file.txt` – Deletes "file.txt" in the current directory.
- `del *.txt` – Deletes all text files in the current directory.
- `del /q C:\Temp\*.log` – Quietly deletes all ".log" files in the "Temp" directory without asking for confirmation.

## ren
Description:
Renames a file or directory.

**Usage:**

```bash
ren [<old-name>] [<new-name>]
```
Examples:

- `ren file1.txt file2.txt` – Renames "file1.txt" to "file2.txt."
- `ren C:\OldName C:\NewName` – Renames the directory "OldName" to "NewName."

## attrib
Description:
Displays or changes file attributes.

**Usage:**

```bash
attrib [<attributes>] [<file-name>]
```
Examples:

- `attrib +r file.txt` – Sets the "Read-only" attribute for "file.txt."
- `attrib -h -r C:\Folder\*.* /s` – Removes the "Hidden" and "Read-only" attributes from all files in the "Folder" directory and its subdirectories.

## type
Description:
Displays the contents of a text file.

**Usage:**

```bash
type [<file-name>]
```
Examples:

- `type file.txt` – Displays the contents of "file.txt."
- `type C:\Temp\log.txt` – Displays the contents of the log file in the "Temp" folder.

### Process Management Commands

This section covers the commands used for managing processes in the Windows operating system.

## tasklist
Description: 
Displays a list of currently running processes.

**Usage:**
```bash
tasklist [options]
```
Examples:

- `tasklist` – Lists all running processes.
- `tasklist /fi "imagename eq notepad.exe"` – Lists all processes with the name "notepad.exe."
- `tasklist /svc` – Displays the services hosted in each process.
- `tasklist /v` – Displays verbose information about running processes.

## taskkill
Description:
Terminates a running process or application.

**Usage:**

```bash
taskkill [options] /pid <process-id> /im <image-name>
```
Examples:

- `taskkill /pid 1234` – Terminates the process with the Process ID (PID) 1234.
- `taskkill /im notepad.exe` – Terminates all instances of Notepad.
- `taskkill /f /im chrome.exe` – Forcibly terminates all instances of Chrome.
- `taskkill /f /pid 5678` – Forcibly terminates the process with PID 5678.

## start
Description:
Starts a new instance of a program or command in a new window.

**Usage:**

```bash
start [<application-or-command>]
```
Examples:

- `start notepad` – Opens a new instance of Notepad.
- `start cmd /k dir` – Opens a new Command Prompt window and runs the dir command.
- `start explorer.exe` – Opens a new instance of Windows Explorer.

## taskmgr
Description:
Opens the Windows Task Manager to monitor and manage running processes.

**Usage:**

```bash
taskmgr
```
Examples:

- `taskmgr` – Opens Task Manager.

## wmic
Description:
The Windows Management Instrumentation Command-line (WMIC) is used to query system information and manage processes.

**Usage:**

```bash
wmic process [<query-options>]
```
Examples:

- `wmic process list brief` – Lists running processes with brief details.
- `wmic process where "name='notepad.exe'" delete` – Terminates the "notepad.exe" process.
- `wmic process get name,processid` – Displays the name and PID of all running processes.

## sc
Description:
Communicates with the Service Control Manager to manage Windows services (start, stop, configure).

**Usage:**

```bash
sc [<command>] [<service-name>] [options]
```
Examples:

- `sc query` – Displays the status of all services.
- `sc stop Spooler` – Stops the Print Spooler service.
- `sc start Spooler` – Starts the Print Spooler service.
- `sc config Spooler start= auto` – Sets the Print Spooler service to start automatically on boot.

## schtasks
Description:
Schedules, deletes, or queries tasks on the local or a remote machine.

**Usage:**

```bash
schtasks [<command>] [options]
```
Examples:

- `schtasks /create /tn "Backup" /tr "C:\BackupScript.bat" /sc daily /st 14:00` – Schedules a daily task named "Backup" to run the script at 2:00 PM.
- `schtasks /query /tn "Backup"` – Queries information about the "Backup" task.
- `schtasks /delete /tn "Backup"` – Deletes the "Backup" task.

## shutdown
Description:
Shuts down or restarts the computer.

**Usage:**

```bash
shutdown [options]
```
Examples:

- `shutdown /s` – Shuts down the computer.
- `shutdown /r` – Restarts the computer.
- `shutdown /l` – Logs off the current user.
- `shutdown /s /t 60` – Shuts down the computer in 60 seconds.
- `shutdown /a` – Aborts a system shutdown.

## powershell
Description:
Starts a PowerShell session, allowing you to run PowerShell commands for advanced process and system management.

**Usage:**

```bash
powershell [<command>]
```
Examples:

- `powershell Get-Process` – Lists all running processes using PowerShell.
- `powershell Stop-Process` -Name notepad – Stops all instances of Notepad using PowerShell.
- `powershell Restart-Computer` – Restarts the computer using PowerShell.

## regedit
Description:
Opens the Windows Registry Editor to view or modify system registry settings.

**Usage:**

```bash
regedit
```
Examples:

- `regedit` – Opens the Registry Editor.

### System Info
This section covers commands used to gather system information.

## systeminfo
Description:  
Displays detailed configuration information about the computer and its operating system.

**Usage:**
```bash
systeminfo
```
Examples:

- `systeminfo` – Displays detailed information about the system, including OS version, memory, and network details.

## msinfo32
Description:
Opens the System Information tool, displaying a graphical view of system information.

**Usage:**

```bash
msinfo32
```
Examples:

- `msinfo32` – Opens the System Information GUI for detailed system hardware and software information.

## wmic
Description:
Queries various system components such as BIOS, CPU, disk drives, and memory.

**Usage:**

```bash
wmic [query]
```
Examples:

- `wmic bios get serialnumber` – Retrieves the system BIOS serial number.
- `wmic cpu get name` – Displays the CPU name.
- `wmic memorychip get capacity` – Displays the total physical memory.
- `wmic diskdrive get status` – Checks the status of the hard disk drive.

## diskpart
Description:
Manages disk partitions, volumes, and virtual hard disks.

**Usage:**

```bash
diskpart
```
Examples:

- `diskpart` – Opens the Disk Partition Manager.
- `list disk` – Lists all disks.
- `select disk 0` – Selects disk 0 for partition management.
- `clean` – Erases all partitions and data from the selected disk.



Tip: Use `ls -la` to see hidden files and detailed file info.

### Network Management 🌐
- Use `ping` to test network connectivity.
- Run `ip addr` (Linux) or `ipconfig` (Windows) to view network configurations.
- Use `traceroute` (Linux) or `tracert` (Windows) to troubleshoot network paths.

---

## 🌟 Advanced Command Line Tips

### Git Version Control 💡
- **Git** is an indispensable tool for tracking changes in your projects.
  - `git status` - See changes and the current state of your repository.
  - `git add` - Stage your changes for a commit.
  - `git commit` - Save your staged changes with a message.
  - `git push` - Push local changes to a remote repository.
- Pro Tip: Use `git log --oneline --graph --decorate` for a clean, visual representation of your commit history.

### Pipes & Redirection 🔄
- Use pipes (`|`) to chain commands together. For example:  
  `cat file.txt | grep "keyword"` will search for "keyword" inside `file.txt`.  
- Redirect output to a file using `>` or `>>`. Example:  
  `command > output.txt` overwrites `output.txt` with the command's output.

### Searching with Grep 🧐
- `grep` is a powerful search tool. Some common options:
  - `grep -i` - Case-insensitive search.
  - `grep -v` - Invert the match (show lines that don't contain the pattern).
  - `grep -o` - Show only the matching part of the line.
  - Use `grep -r "text" .` to search recursively in all files within the current directory.

### Package Management 📦
- Linux: Use `apt-get` or `dnf` to install packages. Example:  
  `sudo apt-get install package_name`
- Windows: Use [Chocolatey](https://chocolatey.org/) or [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/). Example:  
  `choco install package_name`

---

## 📚 More Resources

- **Explainshell**: [explainshell.com](http://explainshell.com/) - Paste any command and get an explanation of each part.
- **Cheat.sh**: `curl cheat.sh/command` - Instant cheat sheets for any command.

---

## 🤝 Contributions

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

### 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

