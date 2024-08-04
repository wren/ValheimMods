# HUD Compass

## Heads-Up Compass with Dynamic Map Markers for Ships, Carts & Portals

Dude, where's my boat? Never lose track of your boats, carts or portals again. A heads-up compass that includes standard pins and dynamic map markers for ships, carts, active and inactive portals on the compass and the map.

HUD Compass combines and enhances the functionality of Immersive Compass and Automatic Map Markers to bring a complete experience to location aids. (see credits below)

- The scaleable compass appears across the top of your screen.
- Toggle the compass on and off in-game.
- Dynamic pins (ships, carts, portals) are shown on the compass and the map, with or without labels. 
- Supports custom ships and carts.
- Active and inactive portals can have different colors. 
- Portal pins display the name you give them. 
- Ship labels can specify the type of ship (Karve, Longship, Raft), as well as custom ships.
- Pin types to include/exclude are configurable. 
- Pin size is relative to marker distance, with configurable limits.
- Configuration to use external images for custom compass and dynamic icon appearance. **See Notes**

## New
- Added beginning of string wildcard match for pin names to support AutoMapPins pin names with "counts", e.g. "\*Raspberry" matches "5 Raspberry"
- Fixed issue with wildcard at end of string
- Added missing "Hammer" alias for excluding pin types
- Fixed colors on compass pins for 'other' player pins

## Configuration

### A - HUD Compass

- **Enable Compass:** Enable or Disable the Compass HUD.@
- **Show Compass:** Show or Hide the HUD compass. Use the Toggle Compass key to change in-game.
- **Toggle Compass Key:** Key used in-game to toggle the compass visibility.

### B - Compass Display

- **Use Player Direction:** Orient the compass based on the direction the player is facing, rather than the middle of the screen.
- **Compass Scale:** Sets the overall scale of the compass on the screen
- **Offset (Y):** Offset from the top of the screen in pixels.
- **Distance (Minimum):** Minimum distance from pin to show on compass.@
- **Distance (Maximum):** Maximum distance from pin to show on compass.@
- **Player Pin Visibility:** Force player pins (multiplayer) to appear or not appear on the compass and map, or let the player decide. Overrides Show My Player Pin if not set to PlayerChoice.@
- **Show My Player Pin:** Shows or hides your player pin (multiplayer) on the compass if playing no-map where visibility setting is not available. Overridden by server if Player Pin Behavior is not set to PlayerChoice.
- **Pins Scale:** Sets the overall scale of the pins on the on the screen
- **Minimum Pin Size:** Enlarge or shrink the scale of the pins at their furthest visible distance.
- **Show Center Mark:** (Optional) Show center mark graphic.

### C - Ignore

- **Pin Names:** Ignore location pins with these names (comma separated, no spaces). End a string with asterisk (*) to denote a prefix.@
- **Pin Types:** Ignore location pins of these types (comma separated, no spaces). Types include: Fire,House,Pin,Portal,Start,Haldir,Hildir,Death,Bed,Shout,Boss,Player,RandomEvent,Ping,EventArea.@

### E - Compass Colors

- **Compass Color:** (Optional) Adjust the main color of the compass.
- **Pin Color:** (Optional) Adjust the color of the location pins on the compass.
- **Center Mark Color:** (Optional) Adjust the color of the center mark graphic.

### F - Dynamic Pins

- **Show dynamic pins on map:** Display pins for ships, carts and portals on the main and minimap. Controlled individually below.@
- **Show dynamic pins on compass:** Display pins for ships, carts and portals on the compass. Controlled individually below.@
- **Player pin refresh pin interval:** Interval in seconds between refresh of player pins on map and compass. Decrease for 'smoother' updates of player pins. Zero refreshes every frame. NOTE: Valheim default for Player pin refresh is 2 seconds. Decreasing can reduce multiplayer performance.@

### G - Dynamic Types

- **Show Ships:** Show ships on the map and compass.@
- **Show Carts:** Show carts on the map and compass.@
- **Show Portals:** Show portals on the map and compass.@

### H - Dynamic Names

- **Show dynamic names on map:** Display boat and cart types (i.e., Raft, Karve, Longship) and Portal names on the large map.

### I - Dynamic Map Colors

- **Active portal color on map:** Color of portal icons with active connections.
- **Portal color:** Color of portal icons on map.
- **Ship color:** Color of ship icons on map.
- **Cart color:** Color of cart icons on map.
- **Use colors on compass:** Use colors for dynamic pins on the compass

### J - Visibility

- **Always Visible:** Always display pins of these types or names (comma separated, no spaces) at full size regardless of distance.@

### Z - Utility

- **LogLevel:** Controls the level of information contained in the log
- **Use External Images:** Compass and dynamic markers will use images located in the mod folder, which can be customized

Configuration items with descriptions ending with "@" are server authoritative.

### In-game reconfiguration

You can use Configuration Manager (or similar) mod to change the configuration without exiting the game. The configuration will reload if you make changes to the config file. 

### Credits

First and foremost, credit goes to **gdragon** for convincing me to pick up development of Immersive Compass, and for _extensive_ suggestions, testing and feedback. Without this help I would have only had half the functionality.

HUD Compass incorporates the excellent functionality of Immersive Compass by GuyDeYoYo (aka Fragnarok, with permission), which credits the original code to Aedenthorn. 

The dynamic markers extensively uses code from Automatic Map Markers - Ship & Cart from Schlangguru, who I made several attempts to contact for explicit permissions but the mod is not maintained.

I will remove this mod if either author objects. Use of the code is within the license requirements of the above mods and is included in the distribution.

### Notes

- With version 1.0.2 HUD Compass can now use external images for the compass and dynamic pins. You may customize or replace these images (at your own risk), but please remember to save a copy of your custom images as they will be overwritten when new versions are deployed.
    - Version 1.0.4 changed to use external images, however, mod managers were not installing images in a Resources sub-folder.
    - Version 1.0.5 has a configuration item **Use External Images** which is set disabled by default. You can turn on use of external images, which R2Modman will install in the same folder as the mod's .dll
- Player Pin Visibility (server controlled setting) affects player pin display on both the compass and the map.
- Show My Player Pin is synced with Visible to Other Players toggle on the map. They are the same.
- An _C. Ignore / Pin Names_ entry can include leading and trailing asterisks (\*)
    - Examples:
    - "Raspberry\*" will match "Raspberry" and "Raspberry xyz" 
    - "\*Raspberry" will match "Raspberry and "abc Raspberry"
    - "\*Raspberry\*" will match "Raspberry", "Raspberry xyz" and "abc Raspberry", but only if the start or end match the entire string 
    - "\*berry" will match "Raspberry", "Blueberry" and "Cloudberry" and anything else ending in "berry" including all berries prefixed with a count (e.g. "3 Raspberry")

**Note:** Wildcard matches can be FPS 'expensive'. Whenevery possible, try to create one that includes multiple pins (i.e. the '\*berry' example above)

### Compatibility issues & defects

- HUD Compass has been tested with OdinsShipsPlus, ValheimRAFT, CustomShips, and CraftyCarts.
- It should work with any mod that adds ship or carts using the standard Ship or Vagon components.
- 'Buildable' ships and carts will show the name of their base unit, e.g. Custom Ship, Raft Base.

- If you find a compatibility issue you can post it on NexusMods. Be sure to include the mod name and version you think may be incompatible.
- If you have a bug please report it on NexusMods. If you do post a bug report, please make sure to include the following:
    - Your version of this mod
    - What you were doing, or attempting to do when it happened
    - If it's repeatable - i.e., can you duplicate it?
    - The exact behavior you observed (or didn't observe)
    - If possible, post a capture of the log file with errors (errors always begin with this mod's name) on Discord


You can find all Neobotics released mods on: 
- Thunderstore: https://tinyurl.com/NeoboticsOnThunderstore 
- Nexus Mods: https://tinyurl.com/NeoboticsOnNexus

Your comments and feedback are always welcome. Post on NexusMods or Discord: https://tinyurl.com/NeoboticsOnDiscord
