# Bash Basics (freeCodeCamp)

These notes cover the fundamental Bash commands and concepts learned while working through the freeCodeCamp Relational Databases Certification.

---

# Terminal

The terminal is a command-line interface (CLI) used to interact with the operating system by typing commands.

## Opening the Terminal (GitHub Codespaces)

1. Click the **☰ (Hamburger Menu)**.
2. Select **Terminal**.
3. Click **New Terminal**.

---

# Common Commands

## `echo`

Displays text in the terminal.

```bash
echo hello terminal
```

**Output**

```text
hello terminal
```

---

## `pwd`

**Print Working Directory**

Displays the full path of the directory you are currently in.

```bash
pwd
```

Example:

```text
/workspaces/project
```

---

## `ls`

**List**

Displays the files and folders in the current directory.

```bash
ls
```

Example:

```text
README.md
freeCodeCamp
script.sh
```

### `ls -l`

Lists files and directories in **long list format**, showing additional information such as:

- File type
- File permissions
- Number of links
- Owner
- Group
- File size
- Last modified date and time
- File or directory name

```bash
ls -l
```

Example:

```text
drwxr-xr-x has
-rw-r--r-- package.json
```

- `d` indicates a **directory**
- `-` indicates a **file**

### `ls -a`

**List All**

Displays all files and folders, including hidden files.

```bash
ls -a
```

Example:

```text
.
..
.gitignore
index.html
images
styles.css
```

> Hidden files begin with a period (`.`).

### `ls --help`

Displays the help menu for the `ls` command.

```bash
ls --help
```

Many Linux commands support the `--help` flag to display documentation and available options.

---

## `cd`

**Change Directory**

Moves into another directory.

```bash
cd <folder_name>
```

Example:

```bash
cd freeCodeCamp
```

### `cd ..`

Moves up one directory level.

```bash
cd ..
```

### `cd ../..`

Moves up two directory levels.

```bash
cd ../..
```

Example:

Current directory:

```text
/workspaces/project/node_modules/has
```

Command:

```bash
cd ../..
```

New directory:

```text
/workspaces/project
```

> **Note:** `..` always represents the **parent directory**. Every additional `../` moves you up one more directory level.

Examples:

```bash
cd ..
```

⬆️ Up one level

```bash
cd ../..
```

⬆️⬆️ Up two levels

```bash
cd ../../..
```

⬆️⬆️⬆️ Up three levels

---

## `mkdir`

**Make Directory**

Creates a new directory (folder).

```bash
mkdir <folder_name>
```

Example:

```bash
mkdir website
```

A **directory** and a **folder** mean the same thing.

You can also create nested directories using a path.

Example:

```bash
mkdir client/src
```

This creates a `src` folder inside the `client` folder.

---

## `touch`

Creates a new empty file.

```bash
touch <filename>
```

Example:

```bash
touch index.html
```

You can create multiple files at once.

Example:

```bash
touch index.html styles.css script.js
```

---

## `cp`

**Copy**

Copies a file or directory.

```bash
cp <source> <destination>
```

Example:

```bash
cp background.jpg images/
```

The original file remains in its original location.

---

## `mv`

**Move**

Moves or renames a file or directory.

### Rename a file

```bash
mv <old_filename> <new_filename>
```

Example:

```bash
mv roboto.font roboto.woff
```

### Move a file

```bash
mv logo.png images/
```

The `mv` command can:

- Rename files
- Rename directories
- Move files
- Move directories

---

## `rm`

**Remove**

Deletes a file.

```bash
rm <filename>
```

Example:

```bash
rm background.jpg
```

> **Warning:** `rm` permanently removes files. They are not moved to the Recycle Bin or Trash.

---

## `find`

Searches for files and directories.

Running `find` without any arguments displays the directory tree.

```bash
find
```

Example:

```text
.
./client
./client/src
./images
./images/background.jpg
./index.html
```

---

## `more`

Displays the contents of a file one screen at a time.

```bash
more package.json
```

---

## `clear`

Clears the terminal screen.

```bash
clear
```

---

# Working with Directories

After using `cd`, the terminal prompt changes to show your current directory.

Use `pwd` to display the full path.

```bash
pwd
```

Example:

```text
/workspaces/project/freeCodeCamp
```

Use `ls` to display the contents of the current directory.

```bash
ls
```

Example:

```text
README.md
notes.txt
script.sh
```

Folders are typically displayed in a different color than files.

Files usually include an extension, such as:

```text
README.md
package.json
script.sh
```

Directories generally do not have file extensions.

---

# Working with Paths

Many commands accept a **path** instead of just a filename.

Example:

```bash
mkdir client/src
```

Creates a `src` directory inside the `client` directory.

Another example:

```bash
cp logo.png images/
```

Copies `logo.png` into the `images` folder.

---

# Creating Files and Directories

A common workflow for starting a website project:

```bash
mkdir website
cd website
touch index.html
mkdir images
```

This will:

1. Create a `website` folder.
2. Move into it.
3. Create an `index.html` file.
4. Create an `images` folder.

---

# Common File Management Workflow

Copy a file:

```bash
cp background.jpg images/
```

Delete the original:

```bash
rm background.jpg
```

Rename a file:

```bash
mv roboto.font roboto.woff
```

Display the project tree:

```bash
find
```

Create a nested directory:

```bash
mkdir client/src
```

---

# Hidden Files

Some files are hidden because their names begin with a period (`.`).

Example:

```text
.gitignore
```

Hidden files usually contain configuration settings.

By default, `ls` does **not** display hidden files.

Use:

```bash
ls -a
```

to display them.

---

# Command Flags

A **flag** changes how a command behaves.

Flags are usually added after the command.

Examples:

```bash
ls -l
```

```bash
ls -a
```

```bash
ls --help
```

Many Linux commands support flags to provide additional functionality.

---

# Key Concepts

## Terminal

A program used to interact with the operating system using text commands.

## Command Line Interface (CLI)

A text-based interface used to run commands.

## Directory

Another name for a folder.

## Parent Directory

The directory one level above your current location.

## Working Directory

The directory you are currently using.

## Path

The location of a file or directory within the file system.

Examples:

```text
client/src
images/background.jpg
```

## Prompt

The text displayed before your cursor indicating the current directory.

## File

A document or piece of data stored on your computer.

## File Extension

The letters after the period in a filename that identify the file type.

Examples:

```text
README.md
package.json
script.sh
```

## Hidden File

A file whose name begins with a period (`.`).

Example:

```text
.gitignore
```

## Source

The original file being copied or moved.

Example:

```bash
cp background.jpg images/
```

`background.jpg` is the source.

## Destination

The location where a copied or moved file will be placed.

Example:

```bash
cp background.jpg images/
```

`images/` is the destination.

## Command Flag

An option added to a command to modify its behavior.

Examples:

```bash
ls -l
ls -a
ls --help
```

## HTML

**HyperText Markup Language**

The standard language used to create web pages.

The main page of most websites is named:

```text
index.html
```

---

# Commands Learned

| Command | Description |
|----------|-------------|
| `echo` | Display text in the terminal |
| `pwd` | Print the current working directory |
| `ls` | List files and folders |
| `ls -l` | List files and folders in long list format |
| `ls -a` | List all files and folders, including hidden files |
| `ls --help` | Display help information for the `ls` command |
| `cd` | Change directories |
| `cd ..` | Move to the parent directory |
| `cd ../..` | Move up two directory levels |
| `mkdir` | Create a new directory |
| `touch` | Create a new empty file |
| `cp` | Copy files or directories |
| `mv` | Move or rename files and directories |
| `rm` | Remove files |
| `find` | Display or search the directory tree |
| `more` | Display the contents of a file |
| `clear` | Clear the terminal screen |
