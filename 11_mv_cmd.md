
# 📁 Linux `mv` Command Practice Notes

The `mv` (move) command is used to move or rename files and directories in Linux.

---

## ✅ Correct `mv` Commands Used

```bash
mv pogo_2022.txt /home/omkar
mv backup_pogo.txt backup_pogo_2020.txt
mv 2011.txt 2022.txt /home/omkar/movies/kids/animation/
mv -i 2011.txt 2010.txt/
mv 2022.txt ../2010.txt
mv aq.mp4 ../movies
mv another.mp4 ../horror/another_2024.mp4
mv -v 2011.txt ../~   # moved file into a directory named '~'
```

---

Incorrect Commands and ✅ Corrections (Simplified for Terminal View)
Wrong: cd 2010.txt
Why: You can't cd into a file.
Correct: cd 2010/ (if 2010 is a directory)
Note: Use cd only with directories.

Wrong: mv -v 2011.txt ../
Why: File was already moved into 2010.txt/, so it's no longer in the current folder.
Correct: mv -v 2010.txt/2011.txt ../
Note: Use the correct path to the source file.

Wrong: cd movies/comedy (while inside ~/movies/kids/animation)
Why: The relative path is wrong — movies is not inside animation.
Correct: cd ~/movies/comedy
Note: Use absolute paths (starting with ~) when unsure about current location.

Wrong: another.mp4
Why: It's not a valid command — shell expects a utility or command, not a filename.
Correct: touch another.mp4
Note: Always start with a command like touch, mv, etc.

## 💡 Notes

- `mv source destination` → moves or renames a file or directory.
- `mv -i` → interactive mode; prompts before overwrite.
- `mv -v` → verbose; shows what’s being moved.
- You can move multiple files into a directory using `mv file1 file2 dir/`.
- You **cannot `cd` into a file**; `cd` is for directories only.
- Avoid using special characters like `~` as directory names unless intended.

---

## 📂 Final Structure Snapshot (using `tree`)

```bash
.
├── 2010.txt/
│   └── 2011.txt
├── backup_pogo_2020.txt
├── pogo.txt
├── '~'/
│   └── 2011.txt (moved here)
```

---

## ✅ Summary

The `mv` command is powerful for managing file structures. Always verify paths and file existence before running `mv`, especially when combining with `-i` or `-v` options.
