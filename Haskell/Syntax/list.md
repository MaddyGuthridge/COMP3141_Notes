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
