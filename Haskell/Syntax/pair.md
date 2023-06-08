Kinda like a `tuple` in Python and Rust?

```haskell
divmod :: Int -> Int -> (Int, Int)
divmod x y = (x `div` y, x `mod` y)
divmod 10 3 -- (3, 1)
```

#### Why not use a Pair to create a multi-argument function?

- Can't partially apply the function
