# Recent menu

Recently played menu for mpv.

## Getting started

### uosc

**[tomasklaen/uosc](https://github.com/tomasklaen/uosc) is required.**

[Menu](https://github.com/tomasklaen/uosc#adding-items-to-menu) - add following to `input.conf`.

```ini
#                   script-binding recentmenu/open                      #! Recently played
```

[Controls](https://github.com/tomasklaen/uosc#set-prop-value) - add following to `uosc.conf - controls`.

```ini
command:history:script-message-to recentmenu open?Recently played
```

### command_palette

**[stax76/mpv-scripts/command_palette](https://github.com/stax76/mpv-scripts?tab=readme-ov-file#command_palette) is required.**

```ini
z                   script-binding recentmenu/open                      #! Recently played
```

or

```ini
z                   script-message-to command_palette show-command-palette "Recent Files"   # Recent Files
```

### select

**It’s a built-in script of mpv that was added in [#14087](https://github.com/mpv-player/mpv/pull/14087).**

[Keybind](https://mpv.io/manual/master/#input-conf) - add following to `input.conf`.

```ini
z                   script-binding recentmenu/open                      #! Recently played
```

### Context Menu

**[tsl0922/mpv-menu-plugin/dyn_menu.lua](https://github.com/tsl0922/mpv-menu-plugin/blob/main/src/lua/dyn_menu.lua) is required.**

[Menu](https://github.com/tsl0922/mpv-menu-plugin/wiki/Configuration) - add following to `input.conf`.

```ini
MBTN_RIGHT          context-menu
_                   ignore                                  #menu: Recently played  #@recent
```

> [!WARNING]
>
> **Due to the limitations of context-menu (mpv-menu-plugin), the menu may show unexpected results.**
>
> - The menu will not be updated in time when the file is deleted
> - The menu will be inconsistent when multiple mpv instances work at the same time

### General

Play most recent one.

```ini
KEY                 script-binding recentmenu/last
```

Use the specified menu provider

```ini
KEY                 script-message-to recentmenu open-recent-menu uosc
KEY                 script-message-to recentmenu open-recent-menu command-palette
KEY                 script-message-to recentmenu open-recent-menu select
```

## Options

```ini
enabled = yes                           # whether to record current playing file, can be used with auto-profile
path = "~~/recent.json"                 # where the history is stored
length = 10                             # number of items
ignore_same_series = yes                # similar file names only record the most recent one
reduce_io = no                          # reduce the number of JSON reads and writes. but menu may show unexpected results.
```
