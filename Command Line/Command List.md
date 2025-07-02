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