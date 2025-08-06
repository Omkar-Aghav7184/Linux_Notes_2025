# 🐧 Linux Text Commands Notes (with Examples)

This file contains simple explanations and real examples of useful text-based Linux commands: `cat`, `echo`, `tac`, and `rev`.

---

## 📁 1. `cat` — Concatenate and Display File Content

### 🔹 Description:
`cat` is used to display, create, concatenate, and redirect file content.

### 🔹 Basic Usage:

```bash
cat filename

Displays the content of the file.

🔹 Examples:
cat a.txt
# Output:
abc

cat b.txt
# Output:
xyz

Combine Files:
cat a.txt b.txt
# Output:
abc
xyz

Redirect Combined Output to a File:

cat a.txt b.txt > c.txt
# Content of c.txt becomes:
abc
xyz

Overwrite File:
cat a.txt > c.txt
# c.txt now contains only:
abc

Append File Content:
cat a.txt >> c.txt
# c.txt content becomes:
xyz
abc

Create a File from User Input:

cat > aa.txt
hello
hi
omkar
aghav
# Press Ctrl + C to save and exit

cat aa.txt
# Output:
hello
hi
omkar
aghav

Append to a File from User Input:
cat >> aa.txt
good morning
hardwork
consistency
mindset
# Press Ctrl + C to save

cat aa.txt
# Output:
hello
hi
omkar
aghav
good morning
hardwork
consistency
mindset

2. echo — Print Text or Variables to Terminal or File

🔹 Description:
Used to display a line of text or output to a file.

🔹 Basic Usage:
echo "text"
🔹 Examples:
echo $"deff"
# Output: deff
Avoid writing echo"something" — no space will give an error.

echo "Good Evening Boys" > gn.txt
# Creates gn.txt with:
Good Evening Boys

echo "Good Afternoon Boys" >> gn.txt
# Appends to gn.txt:
Good Evening Boys
Good Afternoon Boys
📁 3. tac — Reverse cat (Print File in Reverse Line Order)
🔹 Description:
Prints the file contents line by line in reverse (bottom to top).

🔹 Example:
cat foods.txt
# Output:
pizza
samosa
vadapav
misalpav
pavbhaji

tac foods.txt
# Output:
pavbhaji
misalpav
vadapav
samosa
pizza
💡 tac is useful for reading logs or data in reverse order.

📁 4. rev — Reverse Characters in Each Line
🔹 Description:
Prints the content of the file with each line's characters reversed.

🔹 Example:
cat fruits.txt
# Output:
apple
banana
mango
chickoo
kiwi

rev fruits.txt
# Output:
elppa
ananab
ognam
ookcihc
iwik

✅ Summary Table
Command	Description	Use Case Example
cat	View or combine file content	cat a.txt b.txt > c.txt
echo	Print or write text to a file	echo "Hello" > file.txt
tac	Reverse the line order in a file	tac foods.txt
rev	Reverse characters of each line in a file	rev fruits.txt