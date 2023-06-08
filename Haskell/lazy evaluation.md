[[Haskell]] evaluates values lazily, so they are only checked when they are evaluated

Eg: if you have the following in a file
```haskell
y = 2 `div` 0
```

You will only get the divide by zero exception when you query `x` (or call code the queries it)

This is also useful for infinite generators
```haskell
-- An infinitely long list
ones :: [Int]
ones = 1:ones
```

This would cause many problems in most languages, but for Haskell it only causes issues if you try to evaluate all of it.

```haskell
> -- We only need to evaluate the first one
> take 1 ones
[1]
> -- Or in this case, we only need to evaluate the first 5
> take 5 ones
[1, 1, 1, 1, 1]
> -- This one causes problems since we need to evaluate all of it
> ones
[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, .........
```

