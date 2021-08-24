# Backup/Restore gnome-terminal Profiles

# Backup:
Find profile ID and use `dconf` to dump the config.

```
dconf dump /org/gnome/terminal/legacy/profiles:/:08247904-2da9-420b-8018-2ecd905a43de/ > term.dconf
```

# Restore:
Create a new profile from gnome-terminal preferences and then load your custom profile with `dconf`.

```
dconf load /org/gnome/terminal/legacy/profiles:/:08247904-2da9-420b-8018-2ecd905a43de/ < term.dconf
```

