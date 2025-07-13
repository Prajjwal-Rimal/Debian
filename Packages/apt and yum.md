## apt and yum
1. these come with the system to make package management easier 
2. these also install package dependencies
3. yum is for red hat and apt is for Debian

* install a package:

		$ apt install packagename
		$ yum install packagename

* remove a package:

		$ apt remove packagename
		$ yum erase packagename

* update the package:

		$ apt update (refreshes package metadata) / apt upgrade (upgrades an installed package)
		$ yum update

* to know more about the package:

		$ apt show packagename
		$ yum info packagename

4. on newer red hat systems yum is replaced by dnf