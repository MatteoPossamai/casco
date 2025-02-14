# Questions

## Question 1

Why we don't need the Red semantic? (Probably the answer strongly depends on the [Green semantic](#question-2))

## Answer 1

TODO

## Question 2

What is the meaning of the Green semantic?

## Answer 2

TODO

## Question 3

What does it mean to define contract for spectre?

## Answer 3

(Matteo): Following Hardware-Software and Practical Foundation papers, this means to write the model of the CPU that is vulnerable to the given Spectre variant. We need therefore to both model this in the execution and in the leakage model.

## Question 4

Should we care about non terminating programs or programs that fail?

## Answer 4

(Matteo): For non terminating programs probably this does extend to them, since if a subset is safe, the whole is. Assuming that is due to loop and all, if the chunks are, the whole is. For failing, not having type system, the only failure can be in the logic, but that has nothing to do with safety, so we should not care as well.

## Question 5

...
