# credfeto-aur2repo

## Installing

1. clone repo and run install script
2. change pacman.conf to change ``CleanMethod = KeepCurrent``
3. change pacman.conf to add source

```
[aur]
SigLevel = Optional TrustAll
Server = file:///srv/http/aur
```