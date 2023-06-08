A [[Maths|mathematical]] method to prove things for natural numbers ($\mathbb{N}$, $0 \leq n$)

### Base case
A simple case that is used to build up  the rest of the series.

### Inductive case
A complex case that relates an input to itself.

## Example

$f(0) = 0; f(n) = 2 \times n + f(n - 1)$. Prove $f(n) = n^2$.

TODO

## Induction on lists

- `[]` is a list
- For any list `xs`, `x:xs` is also a list (for any item `x`)

This is an inductive definition, meaning we can do induction to prove that functions that consume lists are correct.
