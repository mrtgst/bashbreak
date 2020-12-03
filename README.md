# bashbreak

`bashbreak` is a lightweight program that reminds you to take regular breaks.

Taking regular breaks increases focus and prevents repetitive strain injury; it's good for you, but easy to forget, so `bashbreak` reminds you to take a break and move around regularly.

## Instructions 

The basic idea is to have two kinds of breaks during a work session: short and long. By default, you have 10 min work sprints, separated by short breaks of 1 min and with a long break of 15 min after 4 work sprints. Thus, each "work session" totals 1 h. You can of course change the settings to your liking.

When a break is over, `bashbreak` checks if you are active at the computer before it starts the next work sprint.

You can specify the number of work sessions you want by running `bashbreak` with the `-n` option. If you plan to work for a total of 4 work sessions, type:

	$ bashbreak -n 4

Type `bashbreak -h` to see all available commands:

	Use:
	        bashbreak [OPTION]...

	Options:
	 -n             Specify number of work sessions
	 -h             Print this help
	 -q             Quiet mode (no output to stdout)

## Installation
Link or copy `bashbreak` to a folder in your shell's path variable.


## Dependencies
`bashbreak` can run just in your terminal using bash builtins, but the desktop notifications and idle time checker have some further dependencies.

To see desktop notifications you need `libnotify` and a notification daemon installed, which is standard on most Linux distros running a desktop environment such as GNOME, KDE, Cinnamon etc. If you have a more minimal install and use a window manager, see [https://wiki.archlinux.org/index.php/Desktop_notifications](https://wiki.archlinux.org/index.php/Desktop_notifications).

To check for user idle time, `bashbreak` uses `xprintidle`. 
