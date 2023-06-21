# Default Packages

These packages are either unique to Arquivolta, or only make sense in the context of WSL2. Because WSL packages are disallowed by the AUR, we have to host them ourselves

* `wsl-enable-systemd` - This package forces systemd to be enabled for the distro. Arquivolta relies on systemd to be set up
* `wsl-set-up-wsld` - WSL2 only allows a single command to be executed when a distro starts - this package sets up a wsl.d directory which runs multiple commands on initial boot
* `wsl-use-windows-openssh` - This package configures SSH to use the Windows OpenSSH client, so that SSH keys are shared between Windows and Linux
* `arquivolta-new-user-template` - This package sets up /etc/skel to include the Arquivolta default shell prompt