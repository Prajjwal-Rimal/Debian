## Commands
<ol>
<li>echo [text] => prints the typed text to the display</li>

	$ echo hello world
	hello world

<li>date => displays the current time, timezone, and date</li>
	
	$ date
	Mon Jul  1 02:01:49 AM +0630 2025

<li>whoami => display the username </li>
	
	$ whoami
	janedoe

<li>pwd => print working directory, shows which directory you are in</li>
	
	$ pwd
	/home/janedoe

<li>cd => change directory, used to change directory when needed</li>
	
	lets say we are in document and we want to go to pictures
	$ cd /home/janedoe/pictures
	
	now we have a folder in the pictures tab called images we can simply type
	$ cd images
	and we will be in that folder, only works if we are already inside the parent directory

there are few shortcuts to help us from using absolute and relative paths constantly:
<ul>
<li>cd . (current directory) this is the directory we are currently working in
</li>
<li>
cd .. (Parent directory) this take us to a directory one step above ours
</li>
<li>
cd ~ goes back to the home directory
</li>
<li>
cd - takes to the previous directory we were at
</li>
<li>cd with no flags takes us to the home directory same as cd ~

	$ cd /home/janedoe/Documents
	$ pwd
	/home/janedoe/Documents
	$ cd
	$ pwd
	/home/janedoe
</ul>

<li> List Directories (ls)
<ul>
<li>List all directories : ls</li>

	$ ls
	Documents  Downloads  Music

<li>List all directories including the hidden one's : ls -a</li>

	$ ls -a
	.  ..  .bashrc  .profile  Documents  Downloads  Music

<li>list all the details of the directories : ls -l</li>

	$ ls -l
	drwxr-xr-x 2 user user 4096 Jul 1 11:00 Documents

<li>List all the hidden directories and their details : ls -al / ls -la</li>

	$ ls -al
	$ ls -la
	drwxr-xr-x 20 user user 4096 Jun 30 20:00 ..
	-rw-r--r--  1 user user  220 Apr 15  2020 .bash_logout
	-rw-r--r--  1 user user 3771 Apr 15  2020 .bashrc
	-rw-r--r--  1 user user  807 Apr 15  2020 .profile
	-rw-r--r--  1 user user 1024 Jul 1 12:00 a.txt

<li>List all the files and directories including those that are in the sub directories : ls -R</li>

	THIS DOESN'T SHOW THE HIDDEN FILES BY DEFAULT 
	$ ls -R

	Documents  Downloads  Music  

	./Documents:
	a.txt  b.pdf

	./Downloads:
	a.txt  b.pdf

<li> List the directories in reverse order : ls -r</li>

	$ ls
	a.txt  b.txt  c.txt

	$ ls -r
	c.txt  b.txt  a.txt

<li>List the directories in the last modified order (newest to the oldest) : ls -t</li>

	$ ls -t
	a.txt c.txt d.txt b.txt
	newest first
</ul>

<li>
Touch

<ul>
<li>

	$ touch newtouchtestfile
	This creates a new blank file
</li>
<li>

	$ touch newtouchtestfile
	Doing this on an existing file updates its time stamp
</li>
</ul>
</li>

<li>
File

	$ file <filename>
	this gives us the real type of a file
</li>

<li>
Cat

	$ cat <filename>
	shows the content of the file

	$ cat <filename><filename>
	shows the content of two different files
</li>

<li>
Less
	
	$ less 'Command List.md'
	allows us to see our document in a paged manner
</li>


<li>
History

	$ history
	displays the list of all the commands that have been used

	$ ctrl + R 
	opens a reverse search in which you can search for commands from the history.

	$ clear
	 this clears the terminal screen useful when it feels cluttered. 	
</li>


<li>
Copy (cp)
<ul>
<li> Used to make copies of the file </li>

	$ cp file1.txt /home/janedoe/Documents
	copies the file to the specified directory

	$ cp *.txt /home/janedoe/Documents
	copies all .txt file to the specified path

	$ cp -r folder1/ /home/janedoe/Documents
	recursively copies a folder and all its contents to the specified path

	$ cp -i file1.txt /home/janedoe/Documents
	if we copy a file over to another directory where a file with the same name exits the system will prompt us before overwriting the file

</ul>
</li>


<li>
Move (mv)
<ul>
<li> used to move files and renaming them </li>

	$ mv oldfile newfile
	renames a file

	$ mv file /home/janedoe/Documents
	moves the file to the specified directory

	$ mv file1 file2 /home/janedoe/Documents
	moves multiple files to the specified directory

	$ mv directory1 directory2
	renames the directory

	$ mv -i directory1 directory2
	if we move a file or directory it will 	overwrite anything in the same directory if the directory exits, the -i flag prompts before 	overwriting anything
	basically moves directory 1 to directory 2 and if directory 2 exists then it shows a prompt to the user warning about this

	$ mv -b directory1 directory2
	makes a backup directory if the directory exists before overwriting and naming it with a ~

</ul>
</li>


<li>
Make Directory (mkdir)
<ul>
<li> Used to create a directory a directory or multiple one's if it doesn't exist </li>

	$ mkdir directory1 directory2
	creates two separate directories named directory1 and directory2

	$ mkdir -p a/b/c
	creates a directory and sub-directory at the same time with the  -p (parent flag), so basically a has a sub-directory named b and b has a sub-directory named c

</ul>
</li>


<li>
Remove (rm)
<ul>
<li> used to remove files and directories </li>

	$ rm a.txt
	deletes a file

	$ rm -f a.txt
	force delete a file without confirmation

	$ rm -i a.txt
	prompt confirmation before deleting the file

	$ rm -r directory
	recursively deletes a directory and its files / sub-directories

	$ rmdir directory
	deletes an empty directory

</ul>
</li>


<li>
Find
<ul>
<li> to find files and directories </li>

	$ find /home -name abc.txt
	Used to search for files and directories, starts at /home directory and looks for a file name with abc.txt.

	$ find /home -type d -name Fabc
	Finds directory named Fabc in the /home directory

	$ find /home -type f -name abc.txt
	This command only search for files in the /home directory
</ul>
</li>


<li>
Help
<ul>
<li> to learn how to use a bash command or to learn what flags a bash command has </li>

	$ help pwd

	pwd: pwd [-LP]
    Print the name of the current working directory.
    
	Options:
	-L print the value of $ PWD if it names the current working directory
	-P print the physical directory, without any symbolic links
	By default, `pwd' behaves as if `-L' were specified.
	Exit Status:
	Returns 0 unless an invalid option is given or the current directory cannot be read.
</ul>
</li>


<li>
Man
<ul>
<li> to see the manual of the command / programs </li>

	$ man mv
	opens manual for the move command
</ul>
</li>


<li>
Whatis
<ul>
<li> shows a brief description about the command </li>

	$ whatis ls
	ls (1)               - list directory contents

	$ whatis pwd
	pwd (1)              - print name of current/working directory
	
	$ whatis cat
	cat (1)              - concatenate files and print on the standard output

	$ whatis man
	man (1)              - an interface to the 	system reference manuals
	man (7)              - macros to format man 	pages

</ul>
</li>


<li>
Alias
<ul>
<li> to create a alias </li>
	
	$ alias ll='ls -la'

<li> to save the alias permanently save it to bashrc </li>
	
	$ vim ~/.bashrc

<li> to remove an alias </li>
	
	$ unalias ll

</ul>
</li>


<li>
Exit
<ul>
<li> to exit the terminal</li>

	$ exit

	$ logout if available

</ul>
</li>
</ol>
