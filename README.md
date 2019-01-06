# Little Comp Sci

A little book of compsci notes.

## Complexity Theory

### P(olynomial)-Time

T = 2x
- sorting, searching, zipping, enumerating
- work proprotionate to input
- something is "in P" if it's solvable in polynomial time

### Exp(oentnial)-Time

T = 2^n
- solvable in exponential time (hard)
- time grows factorially with input size

### All Solvable Problems (R)
- All problems solvable in finite time
- P < EXP < R

### N(ondeterministic) Polynomial Time
- Solvable in exponential time
- Verifiable in polynomial time
- Solvable in polynomial time given nondeterministic algorithim 

#### NP-Complete
- Decision problems classifiable in NP
- [Karp's 21 NP-Complete problems](https://en.wikipedia.org/wiki/Karp%27s_21_NP-complete_problems)

#### NP-Hard
- Problems that can be reduced to other problems in NP, but are not within NP
themselves
- "What is optimal in set X for group Y?" vs "Is A optimal for everyone in Y?"
- Halting problem
