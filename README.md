# The Terminal Playbook 💻✨
##Overclock Your Productivity on Windows 🚀
This repository is your ultimate guide to mastering the Windows command line, with a comprehensive focus on Windows-specific tools and techniques. Whether you're a beginner looking to enhance your command line knowledge or an advanced user aiming to sharpen your skills, this guide has everything you need. It’s packed with practical tips, powerful commands, and advanced techniques to streamline your workflow, save time, and boost productivity.

Mastering the Windows command line is a game-changer for users and developers alike. This guide empowers you to:

- Efficiently navigate your system 🔍
- Automate repetitive tasks ⚙️
- Optimize your workflow 🛠️
- Master essential Windows tools like PowerShell and Command Prompt 🧠
Unlock the power of the terminal and take full control of your Windows environment. Your productivity is about to skyrocket! 🚀

## Meta 📜
This guide is perfect for beginners and advanced users alike, offering essential Windows commands without unnecessary fluff. Each tip is curated to provide maximum value and real-world applications.

The guide exclusively focuses on Windows systems, including Command Prompt and PowerShell. We’ll highlight tips and tricks for efficiently using the command line in a Windows environment.

For those interested in learning Linux commands, see our dedicated Linux Commands Guide.

### Windows Command Line Basics
Get Started with Command Prompt or PowerShell
- Command Prompt: The original Windows shell. Simple, fast, and useful for basic tasks.
- PowerShell: A more powerful shell with scripting capabilities, useful for automation and advanced system management.
- Batch File Automation: Create a batch file (`.bat`) to automate repetitive tasks. Write a series of commands in a text file, save it as `.bat`, and run it to execute all commands at once.
- Package Management: Windows: Use [Chocolatey](https://chocolatey.org/) or [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/). Example:  
  `choco install package_name`

### Use Command Line Text Editors 📝
While Windows offers powerful GUI text editors like Notepad++ and Visual Studio Code, having a lightweight command-line text editor can be useful when working in terminal environments:

- Nano: A beginner-friendly command-line text editor (available in WSL).
- Vim: An advanced editor known for speed and efficiency.

---

## Windows Commands Symbols and Syntax

This section provides an overview of common symbols, letters, and punctuation used in Windows command prompts. Understanding these can help you read and write commands more effectively.

### 1. Single Letters and Alphabet Combinations
- **C:** Often used to refer to the C: drive, the main hard drive on many Windows systems.
- **D, E, etc.:** Refer to other drives (D:, E:, etc.) connected to your computer.

### 2. Single Dash (`-`)
- Often used to indicate options or flags in commands. For example, `dir -a` (though in Windows, options often use `/` instead).

### 3. Double Dash (`--`)
- Typically used in other command-line interfaces (like Linux) to signify longer option names, but not commonly seen in Windows.

### 4. Square Brackets (`[]`)
- Indicate optional parameters in command syntax. For example, `dir [<path>]` means you can include a path, but it's not required.

### 5. Curly Braces (`{}`)
- Used in documentation to denote a set of choices. For example, `command {option1|option2}` means you can choose either `option1` or `option2`.

### 6. Parentheses (`()`)
- Used to group commands or parameters. For example, `if (condition) command` indicates that the command will run only if the condition is true.

### 7. Single Quotes (`''`)
- Used to enclose strings, especially when the string contains spaces. For example, `'My Documents'` keeps the phrase intact as one unit.

### 8. Double Quotes (`""`)
- Similar to single quotes but can allow for variable expansion within the string. For example, `"Path to file: %USERPROFILE%"`.

### 9. Exclamation Mark (`!`)
- Used in batch files to denote variables, particularly when using `enabledelayedexpansion`.

### 10. Ampersand (`&`)
- Used to combine multiple commands on a single line. For example, `command1 & command2` runs `command2` after `command1`.

### 11. Less Than (`<`) and Greater Than (`>`)
- **Less Than (`<`):** Used to redirect input to a command. For example, `command < input.txt` takes input from `input.txt`.
- **Greater Than (`>`):** Used to redirect output to a file. For example, `dir > output.txt` saves the directory listing to `output.txt`.
- **Double Greater Than (`>>`):** Appends output to a file instead of overwriting. For example, `echo Hello >> file.txt`.

### 12. Dot (`.`)
- Represents the current directory. For example, `.\file.txt` refers to `file.txt` in the current folder.
- **Double Dot (`..`):** Represents the parent directory. For example, `cd ..` moves up one directory level.

### 13. Colon (`:`)
- Used to denote drive letters (e.g., `C:`) or to specify a label or option in a command (e.g., `:label` in batch scripts).

### 14. Semicolon (`;`)
- Typically used to separate commands in some contexts, though less common in Windows command prompts compared to other systems.

---

## File and Directory Commands 📂 

This section provides the most commonly used commands for managing files and directories in Windows.

### dir
Lists the contents of a directory.

Usage:
```bash
dir [<path>] [options]
```
Examples:

- `dir` – Lists contents of the current directory.
- `dir C:\Users` – Lists contents of the specified directory.
- `dir /w` – Lists directory contents in wide format.
- `dir /p` – Lists the directory contents page by page.
##
### cd
Changes the current directory.

Usage:

```bash
cd [<path>]
```
Examples:

- `cd Documents` – Changes to the Documents directory.
- `cd ..` – Moves up one directory level.
- `cd C:\` – Changes to the root of the C drive.
- `cd /d D:\Projects` – Changes to the specified directory on a different drive.
##
### touch
Create new file in current directory.

Usage:

```bash
touch [filename]
```
Example:

- `touch [filename]` – Create a new file
##
### mkdir
Creates a new directory.

Usage:

```bash
mkdir [<directory-name>]
```
Examples:

- `mkdir Projects` – Creates a new directory named "Projects" in the current location.
- `mkdir C:\NewFolder` – Creates a new folder called "NewFolder" in the root of the C drive.
##
### rmdir
Removes a directory.

Usage:

```bash
rmdir [<directory-name>] [options]
```
Examples:

- `rmdir NewFolder` – Removes an empty directory called "NewFolder."
- `rmdir /s /q C:\Projects` – Removes the directory "Projects" and all of its contents without confirmation.
##
### copy
Copies files from one location to another.

Usage:

```bash
copy [<source>] [<destination>]
```
Examples:

- `copy file.txt D:\Backup\` – Copies "file.txt" to the "Backup" directory on the D drive.
- `copy C:\Data\*.txt D:\Backup\` – Copies all text files from the "Data" folder to the "Backup" folder.
##
### move
Moves or renames files or directories.

Usage:

```bash
move [<source>] [<destination>]
```
Examples:

- `move file.txt D:\Documents\` – Moves "file.txt" to the "Documents" folder on the D drive.
- `move C:\OldFolder C:\NewFolder` – Renames "OldFolder" to "NewFolder."
##
### del
Deletes one or more files.

Usage:

```bash
del [<file>] [options]
```
Examples:

- `del file.txt` – Deletes "file.txt" in the current directory.
- `del *.txt` – Deletes all text files in the current directory.
- `del /q C:\Temp\*.log` – Quietly deletes all ".log" files in the "Temp" directory without asking for confirmation.
##
### ren
Renames a file or directory.

Usage:

```bash
ren [<old-name>] [<new-name>]
```
Examples:

- `ren file1.txt file2.txt` – Renames "file1.txt" to "file2.txt."
- `ren C:\OldName C:\NewName` – Renames the directory "OldName" to "NewName."
##
### attrib
Displays or changes file attributes.

Usage:

```bash
attrib [<attributes>] [<file-name>]
```
Examples:

- `attrib +r file.txt` – Sets the "Read-only" attribute for "file.txt."
- `attrib -h -r C:\Folder\*.* /s` – Removes the "Hidden" and "Read-only" attributes from all files in the "Folder" directory and its subdirectories.
##
### type
Displays the contents of a text file.

Usage:

```bash
type [<file-name>]
```
Examples:

- `type file.txt` – Displays the contents of "file.txt."
- `type C:\Temp\log.txt` – Displays the contents of the log file in the "Temp" folder.
---
## Process Management Commands

This section covers the commands used for managing processes in the Windows operating system.

### tasklist 
Displays a list of currently running processes.

Usage:
```bash
tasklist [options]
```
Examples:

- `tasklist` – Lists all running processes.
- `tasklist /fi "imagename eq notepad.exe"` – Lists all processes with the name "notepad.exe."
- `tasklist /svc` – Displays the services hosted in each process.
- `tasklist /v` – Displays verbose information about running processes.
##
### taskkill
Terminates a running process or application.

Usage:

```bash
taskkill [options] /pid <process-id> /im <image-name>
```
Examples:

- `taskkill /pid 1234` – Terminates the process with the Process ID (PID) 1234.
- `taskkill /im notepad.exe` – Terminates all instances of Notepad.
- `taskkill /f /im chrome.exe` – Forcibly terminates all instances of Chrome.
- `taskkill /f /pid 5678` – Forcibly terminates the process with PID 5678.
##
### start
Starts a new instance of a program or command in a new window.

Usage:

```bash
start [<application-or-command>]
```
Examples:

- `start notepad` – Opens a new instance of Notepad.
- `start cmd /k dir` – Opens a new Command Prompt window and runs the dir command.
- `start explorer.exe` – Opens a new instance of Windows Explorer.
##

### wmic
The Windows Management Instrumentation Command-line (WMIC) is used to query system information and manage processes.

Usage:

```bash
wmic process [<query-options>]
```
Examples:

- `wmic process list brief` – Lists running processes with brief details.
- `wmic process where "name='notepad.exe'" delete` – Terminates the "notepad.exe" process.
- `wmic process get name,processid` – Displays the name and PID of all running processes.
##
### sc
Communicates with the Service Control Manager to manage Windows services (start, stop, configure).

Usage:

```bash
sc [<command>] [<service-name>] [options]
```
Examples:

- `sc query` – Displays the status of all services.
- `sc stop Spooler` – Stops the Print Spooler service.
- `sc start Spooler` – Starts the Print Spooler service.
- `sc config Spooler start= auto` – Sets the Print Spooler service to start automatically on boot.
##
### schtasks
Schedules, deletes, or queries tasks on the local or a remote machine.

Usage:

```bash
schtasks [<command>] [options]
```
Examples:

- `schtasks /create /tn "Backup" /tr "C:\BackupScript.bat" /sc daily /st 14:00` – Schedules a daily task named "Backup" to run the script at 2:00 PM.
- `schtasks /query /tn "Backup"` – Queries information about the "Backup" task.
- `schtasks /delete /tn "Backup"` – Deletes the "Backup" task.

## Open Windows Software
Open Software directly frmo command prompt window.

### taskmgr
Opens the Windows Task Manager to monitor and manage running processes.

Usage:

```bash
taskmgr
```
Examples:

- `taskmgr` – Opens Task Manager.
##
### powershell
Starts a PowerShell session, allowing you to run PowerShell commands for advanced process and system management.

Usage:

```bash
powershell [<command>]
```
Examples:

- `powershell Get-Process` – Lists all running processes using PowerShell.
- `powershell Stop-Process` -Name notepad – Stops all instances of Notepad using PowerShell.
- `powershell Restart-Computer` – Restarts the computer using PowerShell.
##
### regedit
Opens the Windows Registry Editor to view or modify system registry settings.

**Usage:**

```bash
regedit
```
Examples:

- `regedit` – Opens the Registry Editor.
##
### secpol.msc
Opens the Local Security Policy editor to configure security policies on the computer.

Usage:

```bash
secpol.msc
```
Examples:

- `secpol.msc` – Opens the Local Security Policy manager.
##
### gpedit.msc
Opens the Group Policy Editor to configure various system policies.

Usage:

```bash
gpedit.msc
```
Examples:

- `gpedit.msc` – Opens the Group Policy Editor.
##
### taskschd.msc
Opens the Task Scheduler to manage automated tasks on the system.

Usage:

```bash
taskschd.msc
```
Examples:

- `taskschd.msc` – Opens the Task Scheduler.

## System Information
This section covers commands used to gather system information and hardware information.

### systeminfo  
Displays detailed configuration information about the computer and its operating system.

Usage:

```bash
systeminfo
```
Examples:

- `systeminfo` – Displays detailed information about the system, including OS version, memory, and network details.
##
### msinfo32
Opens the Microsoft System Information tool, displaying a graphical view of system information.

Usage:

```bash
msinfo32
```
Examples:

- `msinfo32` – Opens the System Information GUI for detailed system hardware and software information.
##
### wmic
Queries various system components such as BIOS, CPU, disk drives, and memory.

Usage:

```bash
wmic [query]
```
Examples:

- `wmic bios get serialnumber` – Retrieves the system BIOS serial number.
- `wmic cpu get name` – Displays the CPU name.
- `wmic memorychip get capacity` – Displays the total physical memory.
- `wmic diskdrive get status` – Checks the status of the hard disk drive.
##
### diskpart
Manages disk partitions, volumes, and virtual hard disks.

Usage:

```bash
diskpart
```
Examples:

- `diskpart` – Opens the Disk Partition Manager.
- `list disk` – Lists all disks.
- `select disk 0` – Selects disk 0 for partition management.
- `clean` – Erases all partitions and data from the selected disk.
##
### bcdedit
Boot configuration data edit to manage boot options.

Usage:

```bash
bcdedit [command] [options]
```
Examples:

- `bcdedit /set {default} bootmenupolicy legacy` – Enables the legacy boot menu.
- `bcdedit /set increaseuserva 3072` – Allocates more virtual memory to improve performance for certain applications.
##
### powercfg
Configures power settings and manages power consumption, useful for optimizing performance and battery life.

Usage:

```bash
powercfg [options]
```
Examples:

- `powercfg /list` – Lists all power schemes.
- `powercfg /energy` – Generates a detailed energy report, identifying issues with power efficiency.
- `powercfg /hibernate on` – Enables hibernation.
- `powercfg /hibernate off` – Disables hibernation to save disk space.
##
### tsshutdn
Schedules a system shutdown or restart on a remote system via Terminal Services.

Usage:

```bash
tsshutdn [options]
```
Examples:

- `tsshutdn 60 /delay:30 /reboot` – Restarts the system in 60 seconds, with a 30-second warning delay.
- `tsshutdn /powerdown` – Shuts down the system and powers off.
##
### shutdown
Shuts down or restarts the computer.

Usage:

```bash
shutdown [options]
```
Examples:

- `shutdown /s` – Shuts down the computer.
- `shutdown /r` – Restarts the computer.
- `shutdown /l` – Logs off the current user.
- `shutdown /s /t 60` – Shuts down the computer in 60 seconds.
- `shutdown /a` – Aborts a system shutdown.
##
## Windows Optimation and Repair Commands
help to boost performance and maintain system health.

### cleanmgr
Opens the Disk Cleanup utility to remove unnecessary files and free up space.

Usage:

```bash
cleanmgr [options]
```
Examples:

- `cleanmgr` – Opens the Disk Cleanup tool.
- `cleanmgr /sageset:1` – Opens Disk Cleanup with advanced options for selecting files to remove.
- `cleanmgr /sagerun:1` – Runs Disk Cleanup with predefined settings.
##
### defrag
Optimizes and defragments hard drives to improve performance.

Usage:

```bash
defrag [drive:] [options]
```
Examples:

- `defrag C:` – Defragments the C: drive.
- `defrag C: /O` – Optimizes and defragments the C: drive.
- `defrag /C /H /U /V` – Optimizes and defragments all volumes with high priority, updating progress and providing verbose output.
##
### chkdsk
Checks the disk for file system errors and bad sectors, optionally repairs them.

Usage:

```bash
chkdsk [drive:] [options]
```
Examples:

- `chkdsk C:` – Checks the C: drive for errors.
- `chkdsk C: /f` – Fixes file system errors on the C: drive.
- `chkdsk C: /r` – Identifies and repairs bad sectors on the C: drive.
##
### sfc
Scans and repairs protected system files.

Usage:

```bash
sfc /scannow
```
Examples:

- `sfc /scannow` – Scans the system for corrupted or missing files and repairs them.
- `sfc /verifyonly` – Scans for integrity violations without making repairs.
##
### verifier
Driver Verifier Manager checks for faulty drivers that may cause system issues.

Usage:

```bash
verifier [options]
```
Examples:

- `verifier` – Opens the Driver Verifier Manager.
- `verifier /query` – Queries the current settings of the Driver Verifier.
##
### mdsched
Runs the Windows Memory Diagnostic tool to check for memory errors.

Usage:

```bash
mdsched
```
Examples:

- `mdsched` – Opens the Windows Memory Diagnostic tool for a memory test.
##
### dism
Deployment Image Servicing and Management (DISM) is used to repair Windows images, including the Windows Recovery Environment.

Usage:

```bash
dism /Online /Cleanup-Image /RestoreHealth
```
Examples:

- `dism /Online /Cleanup-Image /RestoreHealth` – Repairs a corrupted Windows image.
- `dism /Online /Cleanup-Image /CheckHealth` – Checks if the image has any corruption.

## Windows Security Commands
These commands ensure your system is safe and properly configured.

## mrt
Description:
Runs the Microsoft Malicious Software Removal Tool to scan for and remove malware.

Usage:

```bash
mrt
```
Examples:

- `mrt` – Opens the Microsoft Malicious Software Removal Tool.

## Networking Commands
This section covers essential Windows networking commands that help troubleshoot, configure, and manage network connections.

### ipconfig  
Displays the current Transmission Control Protocol/Internet Protocol (TCP/IP) network configuration for the system, including IP address, subnet mask, default gateway, and Domain Name System (DNS) settings.

Usage:

```bash
ipconfig [options]
```
Examples:

- `ipconfig` – Displays basic network configuration.
- `ipconfig /all` – Shows detailed network configuration, including DHCP and DNS settings.
- `ipconfig /release` – Releases the current IP address of all network adapters.
- `ipconfig /renew` – Renews the IP address for all adapters.
- `ipconfig /flushdns` – Clears the DNS cache to resolve DNS-related issues.
##
### Getmac
Displays the MAC address for network adapters on the system.

Usage:

```bash
getmac
```
Examples:

- `getmac` – Displays the MAC addresses of all network interfaces.
##
###Key Points:
- Troubleshoot network issues with ipconfig, ping, tracert, and netstat.
- Manage network interfaces, routing, and configuration using netsh, route, and net.
- Advanced network diagnostics can be performed using nslookup, telnet, and ftp.
##
###netstat
Displays active Transmission Control Protocol (TCP) connections, routing tables, and network interface statistics.

Usage:

```bash
netstat [options]
```
Examples:

- `netstat` – Lists all active connections.
- `netstat -a` – Shows all active TCP/UDP connections and listening ports.
- `netstat -an` – Displays all active connections in numerical form (IP addresses and port numbers).
- `netstat -b` – Displays the executable involved in creating each connection or listening port.
- `netstat -r` – Displays the routing table.
##
### ping
Sends Internet Control Message Protocol (ICMP) Echo Requests to test connectivity between the system and a remote host.

Usage:

```bash
ping [host] [options]
```
Examples:

- `ping google.com` – Tests the connection to Google's server.
- `ping 192.168.1.1` – Tests connectivity to a local network device.
- `ping -t google.com` – Continuously pings Google's server until interrupted.
- `ping -n 10 google.com` – Sends 10 ping requests to Google's server.
##
### tracert
Traces the route taken by packets to reach a destination host and displays the path taken by data packets across the network.

Usage:

```bash
tracert [host] [options]
```
Examples:

- `tracert google.com` – Traces the path to Google's server.
- `tracert 192.168.1.1` – Traces the path to a local network device
##
### nslookup
Queries the DNS to obtain domain name or Internet Protocol (IP) address mapping information.

Usage:

```bash
nslookup [host] [server]
```
Examples:

- `nslookup google.com` – Retrieves the IP address of Google's server.
- `nslookup 8.8.8.8` – Retrieves the domain associated with the IP address 8.8.8.8.
- `nslookup google.com 8.8.8.8` – Queries the specified DNS server (8.8.8.8) for Google's IP address.
##
### arp
Displays and modifies the Address Resolution Protocol (ARP) cache used to resolve IP addresses to Media Access Control (MAC) addresses.

Usage:

```bash
arp [options]
```
Examples:

- `arp -a` – Displays the current ARP cache.
- `arp -d 192.168.1.1` – Deletes the ARP entry for the specified IP address.
- `arp -s 192.168.1.1 00-14-22-01-23-45` – Adds a static ARP entry.
##
### netsh
Configures network settings, manages firewall rules, and runs network diagnostics.

Usage:

```bash
netsh [context] [command]
```
Examples:

- `netsh interface ip show config` – Displays IP configuration for all network interfaces.
- `netsh int ip reset` – Resets the TCP/IP stack to its default state.
- `netsh winsock reset` – Resets the Winsock catalog, resolving network connectivity issues.
- `netsh advfirewall set allprofiles state on` – Turns on the firewall for all profiles.
- `netsh interface set interface "Ethernet" admin=disable` – Disables a network interface.
- `netsh wlan show profiles` – Displays stored Wi-Fi profiles on the system.
##
### route
Displays and modifies the network routing table used to determine packet forwarding.

Usage:

```bash
route [command] [options]
```
Examples:

- `route print` – Displays the current routing table.
- `route add 192.168.2.0 mask 255.255.255.0 192.168.1.1` – Adds a route to the network 192.168.2.0 via gateway 192.168.1.1.
- `route delete 192.168.2.0` – Deletes the specified route.
##
### net
Used to manage various network-related tasks, including user accounts, shares, and services.

Usage:

```bash
net [command] [options]
```
Examples:

- `net view` – Lists computers and devices on the local network.
- `net user` – Displays all user accounts on the system.
- `net use \\192.168.1.100\SharedFolder` – Connects to a shared folder on another computer.
##
### telnet
A command-line tool for remote communication with servers using the Telnet protocol.

Usage:

```bash
telnet [host] [port]
```
Examples:

- `telnet google.com 80` – Connects to Google's web server on port 80.
- `telnet 192.168.1.1 23` – Connects to a local device using Telnet on port 23.
##
### ftp
A command-line tool for transferring files to and from remote servers using the File Transfer Protocol (FTP).

Usage:

```bash
ftp [host]
```
Examples:

- `ftp 192.168.1.1` – Connects to an FTP server on the local network.
- `ftp example.com` – Connects to a remote FTP server.
##
### Searching with Grep
- `grep` is a powerful search tool. Some common options:
  - `grep -i` - Case-insensitive search.
  - `grep -v` - Invert the match (show lines that don't contain the pattern).
  - `grep -o` - Show only the matching part of the line.
  - Use `grep -r "text" .` to search recursively in all files within the current directory.

---

## 📚 More Resources

- **Explainshell**: [explainshell.com](http://explainshell.com/) - Paste any command and get an explanation of each part.
- **Cheat.sh**: `curl cheat.sh/command` - Instant cheat sheets for any command.

---

### 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

