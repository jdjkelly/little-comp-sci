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

## Lambda Calculus
- Functions are the only data type
- Reduction through application
- Function arity of one (currying - breaking a function with multiple arguments
into chained functions with an arity of one)

```
λx.x
function argument . body/return
```

### Identity
```
λx.x
```

### Constant
```
λx.y
```

### Booleans
- True returns the first value
```
λx.λy.x
```
- False returns the second value
```
λx.λy.y
```

### Conditionals
```
λx.λy.λz.x y z
``
```

### Numbers
```
λf.λx.x         # 0
λf.λx.f x       # 1
λf.λx.f f x     # 2
```

### Combinators
- A higher order function that uses only function application and earlier
defined combinators to define a result from its arguments

#### Omega Combinator
```
λx.xx
```
- Given x, return the application of x to x

#### Y Combinator
- Recursive, fixed point function: yf = f(yf) forall f
- You give it a function as an argument it invokes, it then returns that
function back out to you
```
λf.(λx.f(xx))(λx.f(xx))
```

## Machinery

### Markov Chains
- A set of states with rules that allow transition between those states

### Finite State Machine

#### Deterministic
- Every state has a single transition for every action until we finally reach
acceptance or rejection

#### Nondeterministic
- One or more transitions for a set of actions, and these transitions are
essentially "random"
- Capable of transitioning from one state to the next as a result of some
random choice, independent of prior state

### Pushdown Machine
- A finite state machine with a stack
- Two additional operations: push and pop

### Turing Machine
- Introduced by Turing in ('On Computable Numbers')[https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf]
- Composable machines, equivalent to functions
- (Church-Turing Conjecture)[https://en.wikipedia.org/wiki/Church%E2%80%93Turing_thesis}:
  - > If an algorithim is computable, a Turing Machine can compute it
  - > All total functions are computable

### Von Neumann Machine
- Turing submits plans to National Physics Laboratory: 'Automatic Computing Engine'
- input > ( CPU ( control unit, logic unit) <> memory unit ) > output

## Big O

### O(1)
- order 1
- on the order of 1 operation for all possible inputs
- for all inputs to our program, only one operation will be required
- ex. accessing first element of an array with an index

### O(N)
- order n
- for all inputs to our program, the number of operations grows linearly
- ex. summing an array of numbers

### O(N^2)
