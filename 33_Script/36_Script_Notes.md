What is Script?

--> In Linux, a script is a series of commands written in a scripting language(like bash) that can be executed by the shell.

What is Bash?
---> Bash is both a command-line-interpreter (shell) and a scripting language

Creating a simple Script
#!/bin/bash
echo "Hello ,Linux Scripting"

When you execute a script, the system typically relies on the shebang(the #!/bin/bash line  at the beginning of the script) to determine the interpreter that should be used, regardless of the file extension.This allows you to name your scriptswith or without a .sh extension.

How to Execute Script?

1. bash myFirstScript: This explicitly tells the bash shell to execute the script.It's commonly used for Bash Scripts.

2. sh myFirstScript: This instructs the system to use the default shell.

3. source myFirstScript: This runs the script in the current shell session instead of spawning a new process.It's often used to execute scripts that modify the environment , such as setting environment variables.

4. ./myFirstScript: Requires the script to be made executable
If the file is found and has execute permission, the shell executes it using the appropriate interpreter specified in the shebang line.

or
/home/omkar/myFirstScript: Even though you're not explicitly providing the script file to command like cat or echo, you're instructing the shell to execute the script at the given absolute path.The shell takes care of locating the file and using the correct interpreter to run it.

What if you want to run a script as if it were a command, without specifying the path to the script every time.
---> Add the script to a Directory in the PATH variable.

Path: The PATH variable contains a list of directories where the shell looks for executable files.

You can add the directory containing your script file to the PATH environment variable. 