# Why not Ubuntu / Fedora?

Good question! The goal of Arquivolta is to be an Opinionated, Batteries-included Linux distribution, and part of that is to be able to install _any_ tool available, without having to manage 3rd-party software repos or install one-off software. The [Arch User Repository](https://aur.archlinux.org) contains packages for nearly every piece of software available for Linux, without having to remember, "Oh, I installed IntelliJ by-hand, so I need to update it myself".

## What is the AUR? {#id=aur}

Arch Linux is split into several repositories - the ones managed via official maintaners, and the ones managed by the community. The AUR is a repository of packages that are not maintained by the official maintainers, but are maintained by the community, including non-Free software.

## How does Arquivolta fit in here?

Arquivolta is both an installer, but also adds to the list of base packages provided by Arch Linux, via a [custom repository](https://wiki.archlinux.org/title/unofficial_user_repositories). Arquivolta's custom repo `arquivolta` adds the packages that comprise the base experience and set up systemd in WSL2, configures SSH to be bridged with Windows, and sets the base prompt. Arquivolta also adds the `arquivolta-extras` repo, which packages WSL2 specific apps and tools.

## How do I do $X

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
