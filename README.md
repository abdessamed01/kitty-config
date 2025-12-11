# Kitty Terminal Config

This is my **custom Kitty terminal configuration** for Arch Linux (and compatible systems).  
It provides a sleek, modern, and visually appealing terminal experience.

---

## One-Command Installer

Run this command to automatically set up Kitty, Zsh, Powerlevel10k, plugins, and Fastfetch:

git clone https://github.com/YOUR_USERNAME/kitty-config.git ~/kitty-config && \
sudo pacman -S --noconfirm kitty zsh git fzf fastfetch && \
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" && \
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k && \
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-autosuggestions && \
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting && \
mkdir -p ~/.config/kitty && cp ~/kitty-config/kitty.conf ~/.config/kitty/ && \
mkdir -p ~/.config/fastfetch && fastfetch --gen-config > ~/.config/fastfetch/fastfetch.conf && \
chsh -s $(which zsh)
After running, restart your terminal to see the full setup.

Features
Blurred background with adjustable transparency

Animated cursor trail with glow and fast movement

Modern Powerline-style tabs with slanted separators

Custom dark theme:

Background: #282a36

Foreground: #f8f8f2

Cursor: #50fa7b

Tabs: blue and gray accents

Optimized for Zsh with Powerlevel10k prompt

Compatible with Nerd Fonts for icons in prompt or Fastfetch

Customization Tips
Cursor trail & animation (kitty.conf):

conf
Copy code
cursor_trail 200
cursor_trail_decay 0.05 0.3
cursor_move_animation_duration 0.05
cursor_shadow yes
cursor_shadow_color #50fa7b
cursor_shadow_opacity 0.3
Background blur & transparency:

conf
Copy code
background_opacity 0.85
background_blur_radius 15
Tabs & colors:

c
Copy code
tab_bar_style powerline
tab_powerline_style slanted
active_tab_foreground #ffffff
active_tab_background #4f5bff
inactive_tab_foreground #8888aa
inactive_tab_background #1e1e2e
Zsh plugins are already configured: autosuggestions + syntax highlighting

Fastfetch is pre-generated; you can edit colors, icons, and modules in ~/.config/fastfetch/fastfetch.conf.

License
This configuration is free to use and modify.
Please give credit if sharing publicly.

Enjoy a sleek, fast, and visually stunning terminal experience!
