Because Haskell uses [[currying|curried]] [[function|functions]] by default, you can partially apply a function.

```haskell
> addTwo = (+) 1
> addTwo 3
5
> addTwo 7
9
```