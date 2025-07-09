## Users And Groups
1. traditional operating system -> user and groups
2. for access and permission management
3. file access and ownership is permission dependent
4. each user has their own home directory
5. system used user id's UID to manage users
6. user groups to manage permissions identified with the group id GID
7. Linux has users in addition to the human users, these users can be system daemons that run processes to keep the system functioning
8. ROOT => superuser
<ul>
<li> most powerful user in the system </li>
<li> can access any files </li>
<li> run and kill processes </li>
<li> if root access is needed, and the user has sudo privileges, they can use the sudo command to run commands as root.</li>
<li> sudo command is used to run a command with root access </li>
<li> having sudo privileges does not make a user the root user </li>
</ul>
<br>

##	
shadow is a protected file in the system which  stores encrypted user password hashes and some account management information. 

It is highly protected because it contains sensitive data. 

When we try to access it as a normal user we get denied

		$ cat /etc/shadow
		cat: /etc/shadow: Permission denied

While looking at the content of the file we see that the file has root permissions

		$ ls -la /etc/shadow
		-rw-r----- 1 root shadow 1146 Jun 30 00:14 /etc/shadow
	
By adding the sudo command, since we are a root user we can access the content of our files after entering our password

		$ sudo cat /etc/shadow
		[sudo] password for prajjwal: 
		filecontent

##
Root vs Sudo User

<table>
  <thead>
    <tr>
      <th>Feature</th>
      <th>Root User</th>
      <th>Sudo User</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>UID</td>
      <td>Always 0 </td>
      <td>Usually 1000+</td>
    </tr>
    <tr>
      <td>Access</td>
      <td>Full system access</td>
      <td>Temporary root access via sudo</td>
    </tr>
    <tr>
      <td>Risk</td>
      <td>High (no restrictions)</td>
      <td>Safer (requires password + logs usage)</td>
    </tr>
    <tr>
      <td>Default shell</td>
      <td>/root</td>
      <td>/home/username</td>
    </tr>
    <tr>
      <td>How to become root</td>
      <td>Log in as root or su -</td>
      <td>sudo command</td>
    </tr>
  </tbody>
</table>





