# Python REGEX

Import Re : imports the regex module

## ****Basic Patterns: Ordinary Characters****

Ordinary characters can be used to perform simple exact matches:

```python
pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")

#returns Match!
```

The match() function returns a match object if the text matches the pattern. Otherwise, it returns None.

Sometimes, the syntax involves backslash-escaped characters, and to prevent these characters from being interpreted as escape sequences, use the raw ’r’ prefix.

## ****Wild Card Characters: Special Characters****

Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. They can be thought of as reserved metacharacters.

With the *search* **function**, you scan through the given string/sequence, looking for the first location where the regular expression produces a match

The *group* **function** returns the string matched by the re.

- A period. Matches any single character except the newline character.
- A caret. Matches the **start** of the string.
- A $ Matches the **end** of the string.
- [abc] Matches a or b or c.
- [a-zA-Z0-9] Matches any letter from (a to z) or (A to Z) or (0 to 9).
- Backslash:
  - If the character following the backslash is a **recognized escape character**
    , then the special meaning of the term is taken
  - Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through .
  - \w Lowercase 'w'. Matches any single letter, digit, or underscore.
  - \W Uppercase 'W'. Matches any character *not* part of (lowercase w).
  - \s Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.
  - \S Uppercase 'S'. Matches any character *not* part of \s
  - \d Lowercase d. Matches decimal digit 0-9.
  - \D Uppercase d. Matches any character that is *not* a decimal digit.
  - \t Lowercase t. Matches tab.
  - \n Lowercase n. Matches newline.
  - \r Lowercase r. Matches return.
  - \A Uppercase a. Matches only at the start of the string. Works across multiple lines as well.
  - \Z Uppercase z. Matches only at the end of the string.
  - \b Lowercase b. Matches only the beginning or end of the word.

### ****Repetitions****

- `+` Checks if the preceding character appears one or more times starting from that position.
- `*` Checks if the preceding character appears zero or more times starting from that position.
- ? Checks if the preceding character appears exactly zero or one time starting from that position.
  - {x} Repeat exactly x number of times.
  - {x, } Repeat at least x times or more.
  - {x, y} Repeat at least x times but no more than y times.

    Regex notes taken from: [https://www.datacamp.com/tutorial/python-regular-expression-tutorial](https://www.datacamp.com/tutorial/python-regular-expression-tutorial)

## **shutil — High-level File Operations**

## Copying Files

copyfile() copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.

Because the function opens the input file for reading, regardless of its type, special files (such as Unix device nodes) cannot be copied as new special files with copyfile().

The copy() function interprets the output name like the Unix command line tool cp. If the named destination refers to a directory instead of a file, a new file is created in the directory using the base name of the source.

The permissions of the file are copied along with the contents.

shutil also interprets commands for:

**Working With Directory Trees:**

- copytreee() recurses through the source directory tree, copying files to the destination. The destination directory must not exist in advance.
- symlinks controls whether symbolic links are copied as links or as files. The default is to copy the contents to new files. If the option is true, new symlinks are created within the destination tree.

    **Finding Files:**

- which() scans a search path looking for a named file. Returns None if the file is not found.

    **Archives:**

- make_archive() creates a new archive file
- unpack_archive() extracts an archive

    **File System Space:**

- disk_usage() returns a tuple with total space

    notes taken from: [https://pymotw.com/3/shutil/](https://pymotw.com/3/shutil/)
