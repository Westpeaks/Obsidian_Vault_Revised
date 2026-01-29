
- This setup is for Hyprland configs. In particular, this is for Omarchy. In vanilla Hyprland, you would make these changes in `~/.config/hypr/hyprland.conf`.
- Navigate to `~/.config/hypr/input.conf` and have the following setup configured for the touch pad:
  
  ```vim
  touchpad {
    # Use natural (inverse) scrolling
    natural_scroll = true

    # Use two-finger clicks for right-click instead of lower-right corner
    clickfinger_behavior = true

    # Disable trackpad while typing
    disable_while_typing = true

    # Control the speed of your scrolling
    scroll_factor = 0.4

    # Turn on/off tap to click
    tap-to-click = false

    # Left-click-and-drag with three fingers
    # drag_3fg = 1
  }
  ```  
## Links:

[[2026-01-02]]

2026010233