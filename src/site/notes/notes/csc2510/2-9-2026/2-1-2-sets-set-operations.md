---
{"dg-publish":true,"permalink":"/notes/csc2510/2-9-2026/2-1-2-sets-set-operations/"}
---

# 🥝 SUMMARY
- **sets** = **unordered collection** of object(s), denoted as uppercase variables
	- set builder notation: for any **proposition** $P(x)$ over any universe of discourse, $\{x \,|\, P(x)\}$ is the **set of all** $x$ such that $P(x)$.
	- conceptually, **sets may be infinite**.
		- $\mathbb{N} = \{0, 1, 2, \ldots\}$
		- $\mathbb{Z} = \{\ldots , -2, -1, 0, 1, 2, \ldots \}$
		- $\mathbb{R} = \textrm{all real numbers}$
		- $\mathbb{Q} = \textrm{all rational numbers}$
	- sets are also **objects** so they can be **nested** in other sets
- **set equality** = sets contain **exactly** the same elements
- **set relation** = a **proposition** that object $x$ is an element or member of set $S$.
- sets as objects:
	- **cardinality**: the measure of how many different elements set $S$ has. ($\,|\,S\,|\,$)
	- the **power set** of a set is the set of all the subsets of $S$. $P(S) = \{x \,|\, x \subseteq S\}$
	- for $n \in \mathbb{N}$, an **ordered** n-tuple (sequence of length $n$) is written as $(a_1, a_2, \ldots, a_n)$
	- for sets $A$ and $B$, their **Cartesian product** is $\{(a, b)\,|\,a \in A \land  \in B\}$
## set theory
- **set** = structure, representing **unordered** collection of 0 or more **distinct** (different) objects.
	- **set theory** deals with operations between / relations among / statements about sets.
- **notation**: for sets, we use uppercase variables. ($S$, $T$, $U$)
	- we can denote a set $S$ by writing all elements in curly braces.
	- $\{a, b, c\}$ is the set of whatever 3 objects denoted by $a$, $b$, $c$.
	- **set builder notation**: for any **proposition** $P(x)$ over any universe of discourse, $\{x \,|\, P(x)\}$ is the **set of all** $x$ such that $P(x)$.
		- example: $\{x \,|\, x \textrm{ is an integer where } x > 0 \textrm{ and } x > 5\}$ 
- sets are **inherently unordered** and **distinct**.
	- $\{a, b, c\} = \{c, a, b\} = \{a, b, c, b, a\}$ (ignore order or repetition.)
## set equality
- **set equality**: containing **exactly** the **same elements**.
	- it does not matter how the set is defined or denoted.
	- $\{1,2,3,4\} = \{x \,|\, x > 0 \land x > 5 \land x \in \mathbb{Z} \}$
	- conceptually, **sets may be infinite**.
		- $\mathbb{N} = \{0, 1, 2, \ldots\}$
		- $\mathbb{Z} = \{\ldots , -2, -1, 0, 1, 2, \ldots \}$
		- $\mathbb{R} = \textrm{all real numbers}$
		- $\mathbb{Q} = \textrm{all rational numbers}$
	- examples of **set equality** (how to notate in set builder notation.)
		- $\{2, 3, 5, 7, 11, 13, 17, 19\} = \{x \in \mathbb{Z}: 0 < x < 20 \land \textrm{x is prime}\}$
		- $\{-1, 0, 1\} = \{ x \in \mathbb{R}: \,|\,x\,|\, = x^2\} = \{ x \in mathbb{Z}: -2 < x < 2\}$ 
		- $\{0, 2, 4, 6, \ldots \} = \{ x \in \mathbb{N}: \textrm{x is even}\}$
		- $\{0, 2, 4, 6, \ldots, 18 \} = \{ x \in \mathbb{N}: x < 20 \land \textrm{x is even} \}$
## basic set relations
- $x \in S$ is a **proposition** that object $x$ is an element or member of set $S$.
	- example: $3 \in N, \textrm{"a"} \in \{ x \,|\, x \textrm{ is a letter of the alphabet}\}$
- can define **set equality** in terms of $\in$ relation:
	- $\forall S, T: \, S = T \leftrightarrow (\forall x: x \in S \leftrightarrow x \in T)$
	- "two sets are equal if and only if they have all the same members."
- **the empty set** (denoted by $\emptyset$) is the unique set that contains **no elements**.
	- $\emptyset = \{\} = \{x \,|\, \bot\}$
	- no matter the **domain of discourse**, we have the **axiom**
		- $\lnot \exists x: x \in \emptyset$.
## subset
- $S \subseteq T$ means "$S$ is a subset of $T$"
	- every element of $S$ is also an element of $T$.
	- $S \subset T \Leftrightarrow \forall x \, (x \in S \rightarrow x \in T)$
	- $S \supseteq T$ means "$S$ is a superset of $T$" or "$T$ is a subset of $S$".
		- every element of $T$ is also an element of $S$.
	- note that $S = T \Leftrightarrow S \subseteq T \land S \supseteq T$.
	- $S \nsubseteq T$ means $\lnot(S \subseteq T)$ or $\exists x(x \in S \land x \notin T)$
- $S \subset T$ means that $S \subseteq T$ but $T \nsubseteq S$. This is known as a **proper subset** (S is a proper subset of T.)
	- note that $\subset$ can be ambiguous when it comes to math; it can be used as a shorthand for $\subseteq$. if it is being used as a shorthand you need to use $\subsetneq$.

## sets as objects
- sets are **objects** too!
	- the objects inside of a set may be sets as well.
	- example:
		- let $S = \{ x \,|\, x \subseteq \{1, 2, 3\} \}$
		- then $S = \{ \emptyset, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1, 3\}, \{2, 3\}, \{1, 2, 3\}\}$
		- **note**: $1 \neq \{1\} \neq \{\{1\}\}$
- **cardinality**: the measure of how many different elements set $S$ has. ($\,|\,S\,|\,$)
	- example. $\,|\,\emptyset\,|\, = 0, \,|\,\{1,2,3\}\,|\, = 3, \,|\,\{\{1,2,3\}, \{4, 5\}\}\,|\, = 2$
	- $S$ is infinite if it is not finite ($\,|\,S\,|\, < \aleph_0$)
- **power set operation**
	- the **power set** of a set is the set of all the subsets of $S$. $P(S) = \{x \,|\, x \subseteq S\}$
	- sometimes $P(S)$ is written $2^S$. note for finite $S$, $\,|\,P(S)\,|\, = 2^{\,|\,S\,|\,}$
	- $\,|\,P(\mathbb{N})\,|\, > \,|\,\mathbb{N}\,|\,$.
- **ordered n-tuples**
	- for $n \in \mathbb{N}$, an **ordered** n-tuple (sequence of length $n$) is written as $(a_1, a_2, \ldots, a_n)$
		- the **first** element is $a_1$.
	- these are similar to sets, but order and duplicates matter.
		- $(1,2) \neq (2,1) \neq (2,1,1)$
	- empty sequence, singletons, pairs, triples, quadruples, quintuples, ... *n*-tuples
- **cartesian products of sets**
	- for sets $A$ and $B$, their **Cartesian product** is
		- $\{(a, b)\,|\,a \in A \land  \in B\}$
	- for finite $A$ and $B$, $|A \times B| = |A| |B|$
	- cartesian product is **not** commutative.
		- $\lnot \forall AB: A \times B = B \times A$
	- extends to $A_1 \times A_2 \times \ldots \times A_n \ldots$

## set operators
union operator ... on wed.