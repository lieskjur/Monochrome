# Monochrome
A LeftWM + Polybar theme with a minimal palette of warm colors and a lot of gaps, literal and figurative.

## Features
- All the gaps you could have ever wanted
- [Dunst] and [Rofi] themes
- Support for setting the wallpaper with [nitrogen]
- Status bars drawn on multiple workspaces
- Separation of icon and text fonts (just like the church and state)
- [Polybar] modules with minimal formatting

## Included Polybar modules
Polybar modules are included in [polybar.modules]. By default only the date-time module is applied with the option of adding more in [polybar.config]
- internal
	- date
	- pulseaudio
	- battery
- custom [dependencies]
	- pci
		- brightness [brightnessctl]
	- script
		- updates
	- text
		- powermenu [rofi]

## Modification hints
- `module-left` is drawn using the `polybar.liquid` module
- three separate fonts are used in the polybar
	- `font-0` - text
	- `font-1` - icons (nerd-font recommended)
	- `font-2` - tags (monospace nerd-font recommended)
- you can set your own wallpaper using [nitrogen] as `nitrogen --restore` is run while loading the theme if available.

## other configs that go well with Monochrome
- My [Monokai] theme for Alacritty
- [Picom config] I use

## Dependencies
- core
	- LeftWM
	- Polybar
- default
	- Fira Code Nerd Font
	- Arimo Nerd Font
- optional
	- feh
	- nitrogen
	- dunst

## Installation


## Patches
### Notifications in top right corner
By default I positioned Dunst notifications in the `bottom-right` and with a large offset where they are least likely to overlap with anything I want to see. This patches moves them to the top right corner and aligns them with a window border located there.

## ToDo
- [ ] Rofi theme
- [ ] Picom config