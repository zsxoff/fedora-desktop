# Fedora: Desktop from Netinstall ISO image

My version of a Fedora desktop installation from minimal ISO image.

You can download ISO file from [Fedora: Netinstall ISO image for x86_64](https://getfedora.org/ru/server/download/).

Tested on (this list is updated during testing):

* Fedora 31 Netinstall

## Base environment

Contains groups of:

* Standard utilities
* Base X System
* GNOME Desktop
* Fonts
* NetworkManager

```bash
sudo dnf install -y @standard @base-x @networkmanager-submodules @gnome-desktop @fonts
```

You can activate graphical login by command:

```bash
sudo systemctl set-default graphical.target
```

### GNOME Tweaks and tools

Base Gnome tweak tool:

```bash
sudo dnf install -y gnome-tweak-tool
```

I use the following extensions:

* [Dash to Dock](https://extensions.gnome.org/extension/307/dash-to-dock/)
* [Sound Input & Output Device Chooser](https://extensions.gnome.org/extension/906/sound-output-device-chooser/)

### Additional fonts

* :pencil: Google Croscore Fonts
* :pencil: Google Noto Sans Fonts
* :pencil: Liberation Fonts

```bash
sudo dnf install -y google-croscore-* google-noto-sans-fonts liberation-fonts
```

### Themes and customization

* :art: Flat Remix theme
* :art: Papirus icon theme
* :art: Breeze cursor theme
* :art: Fedora 31 Backgrounds

```bash
sudo dnf install -y flat-remix-theme papirus-icon-theme breeze-cursor-theme
```

### PulseAudio

* :sound: pulseaudio
* :sound: pulseaudio-utils
* :sound: pulseaudio-module-x11

```bash
sudo dnf install -y pulseaudio pulseaudio-utils pulseaudio-module-x11
```

## Additional useful console tools

```bash
sudo dnf install -y aria2 htop neovim ranger tmux
```

## Development

:wrench: **Base Development tools**

```bash
sudo dnf install -y @development-tools
```

:wrench: **Python 3**

```bash
sudo dnf install -y python3 python3-pip python3-devel python3-tkinter
```

## Preferred desktop software

| Software                             | Repo                                                                                  |
| :----------------------------------- | :------------------------------------------------------------------------------------ |
| :globe_with_meridians: Google Chrome | rpm package - [Official site](https://www.google.com/intl/en_us/chrome/)              |
| :memo: Visual Studio Code            | rpm package - [Official site](https://code.visualstudio.com/)                         |
| :page_facing_up: ONLYOFFICE          | rpm package - [Official site](https://www.onlyoffice.com/)                            |
| :page_facing_up: Evince              | Fedora repo - [evince](https://pkgs.org/download/evince)                              |
| :art: GIMP                           | Fedora repo - [gimp](https://pkgs.org/download/gimp)                                  |
| :file_folder: Transmission GTK       | Fedora repo - [transmission-gtk](https://pkgs.org/download/transmission-gtk)          |
| :movie_camera: MPV                   | RPM Fusion Free repo - [mpv](https://pkgs.org/download/mpv)                           |
| :speech_balloon: Telegram            | RPM Fusion Free repo - [telegram-desktop](https://pkgs.org/download/telegram-desktop) |
