
# 🛡️ Linux `chmod` Command Revision Notes

These notes summarize all your recent practice with the `chmod` command and how file permissions were modified using both symbolic and numeric methods.

---

## 📁 Initial `ls -l` Output

You listed files with `ls -l` and observed the default permissions.

Example:
```
-rw-r--r-- 1 omkar omkar   14 Aug  2 22:47  file1.txt
```
Meaning:
- `rw-` = user (read, write)
- `r--` = group (read)
- `r--` = others (read)

Octal equivalent: `644`

---

## ✅ Symbolic `chmod` Usage

| Command | Description |
|--------|-------------|
| `chmod u+x file1.txt` | Added execute to user |
| `chmod o+w file1.txt` | Added write to others |
| `chmod g+w file1.txt` | Added write to group |
| `chmod g+x file1.txt` | Added execute to group |
| `chmod o+x file1.txt` | Added execute to others |
| `chmod u-x file1.txt` | Removed execute from user |
| `chmod g-x file1.txt` | Removed execute from group |
| `chmod o-x file1.txt` | Removed execute from others |
| `chmod o=w file1.txt` | Set others to write-only |
| `chmod o=r file1.txt` | Set others to read-only |
| `chmod o=x file1.txt` | Set others to execute-only |

---

## ❌ Invalid Usage

| Command | Error Reason |
|--------|---------------|
| `chmod 110110100 file1.txt` | `chmod` doesn’t accept binary directly |
| `chmod 0=w file1.txt` | Invalid format – must use symbolic format like `o=w` |

---

## ✅ Numeric `chmod` Usage

| Command | Description |
|--------|-------------|
| `chmod 665 file1.txt` | Sets: user=rw, group=rw, others=r-x |
| `chmod 664 file1.txt` | user=rw, group=rw, others=r |
| `chmod 777 file1.txt` | user/group/others = rwx |
| `chmod 600 file1.txt` | user=rw, group/others = no access |

---

## 🎯 Tip: Converting Binary to Octal

If you want to use binary (e.g., `110110100`), convert it to octal first:

```
110 110 100 → 6 6 4 → chmod 664
```

Use online tools or calculator (in Programmer mode) to convert binary → octal.

---

## 📌 Permission Values

| Symbol | Octal | Description |
|--------|-------|-------------|
| `r--`  | 4     | read        |
| `-w-`  | 2     | write       |
| `--x`  | 1     | execute     |
| `rw-`  | 6     | read + write |
| `r-x`  | 5     | read + execute |
| `rwx`  | 7     | read + write + execute |

---

### ✅ Always Use:

- `chmod u+rw file.txt` → Add read/write to user
- `chmod go-rwx file.txt` → Remove all from group & others

---
