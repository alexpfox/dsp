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

> > * `pwd` - show current working directory path
> > * `mkdir` - creating a directory
> > * `rmdir` - deleting a directory
> > * `touch` - creating a file using `touch` command
> > * `rm` - deleting a file
> > * `mv` - renaming a file
> > * `ls -a` - listing hidden files
> > * `cp -r` directory/ backup/ - copying a file from one directory to another
> > * `cat` - read data from a file
> > * `bash script.sh` - run a bash script
> > * `cd` - change directory
> > * `../` - go up a directory

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

> > * `ls`  - list files
> > * `ls -a`  - list hidden files
> > * `ls -l`  - formatted list
> > * `ls -lh`  - formatted list with extra data
> > * `ls -lah`  - print a pretty, human readable list
> > * `ls -t`  - sort by last edit time
> > * `ls -Glp`  - include a slash if it's a directory, print items in list

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > -R looks handy as you get to display subdirectories, -r for reverse is nice if listing by time and wanting oldest first (-u). <br/>
> > -1 looks especially handy for pretty formatting, -d for sorting only directories.

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs is useful for specifying what text is used inside a command given. <br/>
> > $ \ls | grep Results | xargs touch <br/>
> > this line above would first list the current directory, then look for results matching "Results", then uses Results as the body when opening a new file with touch

 

