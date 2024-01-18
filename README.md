# Recent menu

Recently played menu for mpv integrated with uosc and mpv-menu-plugin.

## Getting started

### uosc

**[tomasklaen/uosc](https://github.com/tomasklaen/uosc) is required.**

[Menu](https://github.com/tomasklaen/uosc#adding-items-to-menu) - add following to `input.conf`.

```ini
KEY                 script-binding recentmenu/open                      #! Recently played
```

[Controls](https://github.com/tomasklaen/uosc#set-prop-value) - add following to `uosc.conf#controls`.

```ini
command:history:script-message-to recentmenu open?Recently played
```

### mpv-menu-plugin

**[mpv-menu-plugin](https://github.com/tsl0922/mpv-menu-plugin) is required.**

[Menu](https://github.com/tsl0922/mpv-menu-plugin?tab=readme-ov-file#messages) - add following to `input.conf`.

```ini
KEY                 ignore                                              #menu: Recently played  #@recent
```

> [!NOTE]
> Due to the limitations of mpv-menu-plugin itself, attention should be paid to:
>
> - The menu will not update when the file is deleted
> - Multiple mpv instances may have inconsistent menus

### Unrelated

Play most recent one.

```ini
KEY                 script-binding recentmenu/last
```

## Options

```ini
path = "~~/recent.json"                 # where the history is stored
length = 10                             # number of items
width = 88                              # number of characters for the item
ignore_same_series = yes                # similar file names only record the most recent one
```
