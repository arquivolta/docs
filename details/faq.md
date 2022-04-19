# Common Questions

### Why does Arquivolta require Windows 11?

Arquivolta relies on [WSLg](http://github.com/microsoft/wslg), which is only available on Windows 11. In the future, Arquivolta generally will take as much advantage as possible of new WSL features, which are generally not ported to older versions of the OS.

### Why is this project called "Arquivolta"

Arquivolta is the Spanish word for an [Archivolt](https://en.wikipedia.org/wiki/Archivolt), an ornamental decoration which adornes an arched opening / doorway. The Arquivolta project is a "decoration" above Arch Linux �

### Why is this a desktop app and not just a Powershell script I can run?

While the initial goal of the Arquivolta installer is to get Arch Linux into WSL, it has a secondary goal of being a companion app to keep your Windows and WSL2 installations in-sync, as well as giving Arquivolta a way to show native UI for things like update reminders.

### How come this isn't installed via the Windows Store, similar to Ubuntu?

Linux distros in the Windows Store are required to have a special partnership with Microsoft. In addition, it's impossible to customize the experience in the same way that we can with a desktop app, or keep the distro up-to-date.
