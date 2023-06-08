
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