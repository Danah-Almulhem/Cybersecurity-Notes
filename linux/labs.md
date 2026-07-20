# Linux labs


## Linux lab 1 - Basic commands.

### Command used

- `pwd` - display the current working directory 

- `ls` - list the files and folders 

- `mkdir Cyberlab` - create a new folder 

- `cd Cyberlab` - entered the folder 

- `touch notes.txt` - creates a file named notes.text 

- `echo "my first linux lab" > notes.txt` - writing into notes.txt 

- `cat notes.txt` - read inside the notes.txt 

- `cp notes.txt notes-copy.txt` - creates a copy from notes.txt 

- `mv notes-copy.txt backup.txt` - change the name of the file 

- `rm backup.txt ` - remove backup.txt file 

---

# Lab 2 - Searching and System Information

## Objective

Learn how to search for files, search inside files, display command history, and use the Linux manual.

## Commands Used
```bash
whoami

history

find . -name notes.txt

man ls

echo "Linux is awesome" > test.txt

grep Linux test.txt

```
## Command Results

### whoami

Displays the current logged-in user.

### history

Displays previously executed commands.

### find . -name notes.txt

Searches for a file named notes.txt starting from the current directory.

### man ls

Opens the manual page for the ls command.

> Press q to exit the manual.

### grep Linux test.txt

Searches for the word Linux inside test.txt.

Output:

Linux is awesome


## What I Learned

- How to identify the current user.

- How to view command history.

- How to search for files.

- How to search for text inside files.

- How to use the Linux manual pages.

## Notes

- man is useful when I forget how to use a command.
- grep searches inside files, not for file names.
- find searches for files and directories.

----

# Lab 3 - Linux File Permissions

## Commands
```bash
touch secret.txt
ls -l
chmod u+x secret.txt
chmod go-w secret.txt
chmod 750 secret.txt
chmod 644 secret.txt
chmod 600 secret.txt
```
## What I learned

- Display file permissions using ls -l.
- Understand the meaning of r, w, and x.
- Permissions are divided into Owner, Group, and Others.
- Change permissions using symbolic mode (`u+x`, `go-w`).
- Change permissions using numeric mode (`750`, 644, `600`).

----

# Lab 4 - Users and Groups

## Objective

Learn how to identify the current user and view group memberships.

## Commands Used

bash
whoami
id
groups


## What I Learned

- Identified the current logged-in user.
- Viewed the user's UID and GID.
- Listed all groups the user belongs to.
- Understood the difference between Owner, Group, and Others.

---

# Lab 5 - File Ownership

## Objective

Learn how to view and modify file ownership.

## Commands Used

```bash
ls -l
groups
sudo chgrp
sudo chown
```

## What I Learned

- Identified the owner and group of a file.
- Learned the purpose of `sudo`.
- Changed the group ownership using `chgrp`.
- Learned how `chown` changes the owner or both the owner and group.

---

# Lab 6 - Viewing and Editing Files

## Objective

Learn how to view, navigate, and edit text files using common Linux commands.

## Commands Used

```bash
cat
less
head
tail
nano
```

## What I Learned

- Displayed the entire contents of a file using `cat`.
- Viewed large files page by page using `less`.
- Displayed the first lines of a file using `head`.
- Displayed the last lines of a file using `tail`.
- Created and edited text files using `nano`.
- Saved changes and exited Nano using keyboard shortcuts.

---

# Lab 7 - Text Processing

## Objective

Learn how to analyze and process text files using common Linux text processing commands.

## Commands Used

```bash
wc
sort
uniq
cut
```

## What I Learned

- Counted lines, words, and characters using `wc`.
- Sorted file contents alphabetically using `sort`.
- Removed duplicate adjacent lines using `uniq`.
- Counted and displayed duplicate lines using `uniq` options.
- Extracted specific fields from a file using `cut`.
- Learned how delimiters and fields work with `cut`.
---

# Lab 8 - grep

## Objective

Learn additional options for the `grep` command.

## Commands Used

```bash
grep -i "linux" notes.txt
grep -n "linux" notes.txt
grep -c "linux" notes.txt
```

## What I Learned

- Used `-i` to ignore letter case.
- Used `-n` to display line numbers.
- Used `-c` to count matching lines.

---
# Lab 9 - Find

## Commands

```bash
touch report.txt

mkdir Projects

find . -name "report.txt"

find . -type f -name "report.txt"

find . -type d -name "Projects"

touch Report.txt

find . -iname "report.txt"
```

## Notes

- `find` → Search for files and directories.
- `.` → Search in the current directory.
- `-name` → Search by exact name (case-sensitive).
- `-iname` → Search by name (case-insensitive).
- `-type f` → Search for files only.
- `-type d` → Search for directories only.

## Examples

```bash
find . -name "notes.txt"

find . -type f -name "report.txt"

find . -type d -name "Projects"

find . -iname "Report.txt"
```
---
# Lab 10 - Pipes

## Objective

Learn how to combine Linux commands using the pipe (`|`) operator.

## Commands Used

```bash
sort fruits.txt | uniq

grep "banana" fruits.txt | wc -l

find . -type f | sort
```

## What I Learned

- Used the pipe (`|`) to pass the output of one command as the input to another.
- Combined `sort` with `uniq` to remove duplicate lines.
- Combined `grep` with `wc -l` to count matching lines.
- Combined multiple commands to make text processing more efficient.
---
# Lab 11 - Output Redirection

## Objective

Learn how to redirect command output into files using `>` and `>>`.

## Commands Used

```bash
echo "Linux" > notes.txt

cat notes.txt

echo "Cybersecurity" > notes.txt

cat notes.txt

echo "Networking" >> notes.txt

cat notes.txt
```

## What I Learned

- Used `>` to redirect command output to a file.
- Learned that `>` overwrites the existing file contents.
- Used `>>` to append output to the end of a file.
- Learned that `>>` preserves the existing file contents.
---
# Lab 12 - cp

## Objective
Learn how to copy files and directories using the `cp` command.

## Commands Used

```bash
touch notes.txt
```

```bash
cp notes.txt notes-backup.txt
```

```bash
mkdir Files
```

```bash
cp notes.txt Files/
```

```bash
mkdir Test
```

```bash
cp -r Test Testcopy
```

```bash
cp -r Files Test
```

## Notes

- Copies files or directories.
- `cp source destination` → Copy a file or directory.
- `cp file1 file2` → Copy a file with a new name.
- `cp file Folder/` → Copy a file into a folder.
- `cp -r Folder1 Folder2` → Copy a directory recursively.
- Without `-r`, directories cannot be copied.
---
# Lab 13 - mv

## Objective

Learn how to move and rename files and directories using the `mv` command.

## Commands Used

```bash
touch notes.txt
```

```bash
mv notes.txt notes_old.txt
```

```bash
mkdir Files
```

```bash
mv notes_old.txt Files/
```

```bash
mkdir Test
```

```bash
mv Test TestFolder
```

## Notes

- Moves or renames files and directories.
- `mv source destination` → Move or rename a file or directory.
- `mv file1 file2` → Rename a file.
- `mv file Folder/` → Move a file into a folder.
- `mv Folder1 Folder2` → Rename or move a directory.
---
# Lab 14 – rm Command

## Objective

Learn how to remove files and directories using the `rm` command.


---

## command used

```bash
touch notes.txt
rm notes.txt
```

Removes the file `notes.txt`.

---



```bash
mkdir Documents
rm -r Documents
```

Removes the directory and all its contents.

---

```bash
touch temp.txt
rm -f temp.txt
```

Removes the file without asking for confirmation.

---

## Notes

- `-r` removes directories recursively.
- `-f` forces deletion without confirmation.
- Use `rm` carefully because deleted files cannot be recovered.