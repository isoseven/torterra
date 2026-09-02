---
{"dg-publish":true,"permalink":"/y3-fall/stats-for-cs/sigma-algebras-and-probability-functions/","dg-note-properties":{}}
---

# 🧮 TLDR
- a **sigma-algebra** ($M$) on a sample space $\Omega$ is a collection of subsets of $\Omega$ satisfying 4 axioms: only contains subsets of $\Omega$, contains $\Omega$ itself, closed under complement, closed under union
	- smallest example: $M = \{ \Omega, \Phi \}$; largest example: $M = \text{power set of } \Omega$
	- $\Omega \neq M$ — $\Omega$ is a single set, $M$ is the whole collection of subsets (axiom 2 only says $\Omega \in M$)
- a **probability function** $P: \underset{\sigma-\text{algebra}}{M} \rightarrow [0, 1]$ must satisfy $P(\Omega) = 1$, additivity over mutually exclusive elements of $M$ (pairwise or countably many)
- **mutually exclusive** events can't both happen, which means they are **not independent**
	- probability 0 does **not** mean an event is the empty set — but the empty set always has probability 0
- for events that aren't mutually exclusive, $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ — e.g. blackout example: $P(M)=.8$, $P(T)=.5$, $P(M \cap T) = .35 \Rightarrow$ not independent, $P(M \cup T) = .8 + .5 - .35 = .95$
- **common mistake**: $P(A) \Rightarrow P(B)$ does **not** mean $P(A^c) \Rightarrow P(B^c)$
- **classical probability**: $P(E) = \frac{|E|}{|\Omega|}$ for equally-likely outcomes
- for continuous sample spaces, the probability of any single exact value is **0** — probability there is measured as **area under a curve**
- **system reliability**: wiring components **in series** (sequentially) makes a system *less* reliable than wiring the same components **in parallel**, even with identical individual probabilities

## Sigma-Algebras (cont. from last class)
- a **sigma-algebra** $M$ on a space $\Omega$ is a set that satisfies:
	1. $\forall E \in M, E \text{ is a subset of } \Omega$
	2. $\Omega \in M$
	3. $\text{if } E \in M, E^c  \in M$
	4. $\text{if } A, B \in M \text{ then } A \cup B \in M$

### Examples
- smallest possible sigma-algebra: $M = \{ \Omega, \Phi \}$
- largest possible sigma-algebra: $M = \text{power set of } \Omega$
- worked example: $\Omega = \{ 1, 2, 3, 4, 5, 6\}$
	- $E_1 = \{1,2\} \; E_2 = \{3,4,5,6\}$ — note $E_2$ is $E_1$'s complement
	- then $M = \{\Omega, \Phi, E_1, E_2\}$
- **why is $\Omega = M$ false?** $\Omega$ is a single set (the whole sample space), while $M$ is a *collection* of subsets of $\Omega$ — per axiom 2, $\Omega$ is only one *element* of $M$, not equal to the whole collection
- *(open question from lecture, still unanswered: why sigma-algebras matter — revisit)*

## Probability Functions
- a **probability function** is a map $P: \underset{\sigma-\text{algebra}}{M} \rightarrow [0, 1]$ satisfying:
	1. $P(\Omega) = 1$
	2. if $E_1, E_2$ are mutually exclusive elements of $M$ then $P(E_1 \cup E_2) = P(E_1) + P(E_2)$
	3. if $E_1, E_2, E_3, \ldots$ is a finite or countably infinite set of mutually exclusive elements of $M$ then $P(\cup E_i)$ = $\sum P(E_i)$
		- requires $E_i \cap E_j = \Phi \; \forall i \neq j$ — true whenever all elements of $M$ are mutually exclusive
- teacher reviewed finding $P(A \cap B)$ and defining independent sets $A$, $B$ (already-familiar material)

## Mutually Exclusive vs. Independent
- **mutually exclusive** events cannot both occur
	- this means they are **not independent** — one happening changes the other's probability (to 0)
- if $P(E) = 0$, that does **not** mean $E$ is the empty set — but the empty set always has $P(\Phi) = 0$

> [!warning]
> common mistake: $P(A) \Rightarrow P(B)$ does **not** mean $P(A^c) \Rightarrow P(B^c)$

### Example: Print Job Queue
- 65% chance a job is first in line, 20% chance it's second in line
- these are **mutually exclusive** (a job can't be both first and second), which means they are **not independent**

### Example: Construction Blackouts
- 80% chance of a blackout Monday, 50% chance of a blackout Tuesday
- $P(M \cap T) = .35$ — since independence would require $P(M) \times P(T) = .8 \times .5 = .4 \neq .35$, the events are **not independent**
- $P(M \cup T) = P(M) + P(T) - P(M \cap T) = .8 + .5 - .35 = .95$

## Classical Probability
- $P(E) = \frac{|E|}{|\Omega|}$

### Example: Rolling a Die Three Times
- let $E$ = "the sum of the three rolls is $\leq 4$"
- listing the elements of $E$: $\{(1,1,1),\ (1,1,2),\ (1,2,1),\ (2,1,1)\}$
- $P(E) = \frac{4}{216}$

### Continuous Case (preview)
- when outcomes can take **any real number**, the probability of any single exact value is **0** — it has to be **measurable**
- in the continuous case, probability = **area under a curve**

## System Reliability
- with the **same** individual component probabilities, wiring components **in series** (sequentially) makes a system **less reliable** than wiring them in parallel
- example system sketched in class: two branches running in parallel —
	- branch 1: through component $A$, then component $B$, for success
	- branch 2: through component $C$, then *either* $D$ **or** $E$, for success
	- (exact board diagram not transcribed)
- **this is where the next class picks back up**

⬅ *back: [[Y3 - Fall/STATS FOR CS/probability-basics\|probability-basics]]*
