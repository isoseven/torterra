---
{"dg-publish":true,"permalink":"/y3-fall/sys-lvl-prog/syllabus-csc3320/","dg-note-properties":{}}
---

# 🐧 TLDR
- **CSC 3320** = Systems-Level Programming; full syllabus lives on the [class webpage](https://hallertau.cs.gsu.edu/~mweeks/csc3320/index.html)
- course covers: **ssh/sftp** for remote file transfer, **Unix/Linux shell** commands, **C programming**, **pipe/fork/exec** and other process mechanisms, and using **structs** to access directory and process data
- grading: 2 tests = 30%, ~5 assignments = 15%, ~14 labs = 25%, participation = 10%, final = 20% (pop quizzes may fold into test grades — unconfirmed)
- **final exam**: Wednesday, December 9, 2026, 16:15–18:45 (subject to change)
- required books: King's *C Programming: A Modern Approach*; Glass & Ables' *Unix for Programmers and Users*
- coursework happens on **snowball** (`ssh schae6@snowball.cs.gsu.edu`) — snowball gets wiped every semester

## Logistics
- syllabus is posted on the [class webpage](https://hallertau.cs.gsu.edu/~mweeks/csc3320/index.html)
- office hours: **room 754, 25 Park Place**
- responsibilities:
	- attend class
	- read the book
	- don't post course materials without the rights to do so

## Grading Breakdown
| component | weight |
| --- | --- |
| 2 tests | 30% |
| assignments (~5) | 15% |
| labs (~14) | 25% |
| participation | 10% |
| final exam | 20% |

- pop quizzes may fold into test grades (unconfirmed — "maybe not...?")

> [!warning]
> Final exam: **Wednesday, December 9, 2026, 16:15–18:45** — might change, double check closer to the date.

## What Will Be Learned
Quick preview of what each of these actually means — the course will cover them properly, but a one-line anchor helps going in:

| topic | quick description |
| --- | --- |
| **ssh** (Secure Shell) | a protocol for securely logging into and running commands on a remote machine |
| **sftp** (SSH File Transfer Protocol) | transfers files between machines securely, built on top of SSH |
| **Unix/Linux shell** | typing commands directly to the OS instead of using a graphical interface |
| **C programming** | a low-level, compiled language that gives direct control over memory |
| **pipe** | connects one process's output directly to another process's input |
| **fork** | a system call that creates a new process by duplicating the current one |
| **exec** | a system call that replaces a process's running program with a different one |
| **struct** | a C construct that groups several related variables together under one name |

## Required Books
- King, *C Programming: A Modern Approach*
- Glass and Ables, *Unix for Programmers and Users*

## Working Environment
- use **snowball**: `ssh schae6@snowball.cs.gsu.edu`
- snowball gets wiped at the end of each semester — don't leave anything important there

➡ *next: [[Y3 - Fall/SYS LVL PROG/unix-shell-and-utilities\|unix-shell-and-utilities]]*
