# Zsh

## List

### [aliases.zsh](aliases.zsh)

A handful of most useful aliases.

## My configuration

1. Install
[zplug](https://github.com/zplug/zplug),
[fasd](https://github.com/clvv/fasd),
[starship](https://starship.rs/),
tmux
2. Put this config in `.zshrc`:

    ```zsh
    set -o emacs

    eval $(starship init zsh)

    source ~/.zplug/init.zsh

    zplug "zpm-zsh/tmux"

    zplug "yous/vanilli.sh"

    zplug "plugins/fasd", from:oh-my-zsh

    zplug "tranzystorek-io/dotfiles", use:"./zsh/aliases.zsh"

    zplug "~/completion", from:local

    zplug load
    ```

3. Run `zplug install`
4. Restart your shell
