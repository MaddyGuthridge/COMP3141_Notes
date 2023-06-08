```haskell
9 * 2 -- Multiplication operator
9 / 2 -- Float division operator (4.5)
9 `div` 2 -- Int division operator (4)
```

### Dollar $ operator
Basically used to make a function apply in reverse order. The equivalent of using parentheses around the remainder of the expression.

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
