Shell Commands Cheatsheet for Linux
Notes

Linux uses a hierarchical file system.

~ represents the home directory (e.g., echo ~ → prints the path to the home directory).

User and System Information

whoami: Displays the username of the current user.

id: Displays info about the user (UID, GID, groups, etc.).

UID: Unique user ID

GID: Main group ID

Groups: All groups you belong to

root: The superuser account.

sudo: “Superuser Do” — runs commands with admin privileges temporarily.

history: Shows all previously entered commands.

Ctrl + R: Search through previous commands (similar to “Find”).

Package Management

apt: Package manager for installing or updating software.

sudo apt install [package]: Install software.

sudo apt update: Update available packages.

install and update: Install or update software.

File and Directory Navigation

pwd: Prints the working directory (current location).

cd [directory]: Change directory.

cd ~: Go to the home directory.

cd ..: Go to the parent directory.

ls: Lists directory contents.

ls -l: Lists contents with additional info (permissions, owner, group, etc.).

ls -a: Shows all files including hidden files.

ls -la: Combines both -l and -a.

ls -lR: Shows all subdirectories and files recursively.

ls -ld: Shows the directory itself.

Example output:

-rw-rw-r-- 1 user user 0 Jul 29 15:11 example.txt


-: File, d: Directory

First section shows permissions, followed by owner and group information.

/: Indicates an absolute path (full location).

File and Directory Creation

touch [filename]: Creates an empty file.

mkdir [directory]: Creates a new directory.

mkdir -p newdir/subdir: Creates a new directory and a subdirectory in it.

. (dot): Any file or directory that starts with . is hidden.

file [filename]: Displays the file type.

File Content and Output

echo: Prints text or redirects output.

echo "Hello world" → Displays text.

echo "Hello" > test.txt → Writes “Hello” into a file.

>: Redirects output to a file (creates it if it doesn’t exist).

cat [filename]: Displays the contents of a file.

cat -n: Displays with line numbers.

less [filename]: Views large files one page at a time.

head [filename]: Displays the first 10 lines.

tail [filename]: Displays the last 10 lines.

head -n [x] or tail -n [x]: Displays x number of lines.

head -c [x] or tail -c [x]: Displays x number of characters.

File Operations

cp [src] [dest]: Copies files or directories.

cp file1 file2: Copies the contents of one file to another.

cp file dir/: Copies a file into a directory.

cp -r dir dir_copy: Copies a directory and its contents (recursive).

Wildcards:

*: Represents all files.

?: Represents one character.

[abc]: Represents any character within brackets.

mv [src] [dest]: Moves or renames files/directories.

mv oldname.txt newname.txt: Renames a file.

mv file dir/: Moves a file into a directory.

rm [file]: Removes files.

rm -f: Force removes files (even if write-protected).

rm -i: Asks for confirmation before removing.

rm -r [dir]: Removes directory and its contents.

rmdir [dir]: Removes empty directories.

Searching and Comparing

find [path] -name [filename]: Finds a file by name.

find [path] -type [filetype] -name [filename]: Finds by type (file or directory).

diff [file1] [file2]: Shows differences between two files.

Example: 1c1 means the first line in file1 differs from the first line in file2.

diff -r dir1 dir2: Compares directories recursively and shows differences.

Permissions and Ownership

chmod [xyz] [file]: Changes permissions.

First digit = owner, second = group, third = others.

Numbers:

4 = Read

2 = Write

1 = Execute

0 = No permission

Example: chmod 700 file → Owner (rwx), Group (none), Others (none).

chown [owner]:[group] [file]: Changes ownership.

Example: sudo chown root:root example.txt.

Aliases and Shortcuts

alias name='command': Creates a shortcut for a command.

Example: alias test_file='echo "Hello, World" > test.txt'.

unalias [name]: Removes an alias.

Help and Documentation

man [command]: Displays manual pages.

help [command]: Shows built-in shell help.

whatis [command]: Gives a brief description of a command.

Miscellaneous

clear: Clears the terminal screen.

.sh files: Shell script files (e.g., script.sh).
