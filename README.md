# Hey! I'm Filing Here

In this lab, I successfully implemented the following 1 MiB ext2 file system with 2 directories (root and lost+found), 1 regular file (hello-world), and 1 symbolic link (hello). Given the ext2 structures and some initial skeleton code, my file system creates a file called cs111-base.img in the current working directory.

## Building

To build the module we can run the following command

```shell
make 	// build the module
```
which creates an executable `ext2-create` in the current working directory.

## Running

After building the source code with the `make` command and obtaining `executable ext2-create` in the current working directory, we can run the executable to create our filesystem image called `cs111-base.img` in our current working directory.


## Cleaning up

TODO
