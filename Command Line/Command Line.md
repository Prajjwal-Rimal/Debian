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

## List Directories (ls)
<ol>
<li>
This is used to list the directories and files in the working directory. We can also specify the path to list the directories of.
</li>

	ls home/janedoe

<li>
Not all files in a directory are visible some are hidden.
</li>

	viewed by passing the -a flag to the ls.

<li>
To see a detailed list of file use a long flag
</li>

	ls -l

The  flags are options to the command. We can also combine the flags to execute them in the order they are opted.

	ls -la or ls -al