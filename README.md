# bashbreak

`bashbreak` is a lightweight program that reminds you to take regular breaks.

Taking regular breaks increases focus and prevents repetitive strain injury; it's good for you, but easy to forget. `bashbreak` reminds you to take a break and move around regularly.

## Instructions 

The basic idea is to have two kinds of breaks during a work session: short and long. By default, you have 10 min work sprints, separated by short breaks of 1 min and with a long break of 15 min after 4 work sprints. Thus, each "work session" totals 1 h (including the breaks). You can of course change the settings to your liking.

When a break is over, `bashbreak` checks if you are active at the computer before it starts the next work sprint.

You can specify the number of work sessions you want by running `bashbreak` with the `-n` option. If you plan to work for a total of 4 work sessions (i.e., 4 hours with the default settings), type:

	$ bashbreak -n 4

By default, `bashbreak` runs in the current terminal so you may want to fork it to the background using the `-B` flag. You can quit a currently running session with `-q`.

Type `bashbreak -h` to see all available commands.

## Installation and configuration
To install, download this repo and run the install script: 

```
git clone https://github.com/mrtgst/bashbreak.git
cd bashbreak
sudo ./setup install
``` 

This will copy `bashbreak` to `/usr/local/bin/` and a default configuration file to `/home/<user>/.config/bashbreak`. Edit the configuration file to change settings.

## Uninstallation

To remove bashbreak and its config files you can call the above setup-script with `sudo ./setup uninstall`. 

## Dependencies
`bashbreak` can run just in your terminal using bash builtins, but the desktop notifications and idle time checker have some further dependencies.

To see desktop notifications you need `libnotify` and a notification daemon installed, which is standard on most Linux distros running a desktop environment such as GNOME, KDE, LXDE etc. If you are not running a full DE, see [wiki.archlinux.org/index.php/Desktop_notifications](https://wiki.archlinux.org/index.php/Desktop_notifications).

To check for user idle time, `bashbreak` uses `xprintidle`, which further assumes you are running the X Window System.
