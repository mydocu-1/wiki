# Shell

## zsh
* https://wiki.archlinux.org/index.php/zsh

Change default user shell

```
# chsh -s /bin/bash
```

## Fish
* https://wiki.archlinux.org/index.php/Fish
* https://fishshell.com/docs/current/tutorial.html

Don't set it as user's default shell, instead set it as default shell for tmux
in `tmux.conf`:

```
# set-option -g default-shell "/usr/bin/fish"
```

