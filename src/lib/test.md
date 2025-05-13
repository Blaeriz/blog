## My Hyprland Rice: Minimal, Black/White

I've been tinkering with my Arch Linux setup for a while, tried i3, Hyprland, dwm, awesome. I prefered Hyprland most.

### Core Components:

Here's a quick rundown of what makes up my current rice:

**OS:** Arch Linux

**Window Manager:** [Hyprland](https://hyprland.org/)

**System Information Tool:** [Fastfetch](https://github.com/fastfetch-cli/fastfetch)

**Bar:** [Hyprpanel](https://hyprpanel.com/) (I used to use waybar but switched to Hyprpanel. Some bugs but good enough)

**App Launcher:** [Rofi](https://davatorium.github.io/rofi/)

**Terminal:** [Alacritty](https://alacritty.org/)

**Notifications:** [Dunst](https://dunst-project.org/)

**Wallpaper Manager:** [Hyprpaper](https://wiki.hyprland.org/Hypr-Ecosystem/hyprpaper/)

**File Manager** [Yazi](https://yazi-rs.github.io/)

**Screenshot Tool:** [Grim](https://github.com/emersion/grim) & [Slurp](https://github.com/emersion/slurp)

**Text Editor:** [Nvim](https://neovim.io/) with [NvChad](https://nvchad.com/)

Command I use to copy ss to clipboard(keybind set in hyprland.conf): 
```bash
bind = ,Print, exec, grim -g "$(slurp -d)" - | wl-copy
```

### Showcase:

![My clean Hyprland desktop showcasing the wallpaper, bar, and overall aesthetic.](/rice.png)

### Grab The Configs:

[Dotfiles](https://github.com/Blaeriz/.dotfiles)

### Final Thoughts:

Small tweaks are constantly being made to this depending on how I feel at that time but this is pretty much what it is.