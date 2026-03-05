---
{"dg-publish":true,"permalink":"/notes/csc2510/2-11-2026/2-2-set-operations-cont/"}
---

## comparison
- **unions** are **the set containing all elements in both** $A$ or $B$. 
	- formally, they are denoted as $\forall A, B: A \cup B = \{ x | x \in A \lor x \in B \}$.
	- also, $A \cup B$ contains all elements of A and B.
		- $\forall A, B: (A \cup B \supseteq A) \land (A \cup B \supseteq B)$ 
	- the **required form** should not have repeats
- **intersections** are the set containing all the elements that are in **both** $A$ and $B$. 
	- formally, they are denoted as $\forall A, B: A \cap B = \{ x | x \in A \land x \in B \}$.
	- also, $A \cap B$ is a subset of A and B.
		- $\forall A, B: (A \cap B \subseteq A) \land (A \cap B \subseteq B)$ 
- two sets $A$, $B$ are called **disjointed** if and only if the intersection is empty. ($A \cap B = \emptyset$)
- for sets $A$, $B$, the **difference/complement** of $A$ and $B$ ($A-B$) is the set of all elements in $A$ but not in $B$.
	- $\{x | x \in A \land x \notin B\} = \{x | \lnot( x \in A \rightarrow x \in B)\}$ 
	- *ex.* $\{1, 2, 3, 4, 5, 6\} - \{2, 3, 5, 7, 9, 11\} = \{1, 4, 6\}$
	- ![set-chomp.png|316](/img/user/zimages/set-chomp.png)
- the **complement** of a set is written as $\bar A$. it is $U-A$
	- the **universe of discourse** can be considered a set (call it $U$)
	- ![set-u.png|315](/img/user/zimages/set-u.png)
- **symmetric difference difference**
	- $A \oplus B$ is the set of elements that are a member of exactly one of A and B, but not both.
	- $A \oplus B = (A - B) \cup (B - A)$
	- *ex.* $A = \{a, b, c, e, f\}, B = \{d, e, f, g\} A \oplus B = \{ e, f \}$
## set identities
### types of set identities
- identity
	- $A \cup \emptyset = A$
	- $A \cap U = A$
- domination
	- $A \cup U = U$
	- $A \cap \emptyset = \emptyset$
- idempotent
	- $A \cup A = A = A \cap A$
- double complement
	- $\overline{(\bar A)} = A$
- commutative
	- $A \cup B = B \cup A$
	- $A \cap B = B \cap A$
- associative
	- $A \cup (B \cup C) = (A \cup B) \cup C$
	- $A \cap (B \cap C) = (A \cap B) \cap C$
- demorgan's law for sets
	- $\overline{A \cup B} = \bar A \cap \bar B$ 
	- $\overline{A \cap B} = \bar A \cup \bar B$
### proving set identities
- to prove statements about sets (form $E_1 = E_2$ where $E_i$ are **set expressions**)
	- **prove** $E_1 \subseteq E_2$ and $E_2 \subseteq E_1$ separately.
	- use **logical equivalences**
	- use a **membership table**
- *ex.* Show $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
	- ![set-example.png](/img/user/zimages/set-example.png)
- *ex.* you could also use truth tables for propositional logic.
	- columns for different set expressions.
	- rows for all combinations of memberships in constituent sets.
	- use "1" to indicate
	- prove equivalence with identical columns
		- prove $(A \cup B) - B = A - B$

| $A$ | $B$ | $A \cup B$ | $(A \cup B) - B$ | $A - B$ |
| --- | --- | ---------- | ---------------- | ------- |
| 0   | 0   | 0          | 0                | 0       |
| 0   | 1   | 1          | 0                | 0       |
| 1   | 0   | 1          | 1                | 1       |
| 1   | 1   | 1          | 0                | 0       |
- prove $(A \cup B) - C = (A - C) \cup (B - C)$

| $ABC$ | $A\cup B$ | $(A \cup B) - C$ | $A-C$ | $B-C$ | $(A-C) \cup (B-C)$ |
| ----- | --------- | ---------------- | ----- | ----- | ------------------ |
| $000$ | $0$       | $0$              | $0$   | $0$   | $0$                |
| $001$ | $0$       | $0$              | $0$   | $0$   | $0$                |
| $010$ | $1$       | $1$              | $0$   | $1$   | $1$                |
| $011$ | $1$       | $0$              | $0$   | $0$   | $0$                |
| $100$ | $1$       | $1$              | $1$   | $0$   | $1$                |
| $101$ | $1$       | $0$              | $0$   | $0$   | $0$                |
| $110$ | $1$       | $1$              | $1$   | $1$   | $1$                |
| $111$ | $1$       | $0$              | $0$   | $0$   | $0$                |
## generalized union/intersections
- binary union operator: $A \cup B$
	- *n*-ary union: $A_1 \cup A_2 \cup \ldots \cup A_n := ((\ldots((A_1 \cup A_2) \cup \ldots ) \cup A_n)$
		- (grouping and order is irrelevant.)
	- "Big U" notation: $\bigcup_{i=1}^{n} A_i$
	- or for infinite sets of sets: $\bigcup_{A \in X} A$
- binary intersection operator: $A \cap B$
	- *n*-ary intersection: $A_1 \cap A_2 \cap \ldots \cap A_n := ((\ldots((A_1 \cap A_2) \cap \ldots ) \cap A_n)$
		- (grouping and order is irrelevant.)
	- "Big Arch" notation: $\bigcap_{i=1}^{n} A_i$
	- or for infinite sets of sets: $\bigcap_{A \in X} A$
