# What does Arquivolta do on top of Arch Linux?

At its core, Arquivolta is an installation of Arch Linux - unlike Arch-derivative distros, it does not fork the core Arch repos. Instead, it installs the core Arch repos, and then adds in two custom repos:

- [arquivolta](https://github.com/arquivolta/repo) - packages that are maintained by the Arquivolta core project and are required for Arquivolta to work.

- [arquivolta-extras](https://github.com/arquivolta/extras) - packages for WSL-specific apps and scripts. Since the [AUR](/details/aur) does not allow WSL-specific packages, we package them here. Packages here are maintained by the Arquivolta team as well as by the community.

In particular, these packages are of particular interest:

- [arquivolta-base](https://github.com/arquivolta/repo/blob/main/arquivolta-base/PKGBUILD) - this metapackage installs several dependencies required to build [Yay](https://github.com/jguer/yay), as well as [setting up systemd](https://github.com/arquivolta/wsl-enable-systemd), [bridging Windows SSH to WSL](https://github.com/arquivolta/wsl-use-windows-openssh), and sets up [/etc/wsl.d](https://github.com/arquivolta/wsl-set-up-wsld), which allows scripts to be executed when the WSL environment is started.

- [arquivolta-new-user-template](https://github.com/arquivolta/arquivolta-new-user-template) - this package installs the default ZSH prompt and adds files to `/etc/skel` , which will get copied into new user accounts (of course, we do this _before_ creating the first user!)

## Can I see this in more detail?

The best place to see exactly what is run when Arquivolta is installed is to look at this file in [the Arquivolta installer](https://github.com/arquivolta/desktop/blob/main/lib/platform/win32/install_arch.dart) - these scripts are executed once the base Arch Linux image is converted and imported.

The tl;dr; version is:

- Set up `pacman` and add Arquivolta's repos
- Set Arch Linux's locale to whatever locale Windows is using
- Install `base`, `base-devel`, `arquivolta-base`, as well as developer tools such as Docker and tmux
- Create a new user account, make sure they can use sudo, and use `/etc/wsl.conf` to set them as the default user
- Build and install `yay`
- Shut down WSL so that we'll restart the distro as the new user account rather than `root` (`/etc/wsl.conf` only gets read when WSL is started)
