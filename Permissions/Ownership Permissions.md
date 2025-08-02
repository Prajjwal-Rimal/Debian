## Ownership Permissions ( ROOT USER MOSTLY )
1. only the root user can change the ownership of the file , normal users can change the group of a file to a group they belong to as long as they own the file
2. if someone copies the file or the directory they become the owner of the copy not the one of the original, ownership transfer does not occur
3. two important commands `chown` and `chgrp`

    | <b>chown</b> | <b>chgrp</b> |
    | ------|-------|
    | change owner, and can change group as well | change group|
    | needs to be a root (sudo) user | doesn't need to be a root (sudo) user look at the note at the end of the table |
    | syntax: `$ sudo chown who_will_own_the_file file_name` <br>or<br> `$ sudo chown who_will_own_the_file:which_group_will_own_the_file file_name` (this command is used for changing file ownership as well as group ownership) | syntax:`$ chgrp which_group_will_own_the_file file_name` <br>or <br> `$ sudo chgrp which_group_will_own_the_file file_name`|
    | example: `$ sudo chown jane file.txt` <br>or<br> `$ sudo chown jane:office file.txt` | example:`$ chgrp office file.txt` <br>or<br>  `$ sudo chgrp headoffice file.txt` |
    | by default the owner is the one who created the file | by default the group owner of the file is the group that user belongs to |
    | requires the User Id (UID) / username | requires the Group Id (GID) / Group name|
    | accepts multiple filenames | accepts multiple filenames |
    |  | <b>note</b> :: a user can change the group owner of a file but only to a group they belong to, a root can change it to anyone.<br> Lets say its joe who changing the groups of a file joe can only change the group of the file to the group he belongs to , a root user can change it to anything|



