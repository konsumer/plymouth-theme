# notnull plymouth-theme

This is an animated bootsplash for plymouth.

![screenshot](https://media.giphy.com/media/4PgwiQCrH3iqkNHN04/giphy.gif)

## installation

You can install it on  a raspberry pi running raspbian, like this:

```sh
sudo apt install -y plymouth plymouth-label plymouth-themes
sudo git clone --depth=1 https://github.com/konsumer/plymouth-theme.git /usr/share/plymouth/themes/notnull
sudo ln -s /usr/lib/arm-linux-gnueabihf/plymouth/script.so /usr/lib/arm-linux-gnueabihf/plymouth/notnull.so
plymouth-set-default-theme notnull
```

Then add something like this to your `/boot/cmdline.txt`:

```
quiet splash plymouth.enable=1 plymouth.ignore-serial-consoles
```

Adapt this to other platforms/distros, as needed.