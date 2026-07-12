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