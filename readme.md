# Bash Terminal commands

In this document, I will be listing some of the most common terminal commands used in bash terminal.


- **Ways to go to home directory.**
  -  `cd` - Go to home directory.
  -  `cd ~` - Go to home directory.
  -  `cd /home/username` - Go to home directory.
  -  `cd $HOME` - Go to home directory.
  -  `cd ../../` - Go two directories back and so on.

- **Some general commands**
  -  `ls` - List all files in the current directory.
  -  `ls -l` - List all files in the current directory in long format including permissions, owner, group, size, and date.
  -  `ls -a` - List all files in the current directory including hidden files.
  -  `ls -la` - List all files in the current directory in long format including permissions, owner, group, size, and date including hidden files.
  - `pwd` - Print working directory.
  - `file filename` - Get the type of file.
  - `cd some\ file\ name` - Go to a directory with spaces in the name.
- **Saving the current directory and going to another directory.**
  - `pushd directory` - Save the current directory and go to the directory which is given.
  - `popd` - Go back to the directory which is saved by pushd.
- `locate filename` - Best way to find the any filename in system, you can either provide the exact filename or part of the filename, it will show you all matching paths. It uses a database which is updated by updatedb command as follows `sudo updatedb`.
- `which filename` - Check if any such tool is installed in the system or not.
- `cal` - Show the calendar of the current month.
- `cal 2021` - Show the calendar of the year 2021.
- `cal 10 2021` - Show calender of 10th month of 2021.
- `date` - Show the current date and time.

- **Command history**
  - `history` - Show the history of commands.
  - `!!` - Run the last command.
  - `!n` - Run the nth command from the history.
  - `!-n` - Run the nth command from the last.
  - Or use up arrow key.

- **Knowing about commands**
  - `whatis command` - Get a one-line description of the command.
  - `apropos keyword` - Search command related to keyword you have provided.
  - `man command` - Get the manual of the command. It is like documentation of some command. Some commands may not have manual.
  - `info command` - Get the info of the command. It is like documentation of some command. Some commands may not have info. Works same as `man` command.

- **Working with files and directories**
  - `mkdir directoryname1 directoryname2` - Create directories, you can provide multiple directories, or you can create directories one by one.
  - `touch filename` - Create a file, if file already exists then it will update the timestamp of the file, more files can be created at once also like `mkdir` command.
  - `cp filename1 filename2` - Copy the file from filename1 to filename2. If filename2 is a directory then it will copy the file to that directory.
    - Example - `cp —/.bashrc bashrc` - Copy the file `.bashrc` to the file `bashrc`.
  - **Note** - If you press tab to auto-complete the filename, then if it does it means file exists.. so inclusively it is working like `ls` command.
  - `mv filename1 filename2` - Move the file from filename1 to filename2. If filename2 is a directory then it will move the file to that directory. Also it can be used to rename the file. In this case filename2 is the new name of the filename1.
  - `rm filename` - It removes the `filename` file, and their is no way you can get back it to your system.
  - `rm *` - It removes all files in the current directory.
  - `rm file*` - It removes all files starting with `file` in the current directory. For example `rm cat*` will remove all files starting with `cat`.
  - `rm -r directory` - It removes the directory and all files and directories inside it.
  - `rm -rf directory` - It removes the directory and all files and directories inside it forcefully.
  - `rmdir directory` - It removes the directory if it is empty.
  - `rmdir *` - It removes all removes all empty directories in the current directory, it is very useful.

- **Working with files content**
  - `cat filename` - Show the content of the file.
  - `cat >> filename` - Append the content to the file, if file does not exist then it will create the file and write content in it. So basically you're saving effor to create a file through `touch`, and editing it through `nano` or `vim`.
  - `cat file1 file2` - Show the content of file1 and file2 combined in terminal.
  - `cat file1 file2 > file3` - Combine the content of file1 and file2 and save it in file3.