Currying is the idea of taking one argument per [[function]], meaning that functions can be [[function|partially-applied]]. Currying can be used in many programming languages, but is given *first-class support* in [[Haskell]].

Here is a curried function in Haskell
```haskell
myFunction x y = x * y
-- A function that takes in `x`, then returns a function that takes in `y`
-- which then returns `x + y`
```

And here is the equivalent in JavaScript.
```js
function myFunction(x) {
  function inner(y) {
    return x * y;
  }
}
```

## Currying and uncurrying

Haskell provides `curry` and `uncurry` functions which allow you to convert to/from functions that take arguments as a pair and functions that use currying.

```haskell
curriedMul x y = x * y
-- Uncurried version accepts a pair as an argument
uncurriedMul (x, y) = x * y

---------------

> curry uncurriedMul  
-- produces a function identical to curriedMul
> uncurry curriedMul
-- produces a function identical to uncurriedMul
```

Due to the "first-class currying" nature of Haskell, there should be almost no reason to write uncurried functions, at least as far as I can tell.