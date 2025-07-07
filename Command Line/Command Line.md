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
</ol>

## Touch
<ol>
<li>allows the user to create new empty files</li>
<li> allows the user to change existing timestamp on the files, it does not delete or modify the content of the file.</li>
</ol>

## File
in Linux a file can be named whatever we want to name it and the extension doesn't matter. Extensions are just the part of the file name and they do not define the file type. The file command checks the real file type.

## Cat 
<ol>
<li>this command is used to display the file contents</li>
<li>short for concatenate</li>
<li>can also combine the output of multiple files</li> 
</ol>

## Less
<ol>
<li>less is more </li>
<li>the command more also does a similar thing </li>
<li>the text is displayes ina page manner</li>
<li>keyboard commands can be used to navigate the file</li>
<ul>
<li>q: quit and go back to the shell </li>
<li>arrow to navigate  </li>
<li>g: moves to the beginning of the file </li>
<li>G: moves to the end of the file </li>
<li>/search: search for specific text inside the document prefacing the word you wanna search with / </li>
<li>h: to get help on how to use less while in less </li>
</ul>
</ol>


## History
<ol>
<li>We have a history command that allows to look through our previously typed commands.
<li>Arrow keys can also be used to navigate through the history. 
<li>Similarly another history short cut is ctrl + R is the reverse search command. 
<li>We can also clear our display with the clear Command. 
<li>In the command line we have auto tab completion which is helpful when we are typing the name of a file, directory, command etc. 
</ol>


## Copy
<ol>
<li> it is much like copy pasting files in other os the only difference this is done by the terminal  </li>
<li> $ cp <filename> < path to copy at >
<li> we can also use wildcards  </li>
<li> wildcard is a character that can be substituted for a pattern based selection  </li>
<ul>
<li> * => matches any number of characters  </li>
<li> ? matches a single character  </li>
<li> [] matches any one character in the bracket  </li>
</ul>
<li> cp *.jpg /home/user/Pictures This command copies all the jpg files to the given path </li>
<li> -r flag is used to copy directories and their content  </li>
</ul>
<li> if we copy a file to a directory that has a same filename, THE FILE WILL BE OVERWRITTEN  </li>
<li> -i flag gives an interactive prompt before overwriting the file </li>
<li> -v flag shows what is being copied </li>
</ol>

## Move 
<ol>
<li> used for moving files and renaming them  </li>
<li> similar to cp command in terms of flags and functionality </li>
<li> we can rename files </li>
<li> we can move files to a different directory </li>
<li> we can move more than one file </li>
<li> we can rename directories as well </li>
<li> like copy if we move a file or a directory it will overwrite anything in the same directory so we can use the -i to prompt overwrite it </li>
<li> we can also create a backup file and it will rename the old version with a  ~ </li>
</ol>
