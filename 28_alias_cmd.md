# Linux Command Notes – Motivational Quotes Setup

## 1. `nano quotes.txt`
- Creates or opens a file named `quotes.txt` in the current directory using the Nano text editor.
- Used to manually add motivational quotes to the file.

---

## 2. `mv quotes.txt nanoTest/`
- Moves the `quotes.txt` file into the `nanoTest` directory.
- Useful for organizing files into specific folders.

---

## 3. `alias quotes= 'cat ~/nanoTest/quotes'`
❌ **Incorrect usage**
- This command has a syntax error: there is an extra space after `=`.
- Also, it’s missing the file extension `.txt`.

✅ **Correct version:**
```bash
alias quotes='cat ~/nanoTest/quotes.txt'

4. nano .bashrc
Opens the .bashrc configuration file (located in the home directory).

You edited this file to add your quotes alias for easier access.

5. source .bashrc
Reloads the .bashrc file so that any changes (like alias creation) take effect immediately.

You did this from both ~/nanoTest and your home directory (~).

6. quotes
Custom alias you created to display your motivational quotes.

Works because you added the alias in .bashrc and sourced it.

7. me
❌ Invalid command

There's no such built-in or custom command named me.

Could be intended for a custom alias like alias me='whoami'.

✅ To create a working me alias: 
alias me='whoami'

✅ Summary
Task	Done Correctly	Notes
Creating and editing quotes file	✅	Used nano quotes.txt
Moving file to nanoTest/	✅	Organized file properly
Creating alias	⚠️	Initially wrong syntax
Editing .bashrc	✅	Added alias manually
Sourcing .bashrc	✅	Alias took effect after sourcing
Using alias	✅	quotes shows file content
Creating me command	❌	Needs a correct alias definition