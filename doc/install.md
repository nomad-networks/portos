# Best installation practices as of now


## Dowload current Manjaro Gnome Edition

You can download it from [manjaro.org](https://manjaro.org/get-manjaro/).


## Install manjaro

### Connect to the Internet

On the top left corner click on any of the icons. From the menu select the top menu (`Wifi not connected.`) and from the pull down menu click on the `Select Network` menu point. Select the desired wifi network, and type the wifi password.

### Partitioning

Run the installer. Standard partitioning scheme for PortOS is one ext4 partition over the whole disk mounte as `/` . The reasoning behind it is that this is the most easly undertandable. When the need rises one needs to understand other partitioning schemes. The swap size is the same as the amount of ram the machine has.

### Password

Use the same password for the admin as the default user, but don't turn on automatic login.

### Reboot

After installation finished reboot the machine and make sure it's starting from the new install.


## Turn off "Hello" screen

Bottom right corner turn off the `Launch at start` switch. After that close the window. You can start it later by `Super` `manjaro hello`.


## Set the time

> This is only necessary if you didn't have internet connection during the installation.

Go to the Settings applet by `Super` `settings`. Find the `Date & Time` tab under the `Details` section or by searching for it. Turn on both the `Automatic Date & Time` and the `Automatic Time Zone` switches. You can leave the settings window open.


## Update the system

Run the terminal by `Super` `terminal` . Type `sudo pacman -Syyu` and give your password. Answer to the questions with yes by pressing `y` .


## Install the 'Hide Top Panel' Gnome extension

In a terminal type `sudo pacman -Syu gnome-shell-extensions` . After installation of the package go to the [Gnome shell extensions](https://extensions.gnome.org/) webpage and install the browser extension. After this find the `Hide top panel` extension and install it.

You can enable or disable it in `Gnome Tweaks` .

From the firefox menu select the `Customize` menu point and remove the Gnome Shell icon from the Firefox toolbar.


## Install zsh and oh-my-zsh

    sudo pacman -Syu zsh git
    chsh -s /bin/zsh

Log out and log back in. Run a terminal, then go to the [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) webpage and follow the installation instructions there. Both `curl` and `wget` should be installed on your machine already.


## Install the lesspass Firefox addon

Go to the [lesspass firefox addon](https://github.com/robbyrussell/oh-my-zsh) webpage and install it.


## Install uBlock Origin Firefox addon

Go to the [uBlock Origin firefox addon](https://github.com/robbyrussell/oh-my-zsh) webpage and install it.


## Night light

Default color temperature of 4000K is too much for my eyes. For me it's better at 5000.

With `dconf-editor` set `org.gnome.settings-daemon.plugins.color night-light-temperature 5000`.
