## Compile source code
1. sometimes software's are not provided through apt or yum, and are given as a source code i.e. we need to build it ourselves 

2. first install tools to compile source code 

		$ sudo apt install build-essential

3. extract the source code package which is generally a compressed tarball file 

		$ tar -xzvf package.tar.gz

4. in the extracted tarball file read the readme file 

5. run a script file to check for the dependencies for the software. if missing well see errors and need to install them

		$ ./configure

6. then compile the software, building the file using a file called makefile

		$ make

7. finally install the program, copying the built files into system folder to run the program 

		$ sudo make install
		# hard to uninstall files with this method because we do not know what files were added 

		or 

		$ sudo checkinstall
		# same as make install but creates a .deb file which can be uninstalled with apt 

