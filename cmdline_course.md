---
layout: default
---
## Intro  
Intended for those interested in learning about language technology,
this course is a beginner-friendly introduction to the basic tools for language technology in a Unix-like environment.

The aim of this course is to familiarise you with concepts like the basics of operating in a Unix-like environment,
basic commands for processing text data, using regular expressions and script writing.
Participants will get a brief introduction to Python for the purpose of learning how to launch a virtual environment 
and how to use pip to install packages.
Additionally, the course provides valuable insight into the usefulness of remote servers and version control tools like Git.  



# Module 1:

The first thing we did was install a command-line environment. Then we started working on some basic commands. 
Additionally, we learned how to handle and navigate files and directories. 
For example, we learned how to copy, move and remove directories and files. 
Later, we learned input/output redirection as well as how to check and change permissions for a file or a directory.

Most of the week’s concepts were easy to grasp, but I struggled a bit with understanding permissions. 
The command for finding the permissions for a specific was simple, 
but it took me a long time to understand what the symbolic notations actually meant. 
Another thing I found challenging was remembering how different options affect commands.

Here are some useful commands from this module:

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

This code is related to navigating directories.
Instead of listing the current directory’s contents, 
ls combined with the option -F lists the contents of a directory located inside the current working directory.
It uses symbols to indicate file types, such as / for a directory.
This command allows you to identify directories without navigating into each one. 


# Module 2:

In this module, we learned about encoding systems like ASCII, Latin-1, and UTF-8.
After getting familiar with them, we learned to convert text files from one encoding system to another 
using dos2unix and unix2dos.
After that, we delved into basic text file operations. 

These operations include:

* Counting the lines, words and characters in a file
	* _wc_ 
* Sorting files in alphabetically and numerically
	* _sort_
* Removing duplicate lines from a sorted file
	* _uniq_
* Searching text files for certain patterns
	* _grep_
* Finding and replacing patterns
	* _sed_

For me, the most useful skill I gained from this module was learning piping.
This allows you to chain commands together so that data can be transferred between them continuously
rather than having to pass it through temporary files.
We also learned to use regex and the sed command to find and replace patterns in a text file.
This module's videos were on how to create frequency lists, word n-grams lists, 
and how to change a text into sentence-per-line format

**Example code for this module:**  
``` 
grep -E '\bcat[a-zA-Z]*\b' example.txt | wc -l  
```

This is a combination of multiple topics from this week. 
The command includes piping, regex and pattern finding.
This command looks for all matching lines starting with “cat” and
counts those lines. 
Instead of having to specify every variation of a word separately,
you can find multiple variations by using regex with grep -E.

I struggled with this module the most since this module had the most material to go through. 
I feel like I would have internalized all the information better if we had practice exercises in between sections. 


# Module 3:

This module focused on scripting, configuration files, and installing programs.
For script writing, we got to implement the commands we had learned to write on the command
line in the previous weeks.
To gain a deeper understanding of scripting, we combined the commands we’ve learned in the past couple of weeks with new concepts.
Instead of doing the time-consuming task of running commands one by one in the terminal, 
a script allows you to execute them in a single step. 
We learned how to set environmental variables temporarily and permanently, as well as how to change the values of existing variables.
In addition to that, we learned about command substitution, which allows us to take the output and save it as the value of a variable.

From this module, I gained a deeper understanding of conditional statements and variables. 
I had some previous knowledge about them from an introductory course to programming, 
but the structure used in scripts is very different from what I’ve previously learned. 

Configuration files were a completely new subject to me. 
I found the information about changing your prompt symbol the most interesting, 
since the information displayed there can increase readability. 
I became more familiar with Python by learning to create virtual environments and install packages through pip.



Example code for this module:  
```
#!/bin/bash

echo "Enter filename"
read filename

if [ -f "$filename" ]
then
    echo "$filename exists in the directory"
    cat "$filename"
else
    touch "$filename"
    echo "File created"
fi                                  
```

This code is related to the conditional statements we learned about in this module. 
It creates an empty file if the specified file does not exists


# Module 4:

The first topic for this module was processes. 
The purpose of the topic was to understand what initiating a process in the operating system 
actually entails and how a process can be identified and killed using PID. 

Through practical exercises, we also got a brief introduction to using remote servers on CSC.
The provided videos introduced commands for connecting to a remote server (ssh) and 
for copying files to and from remote servers (scp).
I became more familiar with config files as we learned to create server-specific settings 
for making an SSH connection.
I think my understanding in this area is still a bit lacking, 
as I couldn’t quite grasp how SLURM jobs work. 
I hope I’ll have a chance to practice using CSC more in the future. 

One of the key concepts explored in the last module was learning how to use Git alongside GitHub.
We learned to create, clone and use repositories on both the local computer and on GitHub. 
Through practical exercises, I began to recognise the importance of version control.
As a beginner, I’m bound to make more mistakes, 
which is why it’s crucial to know how to undo the changes.

Here are some git commands to correct mistakes:

1. If you forgot to stage a file, you can add it to the previous commit with:  
```
git commit --amend
```
2. Want to correct a typo in your commit message? Use:  
```
git commit --amend -m "Corrected message"
```
3. Want to revert changes you’ve already pushed to GitHub? Use:  
```
git revert SHA_of_commit
```
4. Want to restore a specific file to the state of the last commit? Use:  
```
git checkout -- altered_file
```
5. To reset local changes, use:  
```
git reset last_good_SHA
```
Some modes of git reset:  
	* --soft: keeps changes staged
	* --mixed (default): unstages changes
	* --hard: discards changes completely
6. Undo _git reset --hard_  
```
git reflog
git reset SHA_for_return
```

For the final project, we learned the basics of making a website. 
This required using Git, GitHub, and Jekyll. 
We learned how to set up Ruby and how to clone and fork a template repository.
I’ve always wanted to learn how to make a website, but it seemed too difficult to learn.
The repository templates make website design more accessible to beginners.


<h2 style="text-align:center;">Thank you for reading!</h2>

<p style="text-align: center;">
    <img src="assets/images/smiling_cat.jpg" alt="A smiling cat">
</p>
