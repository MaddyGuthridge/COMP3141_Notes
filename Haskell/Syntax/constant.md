```haskell
x :: Int -- Declare a constant and its type
x = 7 -- Constant assignment
```

Note that constants cannot be reassigned. Consider the following assignment:
```haskell
x = x + 1
```

This leads to an infinite loop, since it defines `x` in terms of `x`.

Note that Haskell uses [[lazy evaluation]] on constants.