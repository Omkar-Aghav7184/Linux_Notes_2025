
# 🐧 Linux Redirection and Basic Command Practice

## 📂 Directory Navigation

```bash
cd ~
ls
```

- `cd ~` → Goes to home directory.
- `ls` → Lists files and folders in the current directory.

---

## 📁 Output Redirection

```bash
ls > output.txt
```
- Redirects standard output (stdout) of `ls` command to `output.txt`.
- Overwrites the file if it already exists.

```bash
ls >> output.txt
```
- Appends the output to `output.txt` instead of overwriting.

---

## 🖨️ Viewing File Content

```bash
cat output.txt
```
- Displays the content of `output.txt`.

---

## 📢 Echo Command & Redirection

```bash
echo "hello 1" >> output.txt
```
- Appends the string `hello 1` to the file.

```bash
echo "hello" 2>> output.txt
```
- Attempts to redirect `stderr` (error), but `echo` does not produce errors.
- `"hello"` is printed on screen.

---

## ❌ Capturing Errors (Standard Error - `stderr`)

```bash
ls -z 2>> error.txt
```
- `ls -z` is invalid; error is redirected to `error.txt`.

```bash
ls -z > output1.txt 2> error1.txt
```
- Redirects:
  - `stdout` → `output1.txt` (will be empty)
  - `stderr` → `error1.txt` (will contain error message)

---

## ✅ Valid Command Redirection

```bash
ls -lh > output1.txt 2> error1.txt
```
- `-l` → long listing format
- `-h` → human-readable sizes
- `output1.txt` gets the correct `ls -lh` output
- `error1.txt` remains empty

---

## 📄 Creating Files with `echo`

```bash
echo "This is file1" > file1.txt
echo "This is file2" > file2.txt
```

- Creates and writes to files using `echo`.

```bash
cat file1.txt
cat file2.txt
```

- Displays the contents of each file.

---

## ❌ Incorrect File Merging Attempt

```bash
echo file1.txt file2.txt >> merged.txt
```

- This appends the **text** `file1.txt file2.txt` to the file.
- ❗ Not actual file content.

### ✅ Correct Way to Merge File Content:
```bash
cat file1.txt file2.txt > merged.txt
```

---

## 📝 Summary of Redirection Operators

| Operator | Description                            |
|----------|----------------------------------------|
| `>`      | Redirect stdout, overwrite file        |
| `>>`     | Redirect stdout, append to file        |
| `2>`     | Redirect stderr (errors), overwrite    |
| `2>>`    | Redirect stderr, append to file        |
| `&>`     | Redirect both stdout and stderr        |
| `<`      | Redirect input from a file             |

---

## ✅ Suggestions to Practice Next

- `sort`, `uniq`, `wc`, `head`, `tail`
- `tee` for display + save
- `man` for help pages

```bash
sort file1.txt
wc -l file1.txt
ls | tee ls_output.txt
man ls
```

