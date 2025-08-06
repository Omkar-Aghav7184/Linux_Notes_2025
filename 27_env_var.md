# Linux Environment Variable Commands – Notes

## 1. `echo $VARIABLE_NAME`

- Used to **display the value** of an environment or shell variable.
- `$` is used to **dereference (get value of)** a variable.

### ✅ Example:
```bash
echo $USER
# Output: omkar
If the variable is not defined, it prints a blank line.
echo $undefinedVar
# Output: (blank)

2. printenv
Displays the environment variables of the current shell session.

Shows KEY=VALUE format.

Can be filtered using grep for specific variables.

✅ Example:
printenv | grep USER
# Output: USER=ooo
Shows variables like PATH, USER, HOME, SHELL, etc.

Does not show shell-only variables that were not exported.

3. export
Used to set and export environment variables so they are available to child processes or subshells.

Makes a variable part of the environment, not just the current shell.

✅ Example:
export name="omkar aghav"
This sets the name variable and exports it.

Now it is available to any nested shell.
Non-exported vs Exported:
name="omkar"
echo $name       # ✅ Available in current shell
bash
echo $name       # ❌ Not available in nested shell

export name="omkar aghav"
bash
echo $name       # ✅ Available in nested shell

4. Summary Table
Command	Purpose
echo $VAR	Displays the value of a variable
printenv	Shows exported environment variables
export VAR=value	Sets and exports a variable to child shells
`printenv	grep VAR`
