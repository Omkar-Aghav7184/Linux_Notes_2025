# 📘 `man` Command Cheat Sheet — Linux Manual Pages

## 📌 Basic Syntax
```bash
man [command]          # View manual for a command
man man                # Manual for using man itself
man ls                 # List command manual

Example:
man cat

*****************
Commonly Used Man Commands

man ls        # List directory contents
man cat       # Display file content
man cp        # Copy files/directories
man mv        # Move/rename
man rm        # Remove files
man mkdir     # Create directories
man find      # Search files
man grep      # Search in files
man nano      # Edit files
man bash      # Learn shell behavior
help cd       # For shell built-in commands like cd

****************
Navigation Shortcuts (Inside man pages)
Key	Action
↑ / ↓	Scroll line by line
Space	Page down
b	Page up
/text	Search forward for "text"
n	Next search match
q	Quit manual

*****************
1.Searching & Discovering Commands
man -k [keyword]    # Search man pages by keyword (apropos)
man -f [command]    # Show short description (whatis)

Examples:
man -k copy         # Find all commands related to "copy"
man -f ls           # Shows: ls (1) - list directory contents

2.Manual Sections (Interview & Debug Use)
man 5 passwd        # View section 5: file format for /etc/passwd

Section	Description
1	User commands (ls, cp, etc.)
2	System calls (kernel)
3	Library calls
4	Special files (e.g., /dev)
5	File formats & config files
8	Admin/system commands

***********
If this fails:
man cd

Try:
help cd
man bash        # Learn all shell built-in commands
