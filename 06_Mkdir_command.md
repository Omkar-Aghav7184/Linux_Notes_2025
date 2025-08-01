# 📁 `mkdir` Command in Linux

## 🔹 Purpose:
The `mkdir` (make directory) command is used to **create directories** (folders) in the Linux file system.

---

## 📌 Basic Syntax:
```bash
mkdir [options] directory_name
Common Examples
✅ 1. Create a Single Directory: mkdir movies

✅ 2. Create Multiple Directories at Once: mkdir action horror comedy

✅ 3. Create Nested Directories Using -p (Parent): mkdir -p kids/animation/2025
This creates the whole path (kids, animation, and 2025) if they don’t exist.

⚠️ 4. Avoiding Errors
If you don’t use -p, and parent directories are missing, you'll get an error.

If you accidentally try to create a file instead of a directory, it won’t work. mkdir is only for directories.

🛠️ Useful Options
Option	Description
-p	Create parent directories as needed
-v	Print a message for each created directory
--mode=777	Set permissions while creating

Example:
mkdir -p -v myproject/{src,bin,docs}
🧪 Practice Suggestions (To Level Up)
🔄 Navigation & Listing
Commands: cd, cd .., ls, ls -l, ls -R

Try:
cd ~/movies
ls -R
omkar@LAPTOP-4UCI9HKV:~/movies$ cd ~/movies
omkar@LAPTOP-4UCI9HKV:~/movies$ ls -R
.:
action  comedy  horror  kids

./action:

./comedy:

./horror:

./kids:
animation

./kids/animation:
2010.txt

./kids/animation/2010.txt:

🧹 Deleting Directories

rmdir dirname — for empty folders

rm -r dirname — for non-empty folders

Example:
rm -r kids

🔍 Search & Info
man mkdir — see manual

pwd — print current directory

tree — visualize folder structure (install via sudo apt install tree)

omkar@LAPTOP-4UCI9HKV:~$ tree
.
├── movies
│   ├── action
│   ├── comedy
│   ├── horror
│   └── kids
│       └── animation
│           └── 2010.txt
└── practice_test
    └── foods.txt

8 directories, 1 file