# Simple Notes on `grep`, `tail`, and Related Commands

## Basic `grep` Usage

- **Search for exact word (case-sensitive)**

  ```bash
  grep "meditation" meditations.txt
  ```

- **Search (case-insensitive)**

  ```bash
  grep -i "Meditation" meditations.txt
  ```

- **Search with line numbers**

  ```bash
  grep -n "Meditation" meditations.txt
  grep -in "Meditation" meditations.txt
  ```

- **Count occurrences**

  ```bash
  grep -c "Meditation" meditations.txt
  grep -ic "Meditation" meditations.txt
  ```

- **Match whole word only**

  ```bash
  grep -w "find" meditations.txt
  grep -iw "find" meditations.txt
  ```

- **Search with context lines**

  ```bash
  grep -A3 -B2 "Paneer" foods.txt   # 3 lines after, 2 before
  grep -C2 "Paneer" foods.txt       # 2 lines before and after
  ```

- **Highlight matches (with color)**

  ```bash
  grep --color=auto "meditation" meditations.txt
  ```

- **Lines starting with capital letter**

  ```bash
  grep "^[A-Z]" meditations.txt
  ```

- **Search blank lines**

  ```bash
  grep "^$" meditations.txt
  ```

- **Inverse match (lines NOT containing pattern)**

  ```bash
  grep -v "meditation" meditations.txt
  ```

- **Recursive search in current folder**

  ```bash
  grep -r "Paneer" .
  ```

- **Multiple files**

  ```bash
  grep "^In" -iw meditations.txt foods.txt
  ```

---

## `tail` and Real-Time Monitoring

- **Follow a file live and filter**

  ```bash
  tail -f foods.txt | grep "tomato"
  ```

- **Count specific word occurrences in a file**

  ```bash
  grep -o "tomato" foods.txt | wc -l
  ```

---

## Common Mistakes & Fixes

- ❌ Invalid context option:

  ```bash
  grep -iC "Meditation"
  ```

  ✅ Fix:

  ```bash
  grep -iC2 "Meditation" file.txt
  ```

- ❌ No space after options:

  ```bash
  grep -rw"Pan" foods.txt
  ```

  ✅ Fix:

  ```bash
  grep -rw "Pan" foods.txt
  ```

---

These are essential `grep` usages to help with searching and filtering text efficiently from the terminal.

