## Join and Split

1. the join commands allows us to join multiple files together with a common field (column)
<br>
<br>
2. by default it uses first fields from both files, in field refer to the 1,2,3 numbering, they act as indexes
<br>
<br>
3. since both the files have 1,2,3 the join statement matches the fields and joins the output so 1 matches with 1, 2 with 2 and so on
<code>$join filename filename</code>
<br>
<br>

        file1.txt       file 2.txt

        1 John          1 Doe
        2 Jane          2 Smith
        3 Mary          3 Sue
        

        output:
        1 John Doe
        2 Jane Smith
        3 Mary Sue

<br>
<br>

4. sometimes the field may not match, basically indexes in different positions.

        file1.txt       file 2.txt

        John 1          1 Doe
        Jane 2          2 Smith
        Mary 3          3 Sue
        

        output:
        1 John Doe
        2 Jane Smith
        3 Mary Sue

  * here we see that the files contain numbering in different columns to join this type of file we need to use the following command

	`$ join -1 2 -2 1 filename filename`

* -1 2 : use the second field from file 1
* -2 1 : use the first field from file 2
* we are basically specifying the key values to join at
* to join the file both of the files must be sorted by the index to that we can use 
    <br>
    `$sort filename -o file1.txt`, -o flag represent output, tells us what our output file be named as
* the join command doesn't necessarily need numbers if it was a,a in both the column it would work, if it was apple apple it would work, it just needs a common value in both the fields and is case sensitive
<br>
<br>
5. if we do not have indexes then the join command wont work
<br>
<br>
6. just like join we can also split the files, split is used to break a file into smaller parts
<br>
<code> $ split filename </code>
<br>
by default the file is split at every 100 lines but we can change this behavior with flags

    * -l n : n is the number of lines to be split at `split -l 50 filename`
    * -b n : used to split by size (1K,1M,1G) `split -b 1M filename`
    * --additional-suffix : used to add the required extensions to the necessary files ` split filename --additional-suffix=.txt`, this cannot be used with the join command for join use the stdout (>) redirection method
    
<br>
<br>
7. join use case:

* Merge user info from different files (e.g., names with emails)
* Combine product IDs with prices or descriptions
* Match student roll numbers with grades
* Merge logs or data from multiple systems based on IDs
* Create consolidated reports from separate data sources
<br>
<br>
8. sort use case:

* Prepare files for join (since it requires sorted inputs)
* Sort logs by timestamps or severity levels
* Arrange records by scores, prices, or names
* Remove duplicates using sort | uniq
* Organize tabular or CSV data
<br>
<br>
9. split use case:

* Split large log or data files into manageable chunks
* Break huge files for easier processing or analysis
* Divide datasets for parallel processing or team sharing
* Split files to meet upload or email size limits
* Create smaller test files from a big one



##
summary



To join files, they must be sorted and have index columns or key values. Even if the key columns are not in the same position, we can specify their positions with flags (like -1 and -2). The join happens based on matching index values (e.g., 1 with 1, 2 with 2). The -o flag tells where to output the joined file — if the file exists, it overwrites; if not, it creates it. The split command breaks a large file into manageable chunks. We can specify how many lines per chunk, or what size each split file should be. We can also add suffixes to ensure all split files have the same format.