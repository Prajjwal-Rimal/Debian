## Modifying Permissions USE CAREFULLY
1. `chmod (Change Mode)` command is used to modify file permissions
2. when files and directories are created there <u>permissions are set to default by setting called **umask** </u>, this setting usually write protects a file for everyone besides the user, group and others can not write to it 
3. `chmod` command can change permission for one or more files for all the 3 fields: user, group, others, the permissions can only be set by the user (file owner) and the root user
4. there are two type of permissions:
| Relative Permission | Absolute permission |
| ------------- | ------------- |
| only changes the permissions specified in the command line and leaves others as they were  | this is used to set all 9 permissions using octal numbers |
| syntax: `chmod category operation permission filename`  | syntax: `chmod permissions filename`  |
| example: `chmod u+x file.txt` | example: `chmod 775 file.txt`  |

## Relative Permission Explanation
1. adding permission: `$ chmod u+x file.txt`
	- u refers to user
	- `+` refers to assign
	- x refers to execute

	we are telling the command to give user executing permission for the file file.txt
	
2. abbreviations used by chmod in relative mode
	
		u = user			+ = assign permission
		g = group			- = remove permission
		o = others	
		a = all

					r = read permission
					w = write permission
					x = execute permission

3. removing permission: if we wanted to remove write permissions from the group and other we would type the following :

	` $ chmod go-w file.txt`

4. multiple categories: if we wanted all the categories to have the read permission we would type either of the following command:

	` $ chmod ugo+r file.txt`
	or 
	`$ chmod a+r file.txt`

5. multiple permissions and files: we can also specify multiple file and specify multiple permissions:

	`  $ chmod a+rwx file.txt file2.txt fil3.txt`

## Absolute Permission Explanation
1. achieved by using a string of 3 octal numbers ( octal numbers = 0 - 7 values)
2. a set of 3 bits can represent one octal digit and one category has 3 permissions so one bit per permission
3. permission values:

	| permission | value | octal value |
	|------------|-------|-------------|
	| read | 4 | 100 |
	| write | 2 | 010 |
	| execute | 1 | 001 |
	| total | 7 | 111 |

	6 represents read and write permission

	3 represents write and execute permission  and so on... 

	| binary | octal | permission relative  |
	|------------|-------|-------------|
	| 000 | 0 | --- |
	| 001 | 1 | --x |
	| 010 | 2 | -w- |
	| 011 | 3 | -wx |
	| 100 | 4 | r-- |
	| 101 | 5 | r-x |
	| 110 | 6 | rw- |
	| 111 | 7 | wrx |

4. we have 3 categories and 3 values for each categories so this method we can describe the permission for all 3 categories

5. to assign permission: `$ chmod 777 file.txt`

	adds read write execute permission to all 3 categories

6. to remove permissions:`$ chmod 755 file.txt`
	
	give read write execute permission to the user, read and execute permission to the group and other categories.


## Quick Use Cases:
1. chmod 700 → private script
2. chmod 644 → public HTML file
3. chmod 600 → config file readable only by owner

## Chomd behave differently for files and directories

1. Files:
    1. r (read) →  view the contents of the file.
    2. w (write) →  modify or delete the file.
    3. x (execute) →  run the file as a program/script (if it's executable).

2. Directories: **default permission is rwxr-xr-x or 755 and it should not be changed a directory should not be writable by a group or others or they may tamper with files**
    1. r (read) → You can list the contents of the directory (e.g., ls).
    2. w (write) → You can create, delete, or rename files inside the directory.
    3. x (execute) → You can enter the directory (cd dir/) and access files inside if you know their names.
**both r and x on a directory to see and access its contents**

## example

let’s say i have a folder called imp inside my documents folder, i own it (user: me) and the group owner is also me.

now there’s another user on my pc called bob and he’s part of the me group too.

the folder imp has default permissions rwxr-xr-x (755), and inside it there’s a file called notes.txt with permissions rwxrwxr-x (775)

so here’s what bob can do:

    he can read the file

    he can edit the contents of the file (because group has write access)

    he can run the file if it’s a script (because group has execute access)

but here’s what he can’t do:

    he can’t create new files or folders inside the imp directory (because the directory doesn’t allow group write)

    he can’t delete or rename the file notes.txt (deleting requires write access on the directory itself, not just the file)

so basically, bob can work with the file, but can’t mess with the folder or its structure — a safe way to let group members collaborate on the contents without touching the setup.