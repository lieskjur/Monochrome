# Monochrome
A LeftWM + Polybar theme with a minimal palette of warm colors and a lot of gaps, literal and figurative.

## Features
- Polybars on multiple workspaces
- Separate fonts for icons and text
- Polybar modules without font and background colors or underlines

## Included Polybar modules
Polybar modules are included in [polybar.modules]. By default only the date-time module is applied with the option of adding more 
- internal
	- date
	- pulseaudio
	- battery
- custom [dependencies]
	- pci
		- brightness [brightnessctl]
	- script
		- updates [pamac]
	- text
		- powermenu [rofi]

## Modification hints
- `module-left` is drawn using the `polybar.liquid` module

## Themes that go well with Monochrome
- My [Monokai Alacritty] theme

## Dependencies
- LeftWM
- Polybar
- feh (draw wallpaper in [up])

## Installation


## Patches
### Notifications in top right corner
By default I positioned Dunst notifications in the `bottom-right` and with a large offset where they are least likely to overlap with anything I want to see. This patches moves them to the top right corner and aligns them with a window border located there.

## ToDo
- [ ] Rofi theme
- [ ] Picom config