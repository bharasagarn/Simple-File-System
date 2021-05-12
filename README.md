# Simple-File-System
Implementation of a simplified version of the UNIX file system. A project from the course *CSE 30341 Operating System Principles* of the CSE program at the *University of Notre Dame*.

There are 3 levels :
1. Shell - Allow users to perform operations on the file system such as - debug (printing debugging info about FS), format, mount, create a file, copy (data in/out of the FS). Shell will convert these user commands into FS operations such as - FS.debug, FS.format, FS.create, FS.read, FS.write.
2. File System (FS) - Takes FS operations from the shell and acts accordingly on the SimpleFS disk image with the help of the next level ‘Disk Emulator’. FS is responsible for organizing the data structures on disk and performing all necessary operations required for persistent storage and efficient access of data.
3. Disk Emulator - We can’t work on a whole disk, so we rather emulate a disk by dividing a normal file (disk image) into 4096B (4KB) blocks, allowing FS to read/write only in terms of blocks. Operations include - Disk.read, Disk.write.