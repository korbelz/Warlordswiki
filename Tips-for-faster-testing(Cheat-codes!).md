The following codes can be used in the debug console to greatly speed up your testing. 

To access the debug console when you are playing locally, Press esc key. 

to access the debug console on a server you'll need to type #login admin password in the chat box, then press esc.

Example: #login 1234

global execute works fine for both these commands.  

To swap between commands you've entered press the page down key.

## Cheat codes
This code will kill all the indy on the map. Code by Marii. 

{if ((side _x == Independent) and (alive _x)) Then {_x setDamage 1}} forEach (allUnits);

This code will give you max CP. Code by Gamerdad. 

player setVariable ["BIS_WL_funds", 50000];

use PGDN(page down key) to cycle between command in the debug console


## How to teleport

Shift+alt mouse click on map

## Gods eye view

when playing as an admin. Press esc then the spectator button. This lets you fly around and see all units on the map.

## I made a change to the AI spawn table. How do I see if its working?

example: you changed the value of Kumas on the weighted spawn table but need to see it in action. Go to the warlords_constants file change the value of AI vics per zone to something really high like 20. Using this trick in just about 5 towns you can simulate how common Kumas might be for about 20 towns of normal gameplay.

# Open Warlords
## Cheat codes for faster testing
[2,20000] call OWL_fnc_addFunds;

When playing on a dedicated server you'll need to change the 2 to 'clientOwner' variable since all CP is done server side. TIP: put clientOwner in watch list for quick look up. 

If you need to find an asset on the map from your asset list: player setPos getPos (OWL_playerAssets#0);

Code to kill all indys in a zone for quick capping: {if ((side _x == Independent) and (alive _x)) Then {_x setDamage 1}} forEach (allUnits);

If you need to capture many sectors for testing it can be faster to open the sector init field in the editor and change ownership

OWL_sectorParam_side

		Indicates who owns the sector at the start of the game

		0 - Unclaimed

		1 - Competing side 1 West

		2 - Competing side 2 EAST

		3 - Defending side Indy

