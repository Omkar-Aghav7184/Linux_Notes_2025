
# 📁 Linux `ls` Command Cheatsheet

## 🔹 Basic Usage
| Command | Description |
|---------|-------------|
| `ls`    | Lists directory contents (default view) |

### Example:
```bash
ls
# Output: bin  dev  home  etc ...
```

---

## 🔹 Show Hidden Files
| Command | Description |
|---------|-------------|
| `ls -a` | Lists all files, including hidden (. and ..) |

```bash
ls -a
# Output: .  ..  omkar
```

---

## 🔹 Long Listing Format
| Command | Description |
|---------|-------------|
| `ls -l` | Detailed info: permissions, owner, size, date |

```bash
ls -l
```

---

## 🔹 Human Readable File Sizes
| Command | Description |
|---------|-------------|
| `ls -lh` | Show sizes in KB, MB, etc. |

```bash
ls -alh
```

---

## 🔹 Sorted by Time (Newest First)
| Command  | Description |
|----------|-------------|
| `ls -lt` | Sort by modified time (descending) |
| `ls -lht` | Human-readable + time sort |

```bash
ls -alht
```

---

## 🔹 Reverse Order
| Command  | Description |
|----------|-------------|
| `ls -lr` | Reverse alphabetical order |
| `ls -lhr` | Reverse + human-readable |

```bash
ls -alhr
```

---

## 🔹 Oldest First (Time + Reverse)
| Command     | Description |
|-------------|-------------|
| `ls -ltr`   | Oldest modified files first |
| `ls -alhtr` | All, long, human-readable, time+reverse |

```bash
ls -alhtr
```

---

## 🔹 With Disk Usage (Size First)
| Command     | Description |
|-------------|-------------|
| `ls -s`     | Show size in blocks |
| `ls -alhs`  | Size + All + Long + Human Readable |

```bash
ls -alhs
```

---

> 💾 Save this as `ls-command-cheatsheet.md` and use it for daily Linux practice.
