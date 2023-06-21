# Recent menu

Recently played menu for mpv integrated with uosc.

## Getting started

**[tomasklaen/uosc](https://github.com/tomasklaen/uosc) is required.**

[Menu](https://github.com/tomasklaen/uosc#adding-items-to-menu) - add following to `input.conf`.

```ini
KEY                 script-binding recentmenu/open                      #! Recently played
```

[Controls](https://github.com/tomasklaen/uosc#set-prop-value) - add following to `uosc.conf#controls`.

```ini
command:history:script-message-to recentmenu open?Recently played
```

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
