# Linux Commands Notes

## General Notes
- Linux uses a hierarchical file system.
- `~` represents the home directory.
- `echo ~` prints the path to the home directory.

---

## User and System Information
- `whoami` → Displays the username of the current user.  
- `id` → Displays info about the user (UID, GID, groups).  
  - UID = Unique user ID  
  - GID = Main group ID  
  - Groups = All groups you belong to  
- `root` → Superuser account.  
- `sudo` → Run commands with admin privileges.  
- `history` → Shows previously entered commands.  
- **Shortcut:** `Ctrl + R` → Search previous commands.

---

## Package Management
- `apt` → Package manager.  
  - `sudo apt install [package]` → Install software.  
  - `sudo apt update` → Update package list.  
- `install` and `update` are used to manage packages.

---

## File and Directory Navigation
- `pwd` → Prints working directory.  
- `cd [directory]` → Change directory.  
  - `cd ~` → Home directory.  
  - `cd ..` → Parent directory.  
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
- `cat [file]` → Displays file contents.  
  - `cat -n` → With line numbers.  
- `less [file]` → View large files page by page.  
- `head [file]` → First 10 lines.  
- `tail [file]` → Last 10 lines.  
  - `head -n [x]` or `tail -n [x]` → Show x lines.  
  - `head -c [x]` or `tail -c [x]` → Show x characters.

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

---

## Searching and Comparing
- `find [path] -name [filename]` → Find file by name.  
  - `find [path] -type [f/d] -name [filename]` → By type (file/dir).  
- `diff [file1] [file2]` → Compare two files.  
  - Example: `1c1` → line 1 in file1 differs from line 1 in file2.  
  - `diff -r dir1 dir2` → Compare directories recursively.

---

## Permissions and Ownership
- `chmod [xyz] [file]` → Change permissions.  
  - 4 = read  
  - 2 = write  
  - 1 = execute  
  - 0 = no permission  
  - `chmod 700 file` → Owner full (rwx), group & others none.  
- `chown [owner]:[group] [file]` → Change file ownership.  
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
### Script examples 
- echo '#!/bin/bash\necho "Hello, World"' > script.sh
  - This code creates the (script.sh) file and the "code" in it ( #!/bin/bash\necho "Hello, World") tells it to run it as a bash script and to echo hello world when run.   

## Miscellaneous
- `clear` → Clears the terminal.  
