# 🧪 Bash Command Evaluation Report

## ✅ Correct Arithmetic Commands

```bash
echo $((2+3))      # ➤ 5
echo $((2*3))      # ➤ 6
echo $((2**3))     # ➤ 8 (exponentiation)
echo $((7/3))      # ➤ 2 (integer division)
echo $((17/3))     # ➤ 5
echo $((17%3))     # ➤ 2 (modulo)
echo $((17-3))     # ➤ 14

Correct Subshell Commands
(cd movies/ && ls)         # ✅ Executes 'ls' inside movies/ directory if it exists
(cd movies/ ; ls)          # ✅ Executes both commands, listing after changing directory
(cd moviees/ ; ls)         # ❌ Error: 'moviees' does not exist, then fallback 'ls'
(cd moviees/ || ls)        # ✅ Fallback to ls if directory doesn't exist
(ls;ls)                    # ✅ Runs ls twice

Incorrect or Misused Commands
echo (2+3)       # ❌ Bash sees (2+3) as a subshell, causing syntax error
echo $(2+3)      # ❌ Tries to execute '2+3' as a command – not valid

Correct Way:
echo $((2+3))

Tips and Fixes
Subshell Logic
Use (...) for subshells and conditional sequences:
(cd foldername && ls)
(cd foldername || echo "Failed")

