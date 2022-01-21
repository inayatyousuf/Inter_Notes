

   Name Inayat Yousuf.
   Task: Linux Operating System and its commands.



Linux is an open-source operating system like other operating systems such as Microsoft Windows, the Linux was developed by Linus Torvalds in 1991.

Some commands we use in our daily projects.

1. ls: The “ls” command is used to display a list of content of a directory.
 
2. cd: (Change Directory) command is used to change the current working directory ( i.e.,      in which the current user is working)
Eg cd Desktop. Changes the present directory to the Desktop directory.

3. Pwd: The pwd (print working directory) command is used to display the location of the current working directory. Eg if we are in the Downloads directory if we enter pwd it shows us the absolute path up to the Downloads directory.

4. Mkdir: The mkdir command is used to create a new directory under any directory.
Eg mkdir myPhotos   it will create a directory(folder) of name myPhotos.

5. rmdir: The rmdir command is used to delete a directory.
Eg Above we create a directory named as myPhotos, we can remove this directory by simply typing the command like rmdir myPhotos and hit enter.

6. touch: The touch command is used to create empty files. We can create multiple empty files by executing it once.
Eg touch myFileName.txt   this command will create an empty file of extension txt.
We can create more files with a single command like touch file1.txt file2.txt file3.txt,
 Here we create three files with different file names.
If we type ls command it shows these files but we can also make hidden files which is will be not visible to the ls command. Like we need to just add a dot(.) in front of  the file name eg  touch .myHiddenFile.txt 
Now this file will not be shown if we type simple ls.
To access the hidden files we need to type command ls -a

7. rm: The rm command is used to remove a file. Works the same as the rmdir.
  Eg rm file1.txt

8. cp: The cp command is used to copy a file or directory. Like if we want the above file named file2.txt 

9. mv: The mv command is used to move a file or a directory from one location to another location. This command works somehow like copy and remove. It copy the file and also removes it.  Eg  rm file2.txt

10. Ls -R: This command is used to show files of the directory and if the directory has its subdirectory it also shows the subdirectory files. Which simple ls does not show.
R stands for recursive.

11. clear: this command is used to clear the terminal. Eg type clear and hit enter terminal will clear as soon as we hit enter.

12. history: this command is used to show all commands which we enter till now.

13. echo:  it is used to print whatever we pass it. Eg
echo hello world                 – it will print hello world in the terminal.
OR
echo — The "echo" command helps us move some data, usually text into a file. For example, if you want to create a new text file or add to an already made text file, you just need to type in, “echo hello, my name is inayat >> new.txt”. You do not need to separate the spaces by using the backward slash here because we put in two triangular brackets when we finish what we need to write.

14. Printf:  it is the same as echo but whatever we have to pass it put that in quotes, it also prints the string into the same line not in the new line for that we have to pass “\n”
Eg printf “hello world”    prints hello world but with no newline.
Printf “hello world\n”     prints hello world with a new line.

15. top:  It is used to show those processes which consume the highest resources. Which consumes large amount of memory.
 Eg type top and hit enter.

16. ps:  it is used to list all processes which are running. 
Eg type ps and hit enter.

17. ps -a: it also lists the processes but the difference is that it also lists those which are running in the background. 
 Eg ps -a and hit enter

18. Kill: kill is used to kill or closes the processes. We can kill processes by simply passing it the PID(process ID) which we can get by using top command
Eg kill PID    or   kill 2345
19.head: The head command is used to display the content of a file. It displays the first 10 lines of a file. 
Eg head file1.txt  if the file has 100 lines it will print the first 10 lines.
If we want to print only 5 lines not 10 which is by default. Type the command with -n and number of lines like.
Eg head -n 5 file1.txt       this will change the default behavior of head. 

20. tail: The tail command is similar to the head command. The difference between both commands is that it displays the last ten lines of the file content.
Eg tail file1.txt    this prints the last 10 lines. 
We can also change the default behavior of the tail. We can also print how many lines we want like in the head command.

21. su: The su command provides administrative access to another user. In other words, it allows access of the Linux shell to another user. 
Eg su inayat   provide administrative access to inayat.

22. id: The id command is used to display the user ID (UID) and group ID (GID).
Eg type id and hit enter it will give you uid=1441(admin) gid=1441(admin) groups=1441(admin),34(sudo)

24. cd ..  This command is used to go back one step.

25. passwd: The passwd command is used to create and change the password for a user.
Eg sudo passwd <username>  to change the password we need root access so we write sudo.

26. locate: The locate command is used to locate a file in a Linux system, just like the search command in Windows. This command is useful when you don't know where a file is saved or the actual name of the file. Using the -i argument with the command helps to ignore the case (it doesn't matter if it is uppercase or lowercase). So, if you want a file that has the word “hello”, it gives the list of all the files in your Linux system containing the word "hello" when you type in “locate -i hello”. If you remember two words, you can separate them using an asterisk (*). For example, to locate a file containing the words "hello" and "this", you can use the command “locate -i *hello*this”.
Eg locate file1.txt     this will give us the absolute path up to where the file exists.

27. cat: Use the cat command to display the contents of a file. It is usually used to easily view programs.
Eg cate file1.txt   it will display the content of the file whatever is in the file.

28. df: Use the df command to see the available disk space in each of the partitions in your system. You can just type in df in the command line and you can see each mounted partition and their used/available space in % and in KBs. If you want it shown in megabytes, you can use the command “df -m”.

29. du: Use du to know the disk usage of a file in your system. If you want to know the disk usage for a particular folder or file in Linux, you can type in the command df and the name of the folder or file. 
Eg du Documents  

30. tar: Use tar to work with tarballs (or files compressed in a tarball archive) in the Linux command line. It has a long list of uses. It can be used to compress and uncompress different types of tar archives like .tar, .tar.gz, .tar.bz2, etc. It works on the basis of the arguments given to it. For example, "tar -cvf" for creating a .tar archive, -xvf to untar a tar archive, -tvf to list the contents of the archive, etc.
Eg tar -xvf filename.tar   used to untar the tar file.

31. uname: Use uname to show the information about the system your Linux distro is running. Using the command “uname -a” prints most of the information about the system. This prints the kernel release date, version, processor type, etc.

32. hostname: Use hostname to know your name in your host or network. Basically, it displays your hostname and IP address. Just typing “hostname” gives the output. Typing in “hostname -I” gives you your IP address in your network.


