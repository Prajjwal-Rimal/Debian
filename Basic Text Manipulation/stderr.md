## stderr (standard error)
1. listing the content of a file to a directory that does not exist gives us the following error

		$ ls /fake/directory > peanut.txt
		ls: cannot access '/fake/directory': No such file or directory

2. by default the error messages (stderr) sends the output to the screen and is a deferment stream from stdout

3. the file descriptor for stdin is 0, stdout is 1, and stderr is 2

4. to output error to a file we can use the following command

		$ ls /fake/directory 2> peanut.txt

5. we can also send the error and output of the command to the same file by using the following command

		$ ls /fake/directory > peanuts.txt 2>&1
		sends both the output and error messages to the same file, first the output is sent to the file, then the errors is sent to the same file

6. this command hides errors by redirecting stderr to /dev/null, and shows only normal output if there is any

		$ ls /fake/directory 2> /dev/null

7. this command shows no error or output as both are sent to /dev/null 

		ls /fake/directory >> /dev/null 2>&1
