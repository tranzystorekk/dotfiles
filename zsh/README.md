# Zsh

## List

### [aliases.zsh](aliases.zsh)

A handful of most useful aliases.

### [ldot.zsh](ldot.zsh)

Zsh function that lists only hidden files (aka dotfiles) in the given directory.

## My configuration

1. Install
[zplug](https://github.com/zplug/zplug),
[fasd](https://github.com/clvv/fasd),
[starship](https://starship.rs/),
tmux
2. Put this config in `.zshrc`:

    ```zsh
    eval $(starship init zsh)

    source ~/.zplug/init.zsh

    zplug "zpm-zsh/tmux"

    zplug "yous/vanilli.sh"

    zplug "plugins/fasd", from:oh-my-zsh

    zplug "~/repos/misc/zsh", use:"{aliases,ldot}.zsh", from:local

    zplug load
    ```

3. Run `zplug install`
4. Restart your shell
