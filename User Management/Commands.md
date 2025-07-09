
## Important commands

<table>
  <thead>
    <tr>
      <th>Task</th>
      <th>Command</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Check if you're root</td>
      <td>id -u(0 means root)</td>
    </tr>
    <tr>
      <td>VTo check which user is the root user</td>
      <td>getent passwd 0</td>
    </tr>
    <tr>
      <td>Check who has sudo access</td>
      <td>getent group sudo</td>
    </tr>
    <tr>
      <td>Switch to root user</td>
      <td>su -</td>
    </tr>
    <tr>
      <td>Change root password (if sudo user)</td>
      <td>sudo passwd root</td>
    </tr>
    <tr>
      <td>Disable root login</td>
      <td>sudo passwd -l root</td>
    </tr>
    <tr>
      <td>Re-enable root login</td>
      <td>sudo passwd -u root</td>
    </tr>
  </tbody>
</table>