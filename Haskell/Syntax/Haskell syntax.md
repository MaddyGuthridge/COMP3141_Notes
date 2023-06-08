## Pairs
Kinda like a `tuple` in Python and Rust?

```haskell
divmod :: Int -> Int -> (Int, Int)
divmod x y = (x `div` y, x `mod` y)
divmod 10 3 -- (3, 1)
```

#### Why not use a Pair to create a multi-argument function?

- Can't partially apply the function

## Operators

### Dollar $ operator
Basically used to make a function apply in reverse order

```haskell
reverse [1, 2, 3] ++ [4]
-- (reverse [1, 2, 3]) ++ [4]
reverse $ [1, 2, 3] ++ [4]
-- reverse $ ([1, 2, 3] ++ [4])
```

### Function composition . operator
Used to describe applying a function to the result of another function

```haskell
f (g x)
-- equivalent
f . g x
```