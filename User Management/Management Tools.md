## Use Management Tools

<ol>
<li> used to manage users, accounts, groups, and password </li>
<li>Important user  commands:  </li>
<ul>
<li> adding user: sudo useradd bob </li>
<li> removing user: sudo userdel bob </li>
<li> rename a user: sudo usermod -l <newname> <oldname> </li>
<li> move and rename a users home directory: usermod -d /home/newname -m <username> </li>
</ul>

<li>Important password commands: </li>
<ul>
<li> change a user password: passwd <username> </li>
<li> lock the user account: passwd -l <username> </li>
<li> unlock the account: passwd -u <username> </li>
<li> modify password expiration and aging rules: chage<username> </li>
<li> list the current password age information: chage -l <username> </li>
</ul>

<li> important group commands: </li>
<ul>
<li> to create a new group: groupadd <groupname> </li>
<li> modify the group name: groupmod -n <newname> <oldname>  </li>
<li> delete a group: groupdel <groupname> </li>
<li> add a user to a supplementary group: usermod -aG <groupname><username> </li>
<li> to set or change the group password: gpasswd <groupname> 
</li>
</ul>
</ol>
