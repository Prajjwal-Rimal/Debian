## Translate

1. translate allows us to translate a set of characters into another set of characters.

2. used to:
* translate characters
* delete characters
* squeeze repeated characters

3. `$ tr a-z A-Z`
<br>
converts lowercase to uppercase characters

        $ tr a-z A-Z
        hello
        output: Hello

4. delete specific characters(-d : delete):
`$ tr -d ello`
<br>
this deletes the characters after the -d flag n this case ello

        $ tr -d ello
        hello
        output: h

5. squeez repeated characters (-s : squeez):
`$ tr -s '2'`
<br>
combines repeated characters into one

        $ tr -s '2'
        1222223
        123
