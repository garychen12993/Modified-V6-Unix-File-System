Follow the steps to run the programs:
1. Extract all the files from the zip folder and use WinSCP application (or other similar software)
   to move the files into the current working directory (home directory will suffice) of the UNIX system.
2. Open a terminal and CD into the current working directory.
3. The run file named 'fsaccess' should already available from the zip. Run the following 
   commands to test the simulation

	./fsaccess				(will startup the modified Unix V6 file system)

4. If there is no .out file, or if you want to check to see if it compile correctly, do the following 
   commands:
		
	gcc -o fsaccess fsaccess.c

   Be sure to type in the correct spacings.

5. Commands available for fsaccess:

	initfs - to initialize file system
		initfs <pathname> <number of blocks> <number of i-nodes>
	
	mkdir - create a directory if it doesn't exist
		mkdir <directory name>

	cpin - if external file exists, create a new system file to copy external file into the system file
		cpin <external file name> <system pathname>

	cpout - if system file exists, create an external file to copy system file into the external file
		cpout <system pathname> <external file name>

	rm - if system file exists, remove system file and free it's metadata
		rm <system pathname>

	q - save all changes and quit