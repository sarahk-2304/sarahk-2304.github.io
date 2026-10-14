---
layout: default
---
## Intro  
Intended for those interested in learning about language technology,
this course is a beginner-friendly introduction to the basic tools for language technology in a Unix-like environment.

The aim of this course is to familiarise you with the basics of operating in a Unix-like environment,
basic commands for processing text data, using regular expressions and script writing.
Participants will get a brief introduction to Python for the purpose of learning how to launch a virtual environment 
and how to use pip to install packages.
Additionally, the course provides valuable insight into the usefulness of remote servers and version control tools like Git.  
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

**Example code for this module:**  
``` 
ls -F example_dir 
```

Instead of listing the current directory’s contents, 
ls combined with the option -F lists the contents of a directory located inside the current working directory.
It also uses symbols to indicate file types, such as / for a directory.
This is useful because you avoid having to move to each directory one by one to view their contents.

# Module 2:

This week we learned about encoding systems like ASCII, Latin-1, and UTF-8.
After getting ourselves familiar with them, we learned to convert text files from one encoding system to another 
using dos2unix and unix2dos.
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
We also learned to use regex to find and replace patterns in a text file.

**Example code for this module:**  
``` 
cat example.txt | grep -E '\bcat[a-zA-Z]*\b' | wc -l | less 
```

This code displays the text file's contents, looks for all words starting with “cat”, 
counts the matching lines, and displays the resulting line count. 
Instead of having to type a very specific pattern for the grep command, 
you can find multiple variations of a word by using regex with grep -E.

# Module 3:

This module focused on scripting, configuration files, and installing programs.
For script writing, we got to implement the commands we had learned to write on the command
line in the previous weeks.
To gain a deeper understanding of scripting, we combined the commands we’ve learned in the past couple of weeks with new concepts.
Instead of doing the time-consuming task of running commands one by one in the terminal, 
a script allows you to execute them in a single step. 
We learned how to set environmental variables temporarily and permanently, as well as how to change the values of existing variables.
We also learned about command substitution, which allows us to take the output and save it as the value of a variable.

From this module, I gained a deeper understanding of conditional statements and variables. 
I had some previous knowledge about them from an introductory course to programming, 
but the structure used in scripts is very different from what I’ve previously learned. 

Configuration files were a completely new subject to me. 
I found the information about changing your prompt symbol the most interesting, 
since the information displayed there can increase readability. 
Learning bash prompt customization is also a great way to get a better understanding of how the shell works. 
I became more familiar with Python by learning to create virtual environments and install packages through pip.



Example code for this module:  
```
#!/bin/bash

echo "Enter filename"
read filename

if [ -e "$filename" ]
then
    echo "$filename exists in the directory"
    cat "$filename"
else
    cat > "$filename"
    echo "File created"
fi                                  
```

This code is related to the conditional statements we learned about in this module. 
It first displays the prompt “Enter filename” asking for the user's input. 
Once the user has typed a name of a file, the program then checks if a file with that name exists. 
It then either notifies the user that a file with that name exists and displays the file's content, 
or it creates a file with that name if it can’t find the file.
