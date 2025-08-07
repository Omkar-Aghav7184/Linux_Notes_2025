# 🐧 Linux Command History and mkdir Practice — Omkar

## 📂 Home Directory Contents

```bash
omkar@LAPTOP-4UCI9HKV:~$ ls
'a b c.mp4'   cpTest       file1.txt    hello.log    nanoTest      p1              shortcuts
bin           error.txt    file2.txt    merged.txt   output.txt    pogo_2022.txt   sortTest
catTest       error1.txt   fruits.txt   movies       output1.txt   practice_test   t1.txt

Full History Sample (Start to 1168)
169  cd /home
170  ls
171  ls -a
172  cd .
173  cd ..
174  cd .
175  cd /
176  ls
177  ls srv/
178  ls
179  cd lib
180  ls
181  man
182  man cd
183  man nano
184  cd /
185  ls -a
...
1168  history

mkdir Command History (Filtered)
206  mkdir practice_test
272  mkdir movies
277  mkdir action horror comedy
279  mkdir -p kids/animation/2010.txt
285  man mkdir
301  mkdir p1
317  mkdir test_touch
348  mkdir nanoTest/
357  mkdir rmTest
365  mkdir helloDir/
368  mkdir helloDir/
373  mkdir a/b/c.txt
374  mkdir a/b/c
375  mkdir -p a/b/c
386  mkdir -p testdir/subdir
396  mkdir somedir
401  mkdir subdir/somedir
402  mkdir -p subdir/somedir
422  mkdir cpTest
476  mkdir -p subdir/somdir
610  mkdir sortTest
703  mkdir shortcuts
807  mkdir meals
808  sudo mkdir meals
999  mkdir backend_project_1
1000 sudo mkdir backend_project_1
1055 mkdir catTest
1128 mkdir bin
1169 history | grep "mkdir"

Recent History Commands
1161  crontab -e
1162  cat hello.log
1163  date
1164  cat hello.log
1165  crontab -l
1166  pwd
1167  ls
1168  history
1169  history | grep "mkdir"
1170  history 10

Experimenting with history
omkar@LAPTOP-4UCI9HKV:~$ history | tail
1162  cat hello.log
1163  date
1164  cat hello.log
1165  crontab -l
1166  pwd
1167  ls
1168  history
1169  history | grep "mkdir"
1170  history 10
1171  history | tail

omkar@LAPTOP-4UCI9HKV:~$ history | head
173  cd ..
174  cd .
175  cd /
176  ls
177  ls srv/
178  ls
179  cd lib
180  ls
181  man
182  man cd

omkar@LAPTOP-4UCI9HKV:~$ !!
history | head

//Clearing all history that's why command not found
omkar@LAPTOP-4UCI9HKV:~$ ! 1168
1168: command not found

omkar@LAPTOP-4UCI9HKV:~$ history -c 1168
omkar@LAPTOP-4UCI9HKV:~$ !!
-bash: !!: event not found

Checking and Editing History File
omkar@LAPTOP-4UCI9HKV:~$ echo $HISTSIZE
1000

omkar@LAPTOP-4UCI9HKV:~$ echo $HISTFILESIZE
2000

omkar@LAPTOP-4UCI9HKV:~$ ls -a
.   ..   .bash_history  ... other files ...

omkar@LAPTOP-4UCI9HKV:~$ nano .bash_history

Reset History Behavior
omkar@LAPTOP-4UCI9HKV:~$ history
1  history | tail
2  history
3  echo $HISTSIZE
4  echo $HISTFILESIZE
5  ls -a
6  nano .bash_history
7  history

Deleted Specific Line from History
omkar@LAPTOP-4UCI9HKV:~$ history -d 5
omkar@LAPTOP-4UCI9HKV:~$ history | tail
3  echo $HISTSIZE
4  echo $HISTFILESIZE
5  nano .bash_history
6  history
7  history 5
8  history | tail
9  history | head
10 history
11 history -d 5
12 history | tail



