
# 🐧 Linux Commands Practice Notes - Script Execution & PATH

This markdown file documents and explains all commands used in your terminal session, particularly for working with a script called `hi`. Each command is paired with a simple explanation and example.

---

## 📁 1. Check Current Directory

```bash
pwd
```
**Output:** `/home/omkar`  
🔹 Shows the full path of the current working directory.

---

## 📁 2. List Files

```bash
ls
```
🔹 Lists all files and folders in the current directory.

---

## 📁 3. Create or Edit Script

```bash
nano hi
```
🔹 Opens the file `hi` in nano text editor for writing or editing.

---

## 📁 4. View Script Content

```bash
cat hi
```
🔹 Prints content of the script file.

Example:
```bash
#!/bin/bash
echo "hi $USER"
echo "hi $USER"
...
```

---

## 📁 5. Execute Script (Method 1)

```bash
bash hi
```
🔹 Executes the script using Bash shell.

---

## 📁 6. Execute Script (Method 2)

```bash
sh hi
```
🔹 Executes the script using `sh`. Works unless script has unsupported syntax.

---

## 📁 7. Execute Script Directly

```bash
./hi
```
❌ Error: `Permission denied` (no execute permission yet).

---

## 📁 8. Fix Script Permissions

```bash
chmod a+x hi
```
🔹 Adds execute permission for all users.

Check again:
```bash
ls -l | grep hi
```
Expected: `-rwxr-xr-x`

---

## 📁 9. Direct Execution Works Now

```bash
./hi
```
✅ Outputs multiple lines: `hi omkar`

---

## 📁 10. Source the Script

```bash
source hi
```
🔹 Runs script in the **current shell**. Useful when script modifies environment.

---

## 📁 11. Run with Full Path

```bash
/home/omkar/hi
```
✅ Script runs as expected.

---

## 📁 12. Define and Print Variable

```bash
myVariable=123
echo $myVariable
```
🟢 Output: `123`

Later appears in `source hi` output as well.

---

## 📁 13. Check Command Location

```bash
which pwd
```
🟢 Output: `/usr/bin/pwd`

```bash
which hi
```
❌ No output — `hi` is not in PATH yet.

---

## 📁 14. Check Environment PATH

```bash
echo $PATH
```
🔹 Lists all paths searched for commands.

---

## 📁 15. Organize Custom Scripts

```bash
mkdir bin
mv hi bin
```

Creates a `bin` directory inside home and moves the `hi` script there.

---

## 📁 16. Mistaken Path Check

```bash
ls /bin/hi
```
❌ Not found — your script is in `~/bin`, not `/bin`.

---

## 📁 17. Verify Script Location

```bash
cd bin
ls
```
✅ Confirms that `hi` exists in `~/bin`.

---

## 📁 18. Add `~/bin` to PATH

Edit bash config:
```bash
nano .bashrc
```
Add line at bottom:
```bash
export PATH="$HOME/bin:$PATH"
```

Reload with:
```bash
source .bashrc
```

Now, typing just:
```bash
hi
```
✅ Runs the script globally.

---

## 📁 19. Attempt to Run `hi` (Before PATH Fixed)

```bash
hi
```
❌ Command not found (before `.bashrc` update).

---

## 📁 20. Invalid Relative Execution

```bash
bash hi
sh hi
./hi
```
❌ Fails if not in current directory.

---

## 📁 21. Execute from Absolute Path

```bash
sh ~/bin/hi
./bin/hi
/home/omkar/bin/hi
```
✅ All work fine.

---

## 📁 22. Final Check

```bash
source hi
hi
```
✅ Outputs `hi omkar` multiple times. Final confirmation that setup works.

---

## ✅ Summary of Key Concepts

- Use `chmod +x` to make scripts executable.
- Add personal `~/bin` directory to `$PATH` via `.bashrc`.
- Use `source` when you need variables to persist in the current shell.
- You can run scripts using `bash`, `sh`, or direct path.
- `which` checks if a command is available in your `$PATH`.

---
