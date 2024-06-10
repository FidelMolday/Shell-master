<h1 align="center">Simple Shell</h1>

This is the end of sprint 1 project for the ALX software Engineering class. The task is to develop a simple interactive shell in C.


## Learning Objectives.
By the end of this project, one should have a solid understanding on these concepts, and should be able to explain them to ayone without the help of Gooogle

* [X] Who designed and implemented the original Unix operating system.
* [X] Who wrote the first version of the UNIX shell
* [X] Who invented the B programming language (the direct predecessor to the C programming language)
* [X] Who is Ken Thompson
* [X] How does the shell work
* [ ] What is a pid and a ppid
* [ ] How to manipulate the environment of the current process
* [ ] What is the difference between a function and a system call
* [ ] How to create processes
* [ ] What are the three prototypes of ```main```
* [ ] How does the shell use the PATH to find the programs
* [ ] How to execute another program with the ```execve``` system call
* [ ] How to suspend the execution of a process until one of its children terminates
* [ ] What is ```EOF```  / “end-of-file”?
                                         

## Resources 
[What on Earth is the shell ?](https://en.wikipedia.org/wiki/Unix_shell)

[The thompson shell ](https://en.wikipedia.org/wiki/Thompson_shell)

[The shell and how it works](https://oskarth.com/unix01/)


## List of allowed functions and system calls 
These are the  standard library functions and system calls that are allowed in the project

~~~c
access
chdir
close
closedir
execve
exit
_exit
fflush
fork
free
getcwd
getline
getpid
isatty
kill
malloc
open
opendir
perror
read
readdir
signal
stat
lstat
fstat
strtok
wait
waitpid
wait3
wait4
write
~~~


## Compilation
The program should be compiled this way, without any error

~~~bash
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
~~~

## Testing

The program should look like this in interactive mode 


~~~
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
~~~

but also in non-interactive mode 

~~~

$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
~~~
