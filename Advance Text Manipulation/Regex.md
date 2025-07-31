## RegEx (Regular Expression)

1. before starting lets look at different grep variants:

- **grep**: \
basic command to search for pattern in a file, searches for simple patterns, anchors (^,$) and meta characters (. *)

- **grep -E or egrep**: \
extended regular expression, provides us with additional RegEx features(+,?, or (|), ()) without backslashes \
with basic grep we have to do
		
	```bash
	grep 'colou\?r' file.txt
	```

	but with grep -E we don't need to use the backslash and we can simply

	```bash
	grep 'colou?r' file.txt # need for backslash eliminated
	```

-  **grep -e** \
allows us to specify multiple grep patterns in the command

	```bash
	grep -e 'fail' -e 'error' file.txt
	```

- **grep -P**: \
perl compatible grep allows for perl compatible RegEx, allows us to use advanced RegEx features like \
digits (\d), word character (\w), look ahead (?=), look behinds(?!), non capturing groups(?:), etc. \
this is not available in all Linux distro by default 

	```bash
	grep -P '\d{3}-\d{2}-\d{4}' file.txt
	```

<br>
<br>

2. we have the a text file with the following text
	
		Error: file not found
		This is the end
		by the sea
		ll
		lol
		lool
		color
		colour
		cat
		concatenate
		1234 is a number
		failed
		success
		gray
		grey
		a
		aa
		aaa
		aaaa
		aaaaa
		colouur

3. the 7 important patterns:
<br>

| Pattern  | Usage | Output  | Explanation |
| -------- | ----- | ------- | ----------- |
| ^  | ``` grep "^Error" sample.txt``` | **Error:** file not found | looks at the beginning of the line for the specified word, other positions don't matter |
| $  | ``` grep "sea$" sample.txt``` | by the **sea** | the $ sign looks for the word at the end of the lines, returns all lines ending in the specified pattern |
| .  |``` grep c.t sample.txt```  | **cat** \n con**cat**enate| it is used to search for one character between the specified points, newlines and single characters do not count ie b\\n or b|
| *  |```grep -E 'lo*l' sample.txt```  | ll lol lool | show the repetition of last character 0 or more time, basically saying that show the output for l followed by 0 or more o's and end them at the character l |
| +  |```grep -E 'lo+l' sample.txt``` | lol lool | same thing as `*` but the character has to appear at least once |
| [] |```grep 'gr[ae]y' sample.txt``` | gray grey | searching for characters present in the list, looks at the range specified in the bracket , checks for the character one by one combined with the starting and ending values, **only matches one character at a time** |
| \  |```grep '\:' sample.txt```  | Error**:** file not found | it is used to search for special characters |

4. Special Characters (Meta Characters):
<br>

| Pattern  | Usage | Output  | Explanation |
| -------- | ----- | ------- | ----------- |
| .  |``` grep c.t sample.txt```  | **cat** \n con**cat**enate| it is used to search for one character between the specified points, newlines and single characters do not count ie b\\n or b|
| *  |```grep -E 'lo*l' sample.txt```  | ll lol lool | show the repetition of last character 0 or more time, basically saying that show the output for l followed by 0 or more o's and end them at the character l |
| +  |```grep -E 'lo+l' sample.txt``` | lol lool | same thing as `*` but the character has to appear at least once |
| `|` |```	grep -E 'gray|grey|grape' sample.txt``` | gray grey | basically an or operator shows the output that matches |
| ?     |```grep -E 'colou?r' sample.txt```| color colour | basically a boolean operator, means o or 1 appearance, so when we say colou?r it means u can exist or it can not so it checks for u in between colo(starting) and r(ending), but if we didn't specify the ending it also shows colouur, usually we keep the ending |
| {n}|```grep -P 'a{3}' sample.txt```| aaa aaaa aaaaa | basically checks each word for the consecutive occurrence of the pattern, returns all matching the criteria to make it unique we need to pair it with an anchor points ```grep -P '^a{3}' sample.txt``` | 
| {n,}  |```grep -P 'a{3,}' sample.txt```| aaa aaaa aaaaa | matches 3 consecutive a's at minimum upto infinity |
| {n,m} |```	grep -P 'a{3,4}' sample.txt```| aaa aaaa aaaaa | same as the above two commands defines the minimum number of occurrences and maximum number of occurences, basically saying hey show me the word which has at least 3 a's and a maximum of 4 a's consecutively present in it, but it shows all the output and even the one with 5 a's the last a is ignored and the output is shown to the screen if we want the exact wwe need to use this command ```grep -P '^a{3}' sample.txt```|

5. Anchors and Boundaries
<br>

| Pattern  | Usage | Output  | Explanation |
| -------- | ----- | ------- | ----------- |
|^| ``` grep "^Error" sample.txt``` | Error: file not found | looks at the beginning of the line for the specified word, other positions don't matter |
| $  | ``` grep "sea$" sample.txt``` | by the sea | the $ sign looks for the word at the end of the lines, returns all lines ending in the specified pattern |
| \\b |```grep -P '\bcat\b' sample.txt``` | cat | this is the word boundary searches for the word and returns it if it is unique on its own |
| \\B |```grep -P '\Bcat' sample.txt```  | concatenate | this is the opposite of a word boundary searches for the word and returns it if it is a part of any other word |
