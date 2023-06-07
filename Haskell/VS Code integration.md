To get the best VS Code integration, you should follow these instructions.

1. [Install Stack](https://docs.haskellstack.org/en/stable/)
2.  [Install GHCup](https://www.haskell.org/ghcup/), making sure to
    - Allow GHCup to integrate with Stack
    - Add GHCup to your shell's config (`.zshrc` or `.bashrc`)
3. Restart your terminal, then run `ghcup tui`
4. Choose to install Haskell 9.2.7 (or the latest stable version with the `hls-powered` attribute)
5. Also choose to install the Haskell Language Server (HSL)
6. Launch VS Code and install the Haskell extension