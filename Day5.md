
# `grep` Command

`grep` is used to find patterns in a file or folder.

### Basic Syntax:
```bash
grep [option] "pattern" <file>
```

---

## Examples (logs):

```
Alice lives in apartment A-102, while Bob resides in B-204.
Their friend Carol just moved to Flat C-303.
David, however, prefers house number D-404.
Eve’s address is E-505, and Frank’s is F-606.
The mailing list includes: alice@example.com, bob99@mail.com, carol123@xyz.org.
There’s also an emergency contact: +1-202-555-0173.
Another number is +44-20-7946-0958.
Some random codes: ABC123, XYZ789, and DEF456.
The file was created on 2024-12-25 and last modified on 2025-01-10.
Temperature logs: 22.5°C, 18.3°C, and 19.0°C.
End of log.
```

---

### Example 1:
```bash
grep "in" logs
```
Returns:
```
Alice lives in apartment A-102, while Bob resides in B-204.
The mailing list includes: alice@example.com, bob99@mail.com, carol123@xyz.org.
```
(*Matches "in", "mailing", "includes"*)

---

### Example 2:
```bash
grep -i "in" logs
```
Case-insensitive match.

---

### Example 3:
```bash
grep -w "in" logs
```
Matches only the whole word "in".

---

### Example 4:
```bash
grep -r "in" <folder>
```
Recursively search for "in" inside all files of a folder.

---

### Example 5:
```bash
grep -r -w "in" <folder>
```
Recursive + word match for "in".

---

### Example 6:
```bash
grep -E [reg] <filename>
```
Use extended regular expressions (for `+`, `|`, `{}`, `?`, etc.).

---

### Example 7:
```bash
grep "^In" <fileName>
```
Matches lines that start with "In".

---

### Example 8:
```bash
grep "\b[0-9]{2}\b" <filename>
```
Matches standalone two-digit numbers.

---

### Example 9:
```bash
grep -b "pattern" <fileName>
```
Prints byte offset of each matching line.

---

# `find` Command

```bash
find <directory> <option> <expression>
```

---

### Example 1: Find files by name

```bash
find <dirName> -name <filename>
find <dirName> -name "*.txt"
```
(*Finds files ending with `.txt`*)

---

### Example 2: Find all files in a directory

```bash
find <path>
```

---

### Example 3: Find files by size

```bash
find <dir> -size +100k
```

---

### Example 4: Find files by modification date

```bash
find <dir> -mtime <n>
```

- `-mtime n` → exactly n days ago  
- `-mtime +n` → more than n days ago  
- `-mtime -n` → less than n days ago  

---

### Example 5: Find by type

```bash
find <dir> -type d   # for directories
find <dir> -type f   # for files
```

---

### Example 6: Find excluding a pattern

```bash
find <dir> ! -name "expression"
```

---

### Example 7: Multiple exclude conditions

```bash
find <dir> -type f ! -name "*.txt"
find <dir> -type f ! -name "*.txt" ! -name "*.jpg"
```

---

### Example 8: Find `.mp3` or `.wav` files

```bash
find dummy_fs/ -type f -name "*.mp3" -o -name "*.wav"
```
