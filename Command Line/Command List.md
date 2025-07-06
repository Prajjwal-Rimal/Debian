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
	$ cd home/janedoe/pictures
	
	now we have a folder in the pictures tab called images we can simply type
	$ cd images
	and we will be in that folder

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
	$ -R

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

	$touch newtouchtestfile
	This creates a new blank file
</li>
<li>

	$touch newtouchtestfile
	Doing this on an existing file updates its time stamp
</li>
</ul>
</li>

<li>
File

	$file <filename>
	this gives us the real type of a file
</li>

<li>
Cat

	$cat <filename>
	shows the content of the file

	$cat <filename><filename>
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
	displays the list of all the commands theat have been used

	$ ctrl + R 
	opens a reverse search in which you can search for commands from the history.

	$ clear
	 this clears the terminal screen useful when it feels cluttered. 	
</li>
</ol>
