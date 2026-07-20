
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

**Definition:**

Creates a new directory.

**Syntax:**

```bash
mkdir directory_name
```

**Examples:**

```bash
mkdir Projects
```

```bash
mkdir Folder1 Folder2 Folder3
```

---

## rmdir

**Definition:**

Removes an empty directory.

**Syntax:**

```bash
rmdir directory_name
```

**Example:**

```bash
rmdir Test
```

**Note:**

`rmdir` only removes empty directories.

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

```bash
cp source destination
```

Copy a file or directory.

```bash
cp file1 file2
```

Copy a file with a new name.

```bash
cp file Folder/
```

Copy a file into a folder.

```bash
cp -r Folder1 Folder2
```

Copy a directory recursively.

---

## mv

### Description
## mv

Moves or renames files and directories.

### Syntax
```bash
mv source destination
```

Move or rename a file or directory.

```bash
mv file1 file2
```

Rename a file.

```bash
mv file Folder/
```

Move a file into a folder.

```bash
mv Folder1 Folder2
```

Rename or move a directory.

---

## rm

**Definition:**

Removes files or directories.

**Syntax:**

```bash
rm [option] file_name
```

**Options:**

- `-r` : Remove directories recursively.
- `-f` : Force deletion without confirmation.

**Examples:**

```bash
rm notes.txt
```

```bash
rm -r Documents
```

```bash
rm -f temp.txt
```
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

## Common Options

### -type f

Search for files only.

### -type d

Search for directories only.

### -iname

Search by name (case-insensitive).

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

## Common Options

### `-i`

**Definition**

Ignores uppercase and lowercase letters while searching.

**Syntax**

```bash
grep -i "text" filename
```

**Example**

```bash
grep -i "linux" notes.txt
```

---

### `-n`

**Definition**

Displays the line number of each matching line.

**Syntax**

```bash
grep -n "text" filename
```

**Example**

```bash
grep -n "linux" notes.txt
```

---

### `-c`

**Definition**

Counts the number of matching lines.

**Syntax**

```bash
grep -c "text" filename
```

**Example**

```bash
grep -c "linux" notes.txt
```
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
---

# sudo

## Definition

Runs a command with superuser (root) privileges.

## Syntax

```bash
sudo <command>
```

## Example

```bash
sudo apt update
```

```bash
sudo chown ahmed notes.txt
```

## Common Uses

- Install or remove software.
- Update the system.
- Change file ownership.
- Modify system files.
- Perform administrative tasks.

## When to Use

Use sudo when a command requires administrator (root) privileges.

## When Not to Use

Do not use sudo for normal tasks such as:

- Creating your own files.
- Editing files in your home directory.
- Navigating directories.
- Listing files.

---

# chown

## Definition

Changes the owner of a file or directory.

## Syntax

```bash
chown [owner] filename
```

### Example

```bash
sudo chown ahmed notes.txt
```

Changes the owner of `notes.txt` to `ahmed`.

---

# chgrp

## Definition

Changes the group ownership of a file or directory.

## Syntax

```bash
chgrp [group] filename
```

### Example

```bash
sudo chgrp wireshark notes.txt
```

Changes the group of `notes.txt` to `wireshark`.

---

# cat

## Definition

Displays the entire contents of a file.

## Syntax

```bash
cat filename
```

### Example

```bash
cat notes.txt
```

---

# less

## Definition

Displays a file one page at a time.

## Syntax

```bash
less filename
```

### Example

```bash
less notes.txt
```

---

# head

## Definition

Displays the first lines of a file.

## Syntax

```bash
head filename
head -n filename
```

### Example

```bash
head notes.txt
head -5 notes.txt
```

---

# tail

## Definition

Displays the last lines of a file.

## Syntax

```bash
tail filename
tail -n filename
```

### Example

```bash
tail notes.txt
tail -5 notes.txt
```

---

# nano

## Definition

A simple terminal-based text editor used to create and edit text files.

## Syntax

```bash
nano filename
```

### Example

```bash
nano notes.txt
```

### Useful Shortcuts

- Ctrl + O → Save file
- Ctrl + X → Exit Nano
- Ctrl + W → Search

---
# wc

## Definition

Displays the number of lines, words, and characters in a file.

## Syntax

```bash
wc [option] filename
```

### Example

```bash
wc practice.txt
wc -l practice.txt
wc -w practice.txt
wc -m practice.txt
```

---

# sort

## Definition

Sorts the contents of a file alphabetically.

## Syntax

```bash
sort [option] filename
```

### Example

```bash
sort names.txt
sort -r names.txt
sort -f names.txt
sort names.txt > sorted.txt
```

---

# uniq

## Definition

Removes duplicate adjacent lines from a file.

## Syntax

```bash
uniq [option] filename
```

### Example

```bash
uniq fruits.txt
uniq -c fruits.txt
uniq -d fruits.txt
```

---

# cut

## Definition

Extracts specific fields (columns) from each line of a file using a delimiter.

## Syntax

```bash
cut -d "delimiter" -f field_number filename
```

### Example

```bash
cut -d "," -f1 students.txt
cut -d "," -f2 students.txt
cut -d "," -f3 students.txt
```
---
# Redirection (>)

## Definition

Redirects the output of a command to a file. If the file already exists, its contents are overwritten.

## Syntax

```bash
command > filename
```

### Example

```bash
echo "Linux" > notes.txt
```

---

# Redirection (>>)

## Definition

Appends the output of a command to the end of a file without overwriting its existing contents.

## Syntax

```bash
command >> filename
```

### Example

```bash
echo "Networking" >> notes.txt
```

### Notes

- `>` → Overwrites the file contents.
- `>>` → Appends to the end of the file without overwriting.
---