# Monochrome
A LeftWM + Polybar theme with a minimal palette of warm colors and a lot of gaps, literal and figurative.

## Features
- All the gaps you could have ever wanted
- Theme for Dunst notifications
- Bars drawn on multiple workspaces
- Separation of icon and text fonts (just like the church and state)
- Polybar modules with minimal formatting

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
	- `font-0` for text
	- `font-1` a non-monospace nerd font for vertically scaled icons
	- `font-2` a monospace nerd font for tags (horizontally scaled icons)

## Themes that go well with Monochrome
- My [Monokai Alacritty] theme

## Dependencies
- LeftWM
- Polybar
- feh (draw wallpaper in [up])
- Fira Code Nerd Font
- Arimo Nerd Font

## Installation


## Patches
### Notifications in top right corner
By default I positioned Dunst notifications in the `bottom-right` and with a large offset where they are least likely to overlap with anything I want to see. This patches moves them to the top right corner and aligns them with a window border located there.

## ToDo
- [ ] Rofi theme
- [ ] Picom config