## Environment (env)

1. When we type 
<br>
`$echo $Home to see the path to our home directory` or `$echo $USER to see who we are logged in as` 
<br> the system gains this information from environment variables


2. environment variables are key value pair stored by the OS

3. they define thing like
    * username: `$USER`
    * home directory: `$HOME`
    * current working directory: `$PWD`
    * search path for executable: `$PATH`
    * default shell: `$SHELL`
    * language settings: `$LANG` , etc.

4. `$env` shows us the current environment variables that we have set

5. environment variables have information that shell and other processes can use, make it easier to pass the same configuration to the system.

6.`$echo  $PATH`
<br>
PATH is a special environment variable that tells the shell where to look when you type a command. 

* If a program isn’t in one of the listed folders, the shell won’t find it — even if it exists on your system.
 * /usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
 * returns a list of path separated by colon
 * our system only looks at these directories when we type a command
<br>
<br>
7. sometimes when we download a program from the internet and we try to run it we receive an error that's cause the path has not been set in the system.
  * to solve this we first need to locate our directory where the program is present
  * and then edit our `~/.basrc` and then include the path in the system `export PATH=$PATH:<insert the folders path>` or
* echo 'export PATH=$PATH:<folder path> >> ~/.bashrc 

	* uses echo to write the line export PATH=$PATH:<folder path> into the file ~/.bashrc without deleting what’s already there (because of >>). 
	* In that line, PATH= sets the PATH variable to its current value plus the new folder <folder path>, separated by a colon : which divides folders in the PATH. 
	* Since the line is written with single quotes, the $PATH part is saved exactly as $PATH (not replaced immediately). 
	*  Later, when we open a new terminal or run the .bashrc file, the system replaces $PATH with the actual list of folders to update the search path permanently.


##
Summary:

echo prints to the screen, and when used with a command like echo $VAR it shows the value stored in that variable. env shows us the environment variables that tell us what settings our current system session is using. When we access an env variable, it pulls data from those variables. PATH is an important variable because it shows what folders the system will search when we type a command. If a folder isn’t in the PATH, we won’t see the command even if it’s installed. So we need to manually edit the ~/.bashrc file, which stores PATH and other settings. Updating .bashrc makes the change permanent.

