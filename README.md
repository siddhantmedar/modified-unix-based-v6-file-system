# Modified Unix V6 File System

A simulation of the Unix V6 file system implemented in C.

## Course

CS 5348.001 - Project 2 Part 2

## Description

This project implements a modified Unix V6 file system with the following commands:

| Command | Description |
|---------|-------------|
| `openfs <file>` | Open an existing V6 file system |
| `initfs <file> <blocks> <inodes>` | Initialize a new file system |
| `cpin <external> <internal>` | Copy external file into V6 filesystem |
| `cpout <internal> <external>` | Copy file from V6 filesystem to external |
| `mkdir <name>` | Create a new directory |
| `rm <file>` | Remove a file |
| `cd <dir>` | Change working directory |
| `pwd` | Print current working directory |
| `rootdir` | List root directory contents |
| `q` / `exit` | Quit the program |

## Building

```bash
gcc mod-v6.c -o modv6
```

Or using CMake:

```bash
mkdir build && cd build
cmake ..
make
```

## Usage

```bash
./modv6
```

Then use the commands listed above interactively.

### Example Session

```
>> initfs myfs 1000 100
>> cpin external.txt internal.txt
>> rootdir
>> cpout internal.txt output.txt
>> q
```
