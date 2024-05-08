# Makefiles
Used to automate compile and linking processes for programs. It allows you to compile all the dependencies together in a single step and takes care if any one of them has been modified after the most recent compilation.
Selectively recompiles only the files modified after the last 'make'.

## Syntax
To be exclusively named as "makefile".

- `target` : `prerequisites`
-  ex: `main.out : main.cpp sub.cpp`

Uses a graph structure for representation. All the target at nodes followed by their pre-requisites/dependencies as their children. Thus it finds and recompiles only the files which have some of their children modified.

### Options-
If we want to have some variable parameters to the commands, we can define them at the beginning and the use them in every command.
Ex: 
`CC=g++`
`${CC} main.cpp sub1.cpp`

We can also add flags for optimizations/ parameters for compilations.
Ex:
	`FLAGS=-O3`
	`${CC} main.cpp ${FLAGS] main.o`

- Use `$^` if you want the same prerequisites in the compilations command instead of mentioning each one.
Ex;
	`main.out: main.o sub1.o sub2.o`
	`${CC} ${FLAGS} $^ -o main.out`