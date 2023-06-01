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

### Lazy evaluation
Note that values are lazy-evaluated, so they are only checked when they are evaluated

Eg: if you have the following in a file
```haskell
y = 2 `div` 0
```

You will only get the divide by zero exception when you query `x`

## Operations
```haskell
9 * 2 -- Multiplication operator
9 / 2 -- Float division operator (4.5)
9 `div` 2 -- Int division operator (4)
```

Type queries
```haskell
:t True -- Bool
```

## Functions
Note that Haskell is a *functional* language, not an *imperative* language.
- LHS names the parameter
- RHS describes the return value of the function

Functions map input to output and do nothing else -- there are no side effects. They are much like mathematical functions
```haskell
square :: Int -> Int -- function signature (declaration)
square x = x * x -- Function definition

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
myLogBase base value = log value / log base
```

Example: `applyTwice` to apply a function twice
```haskell
-- TODO: Make args generic
applyTwice :: (Int -> Int) -> Int -> Int
applyTwice f x = f(f x)
```

### Multi-argument functions ***don't exist??***
- Every function takes one value and returns one value
- To create pretend to have a multi-argument function, we just create a function that returns a function that accepts the next argument
- This is called currying

#### ✨Syntactic sugar✨
To call multi-argument functions
```haskell
f x y <=> (f x) y
```
Conversely, the `->` is right-associative
```haskell
a -> b -> c -- a -> (b -> c)
```

#### Operators are also just multi-argument functions

```haskell
:t (+) -- (+) 2 :: Num a -> a -> a
```

You can create *partially-applied* operations like this
```haskell
x = (+) 2  -- creates a function that adds 2
x 2 -- 2 + 2 = 4
x 3 -- 2 + 3 = 5
```

#### Function forwarding

If there is a function `f` which takes argument `x` and returns `g x`, there is no need to declare its argument. The following will suffice:
```haskell
f = g
```

## Lists
Haskell uses lists to store arrays of data
```haskell
[1, 2, 3]  -- declares a list
:t [True, False, True] -- [Bool] 
```

Appending to the list, using the `:` (cons) operator
```haskell
1:2:[] -- create a new list with 1 and 2 added to the end of it
```

### Strings
Essentially a character list
```haskell
String = [Char]  -- TODO: is this the right syntax?
```

## Pairs
Kinda like a `tuple` in Python and Rust?

```haskell
divmod :: Int -> Int -> (Int, Int)
divmod x y = (x `div` y, x `mod` y)
divmod 10 3 -- (3, 1)
```

#### Why not use a Pair to create a multi-argument function?

- Can't partially apply the function