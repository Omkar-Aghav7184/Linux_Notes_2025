
# 📄 Linux `cp` Command Notes and Practice Summary

The `cp` command is used to copy files and directories in Linux.

---

## ✅ Basic Syntax

```bash
cp [OPTION]... SOURCE DEST
```

---

## 📘 Examples & Practice Log

### 1. Copy a file to another directory
```bash
cp t1.txt /home/omkar/
```

### 2. Copy a file with a new name (rename while copying)
```bash
cp pogo.txt pogo_2022.txt
```

### 3. Copy and preserve metadata (timestamps, mode, ownership)
```bash
cp -p pogo.txt backup_pogo.txt
```

### 4. Copy with verbose mode (shows what's being copied)
```bash
cp -v t2.txt t3.txt /home/omkar/p1
```

### 5. Copy interactively (asks before overwriting)
```bash
cp -i fruits.txt /home/omkar/
```

### 6. Force copy (overwrites without asking)
```bash
cp -f file2.txt /home/omkar
```

### 7. Recursively copy a directory
```bash
cp -r subdir subdir_backup
```

---

## 🧠 Common Errors and Fixes

### ❌ Copying file to same path
```bash
cp t1.txt /home/omkar/cpTest
# Fix: Change the destination file name or directory
```

### ❌ Using `-r` with a regular file
```bash
cp pogo.txt -r movies/kids/animation
# Fix: Remove `-r` for files
cp pogo.txt movies/kids/animation/
```

### ❌ Target directory doesn’t exist
```bash
cp pogo.txt /movies/kids/animation/
# Fix: Use correct relative or absolute path
cp pogo.txt ~/movies/kids/animation/
```

---

## 📂 Directory Setup in Practice

```bash
mkdir -p cpTest
touch cpTest/t1.txt cpTest/t2.txt cpTest/t3.txt

mkdir -p p1/subdir/somdir
touch p1/subdir/somdir/fileUp.txt
```

---

## 📝 Summary Table

| Option | Description |
|--------|-------------|
| `-r`   | Copy directories recursively |
| `-i`   | Prompt before overwrite |
| `-f`   | Force overwrite |
| `-p`   | Preserve mode, ownership, timestamps |
| `-v`   | Verbose mode |

---

