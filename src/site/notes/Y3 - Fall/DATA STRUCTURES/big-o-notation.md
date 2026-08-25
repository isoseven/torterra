---
{"dg-publish":true,"permalink":"/y3-fall/data-structures/big-o-notation/","dg-note-properties":{}}
---

# 📈 TLDR
- **data structure** = a way of organizing data that enables efficient access and modification
	- organization → **space**; access/modification → **time**
	- data structures live in **RAM** (temporary/volatile data)
	- examples: list, linked list, stack, queue, set, map, heap, tree
- **Big-O notation** = mathematical notation for the **upper bound** on a function's growth rate
	- found by keeping only the **highest-order term** and dropping constants/non-dominant terms
	- rule 1: if $f(x)$ is a sum of terms, keep the highest-order term, discard the rest
	- rule 2: if $f(x)$ has a term that's a product of factors, drop the constants
- **best case = Big Omega ($\Omega$)**, **average case = Big Theta ($\Theta$)** — but **worst case (Big O)** is what's actually used most in practice, since you're testing for the worst
- worked exercises: constant-time/space operations are $O(1)$; a single loop over the input is $O(n)$ time; building an $n \times n$ matrix is $O(n^2)$ time and space

## what is a data structure
- **data structure** = data organization that enables efficient access and modification
	- data organization → **space** (how much space it takes; e.g. how a zip folder is organized)
	- access and modification → **time** (how much time it takes to modify it — zip folder example again)
- data structures live in **RAM** (temporary data)

## examples of data structures
- list
- linked list
- stack
- queue
- set
- map
- heap
- tree

## what is Big-O notation
- **Big-O notation** = mathematical notation for **upper-bounding a function's growth rate**
	- represents the **upper limit** of the function
	- found by **ignoring constants and non-dominant growth terms**
- **rule 1**: if $f(x)$ is the sum of several terms, keep the highest-order term and discard the others
- **rule 2**: if $f(x)$ has a term that's a product of several factors, the constants are omitted

## composite functions
> [!note]
> This part of the lecture wasn't fully captured — the rule for combining Big-O across composite functions needs to be filled in from a recording or classmate.

- composite function = $c + O(f(x))$
- for something of the form $g(x) \cdot O(f(x))$, the combined bound is written $O(g(x) \cdot O(f(x)))$

## best, average, and worst case
- **best case = Big Omega ($\Omega$)**
- **average case = Big Theta ($\Theta$)**
- **algorithm runtime analysis** generally focuses on **worst case (Big O)**, since worst case is used far more often than best case in practice — you're testing for the worst-case scenario, after all

## exercises: finding time/space complexity

### exercise 1
- task: find the time/space complexity of `print_greetings()`, which simply prints three strings
- **time complexity**: $O(1)$ — count the number of operations
- **space complexity**: $O(1)$ — uses one extra unit of space

### exercise 2
```python
def print_arr(arr):
	for i in range(len(arr)):
		print(arr[i])
```
- **time complexity** = $O(n)$
- **space complexity** = $O(1)$

### exercise 3
```python
def perform_arithmetic_operations(a, b):
	add_res = a + b
	sub_res = a - b
	mul_res = a * b
	div_res = a / b
	print(add_res, sub_res, mul_res, div_res)
```
- **time** = $O(1)$, **space** = $O(1)$

### exercise 4
```python
def count_vowels(s):
	vowels = 0
	for char in s:
		if char in ["a", "e", "i", "o", "u"]:
			vowels += 1
	return vowels
```
- **time** = $O(n)$, **space** = $O(1)$

### exercise 5
```python
def generate_zeros_matrix(n):
	# creates an n x n matrix
```
- **time** = $O(n^2)$, **space** = $O(n^2)$

⬅ *back: [[Y3 - Fall/DATA STRUCTURES/syllabus-csc2720\|syllabus-csc2720]]*
