# zgit

**[WIP]** zgit is simple tig-like git client

## Installation

By using [zplug](https://github.com/b4b4r07/zplug), you can easily install zgit and fzf.

```zsh
zplug "junegunn/fzf-bin", \
    as:command, \
    file:"fzf", \
    from:gh-r, \
    | zplug "b4b4r07/zgit", \
    as:command, \
    of:bin
```

***Requirements***

- [`fzf`](https://github.com/junegunn/fzf)

***Desirable***

- `tmux` (for `fzf-tmux`)
- `ghq` (to find `git` repositories)

## Usage

```console
$ zgit
```

### Configuration

```gitconfig
[zgit "core"]
    action      = status
    fzf_options = "--cycle --multi"
    
[zgit "keybind"]
    add    = ctrl-a
    commit = ctrl-c
    diff   = ctrl-d
```

## License

[MIT](http://b4b4r07.mit-license.org)