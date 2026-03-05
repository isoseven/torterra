---
{"dg-publish":true,"permalink":"/notes/csc1302/1-basics/"}
---

## overview
- variable naming + conventions
- strings and their operators/functions
	- **specifically in this course we learn:** `in` `not` `+` `*` `s[i]` `len()`
- indexing, negative indices, slices (`[2:]`)
- lists and their operators/functions/methods
	- **specifically in this course we learn**: `in` `not in` `+` `*` `l[i]` `len()` `min()` `max()` `sum()` `l.append(x)` `l.count(x)` `l.index(x)` `l.pop()` `l.remove(x)` `l.reverse()` `l.sort(x)`
- tuples
- `input()`
- if / elif / else
- for / nested for
	- **execution control structures**: controls what statements are executed. (if/for/while etc)
- `range()`
- defining functions
- comments
- **docstrings** (a string right after the `def()`)
- mutable/immutable types
- **advanced print()**
	- sep for the separator between arguments.
	- end for the ending of each argument (default newline)
	- `{}.format(item)`
	- **format field width**
		- `{:2}` means there are 2 spaces reserved for a certain output.
		- numbers align right, string align left
		- output type can be b (binary) c (char) d (hex) X (16imal) e (scientific) f (fixed point)
		- `{:3.2f}` means there are 3 spaces reserved and 2 dec. points