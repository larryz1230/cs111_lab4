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
```shell
./ext2-create
```
To help debug our program, the command `dumpe2fs cs111-base.img` dumps filesystem information and `fsck.ext2 cs111-base.img` checks your filesystem for correctness.

Now that we have ensured that we have a valid filesystem, we can begin to mount the image onto our filesystem through the following steps.
1. `mkdir mnt` to create a directory to mnt your filesystem to
2. `sudo mount -o loop cs111 -base.img mnt` to mount your filesystem, loop lets you use a file

After these steps, we have successfully mounted our filesystem in mnt directory.

## Cleaning up

To unmount the filesystem:
1. Run `sudo umount mnt` while in the parent directory
2. Then delete the directory used for mounting when you're done `rmdir mnt`

Finally, to clean up all binary files we can use the command `make clean`
