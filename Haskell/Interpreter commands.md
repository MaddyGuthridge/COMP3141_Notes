## Evaluation

```haskell
> some expression
-- Evaluates the expression and shows its output
```

## Module loading

```haskell
> :l Path/To/My/File.hs
-- Loads the file and imports its contents to the global scope
```

## Module reloading

```haskell
> :r
-- Reloads all loaded modules
```

## Type query

```haskell
> :t SomeObject
-- Shows the type of SomeObject
```

## Getting info
We were only shown how to do this for type classes, but it might work for other things

```haskell
> :info SomeTypeClass
-- Shows a bunch of info about the thing
```

## Running shell commands
You can run commands in a shell, which is useful for quick terminal operations. Note that ``

```haskell
> :! echo "Hello world"
-- Runs the `echo` command with the argument "Hello world"
```