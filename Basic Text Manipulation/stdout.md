## stdout (Standard out)

1. when we run this command in a directory we see that it creates a txt file called peanut with hello world typed inside it 

		$ echo hello world > peanut.txt

2. $ echo hello world on itself prints 'hello world' to the screen using the i/o process. echo command by default accepts input (stdin) and returns output (stdout) 

3. ' > ' is a <u> redirection operator </u> and we can change where we send the output from here, if file doesn't exist it will make one, and if it exits it will overwrite it. 

4. to enter text to the end of the file 

		$ echo hello world >> entering at last line >> peanut.txt