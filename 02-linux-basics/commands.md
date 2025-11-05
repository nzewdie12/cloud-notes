# Linux Commands Notes

## General Notes
- Linux uses a hierarchical file system.
- `~` represents the home directory.
- `echo ~` prints the path to the home directory.
- && combines commands
  - Example: cd ~/project && ls -> goies into projects dir and lists contents
- '|'(pipe): the pipe allows for one operation output to be the input of another
  -  sudo dmseg | grep -iE 'fail|error' > error_page.txt:: This command will first exucute the sudo dmseg commmand and then the output from that would be the input of the grep command
    -  the second '|' is for a multi-word search for grep
-  nano -> work on scripts/file in a text editor
-  tree [dir] -> shows a nested directory structure
-  '$Variable' -> tells the shell to subsititue the variable with the value

- source [file] -> reads and executes the commands in the current sheell environemtn
  - ./[file] -> creates a new shell envoironment to run it   
---


## User and System Information
- `whoami` → Displays the username of the current user.  
- `id` → Displays info about the user (UID, GID, groups).  
  - UID = Unique user ID  
  - GID = Main group ID  
  - Groups = All groups you belong to
- groups [username]: displays groups the user is a part of  
- `root` → Superuser account.  
- `sudo` → Run commands with admin privileges.  
- `history` → Shows previously entered commands.


- **Shortcut:** `Ctrl + R` → Search previous commands.

- sudo useradd [username]: adds a new user
  - sudo useradd -m [username]: creats home folder for the new user
- /etc/passwd: acts as a phone book and can be used to locate if user exists
  - Example: sudo grep -w 'joker' /etc/passwd -> verifies if user was created
- /etc/shadow: to check if user has a password ( not "THE" password)
  - example:  sudo grep 'j.doe' /etc/shadow -> if j.doe has a password it will print something. ***if it is locked it will have a '!' in it***   
- /etc/group: to check the usrs in a group

- 
- sudo passwd [username]: set user password
- sudo passwd -l [username]: locks the user account
  -  sudo passwd -u  [username]: unlocks user account
- sudo usermod -d [new_dir] [username]: moves home dir of username to new dir
- sudo usermod -s /bin/bash [username]: changes the user shell to bash (was sh before)
- sudo usermod -aG [group] [username]: adds the user to the group. (-aG stands for append to group)
- su - [username]: switch user
- sudo userdel -r [username]: deletes user (-r means inlcuding all files/dir and mail spools)

### system info
- ' uname' -> shows kernel name
  - uname -a -> shows kernel version + operating system
- date -> current date and time
- cal -> calendar
- /etc -> system configureation files
- /bin -> holds essential command programs 
- uptime: shows system uptime and load average
- top: works well for system monitoring, shows live system info about CPU and memory usage
- 'dmseg': shows system-level hardware and kernel issues
- 'ps aux': takes a snapshot of all processes running on the system.
  - ps -p 1235 -o pid,ppid, cmd: helps find info(pid, ppid, cmd locatoin) based on the pid (1235) 
- 'pgrep -f [script/file name]: finds the proccessing id (pid) of the script/file
- pkill [file/script]: terminates file/script
- nohup [file]& : allows you to run a script in the background. the & at the end tells it to run in the background
  - Example: nohup your_command > custom_log.txt 2>&1 &  -> runs the script on background without interuptoin + sends standord output and error output into the custom_log file

### networking.
- ip addr: shows the status and configuration of all network interfaces. A way to check if a network interface is up/down.
- ifconfig: shows IP addresses of the network interfaces. (eth0 uis sually the main network interface.)
- ping: pings(sends packets and recives feedback) any ip address.
  - ping -c (count) [ip address]: count= number of packets to be sent.
- ss: can be used to check if any ports are listining and running
  - ss -l: specifies that they are listening (from experementing: is neccasry if want to use the grep commmand also)   
- ufw : aka uncoplicated firewall...: this operates a baisic firewall
  - ufw enable/disable: enables firewall , disables firewall
  - ufw allow/deny [port number]: allows traffic from port number, denys traffic from port number
    - ufw allow ssh: this will act the same as sying ufw allow 22(port for ssh) 

---

## Package Management
- `apt` → Package manager.  
  - `sudo apt install [package]` → Install software.  
  - `sudo apt update` → Update package list.
  - 'apt show [package] -> shows details/info about the package
    - dpkg -s : does something simmilar
  - 'apt remove [package} -> remove package
    - 'apt autoremove' -> removes unused packages.
- `install` and `update` are used to manage packages.

---

## File and Directory Navigation
- `pwd` → Prints working directory.  
- `cd [directory]` → Change directory.  
  - `cd ~` → Home directory.  
  - `cd ..` → Parent directory.
  - 'cd -' -> go to previous directory
- `ls` → Lists directory contents.  
  - `ls -l` → Long format (shows permissions, owner, group).  
  - `ls -a` → Includes hidden files.  
  - `ls -la` → Long format with hidden files.  
  - `ls -lR` → Recursive list of all subdirectories.  
  - `ls -ld` → Show directory info itself.  

**Example output:**
-rw-rw-r-- 1 user user 0 Jul 29 15:11 example.txt

- `-` = file, `d` = directory  
- First section = permissions  
- Next = owner, group, etc.  
- `/` = absolute path.

---

## File and Directory Creation
- `touch [filename]` → Create an empty file.
  - touch [filename{1..5}] -> creates 5 empty numbered files
- 'cat << EOF > [filename] [...] -> allows you to write multiple lines into a file without using \n
- `mkdir [directory]` → Create a new directory.  
  - `mkdir -p newdir/subdir` → Create nested directories.  
- Files starting with `.` are hidden.  
- `file [filename]` → Shows file type.

---

## File Content and Output
- `echo` → Prints or redirects text.  
  - `echo "Hello"` → Prints text.  
  - `echo "Hello" > test.txt` → Writes “Hello” to a file.  
  - `>` redirects output to a file.
  - '>>' appends onto the file ( adds onto the file) 
- `cat [file]` → Displays file contents.  
  - `cat -n` → With line numbers.  
- `less [file]` → View large files page by page.  
- `head [file]` → First 10 lines.  
- `tail [file]` → Last 10 lines.  
  - `head -n [x]` or `tail -n [x]` → Show x lines.  
  - `head -c [x]` or `tail -c [x]` → Show x characters.
- 'grep [word] [file]' -> searches for word in a file
  - 'grep -w [word] [file]' -> searches for **Whole** word in file
  - 'grep -i: case sensitive
  - 'grep -E [pattern1]|[pattern2]: can search for mutiple words at once
 
## Variables

- [VARAIABLE_NAME]=[value] -> to create a shell variable.
  - DIR_VAR="/home/project/app.logs" -> paths require ""
- .zshrc file -> any variable in this file is perminent even if the terminal closes
  - source ~/.zshrc -> ***MUST Run/execute .zshrc in order to use the variable*** 
- read [input_name] -> used to capture user input in terminal
- Common Environemtnal variables
- env ->View all environemtnal variables
  - $PATH -> -> allows you to run executable programs from anywhere in the system, aslong as they are in the PATH directory.
    - export PATH="$PATH:$HOME/my_scripts" -> adds the my_scritps directory to PATH variable
  - $HOME -> Home Dir
  - $USER -> current user
- unset [variable] -> to remove/delete a environemtn variable
---

## File Operations
- `cp [src] [dest]` → Copy files or directories.  
  - `cp file1 file2` → Copy contents.  
  - `cp file dir/` → Copy file into directory.  
  - `cp -r dir dir_copy` → Copy directory recursively.  
- **Wildcards:**  
  - `*` = all files  
  - `?` = single character  
  - `[abc]` = match one of a, b, or c  
- `mv [src] [dest]` → Move or rename.  
  - `mv old.txt new.txt` → Rename.  
  - `mv file dir/` → Move file.  
- `rm [file]` → Remove file.  
  - `rm -f` → Force delete.  
  - `rm -i` → Ask before deleting.  
  - `rm -r [dir]` → Delete directory recursively.  
  - `rmdir [dir]` → Delete empty directory.
 
    
- 'tar' -> archives muliple files into one
  - 'tar -cvf [archived_file.gz] [file1] [file2] -> creates a tar archive with file 1 and file 2.
    - 'tar -czvf [archived_file.gz] -T [filename_with list] -> can create a tar archive with files/dir found in a file with a list of the dir/file names
    - 'z' -> compress the file into the gzip
  - 'tar -tvf [archivved_file.gz] -> to read contents of file without extracting it
    - 'tar -tzvf [archivved_file.gz] -> for compressed file
  - tar -xf [archive_file.gz] [backup_file_path] -> extracts and puts back the backup file from the archive file.
    - tar -xvf [archive_file.tar] -C [new directory where archive is gonna extract] -> extract and "upload" files/dir to new dir
  - gzip [file_to_compress] -> compress file
  - tar options:
    - c -> create
      - C(uppercase) -> used to specify which file to extract into  
    - v -> varbose : print names of files as it processes
    - f -> specify file name
    - z -> dealing with compressed file
    - t -> read contents without extract
    - x -> extract
- zip -r [compressed_file_name] [file_to_compress] -> can compress and is compataible for allmost all operating systems
- unzip -d [dir_to_unzip_into] [zip_file] -> unzip compressed zip file. -d means create dir_to_unzi_inot if it does not exist.  
 
  - 
 
  - ***crontab ??????***

---

## Searching and Comparing
- `find [path] -name "[filename]"` → Find file by name.  
  - `find [path] -type [f/d] -name "[filename]"` → By type (file/dir).
  - ***Find command works for size,date modified, type...***
- `diff [file1] [file2]` → Compare two files.  
  - Example: `1c1` → line 1 in file1 differs from line 1 in file2.  
  - `diff -r dir1 dir2` → Compare directories recursively.

---

## Permissions and Ownership
- `chmod [xyz] [file]` → Change permissions.  
  - 4 = read  (r)
  - 2 = write  (w)
  - 1 = execute  (x)
  - 0 = no permission  
  - `chmod 700 file` → Owner full (rwx), group & others none.  
- Symbolic notation :
  - U = owner/user
  - g = group
  - o = others
  - a = all
  - s = setgid: sets a special persmisson to mean the group/owner/other has ownership of any new files added in directory
    - Example: sudo chmod g+s -R pheonex_project/src -> this would allow any file in the src directory to inhearit the same group ownership as the src directory. 
  - Example: chmod u+x script.sh -> give user/owner(U) execute permissions (x). (+: adds permission) (-: removes permission)
    - chmod +/- [permission]: just use the permission without the user/group to apply to all.
- chown [owner]:[group] [file]` → Change file ownership.  
  - Example: `sudo chown root:root example.txt`


---

## Aliases and Shortcuts
- `alias name='command'` → Create a command shortcut.  
  - Example:  
    ```
    alias test_file='echo "Hello" > test.txt'
    ```
- `unalias [name]` → Remove alias.

---

## Help and Documentation
- `man [command]` → Manual pages.  
- `help [command]` → Shell help.  
- `whatis [command]` → Short command description.

---

## Scripts
- `.sh` files → Shell scripts (e.g., `run.sh`).
- ' '#!' ' -> tells system this is a bash script ( e.g., '#!/bin/bash' ).
  -  '/bin/bash' -> path to bash interpreter
-  ./[script_name] -> to run script
### Script examples 
- echo '#!/bin/bash\necho "Hello, World"' > script.sh
  - This code creates the (script.sh) file and the "code" in it ( #!/bin/bash \n echo "Hello, World") tells it to run it as a bash script and to echo hello world when run.
    - echo '#!/bin/bash' -> mush be in single quotes 
  - use printf '#!/bin/bash\n echo "Hello, world" ' > script1.sh if the bash does not interperate (\n) as new line  

## Miscellaneous
- ' expr [#] [expression] [#] -> allows you to do math operations aka quick calculater
- 'figlet [word] -> creates ascii art from the word
- 'apropos [common_word] -> looks through commands with discripts that contain the common_word
  - ' apropos  password -> passwd ...
- sort -> sorts alphabeticly
- export [variable decloration] -> create a environmental variable (makes it avalibel to child processes)
- `clear` → Clears the terminal.  
