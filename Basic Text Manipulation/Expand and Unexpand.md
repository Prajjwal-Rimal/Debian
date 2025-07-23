## Expand and Unexpand

1. we had a file named Cutpractice.md

2. we can change the tabs to spaces using the expand command

`$ expand Cutpractice.txt`

3. this will convert the tab to the group of spaces we can also use the stdout redirection to send the output to another file

`$ expand Cutpractice.txt > Cutexpanded.txt`

4. just like expand we have an opposite command used to convert spaces into tab

`$ unexpand -a result.txt`

5. `-a` flag in unexpand stands for all it converts all the spaces into tabs not just the ones that are in the beginning of the file, the expand doesn't need this flag as by default it converts every tabs into spaces 

6. use case:
    * helpful when formatting files having spacing and tab formatting
    * dealing with inconsistent spacing or formatting
    * for making file ready for tools, or application that prefer tab over spaces or vice versa
    * to reduce file size : tabs are 1 char spaces are more than 1 char
