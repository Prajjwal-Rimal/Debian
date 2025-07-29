## Grep

1. grep is a command used to search for text pattern's in files or output

2. basic syntax is `$ grep <pattern> <filename>`
example `$ grep fox sample.txt`
this searches for the word fox in sample.txt

3. <b> flags </b>

    * `-i flag`: ignores case when matching, shows all the occurrences of the word fox not case specific ones `grep -i <what to search> <filename>`
    * `-r flag`: is used to search recursively in all the files of a directory ` grep -r <what to search> <directoryname>`
    * `-n flag`: display line numbers of the occurrence `grep -n <what to search> <filename>`

	* `-w flag` : matches us the exact output (whole word not parts of other words)for what we type `grep -w <what to search> <filename>`, returns the exact thing we are searching for 

	* `-c flag` : counts the occurrence `grep -c <what to count for> <filename>`

4. we can also filter the output from grep by using the pipe 
`env | grep -i user`
this searches and displays for user in our environment variables

5. <b>EXPRESSION SEARCH</b> 
`$ ls <directory> | grep '<.txt>'`
this command searches for all the files ending in txt from the specified directory known as regex search: used to match advanced pattern


## PRACTICE COMMAND GREP

1. the `find` command helps us to search for files lets recreate this with grep:<br>

		$ find ~/Documents -name "Grep.md"
		Documents/Grep.md

	returns us the full path after finding the file 
<br>

		$ ls ~/Documents | grep "Grep.md"
		Grep.md`

	so this command list all the content in the directory, | sends the output to the grep command, the grep command finds for the file and returns the file name verifying the file exists in the path

2. Now in this file lets say we want to search for the word grep

		$ grep "grep" Grep.md

		1. grep is a command used to search for text pattern's in files or output
		2. basic syntax is `$ grep <pattern> <filename>`
		example `$ grep fox sample.txt`

    		* `-i flag`: ignores case when matching, shows all the occurrences of the word fox not case specific ones `grep -i <what to search> <filename>`
    	
			* `-r flag`: is used to search recursively in all the files of a directory ` grep -r <what to search> <directoryname>`
    	
			* `-n flag`: display line numbers of the occurrence `grep -n <what to search> <filename>`
		
		4. we can also filter the output from grep by using the pipe 
		`env | grep -i user`
		`$ ls <directory> | grep '<.txt>'`

		... shows and displays all the lines containing the word grep
		
	but one thing to notice is that it doesn't show us ##Grep that cause this is case sensitive

3. To make grep case insensitive

		grep -i "grep" Grep.md
		## Grep
		1. grep is a command used to search for text pattern's in files or output
		2. basic syntax is `$ grep <pattern> <filename>`
		example `$ grep fox sample.txt`


    	... # shows us all the occurrences case insensitive

4. now lets say we want to display the output for the word find as a whole word 

		$ grep -w "find" Grep.md
		1. the `find` command helps us to search for files lets recreate this with grep:<br>
		$ find ~/Documents -name "Grep.md"

		... this searches for the word find and shows the output, it doesn't display the output for words like finding, finder etc

5. we have used grep multiple times in this file lets count for it in a case insensitive way

		$ grep -ic "grep" Grep.md 
		38

		... this is not the number of lines that grep occurs in rather this is the amount of time the word grep has been used 

6. now lets list the number of lines that contain grep (case insensitive)

		$ grep -in "grep" Grep.md 
		1:## Grep
		3:1. grep is a command used to search for text pattern's in files or output

		... displays all the lines with numbers where grep has been used

7. to count the number of lines grep has appeared on we use the word count command with the -l flag:

		$ grep -i "grep" Grep.md | wc -l
		49
		... total number of lines that contain the word grep

8. now lets say i want to search for all the files containing the command grep in the Documents/github/Debian/'Basic Text Manipulation' directory i can use the r flag

		$ grep -r "grep" ~/Documents
		/Documents//Grep.md:1. grep is a command used to search for text pattern's in files or output
		/Documents/Grep.md:2. basic syntax is `$ grep <pattern> <filename>`
		/Documents/Grep.md:example `$ grep fox sample.txt`


		... this searches all the files and folders inside our specified directory and shows us the output of each occurrence in each file

## Include and exclude 

1. we can also pair grep with include and exclude 
2. `grep -r --include="*.md" "grep" ~/Documents`: 
		
	* grep -r : recursively search 
	* -- include="*.md" : looks at all the files ending in .md dont forget the `*`
	* "grep": searches for grep
	* ~/Documents ...: directory to recursively search in
 
	by specifying include we make it so that grep doesn't search files with .png, .exe, .pdf, which allows for faster, cleaner and better results.

3. `grep -r --exclude="*.log" "grep" ~/Documents`:

	* grep -r : recursively search through directories
	* --exclude="*.log" : ignore all files ending with .log 
	* "grep" : search for the pattern “grep”
	* ~/Documents : the directory where the recursive search starts

	using `--exclude` helps skip irrelevant files (like logs, binaries, images), making the search faster and the results cleaner
