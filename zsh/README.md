# Zsh

## List

### [aliases.zsh](aliases.zsh)

A handful of most useful aliases.

## Quick setup

1. Install
[sheldon](https://github.com/rossmacarthur/sheldon),
[starship](https://starship.rs/),
[zellij](https://github.com/zellij-org/zellij),
[zoxide](https://github.com/ajeetdsouza/zoxide)
2. Run these commands to set up sheldon:

    ```console
    sheldon init --shell zsh

    sheldon add --apply fpath --local ~/completion completion
    sheldon add --use zsh/aliases.zsh --github tranzystorek-io/dotfiles aliases
    sheldon add --github yous/vanilli.sh vanilli
    sheldon add --github tranzystorek-io/zellij-zsh zellij-zsh

    sheldon lock
    ```

3. Put this config in `.zshrc`:

    ```zsh
    set -o emacs

    eval "$(starship init zsh)"

    eval "$(sheldon -q source)"

    autoload -U compinit && compinit

    eval "$(zoxide init zsh)"
    ```

4. Restart your shell
