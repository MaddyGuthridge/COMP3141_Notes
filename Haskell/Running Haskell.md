In COMP3141, [[Haskell]], is run by loading code into a [[REPL]] then querying it.

## Using Cabal
Recommended on CSE systems.

```sh
# Run the REPL
$ 3141 cabal repl
```

## Using Stack
Recommended by the course on home systems. The setup script is available [here](https://docs.haskellstack.org/en/stable/).

```sh
# Run the REPL
$ stack repl
```

## Using GHCup
GHCup is a tool to install and manage versions of GHC, the Glorious Glasgow Haskell Compilation System. The setup script is available [here](https://www.haskell.org/ghcup/).

GHCup also allows you to install a language server, allowing for better integration with your IDE, provided it supports the [Language Server Protocol](https://microsoft.github.io/language-server-protocol/).

```sh
# Run the REPL
$ ghci
```
