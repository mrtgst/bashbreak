# bashbreak

`bashbreak` is a lightweight program that reminds you to take regular breaks.

Taking regular breaks increases focus and prevents repetitive strain injury; it's good for you, but easy to forget, so `bashbreak` reminds you to take a break and move around more regularly.

## Features



## Installation



## Dependencies
`bashbreak` can run just in your terminal using bash builtins, but the desktop notifications and idle time checker have some further dependencies.

To see desktop notifications you need `libnotify` and a notification daemon installed, which is standard on most Linux distros running a desktop environment such as GNOME, KDE, Cinnamon etc. If you have a more minimal install and use a window manager, see [https://wiki.archlinux.org/index.php/Desktop_notifications](https://wiki.archlinux.org/index.php/Desktop_notifications).

To check for user idle time, `bashbreak` uses `xprintidle`. 
