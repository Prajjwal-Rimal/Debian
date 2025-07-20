## Cut 
1.in our file practice.txt we have a file that says
<br>
'The quick brown; fox jumps over the lazy     												[ tab ] dog'
<br>
'The quick brown; fox jumps over the lazy dog'

2. cut command extracts specified parts of a line

3. `$cut -c 5 practice.txt` this cuts the fifth character from each line of the file, spaces are also considered character

4. `$cut -f 2 practice.txt` the fields flag cuts everything based on field, it uses tabs as delimiters, it wont work without tabs by default. since we have tabs we should see our output as : 

        dog
        The quick brown; fox jumps over the lazy dog
        # This is because we have tab in the first line so it cuts everything after the tab and displays it

5. we can combine the` field flag(-f)` with the `delimiter flag (-d)` to extract content by our delimiter / any character we specify 
<br>
`cut -f 1 -d";" practice.txt`
<br>
it's output will be as the follows:
        
        The quick brown
        The quick brown

6. above we see that we have use -f 1 & -f 2 
* -f 1 means the first part of the field
* -f 2 means the second part of the field
* so when we type cut -f 2 practice.txt
	
		'The quick brown; fox jumps over the lazy     																dog' 
		output: dog 
* if we said cut -f 1 practice.txt 

		'The quick brown; fox jumps over the lazy     																dog' 
		output : The quick brown; fox jumps over the lazy