## SORT

1. it is used to sort lines in a file
<br>
<br>
2. default (dictionary order): 

`$ sort file.txt`

        file.txt        $sort file.txt
        banana          apple
        cherry          apricot
        apple           banana
        apricot         cherry
        dates           dates

<br>
<br>
3. reverse (-r flag): 

`$ sort -r file.txt`

        file.txt        $sort -r file.txt
        banana          dates
        cherry          cherry
        apple           banana
        apricot         apricot
        dates           apple

<br>
<br>
4. numeric (-n number): 

`$ sort -n file_numbers.txt`

        file_numbers.txt    $sort -n file_numbers.txt
        10                  1
        1                   2
        5                   3
        3                   4
        2                   5
        4                   10

<br>
<br>
5. numeric reverse (-n -r number): 

`$ sort -n -r file_numbers.txt`

        file_numbers.txt    $sort -n -r file_numbers.txt
        10                  10
        1                   5
        5                   4
        3                   3
        2                   2
        4                   1

<br>
<br>
6. redirection ( > & o ): to transfer the output to a new file

` $ sort file.txt > sortedfile.txt`

<br>

` $ sort file.txt -o file.txt # overwriting the original file`

<br>
<br>
7. column selection (-k flag) : 

`$ sort -k column_number file.txt`

        file.txt        $ sort -k 2 file.txt
        1 apple         1 apple
        2 banana        3 apple
        3 apple         2 banana
        4 cherry        4 cherry
        5 dates         5 dates

Basicaly we told it to sort based on the values of the second column

<br>
<br>

8. delimiter (-t flag):

`sort -t ',' file.txt`
<br>
the default delimiter is space or tabs

        file.txt    $ sort -t ',' file.txt
        1 a         1,a
        2 b         2,b
        3 c         3,c
