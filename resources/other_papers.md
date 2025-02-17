# Hardware Software Contracts for Secure Speculation

## Contracts

- Semantic with judgement: $\sigma \rightarrow^{l_n} \sigma$
- Set of all the $l_n$ observation is the architectural trace
- This semantic says what the hardware must adhere to, and must be indistinguishable from an attacker perspective
- An attacker is a projection of micro-architectural state of the machine
- $\{.\} \vdash [.]$ means that the attacker cannot distinguish between two executions of the same program, so the contract is respected
- Example of contracts can be made of observation model and execution model
- On the software side we want to to know, given the HW contract, what are the requirements that we must adhere to in order to have safe programs

# Exorcising Spectre with Secure Speculation

# Avoiding Instruction-Centric Micro-architectural...

## Threat model

- The vulnerability is novel, we have no strict semantic to define it
- Assume that source code is CT in CPU with no given improvement
- The attacker can observe each time the optimization is used, to make the strongest attacker possible and make the framework more robust

## Framework of `cio`

In: source code with secret annotation; Out: secure binary or nothing

### Steps

1. LLVM compilation
2. Checkers for vulnerable snippets with BAP
3. Re-compile LLVM with new Synthesized transformations
4. Double checking

## Outcome

Able to create a patch to the new vulnerabilities with significant penalty both at compile and runtime.
