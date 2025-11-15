# Shell Commands Cheatsheet for Linux

## Notes
- Linux uses a hierarchical file system.

---

## Basic Output & Redirection
- **echo**  
  - Repeats whatever you write.  
    - Example: `echo "Hello world"` → prints *Hello world*
  - Can redirect output into a file.  
    - Example: `echo "Hello world" > testfile.txt`  
      - `>` redirects output (creates the file if it doesn’t exist)
  - Used like "print" (standard output).

---

## User & Permissions Info
- **whoami**  
  - Displays the username of the current user.

- **id**  
  - Displays info about the user, such as UID, GID, and all groups.

- **root**  
  - The superuser on Linux (full system privileges).

- **sudo**  
  - “Superuser Do” — execute commands with admin privileges temporarily.

---

## Package Management (Debian/Ubuntu)
- **apt**  
  - Package manager for installing software.
  - Examples:  
    - `sudo apt install packagename`  
    - `sudo apt update` (updates package lists)

---

## Ownership & Permission Changes
- **chown**  
  - Changes ownership of files.  
    - Example: `sudo chown root:root example.txt`

- **chmod (xxx)**  
  - Changes permissions using numbers:  
    - Read = 4, Write = 2, Execute = 1  
    - Example: `chmod 700 file` → owner full access, others none.

---

## File System Navigation
- **pwd**  
  - Print working directory (your current location).

- **~**  
  - Home directory.  
    - Example: `echo ~` prints full path to home.

- **ls**  
  - Lists directory contents.
  - Variants:  
    - `ls -l`: long format (permissions, owner, group)  
    - `ls -a`: includes hidden files  
    - `ls -la`: combine long + hidden  
    - `ls -lR`: recursive (shows subdirectories)  
    - `ls -ld dirname`: shows directory info  
  - Notes:  
    - `-` at start of permission line = file  
    - `d` at start = directory  
    - Example breakdown:  
      - `-rw-rw-r-- 1 labex labex 0 Jul 29 15:11 example.txt`

- **cd**  
  - Change directory.  
    - `cd ~` → home directory  
    - `cd ..` → parent directory

- **/**  
  - Absolute path indicator.  
    - Example: `/home/example/photos`

---

## Creating & Managing Files and Directories
- **touch**  
  - Creates an empty file.

- **.hiddenfile**  
  - Files starting with `.` are hidden.

- **file**  
  - Shows file type, regardless of file extension.

- **mkdir**  
  - Creates a directory.  
    - `mkdir -p newdir/subdir` creates directories recursively.

---

## Copying, Moving, and Deleting
- **cp**  
  - `cp file file_copy`: copies a file  
  - `cp file dir/`: copies file into a directory  
  - `cp -r dir dir_copy`: copies directories recursively

  **Wildcards:**  
  - `*` matches any string  
  - `?` matches a single character  
  - `[abc]` matches any one character inside brackets

- **mv**  
  - Renames or moves files.  
    - `mv filename newname`  
    - `mv file dir/` moves file to a directory  
    - Example:  
      - `mv testdir/newname.txt ./original_file1.txt`

- **rm**  
  - Removes files.  
    - `rm -f`: force remove  
    - `rm -i`: interactive prompt  
    - `rm -r dir`: remove directory and contents  
  - **rmdir** removes *empty* directories.

---

## Reading File Contents
- **cat**  
  - Displays file contents.  
    - `cat -n` shows line numbers.

- **less**  
  - View long files one screen at a time.

- **head**  
  - First 10 lines of a file.  
  - Options:  
    - `head -n 5`: first 5 lines  
    - `head -c 20`: first 20 characters

- **tail**  
  - Last 10 lines.  
  - Same `-n` and `-c` options as head.

---

## Comparing Files
- **diff file1 file2**  
  - Shows differences between files.  
  - Example:  
    - `1c1` means line 1 of file1 differs from line 1 of file2.  
  - Order matters.

- **diff -r dir1 dir2**  
  - Recursively compares directories.

---

## Searching for Files
- **find**  
  - General search tool.  
  - Examples:  
    - `find /directory -name filename`  
    - `find /dir -type f -name "*.txt"`

---

## Shortcuts & Aliases
- **alias name='command'**  
  - Creates a shortcut for a command.  
    - Example:  
      - `alias test_file='echo "Hello" > test.txt'`

- **unalias**  
  - Removes an alias.

---

## Shell Scripts
- **.sh files**  
  - Shell script files.  
  - Must start with a shebang:  
    ```bash
    #!/bin/bash
    ```

- Make script executable:  
  ```bash
  chmod +x script.sh

---
## Help & Documentation
- man
  - Manual pages for commands.
- help
  - Help for built-in shell commands.
- whatis
  - One-line description of a command.

##Misc
- history
  - Shows previously run commands.
- CTRL + R
  - Reverse search through command history.
- clear
  - Clears the terminal screen.
