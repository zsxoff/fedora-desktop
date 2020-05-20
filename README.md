# Fedora: Desktop from Netinstall ISO image

[![made-with-Markdown](https://img.shields.io/badge/Made%20with-Markdown-2d2d2d.svg)](http://commonmark.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

My version of a Fedora desktop installation from minimal ISO image.

You can download ISO file from [Fedora: Netinstall ISO image for x86_64](https://getfedora.org/ru/server/download/).

Tested on (this list is updated during testing):

* Fedora 31 Netinstall

## Base environment

### 1. Base system

Contains package groups of:

* :checkered_flag: Base X System
* :checkered_flag: Fonts
* :checkered_flag: GNOME Desktop
* :checkered_flag: Hardware Support
* :checkered_flag: Common NetworkManager Submodules
* :checkered_flag: Standard Utilities

```bash
sudo dnf install -y \
    @base-x \
    @fonts \
    @gnome-desktop \
    @hardware-support \
    @networkmanager-submodules \
    @standard
```

You can activate graphical login by command:

```bash
sudo systemctl set-default graphical.target
```

### 2. GNOME Tweaks and Themes

* :wrench: Base Gnome tweak tool:

```bash
sudo dnf install -y gnome-tweak-tool
```

Some useful extensions:

* [Arc Menu](https://extensions.gnome.org/extension/1228/arc-menu/)
* [Dash to Dock](https://extensions.gnome.org/extension/307/dash-to-dock/)
* [Dash to Panel](https://extensions.gnome.org/extension/1160/dash-to-panel/)
* [Freon](https://extensions.gnome.org/extension/841/freon/)
* [Remove Dropdown Arrows](https://extensions.gnome.org/extension/800/remove-dropdown-arrows/)
* [Sound Input & Output Device Chooser](https://extensions.gnome.org/extension/906/sound-output-device-chooser/)
* [Switcher](https://extensions.gnome.org/extension/973/switcher/)
* [Tweaks in System Menu](https://extensions.gnome.org/extension/1653/tweaks-in-system-menu/)

I used this GTK themes and customization:

* :art: [Orchis Theme](https://github.com/vinceliuice/Orchis-theme)
* :art: [Numix Icon Theme Square](https://github.com/numixproject/numix-icon-theme-square)
* :art: [Vimix Cursors](https://github.com/vinceliuice/Vimix-cursors)

```bash
sudo dnf install -y numix-gtk-theme numix-icon-theme-circle breeze-cursor-theme
```

### 3. Additional fonts

* :pencil: Google Croscore Fonts
* :pencil: Google Noto Sans Fonts

```bash
sudo dnf install -y google-croscore-* google-noto-sans-fonts
```

### 4. PulseAudio

* :sound: pulseaudio
* :sound: pulseaudio-utils
* :sound: pulseaudio-module-x11

```bash
sudo dnf install -y pulseaudio pulseaudio-utils pulseaudio-module-x11
```

## 5. Additional useful console tools

* :hammer_and_wrench: Some programs that I use to work:

```bash
sudo dnf install -y aria2 htop neovim ranger tmux
```

## 6. Development

* :wrench: **Base Development tools**

```bash
sudo dnf install -y @development-tools
```

* :wrench: **Python 3**

```bash
sudo dnf install -y python3 python3-pip python3-devel python3-tkinter
```

## Preferred desktop software

Most likely for this you need to [enabling the RPM Fusion repositories](https://docs.fedoraproject.org/en-US/quick-docs/setup_rpmfusion/).

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

## License

This project is licensed under the terms of the [MIT](https://opensource.org/licenses/MIT) license (see [LICENSE](<https://github.com/zsxoff/fedora-desktop/blob/master/LICENSE>) file).
