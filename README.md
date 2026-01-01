# Attack-LOS-with-LOS-Fix
Creates a dynamic potential team waypoint on the map based on where your mouse cursor is pointing when you press the assigned keybind.

### Summary
This script was originally written by ilys a long time ago. It has been updated by me in 2025.
The purpose of this script is to create a dynamic potential team waypoint on the map based on where your mouse cursor is pointing. The script exposed a new keybind. If you press the keybind, then a waypoint will be created on the map where a) your mouse is pointing, and b) the mouse makes contact with the terrain, an object, or a distance limit (if you point into the sky).

This script is incredibly useful for quickly alerting your team about the location of a given enemy player, or just for cordinating something nearby.

This script was updated by me with the following modifications:
* The original script was confusingly written. The result of the code was that, if you're moving the mouse quickly enough, it would create two separate waypoints. The reason for this is that the script was calling sendLOSTarget() twice, once on keypress and once in the callback function. This second call was unnecessary, as the information from the first call was sufficient. As a result, this second call was simply removed.
* I also removed some redundent code. This has no impact on functionality, but repeating the same code irriates me.
