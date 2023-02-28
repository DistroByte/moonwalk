---
layout: post
author: James Hackett
---

# Configuring a Raspberry Pi to use SSH without booting

Flashing a new operating system onto a Raspberry Pi should be an easy task, but sometimes you need to use a monitor, and finding a mini (micro?) HDMI cable can prove difficult, finding a monitor to plug into can be equally as difficult. This post should help alleviate some of those hurdles.

## Choosing your OS

I usually go for Raspbian's 64 bit OS because it's still based on Debian and almost everything that Debian can do on x86, it can do on arm.

You can find the OS [here](https://www.raspberrypi.com/software/operating-systems/#raspberry-pi-os-64-bit).

## Flashing your boot drive

Use [Rufus](https://rufus.ie/en/) or any other bootable USB creator to flash the image onto the USB.

## Enabling SSH without booting the Pi

Once that process has completed, add a file called `ssh` to the `/boot` partition of the drive. You'll find it easily on Windows because it's the only part that Windows can see in the file explorer.

![screenshot of windows file explorer showing the boot drive](https://i.dbyte.xyz/explorer_y4EwzIYoG.png)

## Adding a user

There were changes made to the OS to improve security. Instead of `pi:raspberry` being the default credentials, you now need to create a user by adding a file to the same directory as before, but called `userconf`. Inside that file, add a line containing the desired `username:encrypted-password`. 

Generate your password with the following command:

```
echo 'mypassword' | openssl passwd -6 -stdin
```

Put the output of this command into the file, preceeded by the username and a colon.

More information can be found here: [http://rptl.io/newuser](http://rptl.io/newuser)


