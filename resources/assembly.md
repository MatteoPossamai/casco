# Assembly

Short description of the Assembly-like code adopted in this work, the motivations and open questions.

## Thoughts and motivations

- We don't need a type system. We have the most basic data types, that we can tread as number all the time without dealing with anything else (less complexity);
- As in BIR, each operation should have no side effects and affect 1 variable (register or memory) at a time. This means that probably our language will not have explicit `call` and `ret` functions. This due to the multiple instructions they implement, and the difficulty in modeling the interleaving of all of this sub steps;
- Our representations should be easily translatable from and to real Assembly code;
- We don't want to model anything more complex than memory and registers. No variables, no implicit stack and so on;

## Operations that we want to model

- `mov`
- `cmov`
- All binary operations (add, sub, ...)
- All unary operations (neg, ...)
- `load`
- `store`
- `skip`
- `jmp`
- `jz`
- `lfence`
- ...

## Syntax

### Version 1
Fusion between $\mu ASM$ and BIR.
$$ 
\begin{align}
&\text{BASIC TYPES} \\
&(Registers) & x &\in Regs \\
&(Values) &n, l &\in Vals = \mathbb{N} \cup \{\bot\} \\
&(Operators) &op &\in OPS \\
&\text{SYNTAX} \\ 
&(Expressions) &e &:= \text{n | x | \text{\textbf{skip}}} | \text{\textbf{mov}(x, e)} \\
&&& \text{\textbf{cmov}}(x_d, e_s, e_c) | \text{\textbf{BOP}}(op, e_1, e_2) | \\ 
&&& \text{\textbf{UOP}(op, e)} | \text{\textbf{load}(x, e)} | \text{\textbf{store}(x, e)} | \\
&&& \text{\textbf{beqz}(x, l)} | \text{\textbf{jmp}(l)} | \text{\textbf{lfence}}\\
&(Program) &p &:= \text{n:i  |  p1;p2} \\
\end{align}
$$
