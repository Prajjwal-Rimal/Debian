## Passwd
<ol>
<li> Linux doesn't identify user by username, but rather by the user id (UID)</li>

<li> which user has which id we can find it in /etc/passwd file </li>

<li> this shows us all the users in the system and detailed information about them </li>

<li>
root:x:0:0:root:/root:/bin/bash
<ul>
<li>Username: root
<li>User's password: x 
the password is not really stored in this file, it's usually stored in the /etc/shadow file.  
<ul>
<li> X => password is stored in the /etc/shadow file </li> 
<li> * => user doesn't have login access </li>
<li> blank field user has no password. </li>
</ul>
<li>The user ID:0 means root user any other user is not 0
<li>Primary group ID
<li>GECOS field: for comments about the user
<li>User's home directory: /root
<li> User's shell: /bin/bash 
</ul>
</li>

<li>we see other users in the system besides the real users as well as they are needed to run processes in the background a daemon user is for daemon process </li>

<li> we can edit the /etc/passwd file by using the vipw tool
	
	sudo vipw

</li>
</ol>