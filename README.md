# credfeto-aur2repo

Scripts that integrate with [local AUR Cache](https://github.com/credfeto/credfeto-local-aur-cache) to build the packages that were requested through the local aur cache.


## Installing - Server

With a user that has sudo access 

```bash
git clone https://github.com/credfeto/credfeto-aur2repo.git
cd credfeto-aur2repo
./install
```

Optional:
* Configure `/etc/makepkg.conf` as appropriate [MAN](https://man.archlinux.org/man/makepkg.conf.5)
* Configure `/etc/pacman.conf` as appropriate [MAN](https://man.archlinux.org/man/pacman.conf.5)

## Installing - Client

Add repo to `/etc/pacman.conf` changing the server url to one that matches where you've deployed the server.

```
[aur]
SigLevel = Optional TrustAll
Server = https://aur-repo.example.com/
```


## References

* [Arch Linux — local caching repository and AUR build server](https://blog.cavelab.dev/2023/02/arch-linux-local-repo/) - Inspiration for building this repo
* [local AUR Cache](https://github.com/credfeto/credfeto-local-aur-cache) - Server for running a local AUR metadata server when multiple computers are on a network.
* [Linux Package Cache](https://github.com/credfeto/credfeto-linux-package-cache) - docker compose for running a local package cache for pacman, aur, chaotic-aur and flathub.
* [Dev package Cache](https://github.com/credfeto/credfeto-dev-package-cache) - docker compose for npm and nuget package caches.