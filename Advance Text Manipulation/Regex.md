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
	grep 'colou?r' file.txt # need for 		backslash eliminated
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

