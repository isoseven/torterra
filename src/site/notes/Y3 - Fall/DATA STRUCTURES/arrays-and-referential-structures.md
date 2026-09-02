---
{"dg-publish":true,"permalink":"/y3-fall/data-structures/arrays-and-referential-structures/","dg-note-properties":{}}
---

# 🔗 TLDR
- primary memory is made of **bits**; a computer has huge amounts of it, and every **byte** gets its own memory address
	- memory is **RAM** (random access memory) — any individual byte can be retrieved in $O(1)$ time
- an **array** = a group of related variables stored one after another in memory
- every cell of an array must use the **same number of bytes** — since real data varies in length, **references (pointers)** let arrays hold varying-length data by storing a fixed-size reference in each cell instead of the data itself
- a **reference**: in Python, **everything is an object**, and assigning a variable to an object gives you a reference to that object, not the object itself
- **Python represents a list as an array of object references** (not an array of the objects themselves)
	- `id()` returns a unique **id** for any specific object
	- **lists/tuples are referential structures** — a single list can hold multiple references to the *same* object
- unit goals: find the memory address of characters in a string, visualize referential structures, use `id()`, find the total space usage (in bytes) of an array

## Low-Level Arrays
- primary memory of a computer is composed of **bits**
- computer systems have a huge amount of memory, and each **byte** has a memory address
	- this is considered **random access memory (RAM)**
	- any individual byte of memory can be retrieved in $O(1)$ time
- a group of related variables stored one after another in memory = an **array**
- *(diagram in the original: a row of memory cells/bytes, each with its own address, illustrating an array as contiguous storage)*

## Referential Arrays
- each cell of an array must use the **same** amount of bytes
	- this is why **pointers/references** are used — they let data of varying length be stored together, since every cell just holds a fixed-size reference rather than the data itself

### What is a Reference?
- in Python, **everything is an object**
- assigning a variable to an object means you have a **reference** to it, rather than the actual object itself
- *(diagram in the original: a variable pointing/arrow to the object it references, rather than containing the object directly)*

### References in Python
- **Python represents a list as an array of object references**
	- *(diagram in the original: a Python list drawn as an array of references, each pointing to a separate object elsewhere in memory)*
- *(diagram in the original: likely illustrating object identity — e.g. two variables referencing the same object, and sharing one id)*
	- `id()` returns the unique **id** for any specific object
- **lists and tuples are referential structures** — a single list may include multiple references to the same object

## Goals
- be able to find the memory address of characters in a string
- visualize referential structures
- use the `id()` method
- find the total space usage (in bytes) of a given array

⬅ *back: [[Y3 - Fall/DATA STRUCTURES/big-o-notation\|big-o-notation]]*
