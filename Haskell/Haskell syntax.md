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

## Operations
```haskell
x * 2 -- Multiplication operator
9 / 2 -- Float division operator
9 `div` 2 -- Int division operator
```

## Functions
Note that Haskell is a functional language, not an imperative language.
- LHS names the parameter
- RHS describes the return value of the function

Functions map input to output and do nothing else -- there are no side effects(they are much like mathematical functions)
```haskell
square :: Int -> Int -- function signature (declaration)
square x = x*x -- Function definition

square 2 -- Call the function (notice no parentheses)

-- Order of operations with functions

sqaure 2 + 2 -- 6, it evaluates to (square 2) + 2

square (2 + 2) -- 16
```

