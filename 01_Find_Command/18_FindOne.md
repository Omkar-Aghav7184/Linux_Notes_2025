find Command Usage Notes
🔍 Basic Syntax:find [starting_path] [options] [expression]
📁 1. Find by file name: find /home/omkar -name "foods.txt"
Searches for a file exactly named foods.txt in the /home/omkar directory (and subdirectories).

📄 2. Find all .txt files: find /home/omkar -name "*.txt"
Lists all .txt files recursively from /home/omkar.

📂 3. Find folders/directories with specific name pattern find /home/omkar -type d -name "*movies*"
Finds all directories whose names contain the word movies.


find /home/omkar -name "movi*"
Matches names starting with movi (e.g., movies, movie123).

🧾 4. Case-insensitive search

find -iname "filename"
-iname ignores case when matching file or directory names.


find -type f -iname "*file*"
Finds all files (-type f) with names containing "file" (case-insensitive).


find -type d -iname "*test*"
Finds all directories (-type d) with names containing "test" (case-insensitive).

🗃️ 5. Find in current directory

find . -name "*.txt"
Starts search from current directory (.).

🧠 Tips:
-type f: find files only

-type d: find directories only

-name: exact name match (case-sensitive)

-iname: case-insensitive name match