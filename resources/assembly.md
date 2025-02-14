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
- All branch operations (`jz`, `jnz`, ...)
- `lfence`
- ...

## Syntax

### Version 1

TODO
