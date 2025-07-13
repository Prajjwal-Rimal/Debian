## TAR & GZIP
1. combining a lot of files and packing them into one file is archiving.

2. making the file smaller, that’s compressing.

3. .zip or .rar do both at once, and are most common ones found in the linux system

4. gzip is a tool to compress a file, it compresses files into a single file with the extensions .gz

		$ gzip file1 : compresses the file

		$ gunzip file1.gz : decompresses the file

5. gzip can only work on one file at a time

6. tar is used to combine multiple files into one big file (without compressing).

7. it has the extension of .tar file and is called a tarball

		$ tar cvf tar1.tar file1 file2

	c = create, v = show what its doing, f = name of the output file

		$ tar xvf tar1.tar

	x = extract, v = show what it is doing, f = name of the file to extract

8.  to archive and compress we use both of the methods together and generate a compressed tarball file (.tar.gz)

		$ tar czf archive.tar.gz file1 file2

	here everything for the c and f is same except that the z stands for compress using gzip

		$ tar xzf archive.tar.gz

	this is used to decompress the compressed tarball file using gzip

9. there are other types of files well but they are uncommon and have different compression and decompression methods