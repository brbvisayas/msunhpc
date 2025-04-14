# 01 – Basic Terminal Navigation

Before running any jobs on the cluster, you'll need to know how to **move around the file system**, see where you are, and list files and directories.

---

## 📍 Where Am I?

To check your current location in the file system, use:

`pwd`

Output example:

`/home/training`

This tells you your present working directory.

## Listing Files

To see what’s in your current directory:

`ls`

Ass options for more detail:

```
ls -l     # Long format with permissions and sizes
ls -a     # Include hidden files
ls -lh    # Human-readable sizes
```

## Changing Directories

Move into a directory with:

`cd foldername`

Go up one level with:

`cd ..`

Return to your home **directory**:

`cd ~`

Go to a specific path:

`cd /shared/scratch/orca`

**Absolute Paths**
```
/home/training
/shared/scratch/orca
```

**Relative Paths**
```
.   # Current directory
..  # Directory above current directory
~   # Your home directory
-   # Previous directory
```

Command
What it does
.
The current directory
..
The parent directory
~
Your home directory
TAB
Auto-complete file/folder names
CTRL + C
Cancel current command

| Command        | What it does |
|----------------|-------------|
| `TAB`     | Auto-complete file/folder names |
| `CTRL + C`   | Cancel current command  |
| `CTRL + D`      | Close current session |