## BASH
Bash stands for Born Again Shell. It is programming language used for automation tasks like python. Commands are nothing but functions and options as arguments

## Syntax
```bash
command [options] [arguments]
```
- command : operation to be carried (ls, cd, mkdir)
- options : modify how command works (- or --)
> Single dash (-) Short Options. ex : -l (long listing format), -a (all files) etc single letter. these can be combined.  

> Double dash (--) Long Options. Primarily used for multi character, more descriptive options. ex : ls --size, tar --exclude. 
Double dash explicity indicates end of options, treating subsequent arguments.

- arguments : what command acts on (files, directory etc)

```bash
# Print working directory
pwd

# List files and directory
ls

# options
-l          # Long listing format
-a          # include hidden files (all files)
-h          # human readable sizes
-t          # Sort by modification time
-r          # reverse order while sorting
-R          # list subdirectories recursively
-S          # Sort by file size
-1          # list one file per line
-d          # list directory themselves, not their contents

# Change Directory
cd

# options
/path/to/directory      # go to specific directory
~                       # go to home directory
..                      # go up one level
-                       # go to previous directory
                        # go to home (same as ~)

# Create Directory
mkdir newdirectory

# Create files
touch filename.txt      # Create empty file

# Remove file/ directory
rm filename
rm -r directoryname
rmdir emptydirectory

# options
-r          # delte a folder and everything inside it (recursively)
-i          # ask before deleting each file
-f          # force delete without asking
-v          # verbose mode, show files being removed

# copy
cp sourcefile destinationfile
cp -r sourcedirectory destinationdirectory

# rename
mv oldname newname

# move
mv file newlocation

# file editor nano
nano filename.txt

# search inside file
grep "search_term" filename.txt

# search inside directory
grep -r "search_term" /path

# change permissions
chmod

# help
help            # give complete commands (functions)
help name # gives details about particular command / function

# misc
wget
curl
ip
ping
```
