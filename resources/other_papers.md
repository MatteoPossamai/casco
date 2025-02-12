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