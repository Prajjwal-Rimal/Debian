## WC and LC

1. `wc` command shows the number of lines, words, and bytes in a file

        $ wc filename
        96-> number of lines, 265-> number of words, 5925-> number of bytes(characters)

2. flags:
    * -l (line flag) : this is used to display the line count only
    * -w (word flag): this is used to display the word count only
    * -c (bytes flag): this is used to display the byte count only

3. `nl` command represents line number, it adds line numbers to the file

        file.txt    $nl file.txt
        i           1 i
        drink       2 drink
        milk        3 coffee

4. nl doesn't display the total number of lines it adds them, however if we want to display the line number using nl we can combine it with various other commands and get it

        $ nl file.txt | tail -n 1
        nl file1.txt → Adds line numbers to each line in file1.txt.
        pipe → Sends the output of nl to the next command.
        tail → Displays the  last lines.
        -n 1 → Tells tail to show only the last 1 line.
