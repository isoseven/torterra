---
{"dg-publish":true,"permalink":"/notes/csc2510/1-21-2026/1-3-prop-equiv/"}
---

recap ➡[[notes/csc2510/1-14-2026/1-1-prop-logic-cont\|1-1-prop-logic-cont]]
# 🍿 SUMMARY
- **propositional equivalence** is pretty much like the $\equiv$ for normal mathematic equivalencies.
	- (like $2x+4 \equiv 4+2x$)
- there are a few **equivalence laws**.
	- the "arithmetic identity-like" laws
	- de morgan's law
	- absorption and negation
- you can define implication/biconditional/xor through equivalencies.
- cheat sheet below
![equivalency-cheat-sheet.png|402x337](/img/user/zimages/1-21-2026/equivalency-cheat-sheet.png)
---
## logical equivalence
- **atomic propositions**: a basic, declarative statement in logic that expresses a single idea. can't be broken down further
- **tautology**: compound proposition that is always true no matter what the truth values of its *atomic propositions* are.
	- example: $p \lor \lnot p$
		- will always be true.
- **contradiction**: compound proposition that is always false no matter what the truth values of its *atomic propositions* are.
	- example: $p \land \lnot p$
		- will always be false.
## propositional equivalence
### proving equivalency
- two **textually different** compound propositions may be semantically identical.
	- we call these **equivalent**.
	- various **rules/laws** for equivalency
	- how to prove equivalences using symbolic derivations?
- **Compound** propositions $p$ and $q$ are logically equivalent to each other **IFF** $p$ and $q$ contain the same truth values as each other in all rows of their truth tables.
	- $p$ here is a compound proposition.
	- the symbol $\equiv$ or $\Leftrightarrow$ is a logical equivalency **IFF** $p \leftrightarrow q$ is a tautology.
	- this is not a logical connective; $p \Leftrightarrow q$ is not a compound proposition but rather the statement that $p \leftrightarrow q$ is a tautology.
		- example: $p \lor q \Leftrightarrow \lnot (\lnot p \land \lnot q )$.
		- ![tautology.png|354x140](/img/user/zimages/1-14-2026/tautology.png)
### equivalence laws

> [!note] 
> note: $\top$ = true. $\bot$ = false.

- similar to **arithmetic identities**.
	- **identity**: $p \land \top \Leftrightarrow p$      //      $p \lor \bot \Leftrightarrow p$
		- something + something true will always stay the same.
		- similarly something OR something false will always stay the same.
	- **domination**: $p \lor \top \Leftrightarrow \top$      //      $p \land \bot \Leftrightarrow \bot$
		- the opposite of identity; it doesnt matter if the condition is already met.
	- **idempotent**: $p \lor p \Leftrightarrow p$      //      $p \land p \Leftrightarrow p$
		- having the two same values in either and/or will be equivalent to the same.
	- **double negation**: $\lnot \lnot p \Leftrightarrow p$
		- self explanatory.
	- **commutative**: $p \lor q \Leftrightarrow q \lor p$      //      $p \land q \Leftrightarrow q \land p$
		- $p$ or/and $q$ is the same statement as $q$ or/and $p$.
	- **associative**: $(p \lor q) \lor r \Leftrightarrow p \lor (q \lor r)$      //      $p \land (q \land r) \Leftrightarrow p \land (q \land r)$
		- you may move the parentheses; they do not matter when it comes to the same operator
		- note that associative will have **similar operators** as opposed to distributive.
	- **distributive**: $p \lor (q \land r) \Leftrightarrow (p \lor q) \land (p \lor r)$      //      $p \land (q \lor r) \Leftrightarrow (p \land q) \lor (p \land r)$
		- you may also distribute these similarly to arithmetic.
		- note that distributive will have **different operators** as opposed to associative.
- **De Morgan's law**:
	- **logical equivalences** that show how to correctly **distribute a negation operation** inside a **parenthesized** expression.
		- $\lnot (p \land q) \Leftrightarrow \lnot p \lor \lnot q$      //      $\lnot (p \lor q) \Leftrightarrow \lnot p \land \lnot q$
			- basically $\land$ and $\lor$ **switch** when negating something in parentheses.
- **more equivalence laws**
	- **absorption**: $p \lor (p \land q) \Leftrightarrow p$      //      $p \land (p \lor q) \Leftrightarrow p$
		- in neither of these $q$ will matter. they become **idempotent** if reduced.
	- **negation**: $p \lor \lnot p \Leftrightarrow \top$      //      $p \land \lnot p \Leftrightarrow \bot$
		- comparing $p$ and NOT $p$ will **always lead** to a comparison between TRUE and FALSE.
		- this will lead to another case of **domination**.
x
### defining operators through equivalencies
- **implication**: 
	- $p \rightarrow q \Leftrightarrow \lnot p \lor q$
- **biconditional**:
	- $p \leftrightarrow q \Leftrightarrow (p \rightarrow q) \land (q \rightarrow p)$
	- $p \leftrightarrow q \Leftrightarrow \lnot(p \oplus q)$
- **exclusive or**:
	- $p \oplus q \Leftrightarrow (p \lor q) \land \lnot (p \land q)$
	- $p \oplus q \Leftrightarrow (p \land \lnot q) \lor (p \land \lnot q)$

![equivalency-cheat-sheet.png|402x337](/img/user/zimages/1-21-2026/equivalency-cheat-sheet.png)

