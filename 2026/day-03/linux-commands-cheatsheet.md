- Include **at least 20 commands** with one‑line usage notes
- Add **3 networking commands** (`ping`, `ip addr`, `dig`, `curl`, etc.)
- Group commands by category
- Keep it concise and readable

**BASICS** 
1. pwd - print the work directory
2. man <command> - prints the command
3. ls -<parameter> - list the files in current wokring dir
4. uname -<parameter> - print information of kernel 
5. cd -  change dir
6. clear - clear the dir
7. whoami - print the current user
8. hsitory - print the history of commands
9. date - show time and date

**CREATEING FILE/ DIRECTORY**

In linux exeryting is a file or directory

1. touch <name.ext> - create a file 
   touch python java cpp - create multiple files
   touch books{1..0} - create 10 files named book1 to book10    

2. mkdir - make directory          
    mkdir mandar - make a folder mandar
    mkdir -p mandar/test/release-1 - create dir under a dir whole path
    mkdir test qa prod - make multiple directories
    mkdir version{1..3}

**OPERATIONS ON FILES AND FOLDERS**
1. vim file - open file in vim editor
2. cp - copy
    cp <option> <soucre> <destination>
        options : -r - recursive
                  -v - verbose
                  -f forcefully  


    
    ps, top, pgrep, ls, find, chmod, df, ping, ip addr, curl, ss

    Focused areas:
 • Process Management
 • File System Commands
 • Network Troubleshooting

Practiced commands like:
ps, top, pgrep, ls, find, chmod, df, ping, ip addr, curl, ss, touch, grep, useradd, su, userdel, usermod.

Also reviewed:
- How to check disk usage and file permissions.
- How to test network connectivity and open ports.
- How to inspect service logs using journalctl.