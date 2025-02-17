# Compiler

A compiler $\mathbb{C}$ is a program that translates source code into machine code.
$\mathbb{C} (SRC) = OUT$.

# Contract Aware Compiler

It is a [Compiler](#compiler) that is aware of the contract of the hardware it is compiling for.
$\mathbb{C} (SRC, Contract) = OUT$.

# CASCO

A contact aware secure compiler is a [Contract Aware Compiler](#contract-aware-compiler) whose target code is secure with respect to the given contract.
$\mathbb{C} (SRC, Contract) = \text{OUT } \wedge \text{ OUT is secure on target HW}$.
