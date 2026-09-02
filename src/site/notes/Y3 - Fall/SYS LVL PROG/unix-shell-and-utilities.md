---
{"dg-publish":true,"permalink":"/y3-fall/sys-lvl-prog/unix-shell-and-utilities/","dg-note-properties":{}}
---

# 🐚 TLDR
- chapter 2 covers **Unix utilities for non-programmers**
- the **shell** = a program that acts as a middleman between you and the raw Unix operating system
	- popular shells: **Bourne** (`sh`), **Korn** (`csh`, out of date nowadays), **Bourne Again** (`bash`), `tcsh`, `zsh` — all share the same core functionality, with some differences
- basic utilities: `date`, `man`, `clear`, `stty`, `passwd`
	- `stty -a` lists **meta characters** (control-key shortcuts like `^C` interrupt, `^D` EOF/exit) — the professor noted these (and `stty` itself) aren't that useful day-to-day
- key file/directory utilities: `pwd` (show current path), `cat`/`more`/`page`/`head`/`tail` (view files), `ls`/`cd` (list/navigate), `mv`/`cp`/`rm` (move/copy/remove), `mkdir`/`rmdir` (`rmdir` only works on **empty** folders), `file`/`wc`/`lp`, `vi`/`pico`/`emacs` (terminal text editors), `groups`/`chgrp`/`chmod` (permissions/ownership)
- **directory structure**: `/` (root) sits at the top of the filesystem; `.` = current directory, `..` = parent directory
- plan: use **vi** for this class, to get some familiarity with it

## Chapter 2: Unix Utilities
- this chapter covers **Unix utilities for non-programmers**

## The Shell
- the **shell** = a program that acts as a middleman between you and the raw Unix operating system
	- *(diagram in the original: user ↔ shell ↔ raw Unix OS, illustrating the shell as a middleman)*
- popular shells:
	- **Bourne** (`sh`)
	- **Korn** (`csh`) — out of date nowadays
	- **Bourne Again** (`bash`)
	- `tcsh`, `zsh`
	- all share the same core functionality, with some differences between them

## Utilities
- some basic utilities: `date`, `man`, `clear`, `stty`, `passwd`

### Meta Characters (via `stty -a`)
- the professor noted that `stty` — and these control-key shortcuts in general — aren't all that useful day-to-day, but here's the list:

| shortcut | meaning |
| --- | --- |
| `^` | control prefix (e.g. `^C`) |
| `^H` | erase (backspace) |
| `^W` | werase (ctrl+backspace) |
| `^U` | kill (erase whole line) |
| `^R` | reprint line |
| `^C` | interrupt |
| `^Z` | suspend |
| `^S` / `^Q` | stop / resume printing |
| `^D` | EOF / exit |

### Other Unix Utilities

| utility | meaning |
| --- | --- |
| `pwd` | print working directory — shows the absolute path of the directory you're in |
| `cat` | concatenate — reads data from files and writes it sequentially to standard output (viewing/combining files) |
| `more` | views a text file's contents one screenful at a time |
| `page` | views a text file or output one page at a time |
| `head` | prints the first 10 lines of a file |
| `tail` | prints the last 10 lines of a file |
| `ls` | list — shows what's in a folder |
| `cd` | change directory — moves you |
| `mv` | move — moves a file, or renames it |
| `cp` | copy — duplicates a file or directory |
| `rm` | remove — deletes a file |
| `mkdir` | make directory — creates a new folder |
| `rmdir` | remove directory — removes **only** completely empty folders |
| `file` | determines a file's type |
| `wc` | word count |
| `lp` | physically prints a file |
| `vi`, `pico`, `emacs` | text-based terminal editors |
| `groups` | shows a user's group membership |
| `chgrp` | changes a file/folder's group (ownership) |
| `chmod` | changes what actions are allowed on a file/folder |

## Directory Structure
- `/` (root) sits at the top of the filesystem
- `.` = current directory, `..` = parent directory
- *(diagram in the original: a directory tree rooted at `/`, illustrating `.` as the current directory and `..` as the parent)*

- plan: use **vi** for this class, to get some familiarity with it

⬅ *back: [[Y3 - Fall/SYS LVL PROG/syllabus-csc3320\|syllabus-csc3320]]*
