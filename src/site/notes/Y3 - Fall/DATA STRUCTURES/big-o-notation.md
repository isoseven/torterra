---
{"dg-publish":true,"permalink":"/y3-fall/data-structures/big-o-notation/","dg-note-properties":{}}
---

# 📈 TLDR
- **data structure** = a way of organizing data that enables efficient access and modification
	- organization → **space**; access/modification → **time**
	- data structures live in **RAM** (temporary/volatile — unlike a disk, which persists data)
	- 8 common types: **list, linked list, stack, queue, set, map, heap, tree** — each with different tradeoffs (see table below)
- **Big-O notation** = mathematical notation for the **upper bound** on a function's growth rate
	- found by keeping only the **highest-order term** and dropping constants/non-dominant terms
	- rule 1: if $f(x)$ is a sum of terms, keep the highest-order term, discard the rest
	- rule 2: if $f(x)$ has a term that's a product of factors, drop the constants
	- **product rule** (for composite/nested functions): if a factor $g(x)$ multiplies a piece that's $O(f(x))$, the whole thing is $O(g(x)\cdot f(x))$ — this is how nested loops get analyzed
- **best case = Big Omega ($\Omega$)**, **average case = Big Theta ($\Theta$)** — but **worst case (Big O)** is what's actually used most in practice, since you're testing for the worst
- worked exercises: constant-time/space operations are $O(1)$; a single loop over the input is $O(n)$ time; building an $n \times n$ matrix is $O(n^2)$ time and space

## What Is a Data Structure
- **data structure** = data organization that enables efficient access and modification
	- data organization → **space** (how much space it takes; e.g. how a zip folder is organized)
	- access and modification → **time** (how much time it takes to modify it — zip folder example again)
- data structures live in **RAM** (temporary data) — as opposed to a hard drive/disk, which stores data persistently

## Examples of Data Structures
Quick reference for what each one actually is — your professor will go deeper on these later, but it helps to have a one-line anchor for each name:

| structure | quick description |
| --- | --- |
| **list** | ordered, indexable collection of elements |
| **linked list** | ordered collection where each element points to the next |
| **stack** | LIFO (last-in, first-out) — add/remove from one end only |
| **queue** | FIFO (first-in, first-out) — add at the back, remove from the front |
| **set** | unordered collection of distinct/unique elements |
| **map** | key–value pairs (also called a dictionary or hash map) |
| **heap** | tree-based structure that keeps the smallest (or largest) element quickly accessible |
| **tree** | hierarchical structure of nodes connected by parent/child relationships |

## What Is Big-O Notation
- **Big-O notation** = mathematical notation for **upper-bounding a function's growth rate**
	- represents the **upper limit** of the function
	- found by **ignoring constants and non-dominant growth terms**
- **rule 1**: if $f(x)$ is the sum of several terms, keep the highest-order term and discard the others
- **rule 2**: if $f(x)$ has a term that's a product of several factors, the constants are omitted

## Composite Functions
> [!info]
> The original note flagged this bit as **"didn't see"** — the professor's exact wording wasn't caught live. What follows is the standard rule these fragments were pointing at; double-check it against your slides/textbook once you have them, since this is filled in rather than transcribed.

- a function's cost is often expressed as a **composite**: something like $c + O(f(x))$ — a constant/lower-order piece plus a dominant $O(f(x))$ term.
	- since Big-O only keeps the **highest-order term** (rule 1), $c + O(f(x))$ simplifies down to just $O(f(x))$ — the constant gets absorbed.
- **product rule**: if part of a function is some factor $g(x)$ multiplying a piece that's $O(f(x))$, the combined bound is $O\bigl(g(x) \cdot f(x)\bigr)$.
	- this is the rule behind analyzing **nested structures** — e.g. a loop that runs $g(n)$ times, where each iteration itself costs $O(f(n))$, has total cost $O\bigl(g(n)\cdot f(n)\bigr)$.

## Best, Average, and Worst Case
- **best case = Big Omega ($\Omega$)**
- **average case = Big Theta ($\Theta$)**
- **algorithm runtime analysis** generally focuses on **worst case (Big O)**, since worst case is used far more often than best case in practice — you're testing for the worst-case scenario, after all

## Exercises: Finding Time/Space Complexity

### Exercise 1
- task: find the time/space complexity of `print_greetings()`, which simply prints three strings
- **time complexity**: $O(1)$ — count the number of operations
- **space complexity**: $O(1)$ — uses one extra unit of space

### Exercise 2
```python
def print_arr(arr):
	for i in range(len(arr)):
		print(arr[i])
```
- **time complexity** = $O(n)$
- **space complexity** = $O(1)$

### Exercise 3
```python
def perform_arithmetic_operations(a, b):
	add_res = a + b
	sub_res = a - b
	mul_res = a * b
	div_res = a / b
	print(add_res, sub_res, mul_res, div_res)
```
- **time** = $O(1)$, **space** = $O(1)$

### Exercise 4
```python
def count_vowels(s):
	vowels = 0
	for char in s:
		if char in ["a", "e", "i", "o", "u"]:
			vowels += 1
	return vowels
```
- **time** = $O(n)$, **space** = $O(1)$

### Exercise 5
```python
def generate_zeros_matrix(n):
	matrix = []
	for i in range(n):
		row = []
		for j in range(n):
			row.append(0)
		matrix.append(row)
	return matrix
```
- **time** = $O(n^2)$ — the nested loop visits every one of the $n \times n$ cells once
- **space** = $O(n^2)$ — the returned matrix stores $n \times n$ elements

⬅ *back: [[Y3 - Fall/DATA STRUCTURES/syllabus-csc2720\|syllabus-csc2720]]*
➡ *next: [[Y3 - Fall/DATA STRUCTURES/arrays-and-referential-structures\|arrays-and-referential-structures]]*
