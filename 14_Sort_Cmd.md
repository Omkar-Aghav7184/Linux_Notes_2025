
# 📘 Linux `sort` Command Notes

This document summarizes practical usage of the `sort` command in Linux using example files.

---

## ✅ Files Created

- `foods.txt` – List of food items
- `numbers.txt` – List of numbers
- `logs.txt` – Output of file listings
- `fruits.txt` – Duplicate fruit names
- `price.txt` – Fruit with prices (comma-separated)

---

## 📂 Basic Sorting

### Sort alphabetically (ascending)
```bash
sort foods.txt
```

### Sort alphabetically (descending)
```bash
sort -r foods.txt
```

### Sort numbers (lexicographically)
```bash
sort numbers.txt
```

### Sort numbers (numerically ascending)
```bash
sort -n numbers.txt
```

### Sort numbers (numerically descending)
```bash
sort -nr numbers.txt
```

---

## 📂 Sorting Files by Size in Directory Listing

### Append directory listing to a log file
```bash
ls -lh >> logs.txt
```

### Sort logs by size (5th column, human-readable)
```bash
sort -k5h logs.txt
```

### Sort logs by size (reverse order)
```bash
sort -k5hr logs.txt
```

---

## 📂 Remove Duplicates

### Sort with duplicates (for `fruits.txt`)
```bash
sort fruits.txt
```

### Remove duplicate entries
```bash
sort -u fruits.txt
```

---

## 📂 Sort by Specific Column Using Delimiter

### Sort CSV (comma-separated) by 2nd column numerically
```bash
sort -t',' -k2n price.txt
```

---

## 📂 Count Unique Occurrences

```bash
sort fruits.txt | uniq -c
```

---

## 📂 Display Top/Bottom Results

### Top 3 smallest numbers
```bash
sort -n numbers.txt | head -3
```

### Bottom 3 largest numbers
```bash
sort -n numbers.txt | tail -3
```

---

✅ These examples cover real-world sorting tasks using the Linux `sort` command.
