# zgit

**[WIP]** zgit is simple tig-like git client

## Installation

***Requirements***

- [`fzf`](https://github.com/junegunn/fzf)

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

## Usage

```console
$ zgit    # in git repository
```

## License

[MIT](http://b4b4r07.mit-license.org)