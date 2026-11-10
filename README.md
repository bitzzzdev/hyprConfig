# hyprConfig: E-ink Dotfiles for Hyprland and Quickshell

Hyprland dotfiles configuration that builds a centered pill top bar using Quickshell, featuring dynamic Material You color palettes generated directly from your active wallpaper via matugen.

Maintained by Dev Borah ([@bitzzdev](https://github.com/bitzzdev)).

## Features

- Quickshell top bar: time indicator, workspaces switcher, audio volume, WiFi SSID, and battery status pill.
- Calendar popover: click time indicator to toggle the interactive monthly calendar.
- Dynamic color theming: wallpaper palette extracted in real time via `matugen image ... -j hex`.
- Hyprland key bindings:
  - `SUPER + T`: launch kitty terminal
  - `SUPER + SHIFT + T`: run OCR on selected screen region and copy text to clipboard
  - `SUPER + Q`: close focused window
  - `SUPER + E`: launch nautilus file manager

## Installation

The repository is structured for deployment using GNU `stow`.

### One-command installer (Arch Linux)

```bash
chmod +x ./install-arch.sh
./install-arch.sh
```

### Manual installation

```bash
cd /path/to/hyprConfig
stow -t "$HOME" dotfiles
chmod +x ~/.local/bin/eink-wallpaper
```

## Wallpaper and theme commands

To change wallpaper and automatically regenerate theme colors:

```bash
eink-wallpaper /path/to/wallpaper.png
```

To restore the saved wallpaper on graphical session start (invoked automatically via Hyprland `exec-once`):

```bash
eink-wallpaper --restore
```

## Connect

- Creator: [Dev Borah](https://bitz.is-a.dev)
- GitHub: [bitzzdev](https://github.com/bitzzdev)
- Ko-fi: [bitzzdev](https://ko-fi.com/bitzzdev)
- Reddit: [u/bitzzdev](https://www.reddit.com/user/bitzzdev/)

## License

MIT License. Free to use, adapt, and share.
