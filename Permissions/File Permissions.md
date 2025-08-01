## File Permissions
1. files have different permissions and file modes
2. four part to a file's permissions:
	- first: file type denoted by the first character, d resembles a directory, `-` for a regular file
	- next 3 parts are the actual permissions, each part of the permissions are divided into 3 bits each
		- first 3 bits are user permissions
		- the next 3 bits are group permissions
		- the next 3 bits are other permissions
	- the file permission look like the following:

			drwxrwxr-x
			we can divide it into 4 parts
			d | rwx |rwx |r-x
	- each character represents a different permission
		- r : readable
		- w: writable
		- x: executable ( basically an executable program
		- `-`: empty

3.  
```bash
$ ls -l
total 32
drwxr-xr-x 14 user group 4096 Jul 18 08:05 Documents
drwxr-xr-x  6 user group 4096 Jul 31 16:04 Downloads
drwxr-xr-x  2 user group 4096 Jul 18 08:05 Music
drwxr-xr-x 27 user group 4096 Jul 10 23:03 Pictures
drwxr-xr-x  3 user group 4096 Jul 18 07:54 Postman
drwxr-xr-x  2 user group 4096 Jun 29 23:09 Public
drwxr-xr-x  2 user group 4096 Jun 29 23:09 Templates
drwxr-xr-x  4 user group 4096 Jul 30 18:20 Videos
```

understanding the output above
- **total 32** indicates that all the files shown in the output use 32 block of memory on the disk each block is of 1024 bytes on Linux (512 Unix) 
- **drwxr-xr-x** is the first column shows the file type and permissions
- **14** this is the number of links that the file has, number of links are alternative names for the same file stored in the system, for directory it represents the number of sub directories + parents/self links, the folder has 12 sub directories (12) + self link . (1) + parent link .. (1) = 14 links
- **user** this is the name of the file owner, who creates it becomes the owner, a owner and a root user has full authority over the file others don't
- **group** by default it is a group which a owner belongs to
- **4096** size of the files in bytes , this is only the character count for the file and not the total space it occupies on the disk, this means someone wrote 4096 characters symbols or binary data into the file, for directories it means that the internal table size of the directory is 4096 bytes, the space occupied by a file on the disk is usually larger to see the actual space use `du -h foldername`
- **Jul 18 08:05** represent when the file was last updated / modified, stored to the nearest second, it is modified if its contents have been changed in some way, permission and ownership change do not contribute to modification 
- **Documents** filename arranged in ASCII sequence capital letters come first, if we have a important file that we would like to view up top its better to name it in uppercase