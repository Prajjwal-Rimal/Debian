## File Ownership
1. when we create a file you become its owner and you name appears on the third column, and the owners group name appears on the fourth column
2. if we copy someones file we become the owner of the copy, we can not create files in their directories because the directories are not owned by us and the owner has not provided us with the write access
3. may users can belong to a single group like people working on a project, in this case different users will have the same group owner
4. privilege of the group are set by the group owner
5. as we have discussed in our earlier notes in user management when a new account is created by a sys admin they store the user id(uid) in /etc/passwd file and the group id (gid) in /etc/group
6. there are always **two owners to a file one the user owner and one the group owner**
7. only the **root owner and the user owner can change file permissions and ownership's**

---
1. **Individual Ownership**
   - used to separate system files and personal files on the same computer
   - controls who can read, write, or execute files locally
   - keeps your personal data secure and private from other users on the same machine, many users can use the same machine, multiple logins, shift change , etc

2. **Shared Ownership (Group Ownership)**
   - useful for shared network storage systems like NAS (Network Attached Storage)
   - allows a group of users to access and collaborate on files stored in a shared location
   - group permissions control who can read, modify, or execute files within that shared environment
   - requires proper setup so that all users in the group have compatible user and group IDs for smooth access
- like google docs, drive