---
{"dg-publish":true,"permalink":"/y3-fall/comp-org-prog/computer-abstractions-and-technology/","dg-note-properties":{}}
---

# 🏛️ TLDR
- a **computer** is universal logic: any mechanism designed to process data through sequences of arithmetic or logical operations
	- modern implementation: digital devices running **Von Neumann architecture**
	- hardware is "brain dead" without a program — a program is a written sequence that tells hardware what to do
- **Von Neumann architecture** = the "stored-program" concept, where instructions and data live in the same memory
	- four key components: **CPU** (control unit, ALU, registers), **memory**, **input/output**, **system bus**
	- transistors are the building blocks of all ICs (integrated circuits)
- 4 classes of computers: **personal computers** (general-purpose), **server computers** (network-based, high capacity), **supercomputers** (a type of server for heavy engineering/science calculations), **embedded computers** (hidden inside other systems, low power/cost)
- **7 great ideas in computer architecture**: abstraction, making the common case fast, parallelism, pipelining, prediction, memory hierarchy, dependability via redundancy
- programs run through 3 layers: **application software** (high-level, human-readable) → **system software** (compilers, OS, assembly) → **hardware** (physical bits and encoded instructions)
- inside a **CPU**: **datapath** (moves/processes data), **ALU** (arithmetic/logical operations), **registers** (small, fast storage), **control unit** (directs operations), **cache memory** (fast access to frequently-used data)
- **volatile** main memory loses data when powered off; **non-volatile** secondary memory (disk, flash, HDD, CD/DVD) is long-term storage

## What is a Computer?
- **universal logic**: any mechanism designed to process data through sequences of arithmetic or logical operations
- modern implementation: digital devices running **Von Neumann architecture**
- hardware is "brain dead" without a program — a **program** is a written sequence (in some language) that tells hardware what to do

### Von Neumann Architecture
- the **"stored-program"** concept: instructions and data are stored in the same memory
- four key components:
	- **CPU** (control unit, arithmetic logic unit, registers)
	- **memory**
	- **input/output**
	- **system bus**
- transistors are the building blocks of all **ICs** (integrated circuits)

### Classes of Computers
- **personal computers**: general-purpose, run a variety of software
- **server computers**: network-based, high capacity/performance
- **supercomputers**: a type of server with high capability for engineering and scientific calculations
- **embedded computers**: hidden as components inside other systems — low power, low cost

### Semiconductors
- *(open question from lecture, still unanswered: what semiconductors do and how they're made — revisit)*

## Seven Great Ideas in Computer Architecture
1. **use abstraction to simplify design** — abstraction hides the complexity of lower-level details
2. **make the common case fast** — most systems have operations that occur far more frequently than others; it's better to optimize those than rare cases
3. **performance via parallelism** — performing multiple operations simultaneously
4. **performance via pipelining** — breaking tasks into stages and executing stages of multiple tasks simultaneously
5. **performance via prediction** — anticipating future operations to minimize delays
6. **hierarchy of memories** — memory is organized into a hierarchy (registers, caches, main memory, disk); faster/smaller memories sit closer to the processor
7. **dependability via redundancy** — adding extra components or information to improve reliability in case of failure

## How Does a Program Work?
- **application software**: written in a high-level language
	- closer to the problem domain, easy for humans to understand
- **system software**: compilers, OS, etc.
	- includes **assembly language** — a textual representation of instructions
- **hardware**: processor, memory, I/O, etc.
	- uses physical binary digits (bits) and encoded instructions/data
- *(diagram in the original: a layered stack — application software → system software → hardware — matching the three layers above)*

## What's in a CPU?
- **datapath**: provides hardware paths for processing/moving data
- **ALU**: arithmetic and logical operations
- **registers**: small and fast storage for intermediate results
- **control unit**: directs and coordinates processor operations
- **cache memory**: provides fast access to frequently-used data

## What About Storage?
- **volatile** main memory loses its instructions and data once powered off
- **non-volatile secondary** memory is long-term storage — magnetic disk, flash memory, hard drive, CD/DVD, etc.

⬅ *back: [[Y3 - Fall/COMP ORG + PROG/syllabus-csc3210\|syllabus-csc3210]]*
➡ *next: [[Y3 - Fall/COMP ORG + PROG/computer-performance\|computer-performance]]*
