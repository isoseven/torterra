---
{"dg-publish":true,"permalink":"/notes/csc2510/1-28-2026/1-4-predicates-quantifiers/"}
---

# 👨‍🦼 SUMMARY
- **predicate logic** = propositional logic that allows concise reasoning about **entire classes** of entities
	- subject = the object the sentence is about
	- predicate = property of the subject
- **predicate logic** includes propositional functions of **any** number of arguments.
	- the collection of values that a variable $x$ can take is called $x$'s **universe of discourse**.
- **quantifiers** allow us to narrow the **universe of discourse** of $x$.
	- $\forall$ is the **universal quantifier**. it means that for $P(x)$ all values of $x$ hold true.
	- $\exists$ is the **existential quantifier**. it means that for $P(x)$ at least one value of $x$ holds true.
	- **quantifiers can also be nested** and bind different variables in the same predicate. the order of quantifiers is **important**.
- **equivalence laws to know**:
	- demorgan's law
	- negation of quantifiers
	- order of identical quantifiers
	- distributing quantifiers
- **quantifier scope**
	- the **part** of a logical expression where the **quantifier is applied**.
- **free variables** are undefined variables. ($P(x)$ has a free variable $x$)
- **bound variables** are a free variable that is operated on by a **quantifier**.
## predicates
### predicate logic
- **predicate logic** is an extension of propositional logic that allows concise reasoning about whole **classes** of entities.
	- "$x>1$" , "$x+y = 10$"
	- these are neither true or false when the values of the variables are **not specified**.
- these are used in:
	- formal notation for clear/concise/unambiguous mathematical things.
	- supported by some more sophisticated database query engines
	- basis for automatic theorem provers and other AI systems
### subject and predicates
- the proposition "**the dog is sleeping**" has two parts:
	- the dog = **subject** (the object that the sentence is about)
	- the predicate = **predicate** (a property the subject can have)
- a predicate is modeled as a function $P()$ from objects to propositions.
	- $P(x)$ = "x is sleeping"
- the result of applying a predicate $P$ to an object $x=a$ is the **proposition** $P(a)$.
	- if $P(x)$ = "$x > 1$", then $P(3)$ is the proposition "3 is greater than 1".

> [!warning] 
> the predicate $P$ itself ("is sleeping") is **not** a proposition.
### propositional functions
- predicate logic includes propositional functions of **any** number of arguments.
	- let $P(x,y,z)$ = "$x$ gave $y$ the grade $z$"
- a predicate can depend on more than one variable.
	- $Q(x,y): x^{2} = y$,  $R(x,y,z): x+y = z$
	- $Q(5,25) = \top$,  $R(2,3,6) = \bot$
- the collection of values that a variable $x$ can take is called $x$'s **universe of discourse** (shortened: u.d.).
	- Let $P(x) = x+1 > x$ .
	- we could define the universe of discourse as **the set of integers**.
	- example:
		- a **natural domain** for the variable $x$ in the predicate "$x$ is an odd tnumber" would be the set of **all integers**.
		- If the domain of a variable in a predicate is **not clear** from context, the domain **should be given** with the predicate.

## quantifier expressions
- **quantifiers** allow us to quantify (count) how many objects in the **universe of discourse** satisfy a given predicate.
### $\forall$
 - $\forall$ is the FORALL or **universal quantifier**.
- $\forall x\,P(x)$ means **for all $x$ in the u.d.**, P holds.
- how to disprove it?
	- to prove that a statement of the form $\forall x\,P(x)$ is **FALSE**, it suffices to find a value of $x$ **in the u.d.** such that $P(x)$ is **FALSE**.
- example
	- let $P(x)$ be the predicate "$x$ is full."
	- let the u.d. of $x$ be *parking spaces at GSU*.
	- the **universal quantification** of $P(x),\,\forall x\,P(x)$, is the proposition:
		- "All parking spaces at GSU are full."
		- "Every parking space at GSU is full."
		- "For each parking space at GSU, that space is full."
	- this would be **false** if you find a parking space at GSU that is **empty**.
### $\exists$
 - $\exists$ is the EXISTS or **existential quantifier**.
- $\exists x\,P(x)$ means **there exists an $x$** in the u.d. such that $P(x)$ is true.
- how to disprove it?
	- to prove that a statement of the form $\forall x\,P(x)$ is **FALSE**, you need to show that the predicate is false for **an arbitrary element from the domain**.
		- consider $\exists x\,P(x)$ where $P(x) = x(x+1) < x$
		- this statement is false because there is no positive integer that satisfies $x+1 < x$.
- example
	- let $P(x)$ be the predicate "$x$ is full."
	-  let the u.d. of $x$ be *parking spaces at GSU*.
	- the **existential quantification** of $P(x),\,\exists x\,P(x)$, is the proposition:
		- "Some parking spaces at GSU are full."
		- "There is a parking space at GSU that is full."
		- At least one parking space at GSU is full.
### Equivalence Laws (for quantifiers)
- **DeMorgan's Law**
	- $\forall x\,P(x) \Leftrightarrow P(a) \land P(b) \land P(c) \land \ldots$
	- $\exists x\,P(x) \Leftrightarrow P(a) \lor P(b) \lor P(c) \lor \ldots$
	- this proves (derived from DeMorgan's law)
		- $\forall x\,P(x) \Leftrightarrow \lnot \exists x\, \lnot P(x)$
		- $\exists x\,P(x) \Leftrightarrow \lnot \exists x\, \lnot P(x)$
- **Negation of Quantifiers**
	- $\lnot \exists x\,P(x) \Leftrightarrow \lnot \forall x\,\lnot P(x)$ 
	- $\lnot \forall x\,P(x) \Leftrightarrow \lnot \exists x\,\lnot P(x)$ 
- **Order of Identical Quantifiers**
	- $\forall x\,\forall y\,P(x,y) \Leftrightarrow \forall y\,\forall x\,P(x,y)$
	- $\exists x\,\exists y\,P(x,y) \Leftrightarrow \exists y\,\exists x\,P(x,y)$
- **Distributing Quantifiers**
- $\forall x\,(P(x) \land Q(x)) \Leftrightarrow (\forall x\,P(x)) \land (\forall x\,Q(x))$
- $\exists x\,(P(x) \land Q(x)) \Leftrightarrow (\exists x\,P(x)) \land (\exists x\,Q(x))$
### Scope of Quantifiers
- The **part of a logical expression** to which a **quantifier is applied** is called the **scope of this quantifier**.
	- $(\forall x\,P(x)) \land (\exists y\,Q(y))$
	- $(\forall x\,P(x)) \land (\exists x\,Q(x))$

![activity-evaluating-quantified-statements.png](/img/user/zimages/1-28-2026/activity-evaluating-quantified-statements.png)
### Free and Bound Variables
- an expression like **P(x)** is said to have a **free variable** x.
	- x is undefined.
- a **quantifier** ($\forall$ or $\exists$) operates on an expression having **one or more free variables**, and binds one or more of those variables to produce an expression having **one or more bound variables**.
	- example of binding:
		- $P(x,y)$ has **free variables** $x$ and $y$.
		- $\forall x\,P(x,y)$ has 1 free variable ($y$) and one bound variable ($x$).
		- $P(x)$, where $x=3$ is another way to bind $x$.
		- an expression with **zero** free variables is an actual **proposition**.
		- an expression with **one or more** free variables is still only a **predicate**.
- **more to know about binding**.
	- $\forall x\,\exists x\,P(x)$ : $x$ is not a free variable in $\exists x\,P(x)$, therefore the $\forall x$ binding isn't used.
	- $(\forall x\,P(x)) \land Q(x)$ : $x$ is outside of the scope of the $\forall x$ quantifier and is therefore free.
	- $(\forall x\,\,P(x)) \land (\exists x\,\,Q(x))$ : Legal because there are two **different** $x$s. You can change the second $x$ into a $y$.
	- quantifiers bind as loosely as needed.
		- $\forall x (P(x) \land Q(x))$ makes this a proposition because you can distribute the quantifier.
## nested quantifiers
- a **logical expression** with more than one quantifier that bind **different variables in the same predicate**
	- example:
	- ![nested-quantifier-example.png|489x150](/img/user/zimages/1-28-2026/nested-quantifier-example.png)
- exist within the scope of other quantifiers
	- let the u.d. of $x$ and $y$ be people
	- let $P(x, y)$ = "$x$ likes $y$" (predicate, 2 free vars.)
	- then $\exists y\,P(x,y)$ = "There is someone whom $x$ likes." (predicate, 1 free var $x$)
	- then $\forall x\,(\exists y\,P(x,y))$ = "Everyone has someone who they like." (proposition, 0 free variables.)

> [!warning] 
> the order of quantifiers is **important** and natural language is **ambiguous**!!
> try to express in **unambiguous** english. leave no guessing room.

## notation conventions
- $\forall x\,\forall y\,\forall z\,P(x,y,z) \Leftrightarrow \forall x,y,z\,P(x,y,z) \Leftrightarrow \forall xyz\,P(x,y,z)$
- sometimes u.d. is restricted with quantification:
	- $\forall x>0\,P(x)$ is shorthand for "For all $x$ that are greater than 0, $P(x)$."
	- $\exists x>0\,P(x)$ is shorthand for "There is an $x$ greater than 0 such that $P(x)."

## defining new quantifiers
- as per name, quantifiers can express that a predicate is true of any given **quantity** of objects.