---
{"dg-publish":true,"permalink":"/y3-fall/math-3020-stats-for-cs/08-26-basics-and-syllabus/","dg-note-properties":{}}
---

math 3020
# syllabus
syllabus.
- attendance will be qr code based
- everything is recorded but its still important to take notes.
- you cant do cs w/o math, thats why this is important
	- they are fundamental, all code is mathematically inclined
	- in fact, every data structure is math
- course is built into two parts, probability and statistics
- probability = chap. 2,3,4
- statistics = chap. everything else
# basics part 1
demonstration 1.

make a prediction. 
flip a coin 25 times, heads / tails

i found 13 heads/12 tails
most were in 12-14. shown in a histogram
(bar chart vs histogram. categorical vs numerical data)

3 fundamental ideas of probability
1. experiment (recording # of successes in the experiment)
2. had independent testing
3. everyone did the same experiment (sample distribution)

- there is a variety of responses


# syllabus part 2 (combine w/ first)
** required textbook. probability and statistics for computer scientists, 3rd edition by michael baron, chapman and hall CRC press, 2019

best contact is email: vmiller@[ uni ].edu


course learning outcomes.
- apply prob. laws to concrete problems (like whats involved in it)
- display/interpret data
- statistical inference and interpreting in applied context
- use math tools including calculus and linalg to study probability
- use computer to simulate probability and statistics
- communicate concepts in prob/stat with tech language

expectations.
- be able to integrate $\int_{0}^{1}{xe^x\,dx}$
- i should bring a notebook next time. 😅😅
- brush up on calculus a bit

- infinite attempts on hw
- 1 att on quizzes

# basics whatever part 2

- probability comes from experiments
- experiments have several trials → outcomes
- set of all possible outcomes = sample space = $\Omega$
- subset of $\Omega$ = Event
---
a few examples

flip 3 coins. penny / nickel / dime
- flip once each
- all possible outcomes = sample space = $\Omega$ = {TTT, TTH, THT, HTT, THH, HTH, HHT, HHH} (2^3)
- since they dont affect each other they are independent
- events = A, B, etc (capital letters)
	- events are just subsets
- event A = getting exactly 2 heads = {HHT, HTH, THH}

another example
roll 6 sided dice
A = even numbers
B = \le 4

A union B = {1,2,3,4,6}
A int B = {2,4}
A - B = {6}

# review
empty set ($\emptyset$)
intersections, sets, complements, set difference, demorgans laws, etc. (already learned but list shortly anyways)
how to find out how something is independent or not? (also put in review)
A union B = empty set

