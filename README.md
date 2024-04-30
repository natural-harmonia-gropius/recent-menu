# Recent menu

Recently played menu for mpv.

## Getting started

### Context Menu

**[tsl0922/mpv-menu-plugin/dyn_menu.lua](https://github.com/tsl0922/mpv-menu-plugin/blob/main/src/lua/dyn_menu.lua) is required.**

[Menu](https://github.com/tsl0922/mpv-menu-plugin/wiki/Configuration) - add following to `input.conf`.

```ini
_                   ignore                                  #menu: Recently played  #@recent
```

> [!WARNING]
>
> **Due to the limitations of context-menu (mpv-menu-plugin), the menu may show unexpected results**
>
> - The menu will not be updated in time when the file is deleted
> - The menu will be inconsistent when multiple mpv instances work at the same time

### uosc

**[tomasklaen/uosc](https://github.com/tomasklaen/uosc) is required.**

[Menu](https://github.com/tomasklaen/uosc#adding-items-to-menu) - add following to `input.conf`.

```ini
#                   script-binding recentmenu/open                      #! Recently played
```

[Controls](https://github.com/tomasklaen/uosc#set-prop-value) - add following to `uosc.conf#controls`.

```ini
command:history:script-message-to recentmenu open?Recently played
```

### General

Play most recent one.

```ini
KEY                 script-binding recentmenu/last
```

## Options

```ini
enabled = yes                           # whether to record current playing file, can be used with auto-profile
path = "~~/recent.json"                 # where the history is stored
length = 10                             # number of items
width = 88                              # number of characters for the item
ignore_same_series = yes                # similar file names only record the most recent one
```
