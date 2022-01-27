Name Inayat Yousuf.
Task: Linux File System and some advanced commands.


Linux File System
1. / (Root): Primary hierarchy root and root directory of the entire file system hierarchy.
Every single file and directory starts from the root directory
The only root user has the right to write under this directory
/root is the root user’s home directory, which is not the same as /

2. /bin : Essential command binaries that need to be available in single-user mode; for all   users, e.g., cat, ls, cp. 
Contains binary executables.
Common linux commands you need to use in single-user modes are located under this directory.
Commands used by all the users of the system are located here e.g. ps, ls, ping, grep, cp etc.

3. /boot : Boot loader files, e.g., kernels, initrd. 
Kernel initrd, vmlinux, grub files are located under /boot
Example: initrd.img-2.6.32-24-generic, vmlinuz-2.6.32-24-generic

4. /dev : Essential device files, e.g., /dev/null. 
These include terminal devices, usb, or any device attached to the system.
Example: /dev/tty1, /dev/usbmon0.

5. /etc : Host-specific system-wide configuration files.
Contains configuration files required by all programs.
This also contains startup and shutdown shell scripts used to start/stop individual programs.
Example: /etc/resolv.conf, /etc/logrotate.conf.

6. /home : Users’ home directories, containing saved files, personal settings, etc.
Home directories for all users to store their personal files.
example: /home/pictures, /home/Documents

7. /lib : Libraries essential for the binaries in /bin/ and /sbin/.
Library filenames are either ld* or lib*.so.*
Example: ld-2.11.1.so, libncurses.so.5.7

8. /media : Mount points for removable media such as CD-ROMs (appeared in FHS-2.3).
Temporary mount directory for removable devices.
Examples, /media/cdrom for CD-ROM; /media/floppy for floppy drives; /media/cdrecorder for CD writer

9. /mnt : Temporarily mounted filesystems.
Temporary mount directory where system admins can mount filesystems.

10. /opt : Optional application software packages.
Contains add-on applications from individual vendors.
Add-on applications should be installed under either /opt/ or /opt/ sub-directory.

11. /sbin : Essential system binaries, e.g., fsck, init, route.
Just like /bin, /sbin also contains binary executables.
The Linux commands located under this directory are used typically by the system administrator, for system maintenance purposes.
Example: iptables, reboot, fdisk, ifconfig, swapon

12. /srv : Site-specific data served by this system, such as data and scripts for web servers, data offered by FTP servers, and repositories for version control systems.
srv stands for service.
Contains server specific services related data.
Example, /srv/cvs contains CVS related data.

13. /tmp : Temporary files. Often not preserved between system reboots, and may be severely size restricted.
Directory that contains temporary files created by system and users.
Files under this directory are deleted when system is rebooted.

14. /usr : Secondary hierarchy for read-only user data; contains the majority of (multi-)user utilities and applications. 
Contains binaries, libraries, documentation, and source-code for second level programs.
/usr/bin contains binary files for user programs. If you can’t find a user binary under /bin, look under /usr/bin. For example: at, awk, cc, less, scp
/usr/sbin contains binary files for system administrators. If you can’t find a system binary under /sbin, look under /usr/sbin. For example: atd, cron, sshd, useradd, userdel
/usr/lib contains libraries for /usr/bin and /usr/sbin
/usr/local contains users programs that you install from source. For example, when you install apache from source, it goes under /usr/local/apache2
/usr/src holds the Linux kernel sources, header-files and documentation.


15. /proc : Virtual filesystem providing process and kernel information as files. In Linux, corresponds to a procfs mount. Generally automatically generated and populated by the system, on the fly.
Contains information about system process.
This is a pseudo filesystem contains information about running process. For example: /proc/{pid} directory contains information about the process with that particular pid.
This is a virtual filesystem with text information about system resources. For example: /proc/uptime


Some More Advanced Commands In Linux.

1. grep:  The grep filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern. The pattern that is searched in the file is referred to as the regular expression (grep stands for a global search for regular expression and print out).

Eg grep -i "inayat" file1.txt — The -i option enables to search for a string case-insensitively in the given file. It matches the words like “INAYAT”, “Inayat”, “InaYat”.

We can also display the count of number of matches : We can find the number of lines that matches the given string/pattern 
 
Eg grep -c "inayat" geekfile.txt     output will be a number.

Also used to display the file names that matches the pattern: We can just display the files that contains the given string/pattern. 
 
$grep -l "inayat" *     star is used for all files globally.
We can also pass files instead of star, like this $grep -l "inayat” f1.txt f2.txt f3.xt f4.txt

2. sed: SED command in UNIX stands for stream editor and it can perform lots of functions on file like searching, find and replace, insertion or deletion. Though most common use of SED command in UNIX is for substitution or for find and replace. By using SED you can edit files even without opening them, which is much quicker way to find and replace something in file, than first opening that file in VI Editor and then changing it.
SED is a powerful text stream editor. Can do insertion, deletion, search and replace(substitution).
SED command in unix supports regular expression which allows it perform complex pattern matching.

Replacing or substituting string : Sed command is mostly used to replace the text in a file. The below simple sed command replaces the word “unix” with “linux” in the file.
$sed 's/unix/linux/' file1.txt
Here the “s” specifies the substitution operation. The “/” are delimiters. The “unix” is the search pattern and the “linux” is the replacement string. By default, the sed command replaces the first occurrence of the pattern in each line and it won’t replace the second, third…occurrence in the line.
Replacing the nth occurrence of a pattern in a line : Use the /1, /2 etc flags to replace the first, second occurrence of a pattern in a line. The below command replaces the second occurrence of the word “unix” with “linux” in a line.
$sed 's/unix/linux/2' file1.txt
Replacing all the occurrences of the pattern in a line: The substitute flag /g (global replacement) specifies the sed command to replace all the occurrences of the string in the line.
$sed 's/unix/linux/g' file1.txt

3. uniq: The uniq command in Linux is a command-line utility that reports or filters out the repeated lines in a file. 
In simple words, uniq is the tool that helps to detect the adjacent duplicate lines and also deletes the duplicate lines.
Eg uniq kt.txt

4. service: The service command can be used to manage services on your computer. It’s quite versatile in a way that you can start, stop, and restart a service as well as print details and a list of all available services on your computer. To print a list, use the following command:
       service --status-all
To print a detailed status of a particular service, use:
       service <service_name> status  eg service bluetooth status
As you can see, the service is currently running. That means we can stop or restart it. To restart it, type:
       sudo service bluetooth restart


5. wget: we can use the wget command if you want to download a file from a server to your local computer. The command will 
attempt to download the resource you supplied and it will automatically detect the file extension. For example: If you point it to a website, it’ll download an HTML file. 
Eg wget https://google.com

6. find: Search for files in the given directory, hierarchically starting at the parent directory and moving to sub-directories.
Eg find -name *.sh
The `-name‘ option makes the search case sensitive. You can use the `-iname‘ option to find something regardless of case. (* is a wildcard and searches all the file having extension ‘.sh‘ you can use filename or a part of file name to customise the output).

7. man: The ‘man‘ is the system’s manual pager. Man provides online documentation for all the possible options with a command and its usages. Almost all the command comes with their corresponding manual pages. For example,
Eg man ls — it gives the manual of ls command and press q to exit from manual.

8. Whereis: The ‘whereis‘ command is used to locate the Binary, Sources and Manual Pages of the command. For example, to locate the Binary, Sources and Manual Pages of the command ‘ls‘ 
Eg whereis ls

9. alias: it is a built in shell command that lets you assign name for a long command or frequently used command.
If you use ‘ls -l‘ command frequently, which includes 5 characters including space. Hence  you can create an alias for this to ‘l‘.
Eg  alias l='ls -l' — next time you need to type only l instead of this long command
You can later unalias the command like this unalias l
10. cmp: compare two files of any type and writes the results to the standard output. By default, ‘cmp‘ Returns 0 if the files are the same; if they differ, the byte and line number at which the first difference occurred is reported.
Eg cat file1.txt 
Hi My name is Inayat
Cat file2.txt
Hello, I live in shopian.
Now, let’s compare two files and see output of the command.
cmp file1.txt file2.txt 
Output is – file1.txt file2.txt differ: byte number, line number
11. whoami: In Linux, a whoami command is used to print the currently logged-in username into your Linux system. If you are logged in as a root using sudo command “whoami” command return root as the current user.
Eg whoami

Viewing Ownership and Permissions
The most common way to view the permissions of a file is to use ls with the long listing option, e.g. ls -l myfile. If you want to view the permissions of all of the files in your current directory, run the command without an argument, like this:

ls -l

File Type

In Linux, there are two basic types of files: normal and special. The file type is indicated by the first character of the mode of a file–in this guide, we refer to this as the file type field.

Normal files can be identified by files with a hyphen (-) in their file type fields. Normal files are just plain files that can contain data. They are called normal, or regular, files to distinguish them from special files.

Special files can be identified by files that have a non-hyphen character, such as a letter, in their file type fields, and are handled by the OS differently than normal files.

In each triad, read, write, and execute permissions are represented in the following way:

    Read: Indicated by an r in the first position
    Write: Indicated by a w in the second position
    Execute: Indicated by an x in the third position. In some special cases, there may be a different character here

A hyphen (-) in the place of one of these characters indicates that the respective permission is not available for the respective class. For example, if the group triad for a file is r--, the file is “read-only” to the group that is associated with the file.

The umask command defines the default permissions for newly created files based on the "base" permissions set defined for files and directories. umask 000
Directories have a base permissions set of 777, or read, write, and execute permissions for all users.


   







