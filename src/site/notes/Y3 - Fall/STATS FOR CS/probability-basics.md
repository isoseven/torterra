---
{"dg-publish":true,"permalink":"/y3-fall/stats-for-cs/probability-basics/","dg-note-properties":{}}
---

# 🎲 TLDR
- **probability** comes from **experiments**: repeated trials that produce **outcomes**
	- 3 fundamental ideas: (1) an experiment records the number of successes, (2) trials are **independent**, (3) everyone running the same experiment gets a **sample distribution** of results — expect a variety of responses
- the **sample space** ($\Omega$) = the set of **all possible outcomes** of an experiment
- an **event** = any **subset** of the sample space ($\Omega$)
- set operations apply directly to events: **union**, **intersection**, and **set difference** let you combine or compare events
- demo: flipping a coin 25 times and counting heads produces a **histogram** shaped around the expected 12–14 range (categorical vs. numerical data, bar chart vs. histogram)

## demonstration: coin flips
- flip a coin 25 times, tracking heads vs. tails
	- observed: 13 heads / 12 tails
	- most trial outcomes cluster in the **12–14** range, visualized as a **histogram**
	- (this distinguishes a **bar chart** from a **histogram**, and **categorical** data from **numerical** data)
- **3 fundamental ideas of probability**:
	1. an **experiment** records the number of successes in that experiment
	2. trials are run **independently**
	3. everyone runs the **same experiment**, producing a **sample distribution** — expect a variety of responses across the class

## sample space and events
- **probability** arises from experiments: an experiment has several **trials**, each producing an **outcome**
- the **sample space** ($\Omega$) is the set of all possible outcomes of an experiment
- an **event** is any **subset** of $\Omega$

### example: flipping 3 coins
- flip a penny, nickel, and dime once each
- since the coins don't affect each other, the flips are **independent**
- sample space:
	$$\Omega = \{TTT, TTH, THT, HTT, THH, HTH, HHT, HHH\} \quad (2^3 = 8 \text{ outcomes})$$
- **events** are named with capital letters (A, B, ...) — an event is just a subset of $\Omega$
	- example: event $A$ = "getting exactly 2 heads" = $\{HHT, HTH, THH\}$

### example: rolling a 6-sided die
- let $A$ = even numbers, $B$ = numbers $\le 4$
- set operations on events:

| operation | meaning | result |
| --- | --- | --- |
| $A \cup B$ | union | $\{1,2,3,4,6\}$ |
| $A \cap B$ | intersection | $\{2,4\}$ |
| $A - B$ | set difference | $\{6\}$ |

## for review (already covered in another class, but revisit)
- the **empty set** ($\emptyset$)
- **intersections**, **complements**, **set difference**, **DeMorgan's laws**
- how to determine whether two events are **independent**
- note: if $A \cup B = \emptyset$, that tells you something specific about $A$ and $B$ — worth re-deriving during review

⬅ *back: [[Y3 - Fall/STATS FOR CS/syllabus-math3020\|syllabus-math3020]]*
