# Monochrome
A LeftWM + Polybar theme with a minimal palette of warm colors and a lot of gaps, literal and figurative.

## Features
- matching [Polybar](https://polybar.github.io/), [Dunst](https://dunst-project.org/) and [Rofi](https://github.com/davatorium/rofi) themes
- All the gaps you could have ever wanted
- Support for setting the wallpaper with [nitrogen](https://github.com/l3ib/nitrogen/)
- Status bars drawn on multiple workspaces
- Separation of icon and text fonts (just like the church and state)
- [Polybar](https://polybar.github.io/) modules with minimal formatting

## Included Polybar modules
Polybar modules are included in `polybar.modules`. By default only the date-time module is applied with the option of adding more in `polybar.config`
- internal
	- date
	- pulseaudio
	- battery
- custom
	- pci
		- brightness (dependency: [brightnessctl](https://github.com/Hummer12007/brightnessctl))
	- script
		- updates
	- text
		- [power-menu](https://github.com/jluttine/rofi-power-menu) (dependency: [rofi](https://github.com/davatorium/rofi))

## Modification hints
- `module-left` is drawn using the `polybar.liquid` module
- three separate fonts are used in the polybar
	- `font-0` - text
	- `font-1` - icons (nerd-font recommended)
	- `font-2` - tags (monospace nerd-font recommended)
- you can set your own wallpaper using [nitrogen](https://github.com/l3ib/nitrogen/) as `nitrogen --restore` is run while loading the theme if available.

## other configs that go well with Monochrome
- My Monokai-like theme for Alacritty which can be found in my [`alacritty.yml`](https://github.com/lieskjur/.config-alacritty/alacritty.yml)
- [Picom config](https://github.com/lieskjur/.config-picom) that I use

## Dependencies
- core
	- LeftWM
	- Polybar
- default
	- Fira Code Nerd Font
	- Roboto
- optional
	- feh / nitrogen
	- dunst

## Rofi keybindings
You can also add `rofi -show drun` and power-menu keybindings to your `~/.config/leftwm/config.toml` eg.
```
[[keybind]]
command = "Execute"
value = "rofi -show power-menu -modi power-menu:$HOME/.config/leftwm/themes/current/rofi/rofi-power-menu.sh"
modifier = []
key = "XF86XK_PowerOff"

[[keybind]]
command = "Execute"
value = "rofi -show drun"
modifier = ["modkey"]
key = "p"
```
There are multiple ways in which the included rofi theme can be applied, the method I use is adding
```
@theme "~/.config/leftwm/themes/current/rofi/default.rasi"
```
to my `~/.config/rofi/config.rasi` file

## Patches

<!-- ### Notifications in top right corner
By default I positioned Dunst notifications in the `bottom-right` and with a large offset where they are least likely to overlap with anything I want to see. This patches moves them to the top right corner and aligns them with a window border located there. -->

### [Alternate battery icons](alternate-battery-icons-patch.diff)
A different set of icons for the polybar battery module

### [Window title patch](window-title-patch.diff)
Patch for displaying the focused window's title in the center of the polybar