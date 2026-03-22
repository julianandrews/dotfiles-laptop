# Installation Notes

## Manual steps

- Install FontAwesome in `~/.local/share/fonts` (need the `Solid` variant)
    - Run `fc-cache -fv`
- Install google chrome deb package directly
- Add wallpapers to ~/.local/share/wallpapers
- Install opencode binary in ~/.local/bin

```
# Set up permissions
sudo usermod -a -G render julian
echo "Defaults !admin_flag" | sudo tee /etc/sudoers.d/no-admin-flag
sudo chmod 0440 /etc/sudoers.d/no-admin-flag

# Install Nerd Fonts
FONT_URL="https://github.com/ryanoasis/nerd-fonts/releases/latest/download/DejaVuSansMono.tar.xz"
mkdir -p ~/.local/share/fonts
curl -L "$FONT_URL" \
    | tar -xJ -C ~/.local/share/fonts/ --wildcards '*.ttf' '*.otf'
fc-cache -fv
```

## TODO

### hyprland config

- consider uwsm (systemd for stuff)
- Fix TTY switching
    - Keybindings might work, but only if hyprland isn't broken =/
    - Is there another way?

### neovim config

- LSP
- completion
- linter
- autoformat
