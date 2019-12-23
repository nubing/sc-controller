SC Controller Snap
==================

Snap for sc-controller, driver for Steam and other controllers.

## Links

- [kozec/sc-controller](https://github.com/kozec/sc-controller)

## Known issues

* Unable to download release notes on first run

* Appimage is only 16mb this snap is 75mb

* Requires manual connection of raw-usb and bluetooth interfaces (request auto-connect in forum)

* Udev rules

	`I’ll also mention that a steam controller needs a number of udev rules (one rather unfortunate (KERNEL=="uinput")) to work on the system and snapd doesn’t currently add these. On Ubuntu, installing ‘steam-devices’ deb will put these into place. We’ll be looking at updates to snapd on how to ship these udev rules so people don’t need an external package.`

* Loading indicator icon

	File "/snap/sc-controller/x1/lib/python2.7/site-packages/scc/gui/app.py", line 834, in on_daemon_alive
		self.set_daemon_status("alive", True)
	File "/snap/sc-controller/x1/lib/python2.7/site-packages/scc/gui/app.py", line 1393, in set_daemon_status
		self.window.set_icon_from_file(icon)
	GLib.Error: gdk-pixbuf-error-quark: Couldn't recognize the image file format for file '/snap/sc-controller/x1/share/scc/images/scc-alive.svg' (3)

	https://github.com/kozec/sc-controller/blob/v0.4.6.1/scc/gui/app.py#L1393

	inotifywait -mr --exclude=".*[so|py|h|typelib]$" /snap/sc-controller
