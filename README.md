# slitaz-takeover

A shell script to boot SliTaz from another Linux distro without a boot USB.
Inspired by [takeover.sh].

## Warning

`slitaz-takeover` is currently alpha level software and does contain bugs, use
at your own risk!

You should not run this script on computers you do not currently have physical
access to, as you can and will lose access after the takeover.

This script will mercilessly terminate all running processes during the
takeover, so do not have any unsaved work.

## How to use

To use `slitaz-takeover`:

1. Download `slitaz-takeover`.
1. Optionally inspect the source code.
1. Execute it (as root).

To revert back to your original system, you can simply reboot your computer. All
changes are done in RAM (and `/tmp`) and *shouldn't* harm your system.

The script will give you two chances to cancel (the first one is "safer",
however they should both work). You cannot return to your running system after
the second cancellation prompt, if you change your mind after that you will
need to reboot.

## Known bugs

* Mouse and keyboard input can be intermittent on some devices.
* Any network-mounted directories (such as SMB shares) must be unmounted before running the script, as the network is disabled (along with everything else) before unmounting filesystems.

[takeover.sh]: https://github.com/marcan/takeover.sh
