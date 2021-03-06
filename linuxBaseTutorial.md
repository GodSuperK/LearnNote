### Command
1. pwd 
 -----print working directory
2. cd 
 -----change directory
3. ls  
 -----list directory contents
 - a Include directory entries whose names begin with a dot(.). 
 - l list in long format
 - d directory are listed as plain files(not searched recursively)
 - h human format
 - i for each file, print the file`s file serial number (inode number)
4. mkdir 
 -----make directories
 - p directories are created recursively
5. rmdir 
 -----remove empty directories
6. rm
 -----remove directory entries 
 - r --recursive remove directories and their contents recursively
 - f --force ignore non-existent files and arguments, never prompt 
7. cp [source_file] [target_file] 
 -----copy files and directories
 - r --recursive copy directories recursively
 - p same as --preserve=mode,ownership,timestamps
 --preserve[=ALTER_LIST] preserve the specified attributes
 - d same as --preserve=links
 - a same as -dr --preserve=all
8. mv [source_file] [target_file]
 -----move (rename) files
9. ln [source_file] [target_link_name] 
 -----make links between files, use abs. path
 - s --symbolic make symbolic links instead of hard links
10. locate [pattern]
  -----find files by name   
  - database path: /var/lib/mlocate
  - updatedb  update database  
11. whereis
  -----locate the binary, source, and manual page files for a command
  - b search only
  - m just find location of documentation
12. which 
  -----shows the full path of (shell) commands
13. find [boundary] [condition]
  ----- search for files in a directory hierarchy
  - wildcard 
  - name find by file name
  - iname not case sensitive
  - user find by files owner
  - nouser find files without owner
  - atime find by access time of files
  - ctime find by change time of files
  - mtime find by modify time of files
    - -10 less 10 days
    - 10  equal 10 days
    - +10 greater than 10 days ago
  - size find by file size
    - -25k less 25KB -25M less 25MB
    - 25k  equal 25KB 25M equal 25MB
    - +25k  greater than 25KB
  - inum  find by file inode
  - a and
  - o or
  - exec ls -lh {} \;
14. grep [options] PATTERN [file]  
  ------ include matching
  - i --ignore-case Ignore case distinctions in both the PATTERN and the input files 
  - v --invert-match Invert the sense of matching, to select non-matching lines
15. man [section_number] command
  - f --whatis equivalent to whatis. Display a short description from the manual page
  - k --apropos equivalent apropos. Search the short manual page descriptions for keywords and display any matches.    
16. help
  ----- Display helpful information about builtin commands.
  e.g. help cd
17. info [command]
  - Enter next line
  - u     up node 
  - n     next node
  - p     previous node
  - q     quit 
*******************UNIMPORTANT*****************************
18. zip [compressed file name] [source file]              *
  - r support directory                                   *
19. unzip [compressed file name] [-d directory]           *
20. gzip [source file]                                    *
  - r compressed content of directory                     *
21. gunzip                                                *
  - r unzip the content of directory                      *
22. bzip2 [source file]  unsupport directory              *
  - k keep the source file                                *
23. bunzip2 -d [compressed file]                          *
*********************END***********************************
24. tar [archive_name] [source name]
  - x --extract     Extract files from an archive
  - v --verbose     Verbosely list files processed
  - f --file=ARCHIVE    Use archive file or device ARCHIVE
  - t --list        List the contents of an archive
  - c --create      Create a new archive
  - z --gzip        Filter the archive through zip
  - j --bzip2       Filter the archive through bzip2
  - C --directory=DIR   Change to directory DIR
25. shutdown [option] time 
  - h poweroff halt (init 0)
  - r reboot (init 6)
  - c cancle the last shutdown command
26. runlevel 
  ----- show runlevel
  - 0 halt
  - 1 single user
  - 2 multiuser, without NFS
  - 3 full multiuser mode
  - 4 unused
  - 5 Xll
  - 6 reboot
27. logout
  ----- Log out
28. mount -t type device dir 
  -----The mount command serves to attach the filesystem found on some device to the big file tree.
  dir: the pathname dir refers to the root of the filesystem on device
  - a Mount all filesystems(of the given types) mentioned in /etc/fstab
29. umount [mount_point]
  -----Detaches the file system mentioned from the file hierarchy.
  ---A file system is specified by giving the directory where it has been mounted.
30. fdisk -l 
  -----List the partition tables for the specified devices and then exit
31. w
  -----Show who is logged on and what they are doing
32. who
  -----Show who is logged on 
33. last
  -----Show listing of last logged in users
  - read /var/log/wtmp
34. lastlog
  -----Reports the most recent login of all users or of a given user
35. echo
  -----Display a line of text(echo string to stdout)
  - e '\e[1;31m\e[0m'
36. history [option] [history_file]
  ----- default save 1000 # /etc/profile HISTSIZE=1000
  - c empty the history
  - w Write the history command in the cache to the file # ~/.bash_history
  - !n repeat execute the nth history command
  - !! repeat execute the last history command
  - !str repeat execute the last command beginning with this string
37. wc [option] [FILE]
  ----- count line word byte of FILE, with no FILE or when FILE is - , read stdin
  - c count byte of file
  - w count word of file
  - l count line of file
38. netstate
  -----Print network connections, routing tables, interface statistics, masquerade connections,, and multicast memberships
  - a
  - n
  - ESTABLISHED


### File Type
1. directory d---------
2. file ----------
3. link file l---------

### Shortcuts
1. Ctrl+l Clear screen
2. Ctrl+c Forced to terminate the current command
3. Ctrl+a Move the cursor to the beginning of the line
4. Ctrl+e Move the cursor to the end of the line
5. Ctrl+u Remove everything from the cursor to the beginning of the line
6. Ctrl+z Executed in background
7. Ctrl+r Search in the history command that has been executed



### Tips
1. cd - go to the last directory
2. rm -r directory/* remove files or directories of the directory
3. ll equivalent ls -l
4. hard link 
   - just for file
   - can not cross-device
   - same inode
5. soft link 
   - source file need absolute path
   - different inode
6. active wifi nmtui


### General Directories
1. /bin /sbin /usr/bin /usr/sbin 	storage system command
2. /boot	directory of start system
3. /dev		storage device files
4. /etc		storage configure files
5. /home	home of general users
6. /lib		storage system library files
7. /mnt		directory of mount
8. /media	directory of mount
9. /root	home of root user
10. /tmp	temporary directory
11. /proc	mount point of RAM
12. /sys	mount point of RAM
13. /usr	storage software resources
14. /var	documentation of system2. /boot	directory of start system
3. /dev		storage device files
4. /etc		storage configure files
5. /home	home of general users
6. /lib		storage system library files
7. /mnt		directory of mount
8. /media	directory of mount
9. /root	home of root user
10. /tmp	temporary directory
11. /proc	mount point of RAM
12. /sys	mount point of RAM
13. /usr	storage software resources
14. /var	documentation of system

### Shell
config_file: /etc/shells
how_exit: command: exit
how_run: 1. chmod 755 hello.sh | ./hello.sh
         2. bash hello.sh
alias: 1. alias rm='rm -i' # temporarily effective
       2. vim ~/.bashrc  | source ~/.bashrc  # permanent and effective
       3. unalias [alias]  # remove alias
command priority: 1. Commands executed with absolute or relative paths
                  2. Alias
                  3. Shell internal command
                  4. Search the path according to the command defined by $PATH and execute the first search command


### Output redirection

1. stdin fd:0
   stdout fd:1
   stderr fd:2

2. ifconfig &>test.log # Export stdout and stderr to test.log as a pattern that overwrites the original file
3. ifconfig &>>test.log # Export stdout and stderr to test.log as a pattern that appends the original file
4. ifconfig >>test_stdout.log 2>>test_stderr.log # Append stdout to test_stdout.log and stderr to test_stderr.log
5. ls &>/dev/null
6. wc < file
7. wc << end


### Multi-command execution
1. ; command1 ; command2    # Multiple commands are executed sequentially
2. && command1 && command2  # When command 1 is executed correctly, command 2 is executed (need to return double True)
3. || command1 || command2  # When command 1 fails to be executed, command 2 is executed (need to return 1 True and 1 False)
4. | ll /dev | less  # Use the stdout of the first command as the stdin of the second command

### Wildcard
1. *
2. ?
3. []
4. [-]
5. [^]


### The meaning of special characters in bash
1. ''   In single quotes, all special symbos have no special meaning
2. ""   In quotes, all special symbols have no special meaning (exclude '$' '`' '\')
3. ``   Same as $()
4. $()  Call command of system
5. #    Notes beginning with hash
6. $    Get the value of the variable
7. \    Escape character(Special symbols following backslash behind have no special meaning)
