# Installing Arquivolta into your existing Arch Linux install

If you already have an Arch Linux install in WSL2 (e.g. from ArchWSL), you can effectively migrate to Arquivolta by running the following commands **as root**:

```sh
pacman-key --recv-keys 8C23AC40F9AC3CD756ADBB240D3678F5DF8F474D
pacman-key --lsign-key 8C23AC40F9AC3CD756ADBB240D3678F5DF8F474D

pacman --noconfirm -Sy base base-devel arquivolta-base

echo '%wheel ALL=(ALL:ALL) ALL' > /etc/sudoers.d/00-enable-wheel
echo '' >> /etc/sudoers.d/00-enable-wheel
chmod 644 /etc/sudoers.d/00-enable-wheel

chsh -s /bin/zsh <YOUR USERNAME>
cp /etc/skel/* /home/<YOUR USERNAME>
```
