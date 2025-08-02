
# 🐧 Linux File Sorting and Grep Command Practice

## 📂 Current Directory
```bash
pwd
```
Shows the current working directory.
> Output: `/home/omkar/sortTest`

---

## 📄 List Files
```bash
ls
```
Displays all files in the current directory.

---

## 📏 List Files with Details and Human-readable Size
```bash
ls -lh
```
- Lists files with permissions, owner, size (in KB, MB), and modified time.

---

## 🔤 Sort Files by Size (Ascending)
```bash
ls -lh | sort -k5h
```
- Sorts files by 5th column (size).
- `-k5` → use the 5th column (size)
- `h` → human-readable size sort (K, M, etc.)
- `total 20K` is printed by `ls` by default.

---

## 🔽 Sort Files by Size (Descending)
```bash
ls -lh | sort -k5hr
```
- `r` → reverse order (largest to smallest)
- Same concept, just reverse of above

---

## 🔍 Search for Text in File using `grep`
```bash
cat foods.txt | grep "pizza"
```
- Searches for exact match of `pizza` in `foods.txt`
- No output → not found

```bash
cat foods.txt | grep "paneer"
```
- No output → case-sensitive search didn’t match

```bash
cat foods.txt | grep "Paneer"
```
- Output: `Paneer` → match found with capital "P"

---

## 📉 Display Smallest 3 Files
```bash
ls -lh | sort -k5h | head -3
```
- Shows first 3 lines of the size-sorted list
- Includes `total 20K` line by default

---

## 📈 Display Largest 3 Files
```bash
ls -lh | sort -k5h | tail -3
```
- Shows last 3 (largest) files

---

## ✅ Sort Without Showing `total` Line
```bash
ls -lh | grep -v "^total" | sort -k5h
```
- `grep -v "^total"` removes the `total` line before sorting

---

## 📝 Files Present in Folder
- foods.txt
- fruits.txt
- logs.txt
- numbers.txt
- price.txt

---
