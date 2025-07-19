## RPM & DPKG
1. just like .exe , .rpm and .dpkg are executable files
2. dpkg is exclusive to the Debian system and rpm is exclusive to red hat 
3. to install these packages we can use the package management command , the commands will install the package files not the package dependencies, hence with this method we will have to install the dependencies and all the necessary packages separately, this is why the full package manager is the most popular and widely used one 
4. there will be times when we need to manually install a package, verify it, or remove them:

* Install:

		Debian: $ dpkg -i packagename.deb
		RPM: $ rpm -i packagename.rpm

* remove a package: 

		Debian : $ dpkg -r packagename.deb # r for remove
		rpm : $ rpm -e packagename.rpm # e for erase

* list installed packages:

		Debian: $ dpkg -l 3 l for list
		rpm : $ rpm -qa # q for query and a for all