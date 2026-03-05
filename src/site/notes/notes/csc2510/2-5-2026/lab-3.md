---
{"dg-publish":true,"permalink":"/notes/csc2510/2-5-2026/lab-3/"}
---

1. Let P(x) be the statement “the word x contains the letter a.” What are these truth values?
	- P(orange) = "the word orange contains the letter a" = True
	- P(lemon) = "the word lemon contains the letter a" = False
	- P(true) = "the word true contains the letter a" = False
	- P(false) = "the word false contains the letter a" = True
2. Determine the truth value of each of these statements if the domain of each variable consists of all real numbers. (12 Points)
	- $\exists x\,(x^2 = 2)$ : True ($x = \sqrt{2}$)
	- $\exists x\,(x^2 = -1)$ : False ($\forall x\,(x^2 \ge 0)$)
	- $\forall x\,(x^2 + 2 \ge 1)$ : True ($\forall x\,(x^2 \ge 0)$, $x^2+2 \ge 2$, $2 \ge 1$.)
	- $\forall x\,(x^2 \ne x)$ : False ($x = 0$. $x = 1$)
3. Let C(x,y) mean that student x is enrolled in class y, where the domain for x consists of all students in your school and the domain for y consists of all classes being given at your school. Express each of these statements by a simple English sentence. (18 Points)
	- $C(\textrm{Randy Goldberg}, \textrm{CS 252})$ : Randy Goldberg is enrolled in CS 252.
	- $\exists x\,C(x, \textrm{Math 695})$ : There is a student that is enrolled in Math 695.
	- $\exists y\,C(\textrm{Carol Sitea}, y)$ : Carol Sitea is enrolled in at least one class.
	- $\exists x\,\bigl( C(x, \textrm{Math 222}) \land C(x, \textrm{CS 252})\bigr)$ : There is a student enrolled in both Math 222 and CS 252.
	- $\exists x\,\exists y\,\forall z\,\bigl((x \ne y) \land (C(x,z) \rightarrow C(y,z))\bigr)$ : There are two students such that every class taken by the first student is also taken by the second student.
	- $\exists x\,\exists y\,\forall z\,\bigl((x \ne y) \land (C(x,z) \leftrightarrow C(y,z))\bigr)$ : There are two students that are enrolled in exactly the same classes.
4. Let F(x, y) be the statement “x can fool y,” where the domain consists of all people in the world. Use quantifiers to express each of these statements. (33 Points)
	- Everybody can fool Fred. : $\forall x\,F(x, \textrm{Fred})$
	- Evelyn can fool everybody. : $\forall x\,F(\textrm{Evelyn}, y)$
	- Everybody can fool somebody. : $\forall x\,\exists y\,F(x, y)$
	- There is no one who can fool everybody. : $\lnot \exists x\,\forall y\,F(x, y)$
	- Everyone can be fooled by somebody. : $\forall y\,\exists x\,F(x,y)$
	- No one can fool both Fred and Jerry. : $\forall x\,\lnot\bigl(F(x, \textrm{Fred}) \land F(x, \textrm{Jerry}\bigr)$
	- Nancy can fool exactly two people. : $\exists y_1\,\exists y_2 \Bigl(y_1 \ne y_2 \land F(\textrm{Nancy}, y_1) \land F(\textrm{Nancy}, y_2) \land \forall y_3\,\bigl(y_3 \ne y_1 \land y_3 \ne y_2 \rightarrow \lnot F(\textrm{Nancy}, y_3)\bigr)\Bigr)$
		- there exists two people (unique) that nancy can fool, and for all other people nancy can not fool.
	- There is exactly one person whom everybody can fool. $\exists y\,\Bigl(\forall x\,F(x, y) \land \forall z \bigl(z \ne y \rightarrow \exists x\,\lnot F(x, z)\bigr)\Bigr)$
		- there exists a person that everyone can fool AND for everyone else, not everyone can fool that person.
	- No one can fool himself or herself.
		- $\forall x\,\lnot F(x, x)$
	- There is someone who can fool exactly one person besides himself or herself.
		- $\exists x\,\exists y\,\,\Bigl(y \ne x \land F(x,y) \land \forall z \,\bigl((F(x,z) \land z \ne x\bigr) \rightarrow z\Bigr)$
5. Show that the two statements $\exists x (T(x) \wedge P(x) \wedge \neg Q(x))$ and $\neg \forall x ((T(x) \wedge P(x)) \to Q(x))$ are logically equivalent.
	- $\neg \forall x\,\bigl((T(x) \land P(x))\rightarrow Q(x)\bigr)$
	- $\lnot \forall x\,\bigl((T(x)\land P(x)\bigr) \rightarrow Q(x)) \equiv \exists x\,\lnot \bigl((T(x) \land P(x)\bigr) \rightarrow Q(x))$
	- $\lnot \bigl((T(x)\land P(x)) \rightarrow Q(x)\bigr) \equiv (T(x)\land P(x)) \land \lnot Q(x)$ 
	- $\exists x \,\lnot \bigl((T(x)\land P(x)) \rightarrow Q(x)\bigr) \equiv \exists x \,\bigl((T(x)\land P(x)) \land \lnot Q(x)\bigr)$ 
	- $\exists x \,\bigl((T(x)\land P(x)) \land \lnot Q(x)\bigr) \equiv \exists x \,\bigl(T(x)\land P(x) \land \lnot Q(x)\bigr)$