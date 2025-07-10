## Root
1. one way to get superuser access is by using the SUDO command
2. another command is the substitute user command 
<ul>
<li>su : Switch to root, but keep the existing environment</li>
<li>su - : Switch to root but load the full root environment</li>
<li>su bob : switch to bob, but keep the existing environment</li>
<li>su - bob : switch to bob and load bobs environment</li>
</ul>

3. <u>Environment</u> in Linux refers to a set of settings and variables such as : path, home, user, shell, lang, editor, ps1

4. downside to using the su command is that we don't have the record of commands that we used to change files
5. not everyone will have access to the superuser commands only people listed in <u> /etc/sudoers </u> to view the contents of the file <code> sudo cat /etc/sudoers </code> file can use them we can edit this file with the <u>visudo</u> command

6. When to use which command: 
<ul>
<li>Use sudo to run a single root command without switching users.</li>
<li>Use su to switch to root or another user but keep your environment. </li>
<li> Use su - to switch to root with full login environment.</li>
</ul>