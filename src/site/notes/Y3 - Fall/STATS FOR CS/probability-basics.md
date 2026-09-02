---
{"dg-publish":true,"permalink":"/y3-fall/stats-for-cs/probability-basics/","dg-note-properties":{}}
---

# 🎲 TLDR
- **probability** comes from **experiments**: repeated trials that produce **outcomes**
	- 3 fundamental ideas: (1) an experiment records the number of successes, (2) trials are **independent**, (3) everyone running the same experiment gets a **sample distribution** of results — expect a variety of responses
- the **sample space** ($\Omega$) = the set of **all possible outcomes** of an experiment
- an **event** = any **subset** of the sample space ($\Omega$)
- set operations apply directly to events: **union**, **intersection**, and **set difference** let you combine or compare events
- demo: flipping a coin 25 times and counting heads produces a **histogram** shaped around the expected 12–14 range
	- **histogram**: bars show frequency counts of **numerical** data grouped into ranges (bins)
	- **bar chart**: bars show counts/values for separate **categorical** groups
- if $A \cup B = \emptyset$, both $A$ and $B$ must themselves be empty — that's the only way a union can have zero elements

## Demonstration: Coin Flips
- flip a coin 25 times, tracking heads vs. tails
	- observed: 13 heads / 12 tails
	- most trial outcomes cluster in the **12–14** range, visualized as a **histogram**
	- this is what distinguishes a **bar chart** from a **histogram**: a histogram bins **numerical** data (like a count of heads) into ranges, while a bar chart shows counts for separate **categorical** groups (like eye color or major)
- **3 fundamental ideas of probability**:
	1. an **experiment** records the number of successes in that experiment
	2. trials are run **independently**
	3. everyone runs the **same experiment**, producing a **sample distribution** — expect a variety of responses across the class

## Sample Space and Events
- **probability** arises from experiments: an experiment has several **trials**, each producing an **outcome**
- the **sample space** ($\Omega$) is the set of all possible outcomes of an experiment
- an **event** is any **subset** of $\Omega$

### Example: Flipping 3 Coins
- flip a penny, nickel, and dime once each
- since the coins don't affect each other, the flips are **independent**
- sample space:
	$$\Omega = \{TTT, TTH, THT, HTT, THH, HTH, HHT, HHH\} \quad (2^3 = 8 \text{ outcomes})$$
- **events** are named with capital letters (A, B, ...) — an event is just a subset of $\Omega$
	- example: event $A$ = "getting exactly 2 heads" = $\{HHT, HTH, THH\}$

### Example: Rolling a 6-Sided Die
- let $A$ = even numbers, $B$ = numbers $\le 4$
- set operations on events:

| operation | meaning | result |
| --- | --- | --- |
| $A \cup B$ | union | $\{1,2,3,4,6\}$ |
| $A \cap B$ | intersection | $\{2,4\}$ |
| $A - B$ | set difference | $\{6\}$ |

## For Review (Already Covered in Another Class, but Revisit)
- the **empty set** ($\emptyset$): the unique set containing no elements
- **intersection** ($\cap$): elements common to both sets; **complement**: everything in the universe *not* in the set; **set difference** ($A - B$): elements in $A$ that aren't in $B$
- **DeMorgan's laws**: relate the complement of a union/intersection to the intersection/union of complements
- how to determine whether two events are **independent**: (revisit this — worth re-deriving during review)
- if $A \cup B = \emptyset$: since a union includes every element of both sets, the only way it can have zero elements is if $A$ and $B$ are **both individually empty** ($A = \emptyset$ and $B = \emptyset$)

⬅ *back: [[Y3 - Fall/STATS FOR CS/syllabus-math3020\|syllabus-math3020]]*
➡ *next: [[Y3 - Fall/STATS FOR CS/sigma-algebras-and-probability-functions\|sigma-algebras-and-probability-functions]]*
