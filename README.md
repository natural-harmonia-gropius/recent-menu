# Recent menu

It works, just works

```ini
#                   script-binding recentmenu/open                      #! Recently played
```
If you want an entry in the controls bar of uosc, you can add the following to the `controls=` entry in your `uosc.conf`:

```
command:history:script-message-to recentmenu open?Recently played
```
* Pick your desired title instead of `Recently played`
* Pick another icon instead of `history` from [Google Material Icons](https://fonts.google.com/icons?selected=Material+Icons)
