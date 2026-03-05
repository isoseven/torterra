---
{"dg-publish":true,"permalink":"/notes/csc2510/2-12-2026/lab-4/"}
---

1. First translate the following statements into propositional expressions and then use the rules of equivalence and inference to prove the conclusion. **If the program is efficient, it executes quickly. Either the program is efficient, or it has a bug. However, the program does not execute quickly. Therefore, it has a bug. (use letters E, Q, B)**
	- $E \rightarrow Q$
	  $E \lor B$
	  $\lnot Q$
	  $\therefore B$
2. Prove that the following argument is valid: (¬R ∨ ¬F → S ∧ L) ∧ (S → T) ∧ ¬T → R  
	- $(\lnot R \lor \lnot F \rightarrow S \land L) \land (S \rightarrow T) \land \lnot T$
	  $(\lnot R \lor \lnot F \rightarrow S \land L) \land \lnot S$ (modus ponens)
	  $\big(\lnot(S \land L) \rightarrow \lnot (\lnot R \lor \lnot F)\big) \land \lnot S$ (contrapositive of $\lnot R \lor \lnot F \rightarrow S \land L$)
	  $\big(\top \rightarrow \lnot (\lnot R \lor \lnot F) \big) \land \lnot S$ (because $\lnot S$ is true, we can conclude that $\lnot(S \land L)$ is true)
	  $\lnot (\lnot R \lor \lnot F) \land \lnot S$ (we can remove $\lnot(S \land L)$ because of modus ponens)
	  $z$ (demorgan's law)
	  $R \land F$ (modus ponens)
	  $\therefore R$
3. Let s(x) be “ x is a movie produced by Sayles,” let c(x) be “ x is a movie about coal miners,” and let w(x) be “movie x is wonderful.” We are given premises ∀x(s(x)→ w(x)) and ∃x(s(x) ∧ c(x)) , and we want to conclude ∃x(c(x) ∧ w(x)) . In our proof, y represents an unspecified particular movie.
	- premises:
	  $\forall x \, ( s(x) \rightarrow w(x))$ = every Sayles movie is wonderful
	  $\exists x \, (s(x) \land c(x))$ = there is at least one movie produced by Salyes and about coal miners.
	  $\exists x \, (c(x) \land w(x))$ = there is at least one movie about coal miners that is wonderful
	  $s(y) \rightarrow c(y)$ (we know that this movie y exists)
	  $s(y) \rightarrow w(y)$ 
	  $\therefore w(y)$ (modus ponens, $s(y)$ is true)
	  $\therefore c(y) \land w(y)$ (build conjunction)
4. Prove that if n is a positive integer, then n is even if and only if 7n + 4 is even.