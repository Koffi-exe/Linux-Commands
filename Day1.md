
# 🐧 Linux Basics – Command Cheat Sheet

## 📁 Navigation & Directory Management

### Print Working Directory
```bash
pwd
```
Shows the full path of your current directory.

### List Directory Contents
```bash
ls
```
Displays files and folders in the current directory.

### Change Directory
```bash
cd <directory-name>
```
Navigates into the specified directory.

### Go Back One Directory
```bash
cd ..
```

### Create a Directory
```bash
mkdir <directory-name>
```

### Remove an Empty Directory
```bash
rmdir <directory-name>
```

### Remove a Non-Empty Directory
```bash
rm -r <directory-name>
```
Deletes the directory and all its contents permanently.

---

## 📄 File Management

### Create an Empty File
```bash
touch <filename>
```

### Write Text into a File (Overwrite)
```bash
echo "Your text here" > <filename>
```

### Append Text to a File
```bash
echo "More text" >> <filename>
```

### View File Contents
```bash
cat <filename>
```

### View File with Pagination
```bash
less <filename>
```
-Scroll a page at a time with Space

-Scroll up with b

-Search with /text

-Exit with q

### Remove a File
```bash
rm <filename>
```

---

## 🎯 Challenge 1: The Secret Message

1. Create a directory named after today's date.
2. Inside it, create **three empty files**.
3. Write a secret message in one of them.
4. View the message using `cat` or `less`.
5. Delete the files and directory afterward.

🛠️ Allowed Commands: `pwd`, `ls`, `cd`, `mkdir`, `rmdir`, `touch`, `echo`, `cat`, `less`

---

## 🎯 Challenge 2: The Project Snapshot

1. Create a directory named `project_snapshot`.
2. Inside, create a file called `log.txt`.
3. Add three lines describing a fictional project.
4. Display the contents using both `cat` and `less`.
5. Append a "timestamped" message using `echo`.
6. Delete everything after reviewing.

🛠️ Allowed Commands: `mkdir`, `cd`, `touch`, `echo`, `cat`, `less`, `rm`, `rmdir`

---
