<center> <h3>Command Line </h3></center>
## Shell
<ol>
<li>takes commands form the keyboard and sends them to the os</li>
<li>Terminal / console are just programs that launch the shell</li>
<li>bash => Bourne Again shell</li>
<li>other shells also available such as ksh, zsh, tsch, etc</li>
</ol>

## Directories
<ol>
<li>Every thing in Linux is a file</li>
<li>Hierarchical directory tree to store files</li>
<li>First directory in the file system is known as root</li>
<li> The root folder has many folder and files in which you can store more folder and files</li>
<li>The location to these directories and files is known as a path </li>
<li> We can change the directories when we want to by using cd </li>
</ol>

## Paths
<ol>
Two ways to specify a path:

<ol>
<li>Absolute => this is the path from the root directory. Starting with a slash (/) means starting from a root directory</li>
	/home/janedoe/desktop
<li>Relative => path from where you currently are in the file system. If present in a location and need to navigate inside a file or directory of that location then specification of the entire path is not necessary</li>
	suppose we are in the /home/janedoe/desktop and we want to navigate to a document named xyz 
	we can simply type xyz/ 
</ol>
</ol>

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
</ol>