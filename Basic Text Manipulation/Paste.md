## PASTE
1. paste command is similar to the cat command.

        cat : primarily to display the file content but can concatenate the output of multiple files together
        paste : merges lines together in a file

2. we have a file called Pastepractice.txt with the following text:

        The 
        Quick
        Brown
        Fox

3. `$ paste -s Pastepractice.txt` this command combines all the lines into one, but this command has a default delimiter of tab so we will have a single line of txt but spaced by tabs.

        output: The [tab] Quick [tab] Brown [tab] Fox

4. `paste -d ' ' -s Pastepractice.txt` is used to change the default delimiter, this command separates everything with spaces.

        output: The Quick Brown Fox

5. the explanation of flags is as follows:
    * serialize (-s) : so by default paste merges line from multiple file like we would do in `cat` command, -s flag tell it to merge the lines from the single file into one
    * delimiter (-d) : used to specify a custom delimiter, by default tab so each line it serializes are separated by a tab, but if we change it to a space ' ' now the lines will be separated by space.

6. we can also merge multiple files by using <br>
` paste <filename> <filename>` <br>
we can also use the delimiters and the serial flag <br>
` paste -s -d ',' <filename> <filename>`
