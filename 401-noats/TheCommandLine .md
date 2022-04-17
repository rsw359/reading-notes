# The Command Line

 A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

## Commands

Navigation

### Keywords & Uses

 **pwd**
    - Print Working Directory - Gives Current Location
 **ls**
    - List - lists files within current directory

Paths

**Absolute Paths** specify a location (file or directory) in relation to the root directory.( Always begin with a slash)

**Relative Paths** specify a location (file or directory) in relation to where we currently are in the system.(Do not begin with a slash)

- **~** (tilde) - This is a shortcut for the home directory. eg, if the home directory is /MacBook/roger then you could refer to the directory Documents with the path /MacBook/roger/Documents or ~/Documents
- **.** (dot) - This is a reference to the current directory. eg in the example above we referred to Documents on line 4 with a relative path. It could also be written as ./Documents
- **..** (dotdot)- This is a reference to the parent directory. You can use this several times in a path to keep going up the hierarchy. eg if you were in the path Macbook/roger you could run the command ls ../../ and this would do a listing of the root directory.

 **cd**

- Change Directory- cd followed by a path moves to the specified dir. CD on its own will move to the root directory

## Everything is a File

With linux everything is actually a file. A text file is a file, a directory is a file, the keyboard is a file (one that the system reads from only), the monitor is a file (one that the system writes to only) etc.

### Important Notes

- Extensions are not used~ to determine what type a particular file is, use **file[path]**
- The command line is case sensitive
- Spaces are used to separate items, so spaces cannot be used in names by default. Instead, use:
  - Quotes around the entire item
  - An escape character, which is a backslash ( \ )

 **ls -a**
    - List All - lists the contents of a directory, including hidden files. Also possible using  **ls --**

## **Manual Pages**

The manual pages are a set of pages that explain every command available on the system including what they do, the specifics of how you run them and what command line arguments they accept

 **man [command]**
    - Invokes the manual pages
 **man -k [search term]**
    - Searches for terms within the manual page. Also possible from within the page using **/[search term**

## File Manipulation

It's important to create a directory structure that will help keep data organized in a manageable way so that it can be efficiently searched and manipulated.

 **mkdir [options] [Directory]**
    - Creates a directory
        - **-p**
        tells mkdir to make parent directories as needed
        - **-v**
        makes mkdir list its steps

 **rmdir [options] [Directory]**
    - Remove directory- rmdir supports the **-v** and **-p** options similar to mkdir.
    - A directory must be empty before it may be removed

 **touch [options] [filename]**
    - Creates a new/blank file

 **cp [options] [source] [destination]**
    - Duplicates a file or directory - by default, this will only copy a file. By using the recursive command, or **-r,** *whole directories may be copied*

 **mv [options] [source] [destination]**
    - Moves a file or directory- the recursive command is not needed to move a directory
        - It is possible to provide a new name for the file or directory when moving it.
        - It is possible to rename a file by giving the same directory as the source, but specifying a different name

 **rm [options] [file]**
    - Delete a file - the recursive command can be used to remove non-empty directories

Information taken from:

[https://ryanstutorials.net/](https://ryanstutorials.net/)

Cheat Sheet!:

[https://ryanstutorials.net/linuxtutorial/cheatsheet.php](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
