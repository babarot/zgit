# zgit

zgit is simple git interface.

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

All you have to do is typing `zgit` on your command line.

```console
$ zgit
```

When `zgit` command is executed outside git repository, it find the git repository using the [`ghq`](https://github.com/motemen/ghq) or [`enhancd`](https://github.com/b4b4r07/enhancd). In order to combine, you should write `tool = ghq` or `tool = enhancd` to `gitconfig` file. For more details, see also next section.

## Configurations

You can write the configuration to `~/.gitconfig`.

```toml
[zgit "core"]
    default  = "status"
    tool     = "enhancd"
    lessopen = "| pygmentize -O style=solarized -f console256 -g %s"

[zgit "command"]
    echo   = "ctrl-e"
    add    = "ctrl-a"
    add-p  = "alt-a"
    commit = "ctrl-c"
    diff   = "ctrl-d"

[zgit "action"]
   select-all = "ctrl-z"
```

## Notes

Work in progress.

## License

[MIT](http://b4b4r07.mit-license.org)