# quickTMUX - a quickstart configuration for tmux

This repo customizes tmux in an accessible way by defining keybindings that are more intuitive for infrequent users.
Mouse support is enabled, an indicator icon in the bottom left (<kbd>></kbd>) shows an active prefix key.

## Setup

To install [tmux](https://github.com/tmux/tmux), follow the official installation guides.

Try this config:

```bash
git clone git@github.com:jkschluesener/quicktmux ~/quicktmux
tmux -f ~/quicktmux/tmux.conf
```

Permanently use this configuration:

```bash
git clone git@github.com:jkschluesener/quicktmux ~/.config/quicktmux
# sofltink this config file into the default location
ln -s ~/.config/quicktmux/tmux.conf ~/.tmux.conf
```

## Keybindings Cheatsheet

### Sessions

Create / list / attach to a tmux sessions from your terminal.
|           `$`           | Shell                         |
|:-----------------------:|:------------------------------|
|  Create named session   | `tmux new -s <session-name>`  |
|  List active sessions   | `tmux ls`                     |
|      Kill session       | `tmux kill-session -t <name>` |
| Attach to named session | `tmux a -t <name>`            |

| <kbd>Ctrl</kbd> + <kbd>b</kbd> | Prefix Key          |
|:------------------------------:|:--------------------|
|          <kbd>l</kbd>          | List sessions       |
|          <kbd>d</kbd>          | Detach from session |
|          <kbd>K</kbd>          | Kill session        |

### Panes

|                                <kbd>Ctrl</kbd> + <kbd>b</kbd>                                 | Prefix Key                       |
|:---------------------------------------------------------------------------------------------:|:---------------------------------|
|              <kbd>\|</kbd> <kbd>/</kbd> <kbd>\\</kbd> <kbd>"</kbd> <kbd>%</kbd>               | Split current pane in left/right |
|                            <kbd>"</kbd> <kbd>=</kbd> <kbd>_</kbd>                             | Split current pane in top/bottom |
| <kbd>ctrl</kbd> + <kbd>&#8592;</kbd> <kbd>&#8594;</kbd> <kbd>&#8593;</kbd> <kbd>&#8595;</kbd> | Resize using arrow keys          |
|                                         <kbd>r</kbd>                                          | Rename pane                      |
|                                         <kbd>q</kbd>                                          | Close pane                       |
|                                         <kbd>s</kbd>                                          | Synchronize panes                |

| <kbd>Ctrl</kbd> + <kbd>b</kbd> | Prefix Key             |
|:------------------------------:|:-----------------------|
|          <kbd>t</kbd>          | Tiled layout           |
|          <kbd>h</kbd>          | Even horizontal layout |
|          <kbd>v</kbd>          | Even vertical layout   |

|                                                                                                | No Prefix               |
|:----------------------------------------------------------------------------------------------:|:------------------------|
| <kbd>Shift</kbd> + <kbd>&#8592;</kbd> <kbd>&#8594;</kbd> <kbd>&#8593;</kbd> <kbd>&#8595;</kbd> | Switch to relative pane |

### Windows

| <kbd>Ctrl</kbd> + <kbd>b</kbd> | Prefix Key          |
|:------------------------------:|:--------------------|
|          <kbd>n</kbd>          | Create a new window |
|          <kbd>f</kbd>          | Find window         |
|          <kbd>Q</kbd>          | Close window        |
|          <kbd>w</kbd>          | List windows        |
|          <kbd>R</kbd>          | Rename Window       |

|                                                        | No Prefix                 |
|:------------------------------------------------------:|:--------------------------|
| <kbd>Alt</kbd> + <kbd>&#8592;</kbd> <kbd>&#8594;</kbd> | Switch to relative window |

### Miscellaneous

| <kbd>Ctrl</kbd> + <kbd>b</kbd> | Prefix Key                                  |
|:------------------------------:|:--------------------------------------------|
|          <kbd>z</kbd>          | Zoom current pane (+ as indicator in title) |
|          <kbd>t</kbd>          | Display clock                               |
|          <kbd>o</kbd>          | Reload configuration                        |
|          <kbd>c</kbd>          | Copy mode                                   |
|          <kbd>v</kbd>          | Paste buffer                                |
