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
-- Note that lowercase things are "generics"
applyTwice :: (t -> t) -> t -> t
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

#### Lambdas

```haskell
f = \x -> x * 2
```
