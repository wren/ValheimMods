
## Changelog
### 1.0.12
- Added beginning of string wildcard match for pin names to support AutoMapPins pin names with "counts", e.g. "\*Raspberry" matches "5 Raspberry"
- Fixed issue with wildcard at end of string
- Added missing "Hammer" alias for excluding pin types
- Fixed colors on compass pins for 'other' player pins

### 1.0.11
- Fixed rare issue showing/hiding compass

### 1.0.10
- Fixed compass position issue reported by some users

### 1.0.9
- Added stone portal

### 1.0.8
- Performance tweak

### 1.0.7
- Changed dynamic pin names map configuration and fixed issue with viewing dynamic pin names. See Documentation.

### 1.0.6
- Fixed overwriting custom images

### 1.0.5
- Moved external images to mod root folder for compatibility with R2Modman installation
- Added configuration to use embedded (default) or external images
 
### 1.0.4
- Added ability to show/hide player pins in configuration for NoMap play
- Added server config to force player pins on, off, or let the player decide
- Changed to use images in Resources folder to allow custom compass images

### 1.0.3
- Fixed rare issue with dynamic pins on minimap.
- Fixed show/hide compass being overridden by server setting
- Added separate server authoritative HUD enable/disable

### 1.0.2
- Fixed player loading issue on some systems.

### 1.0.1
- Added support for custom ships & carts
- Fixed dynamic pin colors changing when faded (another player's markers)
- Fixed newly created object's pin displaying as another player's marker (i.e. faded and wrong color)

### 1.0.0
- Initial release
