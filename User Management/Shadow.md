## Shadow

1. The shadow file is used to store information about user authentication
2. requires super user and read permissions

	$ sudo cat /etc/shadow

3. syntax is almost similar to that of the passwd file but with an encrypted password instead of the placeholder
4. the description of the fields are as follows:

<ul>
<li> username: the users login name </li>

<li> encrypted password: the full encrypted password not a placeholder like 'x'
<ul>
<li> ! => account is locked </li>
<li> * => no password login is allowed </li>
<li> blank => no password is set </li>
<li> $6$... => actual hashed password </li>
</ul>
</li>

<li> date of last password change:
<ul>
<li> number of days since Jan 1, 1970 when the password was last changed </li>
<li> if there is 0 the user should change their password in the next login </li>
</ul>
</li>

<li> minimum password age: number of days a user has to wait before changing their password again; stops frequent changes </li>
<li> maximum password age: the maximum number of days the current password can be used </li>
<li> password warning period: how many days before the password expires </li>
<li> password inactive period: number of  days before the account is fully disabled if the user doesn't change their expired password </li>
<li> account expiration period: the day from jan 1 1970 when the account will be disabled completely regardless of its password status  </li>
<li> reserved for future use </li>
</ul> 

5. in many distributions authentication doesn't simply rely on the shadow file and is managed by other mechanisms like PAM (Pluggable Authentication Module)

##

<u><b>prajjwal:$6$abc123...:19500:0:90:7:14:20000:</b></u>

<ol>
  <li>prajjwal – username</li>
  <li>$6$abc123... – password hash</li>
  <li>19500 – password last changed 19500 days after Jan 1, 1970</li>
  <li>0 – can change password anytime</li>
  <li>90 – must change password after 90 days</li>
  <li>7 – gets warned 7 days before it expires</li>
  <li>14 – has 14 days after expiry to still log in</li>
  <li>20000 – account expires permanently on that day</li>
  <li>(empty) – reserved</li>
</ol>

