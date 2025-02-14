# Semantics
Definition of the used semantics, modeling the non speculative and speculative behavior of the [Language](./assembly.md#assembly). 

## Thoughts and motivations
- To make general, we shall probably aim to make the semantic possibly vulnerable on each instruction, except for the one that are supposed to be robust (`cmov`). Does this make sense? Can we actually do this? 