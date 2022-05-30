# Why not Ubuntu / Fedora?

Good question! The goal of Arquivolta is to be an Opinionated, Batteries-included Linux distribution, and part of that is to be able to install _any_ tool available, without having to manage 3rd-party software repos or install one-off software. The [Arch User Repository](https://aur.archlinux.org) contains packages for nearly every piece of software available for Linux, without having to remember, "Oh, I installed IntelliJ by-hand, so I need to update it myself".

### What is the AUR? {#id=aur}

Arch Linux is split into several repositories - the ones managed via official maintaners, and the ones managed by the community. The AUR is a repository of packages that are not maintained by the official maintainers, but are maintained by the community, including non-Free software.

### How do I do $X

| Ubuntu                   | Arquivolta / Arch    |
| ------------------------ | -------------------- |
| apt upgrade              | yay -Syu             |
| apt upgrade package_name | yay -Sy package_name |
| apt install package_name | yay -Sy package_name |
| apt search package_name  | yay -Ss package_name |
| apt remove package_name  | yay -R package_name  |
| apt autoremove           | yay -Rdu             |
| apt list installed       | yay -Q / yay -Qe     |
| apt show package_name    | yay -Qi package_name |
