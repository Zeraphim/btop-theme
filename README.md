# Zeraphim for btop

A dark [btop](https://github.com/aristocratos/btop) theme using the palette from
[Zeraphim for Obsidian](https://github.com/Zeraphim/obsidian-theme).
Deep navy canvas, turquoise selection, sky blue and lavender panels, and
amber-to-coral gradients for processor load and temperature.

## Install

Run these commands from a directory outside your btop configuration folder:

```sh
git clone https://github.com/Zeraphim/btop-theme.git
cd btop-theme
config_dir="${XDG_CONFIG_HOME:-$HOME/.config}/btop"
mkdir -p "$config_dir/themes"
cp themes/zeraphim.theme "$config_dir/themes/zeraphim.theme"
```

Open btop, press `Esc`, choose **Options**, then set **Color theme** to
`zeraphim`. Enable **Theme background** and **Truecolor** for the intended colors.

Alternatively, set these values in your existing `btop.conf` inside the btop
configuration folder:

```ini
color_theme = "zeraphim"
theme_background = True
truecolor = True
```

Restart btop after editing the configuration. If this repository is already
checked out at `~/.config/btop`, the theme is installed and only needs selecting.

## Palette

| Role | Color | Use |
| --- | --- | --- |
| Canvas | `#060a13` | Background and text on bright selection |
| Body text | `#edf7f7` | Values and panel titles |
| Turquoise | `#7fe9d6` | Selection, shortcuts, processor outline, downloads |
| Sky blue | `#5fb8d4` | Network outline, temperature, process details |
| Lavender | `#c4b5fd` | Memory outline and uploads |
| Amber | `#fbbf24` | Middle of load gradients and paused banner |
| Coral | `#e2707a` | High load and temperature |
| Mint | `#6fe0b8` | Free and available memory |

Selected rows and bright banners use dark text for contrast. Load gradients
represent a continuous scale, not configurable warning thresholds.

## Compatibility

Verified with btop 1.4.7. The theme defines all 48 color entries in that version,
including process pause, follow, and banner colors.

Use a terminal with 24-bit color support. btop can approximate the palette in
256-color mode. Forced 16-color mode uses btop's own terminal palette.

## Customize

Edit `themes/zeraphim.theme`, copy it into your user themes folder again, and
restart btop. Each entry uses `theme[name]="#rrggbb"` syntax. Keep dark text on
bright selection and banner backgrounds when changing those colors.
