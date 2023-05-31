## Comments
```haskell
{-
  This is a block comment.
 -}

-- This is an inline comment
```

## Constants
```haskell
x :: Int -- Declare a constant and its type
x = 7 -- Constant assignment
```

Note that constants cannot be reassigned. Consider the following assignment:
```haskell
x = x + 1
```

This leads to an infinite loop, since it defines `x` in terms of `x`.

## Operations
```haskell
9 * 2 -- Multiplication operator
9 / 2 -- Float division operator (4.5)
9 `div` 2 -- Int division operator (4)
```

## Functions
Note that Haskell is a *functional* language, not an *imperative* language.
- LHS names the parameter
- RHS describes the return value of the function

Functions map input to output and do nothing else -- there are no side effects. They are much like mathematical functions
```haskell
square :: Int -> Int -- function signature (declaration)
square x = x*x -- Function definition

square 2 -- Call the function (notice no parentheses)

-- Order of operations with functions

sqaure 2 + 2 -- 6, it evaluates to (square 2) + 2

square (2 + 2) -- 16
```

### First-class functions

Functions are values, just like variables, and they can be used like them.

- Lists of functions
- Functions as arguments to other functions
- Functions as return values from other functions

Example: `myLogBase` to compute a logarithm with a specific base

```haskell
{-
  Returns a function that computes a logarithm at a specific base
 -}
myLogBase :: Double -> Double -> Double
myLogBase = 
```

### Multi-argument functions ***don't exist??***
