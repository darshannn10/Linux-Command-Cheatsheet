## Basics

- `date` : displays the current time and date
```
┌──(darshan㉿kali)-[~]
└─$ date                            
Thu Dec 21 08:40:05 AM EST 2022
```                        

---

- `cal` : displays a calendar of the current month
```
┌──(darshan㉿kali)-[~]
└─$ cal
   December 2022      
Su Mo Tu We Th Fr Sa  
             1  2  3  
 4  5  6  7  8  9 10  
11 12 13 14 15 16 17  
18 19 20 21 22 23 24  
25 26 27 28 29 30 31               
```
---

- `df` : the current amount of free space on our disk drives
```
┌──(darshan㉿kali)-[~]
└─$ df  
Filesystem     1K-blocks     Used Available Use% Mounted on
udev             1967972        0   1967972   0% /dev
tmpfs             402392      976    401416   1% /run
/dev/sda1       81000912 25544808  51295492  34% /
tmpfs            2011956        0   2011956   0% /dev/shm
tmpfs               5120        0      5120   0% /run/lock
tmpfs             402388       72    402316   1% /run/user/1001
              
```
---
- `free` : display the amount of free memory
```
┌──(darshan㉿kali)-[~]
└─$ free   
               total        used        free      shared  buff/cache   available
Mem:         4023912      620728     2735516        8572      667668     3169552
Swap:         998396           0      998396
                                           
```
---

## 𝐍𝐚𝐯𝐢𝐠𝐚𝐭𝐢𝐨𝐧

- `pwd` : print working directory
```
┌──(darshan㉿kali)-[~]
└─$ pwd                 
/home/darshan
                
```
---

- `cd` : change directory
```
┌──(darshan㉿kali)-[~]
└─$ cd practise           
                                                                                       
┌──(darshan㉿kali)-[~/practise]
└─$ pwd
/home/darshan/practise
                                                                                       
┌──(darshan㉿kali)-[~/practise]
└─$ ls 
hackthebox

```
---

- `cd` shortcuts

Shortcut | Result
---|---
cd | Changes the working directory to your home directory.
cd - | Changes the working directory to the previous working directory.
cd ~user_name | Changes the working directory to the home directory of user_name. For example, typing cd ~bob will change the directory to the home directory of user “bob.”

---

- `ls` : List directory contents
>   - `ls -l`: output in long format
>   - `ls -t`: the t option to sort the result by the file’s modification time.
>   - `ls -lt --reverse`: --reverse to reverse the order of the sort.
```
┌──(darshan㉿kali)-[~]
└─$ ls
BugBounty  Documents  Music     practise  Templates
Desktop    Downloads  Pictures  Public    Videos
                                                                                       
┌──(darshan㉿kali)-[~]
└─$ ls /usr      
bin  games  include  lib  lib32  lib64  libexec  libx32  local  sbin  share  src                                                                                      
                                                                                       
┌──(darshan㉿kali)-[~/Desktop]
└─$ ls -l 
total 112
drwxr-xr-x  3 darshan darshan  4096 Aug 30 14:40 Binary_Exploitation
drwxr-xr-x  3 darshan darshan  4096 Nov  6 15:18 Bounty
drwxr-xr-x  2 darshan darshan  4096 Sep  8 03:12 hashes
drwxr-xr-x  8 darshan darshan  4096 Dec  4 00:55 PentesterLab
-rw-r--r--  1 darshan darshan  5493 Nov  8 10:26 php-rev-shell.php
drwxr-xr-x  3 darshan darshan  4096 Dec  4 00:58 PicoCtf
-rw-r--r--  1 darshan darshan 73728 Dec  4 14:10 squirrelwaffle.dll
drwxr-xr-x 27 darshan darshan  4096 Nov  8 04:45 TryHackMe
drwxr-xr-x  2 darshan darshan  4096 Sep 24 07:15 tty_shells
drwxr-xr-x  4 darshan darshan  4096 Dec  5 10:11 workspace                                                                                                                       
                                                                            
┌──(darshan㉿kali)-[~/Desktop]
└─$ ls -lt
total 112
drwxr-xr-x  4 darshan darshan  4096 Dec  5 10:11 workspace
-rw-r--r--  1 darshan darshan 73728 Dec  4 14:10 squirrelwaffle.dll
drwxr-xr-x  3 darshan darshan  4096 Dec  4 00:58 PicoCtf
drwxr-xr-x  8 darshan darshan  4096 Dec  4 00:55 PentesterLab
-rw-r--r--  1 darshan darshan  5493 Nov  8 10:26 php-rev-shell.php
drwxr-xr-x 27 darshan darshan  4096 Nov  8 04:45 TryHackMe
drwxr-xr-x  3 darshan darshan  4096 Nov  6 15:18 Bounty
drwxr-xr-x  2 darshan darshan  4096 Sep 24 07:15 tty_shells
drwxr-xr-x  2 darshan darshan  4096 Sep  8 03:12 hashes
drwxr-xr-x  3 darshan darshan  4096 Aug 30 14:40 Binary_Exploitation
          
          
┌──(darshan㉿kali)-[~/Desktop]
└─$ ls -lt --reverse
total 112
drwxr-xr-x  3 darshan darshan  4096 Aug 30 14:40 Binary_Exploitation
drwxr-xr-x  2 darshan darshan  4096 Sep  8 03:12 hashes
drwxr-xr-x  2 darshan darshan  4096 Sep 24 07:15 tty_shells
drwxr-xr-x  3 darshan darshan  4096 Nov  6 15:18 Bounty
drwxr-xr-x 27 darshan darshan  4096 Nov  8 04:45 TryHackMe
-rw-r--r--  1 darshan darshan  5493 Nov  8 10:26 php-rev-shell.php
drwxr-xr-x  8 darshan darshan  4096 Dec  4 00:55 PentesterLab
drwxr-xr-x  3 darshan darshan  4096 Dec  4 00:58 PicoCtf
-rw-r--r--  1 darshan darshan 73728 Dec  4 14:10 squirrelwaffle.dll
drwxr-xr-x  4 darshan darshan  4096 Dec  5 10:11 workspace
                                                                                                   
```
---

- `file filename` :  the file command will print a brief description of the file’s contents
```
┌──(darshan㉿kali)-[~/Desktop/TryHackMe]
└─$ file flag.txt             
flag.txt: ASCII text, with no line terminators
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/TryHackMe]
└─$ file pack.ovpn 
pack.ovpn: ASCII text

```
---

- `less` : allows us to scroll forward and backward through a text file.
  - `Note: less is more. Means both commands are same` 
```
┌──(darshan㉿kali)-[~/Desktop/TryHackMe]
└─$ cat example | less
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/TryHackMe]
└─$ less example
```

Command | Action
--- | ---
`PAGE UP` or `b` | Scroll back one page
`PAGE DOWN` or `space` | Scroll forward one page
`Up arrow` | Scroll up one line
`Down arrow` | Scroll down one line
`G` | Move to the end of the text file
`1G` or `g` | Move to the beginning of the text file
`/characters` | Search forward to the next occurrence of characters
`n` | Search for the next occurrence of the previous search
`h` | Display help screen
`q` | Quit less


---

## 𝐌𝐚𝐧𝐢𝐩𝐮𝐥𝐚𝐭𝐢𝐧𝐠 𝐟𝐢𝐥𝐞𝐬 𝐚𝐧𝐝 𝐝𝐢𝐫𝐞𝐜𝐭𝐨𝐫𝐢𝐞𝐬

- Wildcards:

Wildcards | Meaning
--- | ---
`*` | Matches any character
`?` | Matches any single character
`[characters]` | Matches any character that is a member of the set characters
`[!characters]` | Matches any character that is not a member of the set characters
`[:class:]]` | Matches any character that is member of the specified class

- List of most commonly used character classes

Character class | Meaning
--- | ---
`[:alnum:]` | Matches any alphanumeric character
`[:alpha:]` | Matches any alphabetic characters
`[:digit:]` | Matches any numerical
`[:lower:]` | Matches any lowercase letter
`[:upper:]` | Matches any uppercase


- Wildcard examples:

Pattern | Matches
--- | ---
`*` | All files
`g*` | Any file beginning with g
`b*.txt` | Any file beginning with b followed by any characters and ending with .txt
`Data???` | Any file beginning with Data followed by exactly three characters
`[abc]*` | 	Any file beginning with either an a, a b, or a c
`BACKUP.[0-9][0-9][0-9]` | Any file beginning with BACKUP. followed by exactly three numerals
`[[:upper:]]*` | Any file beginning with an uppercase letter
`[![:digit:]]*` | Any file not beginning with a numeral
`*[[:lower:]123]` | Any file ending with a lowercase letter or the numerals 1, 2, or 3

- `Wildcards can be used with any command that accepts filenames as arguments`

---

- `mkdir` - make directory
    - `mkdir dir` - single directory
    - `mkdir dir1 dir2 dir3` - multiple directories
    
    
```
┌──(darshan㉿kali)-[~/Desktop/practise]
└─$ mkdir commandline
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise]
└─$ ls
commandline  TryHackMe


┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ mkdir dir1 dir2 dir3
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ ls
dir1  dir2  dir3

```
---

- `cp` - copy files and directories
    - `cp item1 item2` : copy single file item1 into item2
    - `cp item... directory` : copies multiple items (either files or directories) into a directory.

Option | Meaning
--- | ---
`-a`,`--archive` | Copy the files and directories and all of their attributes, including ownerships and permissions.
`-i`, `--interactive` | Before overwriting an existing file, prompt the user for confirmation. 
`-r`, `--recursive` | Recursively copy directories and their contents. This option (or the -a option) is required when copying directories.
`-u`, `--update` | When copying files from one directory to another, only copy files that either don’t exist or are newer than the existing corresponding files in the destination directory. This is useful when copying large numbers of files as it skips files that don’t need to be copied
`-v`, `--verbose` | Display informative messages as the copy is performed.

- `mv` is same as `cp`

---

- `rm file` : remove files and directories
- `rm -rf file` : remove entire directory in one command

Option | Meaning
--- | ---
`-i`, `--interactive` | Before deleting an existing file, prompt the user for confirmation.
`-r`, `--recursive` | Recursively delete directories. This means that if a directory being deleted has subdirectories, delete them too. To delete a directory, this option must be specified.
`-f`, `--force` | Ignore nonexistent files and do not prompt. This overrides the --interactive option.
`-v`, `--verbose` | Display informative messages as the deletion is performed.

---

- `ln` : create links
    - `ln file link` : create a hard link
    - `ln -s item link` : creates a symbolic link

---

## 𝐖𝐨𝐫𝐤𝐢𝐧𝐠 𝐰𝐢𝐭𝐡 𝐜𝐨𝐦𝐦𝐚𝐧𝐝𝐬

- `type`: is a shell builtin that displays the kind of command the shell will execute

```
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ type ls                          
ls is an alias for ls --color=auto
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ type ssh
ssh is /usr/bin/ssh
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ type cd 
cd is a shell builtin
                          
```
---

- `which` : Display an Executable’s Location

```
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ which ls               
ls: aliased to ls --color=auto
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ which pwd
pwd: shell built-in command
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ which cd 
cd: shell built-in command
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ which gedit
/usr/bin/gedit
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ which firefox
/usr/bin/firefox
                       
```

---

- `man` : Display a Program’s Manual Page

```
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ man ls         
```

```
LS(1)                               User Commands                              LS(1)

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

DESCRIPTION
       List  information  about  the FILEs (the current directory by default).  Sort
       entries alphabetically if none of -cftuvSUX nor --sort is specified.

       Mandatory arguments to long options are mandatory for short options too.

       -a, --all
              do not ignore entries starting with .

       -A, --almost-all
              do not list implied . and ..

       --author
              with -l, print the author of each file

 Manual page ls(1) line 1 (press h for help or q to quit)

```

---

- `apropos` - Display Appropriate Commands

```
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ apropos copy
cifsdd (8)           - convert and copy a file over SMB
COPY (7)             - copy data between a file and a table
cp (1)               - copy files and directories
cpgr (8)             - copy with locking the given file to the password or group file
cpio (1)             - copy files to and from archives
cppw (8)             - copy with locking the given file to the password or group file
dd (1)               - convert and copy a file
debconf-copydb (1)   - copy a debconf database
docker-container-cp (1) - Copy files/folders between a container and the local filesystem
docker-cp (1)        - Copy files/folders between a container and the local filesystem
git-checkout-index (1) - Copy files from the index to the working tree
install (1)          - copy files and set attributes
llvm-objcopy-13 (1)  - object copying and editing tool
mariadb-hotcopy (1)  - a database backup program
mysqlhotcopy (1)     - a database backup program
ntfscp (8)           - copy file to an NTFS volume.
objcopy (1)          - copy and translate object files
ptrepack (1)         - Copy any PyTables Leaf, Group or complete subtree into another file.
rcp (1)              - OpenSSH secure file copy
rsync (1)            - a fast, versatile, remote (and local) file-copying tool
scp (1)              - OpenSSH secure file copy
ssh-copy-id (1)      - use locally available keys to authorise logins on a remote machine
svnversion (1)       - Produce a compact version identifier for a working copy.
vfs_shadow_copy (8)  - Expose snapshots to Windows clients as shadow copies.
vfs_shadow_copy2 (8) - Expose snapshots to Windows clients as shadow copies.
x86_64-linux-gnu-objcopy (1) - copy and translate object files
                                                                                       
```

---

- `whatis` : Display One-line Manual Page Descriptions

```
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ whatis rm    
rm (1)               - remove files or directories
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ whatis rm    
rm (1)               - remove files or directories
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ whatis sudo
sudo (8)             - execute a command as another user
                            
```

---

- `info` : Display a Program’s Info Entry

```
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ info ls

```

```
Next: dir invocation,  Up: Directory listing

10.1 ‘ls’: List directory contents
==================================

The ‘ls’ program lists information about files (of any type, including
directories).  Options and file arguments can be intermixed arbitrarily,
as usual.

   For non-option command-line arguments that are directories, by
default ‘ls’ lists the contents of directories, not recursively, and
omitting files with names beginning with ‘.’.  For other non-option
arguments, by default ‘ls’ lists just the file name.  If no non-option
argument is specified, ‘ls’ operates on the current directory, acting as
if it had been invoked with a single argument of ‘.’.

   By default, the output is sorted alphabetically, according to the
locale settings in effect.(1)  If standard output is a terminal, the
output is in columns (sorted vertically) and control characters are
output as question marks; otherwise, the output is listed one per line
and control characters are output as-is.

-----Info: (coreutils)ls invocation, 56 lines --Top------------------------------------
Follow xref: gument is specified, ‘ls’ operates on the current directory, acting asif 
```

---

- `alias` : Creating Our Own Commands with alias
    - `trick: It’s possible to put more than one command on a line by separating each command with a semicolon`
    - `command1; command2; command3...`

```
[me@linuxbox ~]$ cd /usr; ls; cd -
bin  games  include  lib  local  sbin  share  src
/home/me
[me@linuxbox ~]$
```
```
[me@linuxbox ~]$ type foo
bash: type: foo: not found
```
```
[me@linuxbox ~]$ alias foo='cd /usr; ls; cd -'
[me@linuxbox ~]$ foo
bin  games  include  lib  local  sbin  share  src
/home/me
[me@linuxbox ~]$
[me@linuxbox ~]$ type foo
foo is aliased to `cd /usr; ls; cd -'
```
```
[me@linuxbox ~]$ unalias foo
[me@linuxbox ~]$ type foo
bash: type: foo: not found
```

---

## 𝐑𝐞𝐝𝐢𝐫𝐞𝐜𝐭𝐢𝐨𝐧

- `<command> > <file>` : Redirecting Standard Output

```
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ ls -l /usr/bin > ls-output.txt
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ ls -l                         
total 200
drwxr-xr-x 2 darshan kali   4096 Dec 23 08:52 dir1
drwxr-xr-x 2 darshan kali   4096 Dec 23 08:52 dir2
drwxr-xr-x 2 darshan kali   4096 Dec 23 08:52 dir3
-rw-r--r-- 1 darshan kali 191762 Dec 23 08:59 ls-output.txt

                                                                   
```

---

- `command >> file` - append redirected output to a file instead of overwriting the file

```
[me@linuxbox ~]$ ls -l /usr/bin >> ls-output.txt
```

---

- `0>` OR `<` : redirecting standard input
- `>` : redirecting standard output
- `2>` : redirecting standard error

```
[me@linuxbox ~]$ ls -l /bin/usr 2> ls-error.txt
```

---

- `ls -l /bin/usr > ls-output.txt 2>&1` OR ` ls -l /bin/usr &> ls-output.txt`: Redirecting Standard Output and Standard Error to One File
- `ls -l /bin/usr 2> /dev/null` : Disposing unwanted output

---

- `command1 | command2` : Pipeline
- `wc` : Print line, Word, and Byte counts
- `grep` : print line matching pattern
- `head -n <number of lines> ls-output.txt` : print initial lines of file
- `tail -n <number of lines> ls-output.txt` : print last lines of files 
- `tee` : Read from Stdin and Output to Stdout and Files
- 

```
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ wc ls-output.txt 
  2812  26863 191762 ls-output.txt

```
```
[me@linuxbox ~]$ head -n 5 ls-output.txt
total 343496
-rwxr-xr-x 1 root root       31316 2017-12-05 08:58 [
-rwxr-xr-x 1 root root        8240 2017-12-09 13:39 411toppm
-rwxr-xr-x 1 root root      111276 2017-11-26 14:27 a2p
-rwxr-xr-x 1 root root       25368 2016-10-06 20:16 a52dec
[me@linuxbox ~]$ tail -n 5 ls-output.txt
-rwxr-xr-x 1 root root        5234 2017-06-27 10:56 znew
-rwxr-xr-x 1 root root         691 2015-09-10 04:21 zonetab2pot.py
-rw-r--r-- 1 root root         930 2017-11-01 12:23 zonetab2pot.pyc
-rw-r--r-- 1 root root         930 2017-11-01 12:23 zonetab2pot.pyo
lrwxrwxrwx 1 root root           6 2016-01-31 05:22 zsoelim -> soelim
```

---

## 𝐒𝐞𝐞𝐢𝐧𝐠 𝐭𝐡𝐞 𝐰𝐨𝐫𝐥𝐝 𝐚𝐬 𝐭𝐡𝐞 𝐬𝐡𝐞𝐥𝐥 𝐬𝐞𝐞𝐬 𝐢𝐭

- `echo` : Display a line of text
    - `echo *` : works same as `ls`
    - `echo D*` : Display files/directories which starts with D
    - `echo *s` : Display files/drectories which ends with s
    - `echo [[:upper:]]*` : Display files/directories that starts with uppercase letters 
    - `echo /usr/*/share` : display all directories between /usr/ & /share
    - `echo ~` : tilde expansion

```
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ echo hello there, my name is darshan!
hello there, my name is darshan!
                                                                                       
┌──(darshan㉿kali)-[~/Desktop/practise/commandline]
└─$ echo *                               
dir1 dir2 dir3 ls-output.txt
                                                                                       
┌──(darshan㉿kali)-[~]
└─$ echo D*
Desktop Documents Downloads
                                                                                       
┌──(darshan㉿kali)-[~]
└─$ echo *s
Documents domains Downloads Pictures SecLists Templates Videos
                                                                                       
┌──(darshan㉿kali)-[~]
└─$ echo [[:upper:]]*
Binary_Exploitation Bounty PentesterLab PicoCtf TryHackMe
                                                                                       
┌──(darshan㉿kali)-[~]
└─$ echo /usr/*/share  
/usr/local/share
                                                                                      
┌──(darshan㉿kali)-[~]
└─$ echo ~           
/home/darshan
                                                                                  
```

- Arithmetic Expansion:
    - `$((expression))` 
   
```                                                                                      
┌──(darshan㉿kali)-[~]
└─$ echo $((2 + 2))
4

┌──(darshan㉿kali)-[~]
└─$ echo $(($((5**2)) * 3))
75
      
```

Operator | Description
--- | ---
`+` | Addition
`-` | Subtraction
`*` | Multiplication
`/` | Division (but remember, since expansion supports only integer arithmetic, results are integers)
`%` | Modulo, which simply means “remainder”
`**` | Exponentiation

- Brace Expansion: create multiple text strings from a pattern containing braces

```
┌──(darshan㉿kali)-[~]
└─$ echo Front-{A,B,C}-Back
Front-A-Back Front-B-Back Front-C-Back
                                                                                       
┌──(darshan㉿kali)-[~]
└─$ echo Number_{1..5}
Number_1 Number_2 Number_3 Number_4 Number_5
                                                                                       
┌──(darshan㉿kali)-[~]
└─$ echo {01..15}
01 02 03 04 05 06 07 08 09 10 11 12 13 14 15
                                                                             ┌──(darshan㉿kali)-[~]
└─$ echo a{A{1,2},B{3,4}}b
aA1b aA2b aB3b aB4b

                                                   
```

- Parameter expansion: `echo $var`
- Command Substitution
    -  `echo $(ls)`
    -  `ls -l $(which cp)`
    -  `file $(ls -d /usr/bin/* | grep zip)`
   
---

- Quoting:
    - Double Quotes: If we place text inside double quotes, all the special characters used by the shell lose their special meaning and are treated as ordinary characters. The exceptions are $ (dollar sign), \ (backslash), and ` (backtick).
    - Single Quotes: If we need to suppress all expansions, we use single quotes.
- Escaping Characters:
    - `\` : is used for escaping
- Backslash Escape Situation:

Escape Sequence | Meaning
--- | ---
`\a` | Bell (an alert that causes the computer to beep)
`\b` | Backspace
`\n` | Newline; on Unix-like systems, this produces a line feed
`\r` | Carriage return
`\t` | tab

```
┌──(darshan㉿kali)-[~]
└─$ sleep 10; echo -e "Time's up\a"
Time's up
           
```
---

## 𝐀𝐝𝐯𝐚𝐧𝐜𝐞𝐝 𝐊𝐞𝐲𝐛𝐨𝐚𝐫𝐝 𝐓𝐫𝐢𝐜𝐤𝐬

- `clear` : Clear the terminal screen
- `history` : Display or manipulate the history list

- Cursor Movement:

Key | Action
--- | ---
`CTRL-A` | Move the cursor to the beginning of line
`CTRL-E` | Move cursor to the end of the line
`CTRL-F` | Move cursor forward one character; same as the right arrow key
`CTRL-B` | Move cursor backward one character; same as the left arrow key
`ALT-F` | Move cursor one word forward
`ALT-B` | Move cursor backward one word
`CTRL-L` | Clear screen and move the cursor to the top left corner. Same as `clear` command

---
- Modifying Text


Key | Action
--- | ---
`CTRL-D` | Delete the character at the cursor location
`CTRL-T` | Transpose the character at the cursor location
`ALT-T` | Transpose the word at the cursor location with the one preceding it.
`ALT-L` | Convert the characters from the cursor location to the end of the word to lowercase.
`ALT-U` | Convert the characters from the cursor location to the end of the word to uppercase.

---

- History Expansion

Sequence | Action
--- | ---
`!!` | Repeat the last command. It is probably easier to press the up arrow and ENTER
`!number` | Repeat history list item `number`.
`!string` | Repeat last history list item starting with `string`
`!?string` | Repeat last history list item containing  `string`


---

## 𝐏𝐞𝐫𝐦𝐢𝐬𝐬𝐢𝐨𝐧𝐬

- `id` : Display user identity
- `chmod` : Change a file’s mode
- `umask` : Set the default file permissions
- `su` : Run a shell as another user
- `sudo` : Execute a command as another user
- `chown`: Change a file’s owner
- `chgrp`: Change a file’s group ownership
- `passwd`: Change a user’s password

- Permission attribute Examples:

File Attributes | Meaning
--- | ---
`-rwx------` | A regular file that is readable, writable, and executable by the file’s owner. No one else has any access.
`-rw-------` | A regular file that is readable and writable by the file’s owner. No one else has any access.
`-rw-r--r--` | A regular file that is readable and writable by the file’s owner. Members of the file’s owner group may read the file. The file is world-readable.
`-rwxr-xr-x` | A regular file that is readable, writable, and executable by the file’s owner. The file may be read and executed by everybody else.
`-rw-rw----` | A regular file that is readable and writable by the file’s owner and members of the file’s group owner only.
`lrwxrwxrwx` | A symbolic link. All symbolic links have “dummy” permissions. The real permissions are kept with the actual file pointed to by the symbolic link.
`drwxrwx---` | A directory. The owner and the members of the owner group may enter the directory and create, rename, and remove files within the directory.
`drwxr-x---` | A directory. The owner may enter the directory and create, rename, and delete files within the directory. Members of the owner group may enter the directory but cannot create, delete, or rename files.

---

- `chmod` : Change File Mode
    - 6(rw-)
    - 7(rwx)
    - 5(r-x)
    - 4(r--)
    - 0(---)
    
Symbol | Meaning
--- | ---
`u` | Short for "user" but means the file or directory owner.
`g` | Group owner
`o` | Short for "others" but means world
`a` | Short for "all". This is a combination of `u`, `g`, and `o`.

- If no character is specified, “all” will be assumed. The operation may be a + indicating that a permission is to be added, a - indicating that a permission is to be taken away, or a = indicating that only the specified permissions are to be applied and that all others are to be removed.

Notation | Meaning
--- | ---
`u+x` | Add execute permission for the owner.
`u-x` | Remove execute permission from the owner.
`+x` | Add execute permission for the owner, group, and world. This is equivalent to a+x.
`o-rw` | Remove the read and write permissions from anyone besides the owner and group owner.
`go=rw` | Set the group owner and anyone besides the owner to have read and write permissions. If either the group owner or the world previously had execute permission, it is removed.
`u+x,go=rx` | Add execute permission for the owner and set the permissions for the group and others to read and execute. Multiple specifications may be separated by commas.

---

## 𝐏𝐫𝐨𝐜𝐞𝐬𝐬𝐞𝐬

- `ps` : Report a snapshot of current processes
- `top` : Display tasks
- `jobs` : List active jobs
- `bg` : Place a job in the background
- `fg` : Place a job in the foreground
- `kill` : Send a signal to a process
- `killall` : Kill process by name
- `shutdown` : Shut down or reboot the system



---

## 𝐍𝐞𝐭𝐰𝐨𝐫𝐤𝐢𝐧𝐠

- `ping` : Checks if a network is reachable, `ping` command sends a special network packet called an `ICMP ECHO_REQUEST` to a specified host. Most network devices receiving this packet will reply to it, allowing the network connection to be verified.

```
┌──(darshan㉿kali)-[~/Desktop]
└─$ ping google.com
PING google.com (142.250.77.46) 56(84) bytes of data.
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=1 ttl=119 time=5.90 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=2 ttl=119 time=5.28 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=3 ttl=119 time=5.85 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=4 ttl=119 time=6.54 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=5 ttl=119 time=5.62 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=6 ttl=119 time=6.25 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=7 ttl=119 time=13.6 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=8 ttl=119 time=6.20 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=9 ttl=119 time=5.35 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=10 ttl=119 time=29.6 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=11 ttl=119 time=5.89 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=12 ttl=119 time=5.52 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=13 ttl=119 time=5.57 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=14 ttl=119 time=6.34 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=15 ttl=119 time=5.56 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=16 ttl=119 time=6.02 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=17 ttl=119 time=5.32 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=18 ttl=119 time=5.26 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=19 ttl=119 time=5.43 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=20 ttl=119 time=5.77 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=21 ttl=119 time=5.47 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=22 ttl=119 time=5.48 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=23 ttl=119 time=5.43 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=24 ttl=119 time=5.42 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=25 ttl=119 time=11.0 ms
64 bytes from bom07s26-in-f14.1e100.net (142.250.77.46): icmp_seq=26 ttl=119 time=5.35 ms
^C
--- google.com ping statistics ---
26 packets transmitted, 26 received, 0% packet loss, time 25043ms
rtt min/avg/max/mdev = 5.258/7.113/29.557/4.846 ms
                                                                    
```

---

- `traceroute` : lists all the “hops” network traffic takes to get from the local system to a specified host.

```
┌──(darshan㉿kali)-[~/Desktop]
└─$ traceroute google.com
traceroute to google.com (142.250.77.46), 30 hops max, 60 byte packets
 1  * * * (* * *)  4.305 ms  4.202 ms  4.180 ms
 2  * * *
 3  * * *
 4  * * *
 5  * * *
 6  * * *
 7  * * *
 8  * * *
 9  * * *
10  * * *
11  * * *
12  * * *
13  * * *

```

---

- `ip a` : It replaces the earlier and now deprecated `ifconfig` program. 

```
┌──(darshan㉿kali)-[~]
└─$ ip a    
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 00:0c:29:c5:88:a0 brd ff:ff:ff:ff:ff:ff
    inet 192.168.x.x/24 brd 192.168.x.x scope global dynamic noprefixroute eth0
       valid_lft 1630sec preferred_lft 1630sec
    inet6 fe80::20c:29ff:x:x/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever

```

---

- `netstat` : The netstat program is used to examine various network settings and statistics.
    - `-r` option will display the kernel’s network routing table
    - `ie` : we can examine the network interfaces in our system

```
┌──(darshan㉿kali)-[~]
└─$ netstat -ie  
Kernel Interface table
docker0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet xx.xx.xx.xx  netmask 255.255.0.0  broadcast xx.xx.xx.xx
        ether xx:xx:xx:xx:xx:xx  txqueuelen 0  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.xx.xx  netmask 255.255.255.0  broadcast 192.168.xx.xx
        inet6 xxxx::xxxx:xxxx:xxxx:xxxx  prefixlen 64  scopeid 0x20<link>
        ether xx:xx:xx:xx:xx:xx  txqueuelen 1000  (Ethernet)
        RX packets 2378  bytes 385580 (376.5 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 252  bytes 29803 (29.1 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        
                                                                                                       
┌──(darshan㉿kali)-[~]
└─$ netstat -r 
Kernel IP routing table
Destination     Gateway         Genmask         Flags   MSS Window  irtt Iface
default         192.168.1.1     0.0.0.0         UG        0 0          0 eth0
xx.xx.xx.xx     0.0.0.0         255.255.0.0     U         0 0          0 docker0
xx.xx.xx.xx     0.0.0.0         255.255.255.0   U         0 0          0 eth0


```

---

Transporting Files over a Network
    
- `ftp` : `ftp` is used to communicate with FTP servers, machines that contain files that can be uploaded and downloaded over a network. `FTP` (in its original form) is not secure because it sends account names and passwords in cleartext.

```
[me@linuxbox ~]$ ftp fileserver
Connected to fileserver.localdomain.
220 (vsFTPd 2.0.1)
Name (fileserver:me): anonymous
331 Please specify the password.
Password:
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> cd pub/cd_images/ubuntu-18.04
250 Directory successfully changed.
ftp> ls
200 PORT command successful. Consider using PASV.
150 Here comes the directory listing.
-rw-rw-r--    1 500      500      733079552 Apr 25 03:53 ubuntu-18.04-desktop-amd64.iso
226 Directory send OK.
ftp> lcd Desktop
Local directory now /home/me/Desktop
ftp> get ubuntu-18.04-desktop-amd64.iso
local: ubuntu-18.04-desktop-amd64.iso remote: ubuntu-18.04-desktop-amd64.iso
200 PORT command successful. Consider using PASV.
150 Opening BINARY mode data connection for ubuntu-18.04-desktop-amd64.iso (733079552 bytes).
226 File send OK.
733079552 bytes received in 68.56 secs (10441.5 kB/s)
ftp> bye
```

Command | Meaning
--- | ---
`ftp fileserver` | Invoke the `ftp` program and have it connect the FTP server `fileserver`
`anonymous` | Login name. After the login prompt, a password prompt will appear. Some servers will accept a blank password; others will require a password in the form of an email address. In that case, try something like user@example.
`cd` | change directory
`ls` | list directory
`lcd Desktop` | Change the directory on the local system to ~/Desktop. In the example, the ftp program was invoked when the working directory was ~. This command changes the working directory to ~/Desktop.
`get` | transfer file from remote server to local system
`bye` | Log off the remote server and end the ftp program session. The commands quit and exit may also be used.

- `lftp` is a Better ftp

---

- `wget` : It is useful for downloading content from both web and FTP sites. Single files, multiple files, and even entire sites can be downloaded. 

```
[me@linuxbox ~]$ wget http://linuxcommand.org/index.php
--11:02:51--  http://linuxcommand.org/index.php
           => `index.php'
Resolving linuxcommand.org... 66.35.250.210
Connecting to linuxcommand.org|66.35.250.210|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]

    [ <=>                                 ] 3,120         --.--K/s

11:02:51 (161.75 MB/s) - `index.php' saved [3120]
```

---

- `ssh` : SSH solves the two basic problems of secure communication with a remote host.
    - It authenticates that the remote host is who it says it is (thus preventing so-called man-in-the-middle attacks).
    - It encrypts all of the communications between the local and remote hosts.
    - `ssh remote-sys` : To connect to a remote host named remote-sys
    - `ssh username@remote-sys` : login with specific username
    - `ssh remote-sys <command>`: to execute just a single command



```
[me@linuxbox ~]$ ssh remote-sys
The authenticity of host 'remote-sys (192.168.1.4)' can't be established.
RSA key fingerprint is 41:ed:7a:df:23:19:bf:3c:a5:17:bc:61:b3:7f:d9:bb.
Are you sure you want to continue connecting (yes/no)?
```

---

- `scp` - (secure copy). copy files from local host to remote host

```
[me@linuxbox ~]$ scp remote-sys:document.txt .
me@remote-sys's password:
document.txt                           100% 5581     5.5KB/s   00:00
[me@linuxbox ~]$
```

- `sftp` : SSH file-copying program

```
[me@linuxbox ~]$ sftp remote-sys
Connecting to remote-sys...
me@remote-sys's password:
sftp> ls
ubuntu-8.04-desktop-i386.iso
sftp> lcd Desktop
sftp> get ubuntu-8.04-desktop-i386.iso
Fetching /home/me/ubuntu-8.04-desktop-i386.iso to ubuntu-8.04-desktop-i386.iso
/home/me/ubuntu-8.04-desktop-i386.iso 100%  699MB   7.4MB/s   01:35
sftp> bye
```

---


## 𝐒𝐞𝐚𝐫𝐜𝐡𝐢𝐧𝐠 𝐟𝐨𝐫 𝐟𝐢𝐥𝐞𝐬

- `locate` : Find files by name
- `find` : Search for files in a directory hierarchy
- `xargs ` : Build and execute command lines from standard input
- `touch` : Change file times
- `stat`: Display file or file system status

---

- `find` : find files the hard way
    - `find ~` : to produce a listing of our home directory
    - `find ~ | wc -l` : to count the number of files.
    - `find ~ -type d | wc -l` : `-type d` limit the search to directories
    - `find ~ -type f | wc -l` : `-type f` limit the search to regular files 
    - `find ~ -type f -name "*.JPG" -size +1M | wc -l`: all the regular files that match the wildcard pattern *.JPG and are larger than one megabyte

File type | Description
--- | ---
`b` | Block special device file
`c` | Character special device file
`d` | Directory
`f` | Regular file
`l` | Symbolic link


- find size units

Character | Unit
--- | ---
`b` | 512-byte blocks. This is default if no unit is specified.
`c` | Bytes
`w` | 2-byte words
`k` | Kilobytes (units of 1,024 bytes)
`M` | Megabytes (units of 1,048,576 bytes)
`c` | Gigabytes (units of 1,073,741,824 bytes)

- More about `find` options: [Find cheatsheet](https://github.com/darshannn10/Linux-Command-Cheatsheet/blob/main/find-cheatsheet.md)

---

- `xargs` -  It accepts input from standard input and converts it into an argument list for a specified command

```
find ~ -type f -name 'foo*' -print | xargs ls -l
-rwxr-xr-x 1 me   me 224 2007-10-29 18:44 /home/me/bin/foo
-rw-r--r-- 1 me   me   0 2016-09-19 12:53 /home/me/foo.txt
```

---
