## Tail
1. by default tail lets us see the last 10 lines of a file

        `$tail Cut.md`

2. like head we can use the number of line flag to change the number of lines we see 

        `$tail -n 15 Cut.md`

3. we also have the follow flag (-f) , this will follow the file as it grows, as the file changes well see everything that is being added to the file

        `$tail -f Cut.md`

4. Use cases:
    * Monitoring logs as they’re being written in real time
        
        `$tail -f /var/log/syslog`

    * Debugging running scripts or apps by watching output live
        
        `$tail -f output.log`

    * Checking the most recent entries of long data files
    * Observing changes made by other users or processes to a file
