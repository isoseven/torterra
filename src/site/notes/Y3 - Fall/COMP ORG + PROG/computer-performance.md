---
{"dg-publish":true,"permalink":"/y3-fall/comp-org-prog/computer-performance/","dg-note-properties":{}}
---

# ⏱️ TLDR
- **response time**: how long it takes to do one task
- **throughput** (bandwidth): number of tasks completed per unit time
- **relative performance**: performance $= 1/\text{execution time}$; "X is $n$ times faster than Y" means $P_x / P_y = \text{execution time Y} / \text{execution time X} = n$
- 2 ways to measure execution time: **elapsed time** (total time incl. processing, waiting, overhead) vs. **CPU time** (pure processing time — split into **user CPU time** and **system CPU time**)
- $\text{CPU Time} = \text{CPU Clock Cycles} \times \text{Clock Cycle Time} = \frac{\text{CPU clock cycles}}{\text{Clock Rate}}$ — performance improves by reducing clock cycles or increasing clock rate
- **CPI** (cycles per instruction) varies by instruction class; $\text{CPI} = \frac{\text{Clock Cycles}}{\text{Instruction Count}} = \sum_{i=1}{n} \frac{\text{CPI}_i * \text{Instruction Count}_i}{\text{Instruction Count}}$ (weighted average)
- **multiprocessors**: multicore chips need explicit parallel programming (unlike instruction-level parallelism, which is hidden from humans) — hard because of load balancing and synchronization
- misconception: naively expecting **Amdahl's law** to give a proportional improvement from improving just one aspect of a computer (e.g. 60Hz→120Hz feels like a bigger jump than 120Hz→180Hz, even though both are +60Hz)
- misconception: "computers at low utilization use little power" is a **fallacy** — power benchmarks show ~50% power draw at only 10% load

## Computer Performance
- **response time**: how long it takes to do one task
- **throughput** (also called bandwidth): number of tasks completed per unit time
- both are affected by things like replacing the processor with a faster one, or adding more processors

## Relative Performance
1. defining performance: $\text{performance} = 1/\text{execution time}$
2. comparing performance: "X is $n$ times faster than Y" means
	$$P_x / P_y = \text{execution time Y} / \text{execution time of X} = n$$

### Measuring Execution Time
1. **elapsed time**: total time to complete a task, including processing, waiting, and overhead time (processing time, I/O time, OS overhead, idle time)
2. **CPU time**: pure processing time spent by the CPU on a specific task
	- **user CPU time**: time spent executing user-level code
	- **system CPU time**: time spent executing OS code
- **CPU clock**: clock cycles are the time intervals in which hardware events take place
	- *(diagram in the original: a timeline showing individual clock cycles/ticks)*

## Basic Relationships
### Clock Period Units
| unit | symbol |
| --- | --- |
| 1 second | s |
| 1 millisecond | ms |
| 1 microsecond | μs |
| 1 nanosecond | ns |
| 1 picosecond | ps |
| 1 femtosecond | fs |
| 1 attosecond | as |

### Frequency Units
| unit | rate |
| --- | --- |
| 1 kilohertz | 1000 cycles per second |
| 1 megahertz | $10^6$ cycles/sec |
| 1 gigahertz | $10^9$ cycles/sec |
| 1 terahertz | $10^{12}$ cycles/sec |

### CPU Time
$$\text{CPU Time} = \text{CPU Clock Cycles} \times \text{Clock Cycle Time} = \frac{\text{CPU clock cycles}}{\text{Clock Rate}}$$
- performance improves by reducing the number of clock cycles, or by increasing the clock rate

### Instruction Count and CPI
- clock cycles = instruction count × cycles per instruction
- CPU time = instruction count × CPI × clock cycle time = instruction count × CPI / clock rate
- different instruction classes take different numbers of cycles
- clock cycles = $\sum_{i=1}^{n} \text{CPI}_i * \text{Instruction Count}_i$
- **weighted average CPI**:
	$$\text{CPI} = \frac{\text{Clock Cycles}}{\text{Instruction Count}} = \sum_{i=1}{n} \frac{\text{CPI}_i * \text{Instruction Count}_i}{\text{Instruction Count}}$$

## Multiprocessors
- **multicore microprocessors**: more than one processor per chip
- multicore requires **explicit parallel programming**
	- compare with **instruction-level parallelism**: hardware executes multiple instructions at once, hidden from humans
	- explicit parallel programming is hard: programming for performance, load balancing, optimizing communication and synchronization

## Common Misconceptions

> [!warning]
> **Amdahl's law misconception**: improving one aspect of a computer and expecting a *proportional* improvement in overall performance. Think of it like going from 60Hz to 120Hz vs. 120Hz to 180Hz — same +60Hz jump, but they don't feel equally impactful.

> [!warning]
> **Fallacy**: "computers at low utilization use little power." Power benchmarks show ~50% power draw at only 10% load — this is why processors should be designed so power is proportional to load.

⬅ *back: [[Y3 - Fall/COMP ORG + PROG/computer-abstractions-and-technology\|computer-abstractions-and-technology]]*
