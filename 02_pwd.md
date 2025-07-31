pwd - print name of current/working directory

SYNOPSIS
       pwd [OPTION]...


# 📁 Linux Terminal Practice — `pwd`, `cd`, `ls` Commands

## ✅ Command: `pwd`
**Purpose:**  
Prints the **absolute path** of the current working directory.

### Example:
```bash
omkar@LAPTOP-4UCI9HKV:~$ pwd
/home/omkar


cd /           # Go to root directory
cd home        # Enter the /home directory (from root)
cd ~           # Go to your home directory (/home/omkar)
cd ..          # Go one level up
cd omkar       # Enter omkar directory (inside /home)

cd /
ls
# Output:
# bin  boot  dev  etc  home  lib  media  opt  proc  root  run  sbin  srv  tmp  usr  var
