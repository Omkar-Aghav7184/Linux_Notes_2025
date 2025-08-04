find Command Practice Notes
🔍 Basic Search: find . -name "*.txt"
Finds all .txt files in the current directory and subdirectories.

📂 Search for Specific File Sizes
find . -type f -name "*.txt" -size +1k   # Files greater than 1KB
find . -type f -name "*.txt" -size -1k   # Files smaller than 1KB
find . -type f -size +20M                # Files larger than 20MB
✅ Use lowercase k, m, g for kilobytes, megabytes, gigabytes respectively.
❌ K, M, G are invalid in GNU find.

📁 Find Empty Files and Directories

find . -type f -empty             # Empty files
find . -type d -empty             # Empty directories
🕒 Find Recently Accessed Files
find . -atime -30                 # Accessed in the last 30 days
🧠 Combine Conditions (Logical Operators)
find . \( -name "*.txt" -or -name "*.mp4" \)         # .txt or .mp4 files
find . \( -size +20M -atime -30 -not -size +1k \)    # Complex condition
🧠 Use \( and \) to group expressions.
-and, -or, -not are logical operators.

⚡ Use -exec to Perform Actions
find . -name "*.txt" -exec ls {} \;         # List all .txt files
find . -exec file {} \;                    # Show file type for all
find . -exec echo {} \;                    # Print each file/directory path
🚫 Exclude by Name
find . ! -name "*.txt"          # Files/directories not ending with .txt
🧱 Handling Spaces in Filenames
touch "a b c.mp4"               # Creates a file with spaces
🚨 Avoid using xargs without -0 when files have spaces. Prefer:


find . -type f -print0 | xargs -0 file
💡 Bonus Tips
find . | xargs file → Get file types, but breaks with spaces.

ls -alh → Human-readable file sizes (helps to visually check file size).