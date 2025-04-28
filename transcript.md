Hello! My name is Aleksandr. 
Today we will learn about the basic Unix commands - tools that will allow you to effectively manage files, 
directories and processes on the command line. These commands are the foundation for working in Unix-like systems, 
and knowing them will greatly simplify your work.

Let's start with the ls command.
This command shows a list of files and directories in the current directory.
Just type:

$ ls
You will see a list of files in current directory. 
But if you want to get more detailed information - access rights, owner, size and modification date - use the key:

$ ls -l

Also, to see hidden files that start with a dot, add the key: 

$ ls -a

You can combine keys:

$ ls -la
You will see a list of  all files in current directory

Let's move on to the (cd - command).

$ cd Documents

The cd (change directory) command is used to navigate the file system in the terminal. 
Unlike ls, it does not display the contents of directories, but changes the current working directory.
Option for using the command to back previous directory:

$ cd ..
And if use only cd / cd ~ command you go to home directory

To quickly check where you are, run the pwd command - (Print Working Directory). It will print the full path to the current directory.

$ pwd

Now let's talk about copying files. The cp (copy) command is used to copy. 
For example, to copy the file.txt file to the Backup folder

$ cp file.txt Backup/

If you need to copy the entire directory along with its files, use the -r switch (recursively)

$ cp -r Folder1 Folder2/

Moving and renaming files - mv command.

To rename the file oldname.txt to newname.txt
Also mv can move files to other directories.

$ mv oldname.txt newname.txt
and try move to file
mv newname.txt Folder/

Deleting files and directories is done by the rm command. To delete a file, use:

$ rm temp.txt

To delete a directory with all files inside, use the -r switch.

$ rm -r OldFolder
The rm command permanently deletes data!

Creating new directories is the mkdir command.

$ mkdir nameFolder

To remove an empty directory, use rmdir

$ rmdir OldFolder

Viewing File Contents - (cat Command)
To display the contents of a file in the terminal, run:

$ cat file.txt

If the file is very large you cant see only part information, 
it is better to use the less or more commands, which allow you to view it page by page:

$ less largefile.log

You can navigate the file by pressing the arrows or the Page Up/Page Down keys. To exit, press q.

Creating new files is the (touch - command).
It creates an empty file or updates its timestamp:

$ touch newfile.txt

Search for files (find - command).
To find all files with the .txt extension in the current directory and its subdirectories, use:

$ find . -name "*.txt"
Here . denotes the current directory.

Search inside files (grep - command).
If you want to find lines containing specific text, such as file.txt, write:

$ grep "find text" file.txt
You can also search the entire catalog:

$ grep -r "error" .

Working with processes  (ps — command).
To see all running processes, use:

$ ps aux
You can see PID processes.
If you need to kill a process, find its PID (process number) and execute kill:

$ kill processPID

If the process is not finished, use kill -9:

$ kill  -9 processPID

Output of text or variables (echo — command).

$ echo "Hello, Unix!"
This is useful for displaying messages or variable values.

To get help on any command, use the man command. For example, to see what the ls command can do, run:

$ man ls
This will open a detailed guide on how to use the command.

This concludes my overview of the basic Unix commands. 
Knowing these tools is the key to effective work in the command line. 
Practice, experiment, and don't be afraid to learn new commands. 
In the future, they will become a natural part of your work. 
Thanks for your attention! Good luck in mastering Unix!
