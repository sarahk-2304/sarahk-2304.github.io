---
layout: default
---
## Intro  
This course teaches you the basic tools for language technology in Ubuntu. 
The course consists mostly of independent work, but there were also in-person support sessions every other week.

# Module 1:

The first thing we did was install a command-line environment. Then we started learning some basic commands. 
Additionally, we learned how to handle and navigate files and directories. 
For example, we learned how to copy, move and remove directories and files. 
We also learned input/output redirection as well as how to check and change permissions for a file or a directory.

Most of the week’s concepts were easy to grasp, but I struggled a bit with understanding permissions. 
The command for finding the permissions for a specific was simple, 
but it took me a long time to understand what the symbolic notations actually meant. 
Another thing I found challenging was remembering how different options affected commands.

Here are some useful commands we learned:

| Command | Explanation | 
| ------------------ | ------------- |
| ls                    | Lists the current working directory’s contents |
| pwd                | Displays the full path to the current directory |
| cd                   | Changes the current working directory |
| cat                  | Displays file contents |
| wget               | Downloads content from the internet | 
| echo               | Prints text to standard output or writes it to a file using redirection |
| cp                   | Copies files and directories | 
| mv                  | Moves or renames files | 

# Module 2:

This week we learned about encoding systems like ASCII, Latin-1, and UTF-8.
After getting ourselves familiar with them, we learned to convert text files from one encoding system to another.
After that, we delved into basic text file operations. 

These operations include:

* Counting the lines, words and characters in a file
	* _wc_ 
* Sorting files in alphabetically and numerically
	* _sort_
* Removing duplicate lines from a sorted file
	* _uniq_
*  Searching text files for certain patterns
	* _grep_

One of the most useful things we learned was piping commands. 
This allows you to chain commands together so that data can be transferred between them continuously
rather than having to pass it through temporary files.
