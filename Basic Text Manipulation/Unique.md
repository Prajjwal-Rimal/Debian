## Unique (uniq)

1. it is a tool for parsing text
2. we can use the unique command to remove duplicates:
`$ uniq file.txt`

        example: file.txt       $ uniq file.txt
        banana                  banana
        banana                  peach
        peach                   apple
        peach                   mango
        apple                   orange
        apple
        mango
        mango
        orange
        
        # this removes all the duplicates from the file

3.  we can also count the number of occurrences:
`$ uniq -c file.txt` (-c flag: count flag)

        $ uniq -c file.txt
        2 banana
        2 peach
        2 apple
        2 mango
        1 orange
        
        # this shows the count of occurrences in a file

4. we can also just get the unique values
`$ uniq -u file.txt` ( -u flag: unique flag)

        $ uniq -u file.txt
        orange
        
        # shows the unique value in the file

5. we can also get the list of duplicate values
`$ uniq -d file.txt` ( -d flag: duplicate flag)

        $ uniq -d file.txt
        banana
        peach
        apple
        mango
        
        # shows the duplicate value in the file

6. unique doesn't detect the duplicate values unless they are adjacent, in case we have an file where we need to detect uniques and the values are not adjacent we can use the `sort` command sort the file use a `| pipe operator` to process and send the output to the `uniq` command

` $ sort file.txt | uniq`


<b><u> uniq and sort work on Single words, Full sentences (as long as each sentence is on its own line), Numbers and numerical values,Paragraphs only work if the entire paragraph is written on a single line. </u></b>