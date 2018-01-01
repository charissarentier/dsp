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

> > * pwd = show current working directory path
* mkdir = creating a directory
* rmdir = deleting a directory
* touch filen.ext = creating a file using `touch` command
* del filn.ext = deleting a file
* mv oldname newname = renaming a file
* ls -a = listing all, including hidden, files in a directory
* cp source destination = copying a file from one directory to another
* cat filn.ext = print whole file
* echo = look at and print environment details

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

> > `ls` = lists the files in the directory
`ls -a`  = lists all, even hidden, files in the directory
`ls -l`  = lists the files in directory with all details 
`ls -lh` = lists the files in directory with all details, with file size specified in B/K/M/G
`ls -lah`= lists all, even hidden, files in the directory with all details, with file size specified in B/K/M/G
`ls -t`  = lists the files in the directory sorted based on last modified (desc)
`ls -Glp`= lists the files in directory with all details, directories with / (Paths) and with a color highlight (from G)

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > * -u	= displays files by the file access time
* -R = displays subdirectories as well
* -r = displays files in reverse order
* -a = displays all files
* -t = displays newest files first

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > It executes a given command on a series of things in order. For example, if you would want to move every file of a certain type over to a different owner, you'd be able to execute the change of ownership on each of them.

E.g. find / -name .txt | xargs -n 1 chown new_owner

 

