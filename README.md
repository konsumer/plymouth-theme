# nullos plymouth-theme

This is an animated bootsplash for plymouth.

## installation

You can install it on  a raspberry pi runnign raspbian, like this:

```sh
sudo apt install -y plymouth plymouth-label plymouth-themes
sudo git clone --depth=1 https://github.com/konsumer/plymouth-theme.git /usr/share/plymouth/themes/notnull
sudo ln -s /usr/lib/arm-linux-gnueabihf/plymouth/script.so /usr/lib/arm-linux-gnueabihf/plymouth/notnull.so
plymouth-set-default-theme notnull
```

Then add somethign liek this to your `/boot/cmdline.txt`:

```
quiet splash plymouth.enable=1 plymouth.ignore-serial-consoles
```