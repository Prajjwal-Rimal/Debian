<ul>
<li>Check if you're root (0 means root):
	
	$ id -u
	#1000 i.e. not a root user
	#0 a root user

<li>Check which user is the root user: 
	
	$ getent passwd 0
	# root:x:0:0:root:/root:/bin/bash
	# username : password placeholder : user id(UID) : GROUP ID(GID) : user description :home directory for the user : default shell used by the user

<li>Check who has sudo access: 

	$ getent group sudo
	# sudo:x:27:janedoe
	# group name : password placeholder : group id(GID) : member name


<li>Switch to root user but keep current environment: 

	$ su

<li>Switch to root user with full environment: 
	
	$ su -

<li>Switch to another user (e.g., bob) without full environment: 

	$ su bob

<li>Switch to another user (e.g., bob) with full environment: 

	$ su - bob

<li>Run a single command as root: 

	$ sudo <command>

<li>Change root password (if sudo user): 

	$ sudo passwd root

<li>Show groups the current user belongs to: 	
	
	$ groups
	# janedoe cdrom floppy sudo audio dip video plugdev users netdev bluetooth lpadmin scanner
	# basically means janedoe has access to all these things in the system

<li>Show groups a specific user belongs to: 

	$ groups <username>
	# janedow : janedoe cdrom floppy sudo audio dip video plugdev users netdev bluetooth lpadmin scanner
	# groups : Groups your current user belongs to
	# groups <username>: Groups a specific user belongs to


<li>Show all users in a specific group: 

	$ getent group <groupname>
	
	$ getent group sudo
	# sudo:x:27:janedoe


<li>View the sudoers file (contains info about the sudo users) : 

	$ sudo cat /etc/sudoers
	# only for viewing the file

<li>Safely edit the sudoers file: 

	$ sudo 
	$ visudo

<li>Show your current PATH environment variable: 

	echo $ PATH

<li> to edit the /etc/passwd file 
	
	$ sudo vipw

<li> Add user:

	$ sudo useradd username

<li> Remove user:

	$ sudo userdel username

<li> Rename user:

	$ sudo usermod -l newname oldname

<li> Move and rename user’s home directory:

	$ sudo usermod -d /home/newname -m username

<li> Change user password:

	$ passwd username

<li> Lock user account:

	$ passwd -l username

<li> Unlock user account:

	$ passwd -u username

<li> Modify password expiration/aging rules:

	$ chage username

<li> List current password age info:

	$ chage -l username

<li> Create new group:

	$ groupadd groupname

<li> Modify group name:

	$ groupmod -n newname oldname

<li> Delete group:

	$ groupdel groupname

<li> Add user to supplementary group:

	$ usermod -aG groupname username

<li> Set or change group password:

	$ gpasswd groupname

<li> View /etc/shadow file (requires sudo):

	$ sudo cat /etc/shadow

<li> Edit /etc/shadow file (not recommended):

	$ sudo vim /etc/shadow

<li> Check permissions of /etc/shadow:

	$ ls -la /etc/shadow

</ul>
