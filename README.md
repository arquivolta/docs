# What is Arquivolta

Arquivolta is an opinionated Linux distro built specifically for WSL2 users on Windows 11, as a customization of [Arch Linux](https://archlinux.org). Rather than being an operating system that _happens_ to work in WSL, Arquivolta is _designed_ to work specifically as a companion to Windows 11, built for modern developers as well as users who want to use a hassle-free, batteries included Linux environment.

_(Fill in a really great screenshot here!)_

## How is Arquivolta different?

- Arquivolta installs via the [Arquivolta Installer](https://link/to/download/page), a Windows 11 app that installs everything for you, using your Windows install to answer all of the reduntant questions that other distros ask users.

- Arquivolta is based on Arch Linux, which includes the [AUR](https://aur.archlinux.org), as well as [Yay](https://github.com/Jguer/yay). The AUR includes **everything** - no more fiddling with third-party repos or downloading packages to get popular software such as [Google Chrome](https://aur.archlinux.org/packages/google-chrome), [GPU-accelerated Tensorflow](https://archlinux.org/packages/community/x86_64/python-tensorflow-cuda), [Android Studio](https://aur.archlinux.org/packages/android-studio), or any other software package. If it's free, it's probably There.

- Arquivolta is the only place that is committed to packaging as many WSL2-specific applications and utilities as possible, and making the most useful ones built-in. Features such as [Windows Hello](https://link/to/that/thing) work out of the box, and useful utilities such as [wslu](https://github.com/wslutilities/wslu) are just as easy to install as native Linux applications.

- For developers, SSH and HTTPS Git Credentials are configured to Just Work with the Windows-based installation you already have. No more entering SSH keyphrases over and over!

- Also for developers, Arquivolta sets up [systemd](https://en.wikipedia.org/wiki/Systemd) by default. No more starting mysqld or Docker by hand, and setup guides written with Linux users in mind work more often.

## What exactly does this do / how specifically is this different than Arch Linux?

All of these questions can be answered in the [Technical Differences](details/differences.md) section, down to the exact scripts that Arquivolta executes. In short, Arquivolta is Arch Linux with a few custom repos in-box, that is configured via information in Windows. Linux shouldn't need to ask questions like your preferred language or timezone in WSL, we already know that! The Arquivolta installer collects information like this and sets up the system for you.

## What telemetry does Arquivolta collect?

onnec

## Getting Help / Contributing

#### [Join the Discord community!](https://discord.gg/yJHg3Khvnk)

The Discord is a great way to get help, talk to the devs, as well as discuss cool ideas or new features!
