# Hardware Software Contracts for Secure Speculation

## Contracts
- Semantic with judgement: $\sigma \rightarrow^{l_n} \sigma$
- Set of all the $l_n$ observation is the architectural trace
- This semantic says what the hardware must adhere to, and must be indistinguishable from an attacker perspective
- An attacker is a projection of micro-architectural state of the machine
- $\{.\} \vdash [.]$ means that the attacker cannot distinguish between two executions of the same program, so the contract is respected 
- Example of contracts can be made of observation model and execution model
- On the software side we wanto to know, given the HW contract, what are the requirements that we must adhere to in order to have safe programs

# Exorcising Spectre with Secure Speculation


# Avoiding Instruction-Centric Microarchitectural...
Mitigate "automatically" future threads with a framework that used the description and the countermeasures that are developed by researchers. 

## Background
- For make a non-CT program a CT program, there are tools as the proposed `cio` that uses synthetic generations of patches for vulnerabilities. 
- Some optimizations can be done at the OS level with bits, and they are not always easy to apply depending on the platform. Sometime is better to set these bits instead of transforming the code, and `cio` can do this. 
- HW for constant time instruction is unreliable

## Theat model
- The vulenrability is novel, we have no strict semantic to define it
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