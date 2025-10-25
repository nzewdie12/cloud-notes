# Shell Commands Cheatsheet for Linux

## NOtes:
- linux uses hieracahal file system


## Commands

- echo: Repeats whatever you write // EX. echo "Hello world" --> Hello world
  - echo is also used as print. aka (standard output) // echo "Hello world" > testfile.txt ( will print hello world in testfile.txt)
  - >: redirects the output of echo into the file. If the file does not exist, it will create the file and redirect the echo into it.
  -


- whoami: Displays the username of the current user
- id: displays info about user ( such as user group and uid) --> output will have UID (unique user id ), GID(main group user is apart of ) and groups ( all groups you are a member of)
- root: is the superuser

  
- sudo: stands for Superuser Do and allows for you to execute commands with admin privilage (temperarily)
- apt: package manager for installing software
- install and update: as the name says install "xxx" or update does just that
  -  combined use: $ sudo apt update

- Chown: is used to change ownership// ex. sudo shown root/root example.txt 

- pwd: print working directory. Current location in the file system
- " ~" : is the home directory // ex . echo ~ --> the path to the home directory
  
- ls: list home directory
  - ***Combo would be {  ls ~  --> lists the contents of home directory***
  -  ls -l: lists contents with additioinal info ( including its permissions, owner, and group.)
    -  ls -l "directory name" : can list contents in the directory
      - //Results =
       - "-" in the first char meand file while "d" in the first means directory
       - after the dashes( basicaly just current permisions) the first "name" is current owner and second "name" is the current group of the file. 
         - ///ex. -rw-rw-r-- 1 labex labex 0 Jul 29 15:11 example.txt //// 0 fiile size in bytes, date last modified, and file neame
  -  ls -a: shows all files including hidden files
  -  ls -la: combines both
  -  ls -lR: shows all sub dir and files in a dir
  -  ls -ld: shows directory

-  "-R" : makes wide spread changes to all files and sub dir
  
 
-  ".." means directory above // ex cd .. ---> go to the parent directory
-  cd: means change directory,  basically like saying go to// ex. cd ~ --> go to home directory
-  "/": absolute path. starting with "/" means giving a full location // ex. /home/examplefile/photos
  
-  touch: creates an empty file //ex. touch testfile.txt
-  ".": any file or directory that starts with "." is a hidden// ex. echo "Hidden file" > .hiddenfile ( .hiddenfile is a hidden file)
- file:  tells what type of file it is //ex file pic.jpeg --> txt file ( doesnt have to match name in linux)
-  mkdir: creates a directory
  - -p (newdir/subdir): creates a new dirctory and a subdiretocty in it

  
-  cp "filename" "filename_copy": cp copys the contents of filename and saves it in the new file copy "filename_copy"
  - cp "file" "directry"/: copies file into directory
  - cp -r "directory" "directory copy": copies directory ( r means recursive and neccdasry for copying dirfectory contents accuratly)
  - ## It is possible to copy and move at the same time. Make sure to include the /destination/"copied file name"
  - Wildcards
    - cp * : the wildcard of wildcards, it's used to represent all single characters or any string.
    - ? used to represent one character
    -[] used to represent any character within the brackets 

- mv "filename" "newfilename": changes the name of file. also works with directories ( mv "dirname" "newdirname")
  - mv "file" "directory"/: moves file into directory
  - //test comand// mv testdir/newname.txt ./original_file1.txt : changes newname.txt name to original_file1.txt and ./ moves it into the current directory

- rm: removes files
  - rm -f: force removes files even if they are wirte protected
  - rm -i: remove files with a flag. It asks to confirm you want to remove the file
  - rm -r "directory": removes contents in the directory and the directory itself
  - rmdir "dir": removes empty directories
 
- cat: displays contents of a file/ read files
  - cat -n: display with line numbers
- less: To view large files 

- head: displays the first 10 lines
- Tail: displays the last 10 lines
  - head(or tail) -n(x)  where x is the number of lines]: displays x number of lines
  - head(or tail) -c(x) where x is htenymebr of characters: displays x number of charactiers

- diff "file1" "file2" : will show the diffrences in the files. it will tell the line ini which the change is in // ex. 1c1 = first line in first file is different than the first line in second file ***Depending on which file is first, changes the result***
  - diff -r (dir) (dir2): works with directories and shows files that are missing in one that is present in the other


- chmod (xxx) : Change permission for 1st x = owner permission, 2nd x= group's permission, 3rd x = others' permissions.
  - numbers from 0 to 7 calculated as follows
    - 4 read permission, 2 Write permission, 1 execute permission, 0 no permssion
    - ex. 700 is Owner(Read, write, Execute [ 4+2+1), group(none 0), others(none 0)
   
- history : shows all the commands you have inputed before
  - ctrl + R : basiclay works as a search of the preivous comand (ie simmilar to cmnd F in google)

- find : to find a file
  - find /(Directory) - name (filename): to find a file in a directory or its subdirectory
  - find /(dir) -type (filetype) - name (filename): to find file based on file type

- alias='(Command)': creats a sort of variable for a command. // ie.  alias test_file='echo "Hello, World \n Hello z\n z is me" > test.txt'
  - unalias: to undo. 


- man, help, whatis: bwill give you more info on how to use a command

- clear : clears terminal
