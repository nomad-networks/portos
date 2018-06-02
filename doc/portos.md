# PortOS

PortOS is a secure, powerful and user friendly Linux distribution optimized for running on preselected hardware. PortOS's current target audience are web heavy users, coders, web developers, digital currency, scientists, researchers traders.

In it's current form it's not a full fledged distribution yet but a Manjaro Linux installation configured in our certain way. The configuration is optimized for specific hardware. Most probably the configuration makes sense on other hardware too, but testing on other than Port hardware is done by the community and not the PortOS team.


## Philosophy

PortOS's main goal is to standardize the user experience on Port hardware.

## The hardware

Currently PortOS is targeted on the Port One as the hardware platform.

The Port One is a refurbished and *balanced* Lenovo Thinkpad X230 which runs PortOS. By rebalanced we mean, that it uses a fast SSD instead of a conventional hard disk, and it has at least 8MB of fast RAM.


## The desktop environment

PortOS uses the Gnome 3 desktop environment. Currently we're using the Gnome oriented installation image to achieve this.


## Shell

We use zsh. We also add oh-my-zsh to the mix.


## Keyboard commands

We strongly believe that standardization of the desktop level keyboard commands would benefit the users tremendously. Our idea is to collect all DE level commands under the *win* key. We can safely do that since we are developing the OS for hardware that supports one. This way we can free *shift*, *ctrl* and *alt* for the application layer.


## Keyboard layout

Adding a keyboard layout to Manjaro Gnome after installation is tricky, so we must fix it first. We also need to send a bug report regarding this to Manjaro.


## Full screen

Since the X230 features a relatively small screen, we encourage our users to use a full screen oriented layout. We need to install the hide-top-panel extension for this. We also need to turn off in Firefox the auto-hide feature of the location bar.


## Software installation

We need to implement 'meta' a meta package manager (PM) which supports at least the following package managers:

1. pacman
2. pip
3. npm
4. apm
5. gnome-extensions

Meta is a script that uses the underlying package managers to do the heavy lifting. Its user interface is a simplified and unified version of the functionalities of all supported PMs. Another fundamental idea of `meta` is that it concentrates onlt for the most basic and easily understandable operations:

1. search for packages
2. install packages
3. remove packages
4. update packages
5. update the system

Every other functionality is only accessible with the underlying PM.


## Support


## Night light

Default color temperature of 4000K is too much for my eyes. For me it's better at 5000.

With `dconf-editor` set `org.gnome.settings-daemon.plugins.color night-light-temperature 5000`.
