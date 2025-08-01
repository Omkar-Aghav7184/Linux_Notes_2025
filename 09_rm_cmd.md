# 🧹 Linux `rm` Command – Complete Notes

The `rm` (remove) command is used to delete files and directories in Unix/Linux systems.

---

## 🔸 Basic File Deletion

```bash
rm filename.txt
Removes a file named filename.txt.

No prompt by default
🔸 Deleting Multiple Files
rm file1.txt file2.txt file3.txt
Deletes all listed files in one go.

 Deleting Empty Directories
 rm -d dirname/
Removes an empty directory.

Will fail if the directory contains any files/subdirectories.

Recursive Directory Deletion
rm -r dirname/

Removes a directory and all of its contents.
Force Delete (No Prompt)
rm -f filename.txt
Deletes the file without confirmation, even if it's write-protected.

🔸 Force Delete Directory (Recursive & No Prompt)
rm -rf dirname/
Deletes everything recursively and silently.

🚨 Extremely powerful and dangerous if misused.

🔸 Interactive Deletion (Safe Mode)
rm -i filename.txt
Prompts before deleting each file.

rm -ri dirname/
Prompts before deleting each item recursively.

🔸 Verbose Deletion
rm -v filename.txt
Displays a message for each deleted file.

rm -rv dirname/
Displays messages while recursively deleting.

🔸 Common Examples
✅ Create and Delete File
touch test.txt
rm test.txt
✅ Create and Delete Empty Directory
mkdir testdir
rm -d testdir

✅ Create and Delete Nested Directory with Files
mkdir -p a/b/c
touch a/b/c/file.txt
rm -r a

🔸 Combine Flags
Command	Description
rm -rf folder/	Force delete folder & all contents
rm -ri folder/	Recursive interactive deletion
rm -rv folder/	Recursive + verbose output
rm -r -f folder/	Equivalent to rm -rf
Use with caution!

$ mkdir rmTest
$ cd rmTest/
$ touch hello.txt
$ ls
hello.txt
$ rm hello.txt
$ ls
$ mkdir helloDir/
$ ls
helloDir
$ rm -d helloDir/
$ mkdir helloDir/
$ rm helloDir/
rm: cannot remove 'helloDir/': Is a directory
$ rm -d helloDir/
$ mkdir -p a/b/c
$ ls
a
$ cd a/b/c
$ touch c.txt
$ cd ../../..
$ rm -r a
$ mkdir -p testdir/subdir
$ touch testdir/fileOne.txt
$ cd testdir
$ ls
fileOne.txt  subdir
$ cd ..
$ rm -r testdir
$ mkdir somedir
$ rm -rf somedir
$ mkdir -p subdir/somedir
$ cd subdir/somedir
$ ls -R
.:
$ cd ../..
$ ls -R
.:
subdir

./subdir:
somedir

./subdir/somedir:
$ rm -rf subdir
$ touch rmTest.txt
$ rm -ri rmTest.txt
rm: remove regular empty file 'rmTest.txt'? y
$ rm -rv rmTest
rm: cannot remove 'rmTest': No such file or directory
$ rm -rv subdir
rm: cannot remove 'subdir': No such file or directory
$ cd ..
$ rm -rv rmTest
removed directory 'rmTest'
