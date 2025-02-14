# CASCO

Contract Aware Secure COmpilation

## Idea

If we give a compiler the Hardware [Contract](./other_papers.md#contracts), then the compiler generates code that is secure with respect to the given contract, applying where required the necessary safety checks (I.E. `lfence`). Probaly a patch mechanism to achive this.

If we are able to make a compiler `CASCO`, then the output is secure (by definition, scafolding).

From a [Contract](./other_papers.md#contracts), we want to have a compiler that as well adhere to the contract.

This must be parametric (generic framework), so must support a number of contracts:

- `CT` and `ARC` from [Hardware Software Contracts for Secure Speculation](./other_papers.md#hardware-software-contracts-for-secure-speculation);
- ???

## Goal

Be able to generalize a framework able to prove $\text{prog} \vdash \text{CT(CPU)}$ (where CPU is the contract of the Hardware).

## Required steps

- [ ] Prove that CPU respects the contract (vendor IIRC)
- [ ] Compiler is `CASCO`, and therefore $\mathbb{C} \vdash \text{CT(CPU)}$

## Roadmap

- [ ] Define language for represent code (ASM-like)
- [ ] Define non speculative semantic (blue language) (same as Spectector???)
- [ ] Define speculative semantic (green language)
- [ ] Define at least 2 contracts for spectre B(ranch), S(tore)
- [ ] TODO ???

## Semantics

- [ ] Blue Semantics, for non speculative execution
- [ ] Green Semantics (what does it mean???)
- [ ] Red Semantics (no needed, WHY???)
      Preservation should happen between Blue and Green (???).

### Meaning

Blue -> Green = ???
Green -> Red = ??? (we assume this to be true???)
