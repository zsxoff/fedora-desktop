# Fedora: Desktop from Netinstall ISO image

My version of a Fedora desktop installation from minimal ISO image.

You can download ISO file from [Fedora: Netinstall ISO image for x86_64](https://getfedora.org/ru/server/download/).

Tested on (this list is updated during testing):

* Fedora 31 Netinstall

## Base environment

### 1. Base system

Contains package groups of:

* :checkered_flag: Standard utilities
* :checkered_flag: Base X System
* :checkered_flag: GNOME Desktop
* :checkered_flag: Fonts
* :checkered_flag: NetworkManager

```bash
sudo dnf install -y @standard @base-x @networkmanager-submodules @gnome-desktop @fonts
```

You can activate graphical login by command:

```bash
sudo systemctl set-default graphical.target
```

### 2. GNOME Tweaks and tools

* :wrench: Base Gnome tweak tool:

```bash
sudo dnf install -y gnome-tweak-tool
```

I use the following extensions:

* [Dash to Dock](https://extensions.gnome.org/extension/307/dash-to-dock/)
* [Sound Input & Output Device Chooser](https://extensions.gnome.org/extension/906/sound-output-device-chooser/)

### 3. Additional fonts

* :pencil: Google Croscore Fonts
* :pencil: Google Noto Sans Fonts
* :pencil: Liberation Fonts

```bash
sudo dnf install -y google-croscore-* google-noto-sans-fonts liberation-fonts
```

### 4. Themes and customization

* :art: Flat Remix theme
* :art: Papirus icon theme
* :art: Breeze cursor theme

```bash
sudo dnf install -y flat-remix-theme papirus-icon-theme breeze-cursor-theme
```

### 5. PulseAudio

* :sound: pulseaudio
* :sound: pulseaudio-utils
* :sound: pulseaudio-module-x11

```bash
sudo dnf install -y pulseaudio pulseaudio-utils pulseaudio-module-x11
```

## 6. Additional useful console tools

* :hammer_and_wrench: Some programs that I use to work:

```bash
sudo dnf install -y aria2 htop neovim ranger tmux
```

## 7. Development

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
