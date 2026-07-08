
# Linux Commands

## pwd

### Description
Displays the current working directory.

### Syntax
pwd

### Example
`pwd`

Output:
/home/kali

### Notes
- Does not require any arguments.
- Useful for checking your current location.

---

## ls

### Description
Lists files and directories in the current directory.

### Syntax
ls [option] [directory]

### Parameters

| Parameter | Description |
|-----------|-------------|
| option | Optional flags such as -l or -a |
| directory | The directory to display (optional) |

### Examples
- `ls`
- `ls -l ` show extra information
- `ls -a `show hidden files

---

## mkdir

### Description
Creates a new directory.

### Syntax
mkdir directory_name

### Example
`mkdir CyberLab`

---

## cd

### Description
Changes the current working directory.

### Syntax
cd directory_name

### Examples
```bash
cd CyberLab
cd ..
cd ~ 
```

### Symbols

| Symbol | Meaning |
|--------|---------|
| . | Current directory |
| .. | Parent directory |
| ~ | Home directory |

---

## touch

### Description
Creates a new empty file.

### Syntax
touch filename

### Example
`touch notes.txt`

---

## echo

### Description
Prints text to the terminal or writes text into a file.

### Syntax
echo "text"

To write text into a file:
echo "text" > filename

### Example
`echo "Linux is awesome" > test.txt`

### Notes

- If the file does not exist, it will be created automatically.
- If the file already exists, > replaces its content.
- Use >> to append text instead of replacing it.

---

## cat

### Description
Displays the contents of a file.

### Syntax
cat filename

### Example
`cat test.txt`

---

## cp

### Description
Copies files or directories.

### Syntax
cp source destination

### Example
`cp notes.txt backup.txt`

---

## mv

### Description
Moves or renames files and directories.

### Syntax
mv source destination

### Rename Example
`mv backup.txt notes-copy.txt`

### Move Example
`mv notes.txt Documents/`

---

## rm

### Description
Deletes files or directories.

### Syntax
rm filename

### Example
`rm backup.txt`

To remove a directory:
rm -r folder_name

> Warning: rm permanently deletes files.

---

## whoami

### Description
Displays the current logged-in user.

### Syntax
whoami

### Example
`whoami`

Output:
kali

---

## history

### Description
Displays the list of previously executed commands.

### Syntax
history

### Example
`history`

---

## find

### Description
Searches for files and directories.

### Syntax
find [path] [option] [expression]

### Example
`find . -name notes.txt`

### Breakdown

| Part | Description |
|------|-------------|
| . | Search from the current directory |
| -name | Search by file name |
| notes.txt | Name of the file |

---

## grep

### Description
Searches for specific text inside a file.

### Syntax
grep "text" filename

### Example
`grep Linux test.txt`

Output:
Linux is awesome

---

## man

### Description
Displays the manual page for a command.

### Syntax
man command

### Example
`man ls`

### Notes

- Press q to exit the manual page.
- Useful for learning command options and usage.

-----

## chmod

### Description

The chmod (Change Mode) command is used to change the permissions of files and directories in Linux.

### Syntax
chmod [options] mode file

### Example
`chmod 755 script.sh`

Changes the file permissions to rwxr-xr-x.

## Permission symbol meaning

| Symbol | Meaning |
|--------|---------|
|r| Reading|
|w|Writing|
|x|Execute|

## Permission Targets

| Symbol| Meaning|
|-------|--------|
|u| The user (owner)|
|g| Groub|
|o| Others|
|a| All|

## Permission Operators

| Permission | Meaning |
|------------|------|
| + | Add permission |
| - | Remove permission |
| + | set exact permission |

## Permission Values

| Permission | Value |
|------------|------|
| r | 4 |
| w | 2 |
| x | 1 |

## Common Examples

| Number | Permission |
|---------|------------|
| 644 | rw-r--r-- |
| 750 | rwxr-x--- |
| 755 | rwxr-xr-x |
| 600 | rw------- |

---

# User and Group Commands

## whoami

### Description

Displays the username of the current logged-in user.

### Syntax

```bash
whoami
```

### Example

```bash
whoami
```

Output:

```text
kali
```

---

## id

### Description

Displays the current user's UID, GID, and all groups they belong to.

### Syntax

```bash
id
```

### Example

```bash
id
```

---

## groups

### Description

Displays all groups the current user belongs to.

### Syntax

```bash
groups
```

### Example

```bash
groups
```