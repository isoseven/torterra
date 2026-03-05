---
{"dg-publish":true,"permalink":"/notes/csc2510/1-12-2026/1-1-prop-logic/"}
---

# 👽 SUMMARY
- propositions are declarative statements. they are true or false.
- operators create new statements.
- connectives are operators that deal with propositions/booleans.
- compound propositions are propositions + connectives

---

## what is propositional logic?
- Logic of compound statements built from **simpler statements** using **boolean connectives**
- **boolean connectives** (see below)
## propositions
- proposition = declarative statement that is true or false.
	- example: 
		- is it raining? (yes)
		- 1+2=3 (no)
		- who's there? (not a proposition)
		- 1+2 (no)
## operator/connective
- **operator/connective** = combines 1+ operand expressions into larger expression
	- unary operators: modifies 1 operand (-3, !True)
	- binary operators: connects 2 operands in some way (3x4, 12 / 4, True OR False)
	- negation operator:
		- $\lnot p$ = "it is not the case that p." / "not p"

| $p$ | $\lnot p$ |
| --- | --------- |
| T   | F         |
| F   | T         |
( here is a truth table for $\lnot p$. )

- **proposition/boolean** = truth values instead of on numbers
- **compound proposition** = existing propositions using logical operators
- boolean connectives:
and: $\land$       or: $\lor$       not: $\lnot$         xor: $\oplus$           implication: $\rightarrow$        equivalence: $\iff$