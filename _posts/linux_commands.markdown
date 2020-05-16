---
layout: post
title:  "Basic linux commands for beginner"
date:   2016-08-01 21:03:36 +0530
categories: Shell Vim
---

I created this document for my colleagues so that they can switch from windows to Ubuntu quickly. Got this from different sources.

I think this will be useful for others also. So, I am publishing it here.

* ls : listing content of the current directory
* ls -l : l for long listing! (-rwxrw-r-- 1 ee51ab beng95 2450 Sept29 11:52 file1)
* ls -a : list content with hidden files
* mkdir <dir_name> : create directory (folder)
* cd <dir_path or dir_name>: change directory
* cd . : change to current directory (.(dot) is represented for current directory)
* cd .. : change to parent directory (.. represents parent directory)
* pwd : print working directory (current directory path)
* cd or cd ~ : changes to home directory (~ represents to home directory)
* cp <src_file_path> <dest_file_path> : copy file
* mv <src_file_path> <dest_file_path> : move file (if src = dest, it will rename the file)
* rm <file_path> : remove file
* rmdir <dir_path> : remove directory (directory should be empty)
* clear : clear screen (Ctrl + l)
* cat <file_name>  : display the content of the file
* less : writes the contents of a file onto the screen a page at a time (q for quir, space_bar for next page)
* head <file_name> : writes first 10 lines of file
* head -5 <file_name> : writes first 5 lines of the file
* tail <file_name> : writes last 10 lines of the file
* tail -15 <file_name> : writes last 15 lines of the file
* grep “string” <file_name> : prints each line containing the given string in the file -i : to ignore case distinctions, -v : to ignore lines containg string,-n : print with line number,-c : print total count of matched lines
* can use -ivc also
* wc -w <file_name> : prints number of words in the file
* wc -l <file_name> : prints number of lines in the file
* who : logged in users
* who | wc -l : no. of users logged in
* whatis <command> : one line desc of command
* man <command> : manual of command
* * ?


* cal : displays a calendar
* date : print or set the system date and time
* find <source> -name <file_name> : search for files in a directory hierarchy
* locate <file_name>: print the file with path.
* whereis : print instances of a command
* apt-get : Search for and install software packages (Debian/Ubuntu)
* free : Display memory usage in kelobytes(-m : to see the memory in MB - megabytes)
* history : To see the Previous commands
* hostname : Print or set system name
* ifconfig : Configure a network interface
* passwd  : Modify a user password
* su : switch one user to another

# To reduce and adjust brightness in ubuntu

1. Goto     :  ```sudo vi /etc/default/grub```
2. Change:   
```
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash" acpi_backlight=vendor“
GRUB_CMDLINE_LINUX="acpi_osi=Linux"
```
3. Update :  ``` sudo update-grub```



# Set / change / reset the MySQL root password on Ubuntu Linux. 
Enter the following lines in your terminal.

1. Stop the MySQL Server.
```sudo /etc/init.d/mysql stop```
2. Start the mysqld configuration.
```sudo mysqld --skip-grant-tables &```
3. Login to MySQL as root.
```mysql -u root mysql```
4. Replace YOURNEWPASSWORD with your new password!
```UPDATE user SET Password=PASSWORD('YOURNEWPASSWORD') WHERE User='root'; FLUSH PRIVILEGES; exit;```


File to see the memory info :- /proc/meminfo memory information
Neatbeans Cache file path : ~/.netbeans/7.0/var/cache

# Using vim editor
To install       ``` apt-get install vim```
To open(new or old)     ```vim <file_name> ```
To insert           ```i - takes to insert mode.```
press **Esc** to return to **view** mode

```
:w - to save file
:q - to quit file
x - to delete a character   
ndd - to cut or del ‘n’ lines (e.g press 10dd to remove 10 lines )
nyy - to copy ‘n’ lines    
p - to paste
u - to undo
```

query to find MySql Log File path : ```select @@general_log_file;```
query to enable Log File : ```set GLOBAL general_log = ‘ON’;```
Mysql Log File path in ubuntu :- ``` /var/lib/mysql/vaibhav-laptop.log```
