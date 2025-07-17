## Pipe and Tee
1. when we type a command like `ls -la` we see all the hidden files as the output
2. we have another method to see the output of this command by using the pipe method

		$ la -la /etc | less
	
	* ls -la /etc this command lists all the files and their details from the etc directory
	* `|` take the output of `ls -la /etc` and sends it to less 
	* less allows us to view files in a paged format
	* so basically we are viewing the output on a paged format 

3. this was about showing command in a better readable format but what if we want the command output to be shown in an terminal and also to be sent to a file

		ls -la /etc | tee peanut.txt

	* basically a T
	* take input so that's from `ls -la /etc`
	* the pipe command send the output to the second command `tee peanut.txt`
	* the tee command makes it so that the output is displayed on the screen and is also written to the specified file