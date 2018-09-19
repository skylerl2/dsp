# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > pwd: print working directory
> > mkdir: make directory
> > rm -R: delete directory and all contents
> > touch filename.txt: create file
> > rm: delete file
> > mv: move file to new location (rename)
> > -a: extension to list all hidden files and folders
> > cp: copy file to specified location
> > ls: list contents of current directory
> > clear: erase the text in the shell


---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > ls: lists contents of current directory
> > ls -a: lists contents of current directory, including hidden files or folders
> > ls -l: lists contents of current directory in long form
> > ls -lh:lists contents of current directory in long form and humanreadable format
> > ls -lah:lists contents of current directory in long form, including hidden files or folders, and humanreadable format
> > ls -t: lists contents of current directory sorted by timestamp
> > ls -Glp: lists contents of current directory in different color text (?) in long form and path format (forward slash at end)

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > -C, -m, -r, -R, -u

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > ### xargs converts standard input into command line input
> > find /directory -name filename -type f -print | xargs /bin/rm -f 
> > ### this will find any file in /directory with "filename" in the name and pass each one individually through the remove command to be deleted
