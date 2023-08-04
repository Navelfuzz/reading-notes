# CF 401: Java // Prep: Practice the Terminal

## The Command Line: CLI for short

### Tasks
Working as a tech professional will often involve interacting with the terminal on your computer. 
This prework will introduce you to some of the more common commands involved in traversing directories and manipulating 
files on your machine.

[Bash Command Line Tutorials](https://ryanstutorials.net/linuxtutorial/)

Go through the sections and reflect on insights gained.

[The Command Line](https://ryanstutorials.net/linuxtutorial/commandline.php)


[Basic Navigation](https://ryanstutorials.net/linuxtutorial/navigation.php)
Absolute and Relative Paths
There are 2 types of paths we can use, absolute and relative. Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).

To begin with, we have to understand that the file system under linux is a hierarchical structure. At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.

Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )

*I put this note here because I often confuse the terminology and 'route' differences of Absolute and Relative paths, it doesn't affect my ability to navigate linux or any other CLI/FS but if I were taking a test and was asked to explain which is which.. 60% I get it backwards*

[More About Files](https://ryanstutorials.net/linuxtutorial/aboutfiles.php)


[Manual Pages](https://ryanstutorials.net/linuxtutorial/manual.php)

`man <command to look up>`

such as: `man ls`

returns: 

```
user@bash: man ls
Name
    ls - list directory contents
    
Synopsi
    ls [option] ... [file] ...
    
Description
    List information about the FILEs (the current directory by default). Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.
    
    Mandatory arguments to long options are mandatory for short options too.
    
    -a, --all
        do not ignore entries starting with .
        
    -A, --almost-all
        do not list implied . and ..
...
```

[File Manipulation](https://ryanstutorials.net/linuxtutorial/filemanipulation.php)

`rmdir [options] <Directory>`

[Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

## Basic Navigation
`pwd`
Where am I in the system.

`ls [path]`
Perform a listing of the given path or your current directory.
Common options: -l, -h, -a

`cd [path]`
Change into the given path or into your home directory.

`Path``
A description of where a file or directory is on the filesystem.

`Absolute Path`
One beginning from the root of the file system (eg. /etc/sysconfig ).

`Relative Path`
One relative to where you currently are in the system (eg. Documents/music ).

`~ (tilde)`
Used in paths as a reference to your home directory (eg. ~/Documents ).
`. (dot)`
Used in paths as a reference to your current directory (eg. ./bin ).

`.. (dot dot)`
Used in paths as a reference to your current directories parent directory (eg. ../bin ).

`TAB completion`
Start typing and press TAB. The system will auto complete the path. Press TAB twice and it will show you your alternatives.

## Piping and Redirection

`>`
Redirect STDOUT to a file.

`>>`
Append STDOUT to the end of a file.

`2>`
Redirect the STDERR to a file.

`<`
Pass the contents of a file to a program as STDIN.

`|`
Feed the STDOUT of the program on the left as STDIN to the program on the right.

## More About Files
`file [path]`
Find out what type of item a file or directory is.

`Spaces in names`
Put whole path in quotes ( " ) or a backslash ( \ ) in front of spaces.

`Hidden files and directories`
A name beginning with a . (dot) is considered hidden.

## Vi / Vim
View our [Vim Cheat sheet](https://ryanstutorials.net/linuxtutorial/cheatsheetvi.php)

## Permissions

`r (read) w (write) x (execute)`

`Owner or User, Group and Others`

`ls -l [path]`
View the permissions of a file or all items in a directory.

`chmod <permissions> <path>`
Change permissions. Permissions can be either shorthand (eg. 754) or longhand (eg. g+x).

## Filters
`head`
Show the first n lines.

`tail`
Show the last n lines.

`sort`
Sort lines in a given way.

`wc`
How many words, characters and lines.

`grep`
Search for a given pattern.
See more on our [Grep Cheat sheet](https://ryanstutorials.net/linuxtutorial/cheatsheetgrep.php)


## Useful Commands
`du -sh ./*`
Find the size of every directory in your current directory.

`df -h`
Display how much disk space is used and also free.

`basename -s .jpg -a *.jpg | xargs -n1 -i cp {}.jpg {}_original.jpg`
Make a copy of every jpg image file in the current directory and rename adding 
_original.

`find /home -mtime -1`
Find all files in the given directory (and subdirectories) which have been modified in the last 24 hours.

`shutdown -h now`
Shutdown the system. (Replace -h with -r for reboot.)

## Manual Pages
`man <command>`
View the man page for a command.

`man -k <search term>`
Search for man pages containing the search term.

`Press q to exit man pages`

## File Manipulation
`mkdir <directory name>`
Create a directory

`rmdir <directory name>`
Remove a directory (only if empty).

`touch <file name>`
Create a blank file.

`cp <source> <destination>`
Copy the source file to the destination.

`mv <source> <destination>`
Move the source file to the destination.
May also be used to rename files or directories.

`rm <path>`
Remove a file or directory.
Common options: -r -f

## Wildcards
`May be used anywhere in any path.`

`*`
Zero or more characters (eg. b*).

`?`
Single character (eg. file.???).

`[ ]`
Range (eg. b[aio]t).

## Process Management
`CTRL + C`
Cancel the currently running process.

`kill <process id>`
Cancel the given process.
Include the option -9 to kill a stubborn process.

`ps`
Obtain a listing of processes and their id's.
Including the option aux will show all processes.

`CTRL + Z`
Pause the currently running process and put it in the background.

`jobs`
See a list of current processes in the background.

`fg <job number>`
Move the given process from the background to the foreground.