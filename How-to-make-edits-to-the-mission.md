For basic editing these 3 files will be the ones you will use. 

Requisition.inc file is the file to adjust what players can buy and the cost of each item

Warlords_constants.inc is the main adjustment file that has the mission specific settings

WL2_loadfactioncclasses file is the file to adjust the AI spawn tables for enemy towns

## How to make a edit locally

Follow the step in the how to download and run wiki page

Open up your text editor of choice. Examples: notepad, VScode, etc. 

Open up one of the above files. Remember they are in the my documents/arma 3 profile folder on your computer.

Change a setting in the file then save.

Open up the editor in arma 3 load the mission and play as MP to test the change you made.

## How to make edits on github

Better guidelines for making edits can be found here: https://github.com/korbelz/WarlordsReduxMe.altis/blob/main/CONTRIBUTING.md

Go to the project page you want to make an edit for.

"Fork" the repo so you have a working copy

"clone" the repo which is basically downloading it to your computer. Put the clone where you normally put your mission files

Make edits, test them in the editor(even better if you test on a server)

Upload your changes(push) to github. Using a desktop app like github desktop make this much more straight forward. 

Once the changes are on your "fork" you submit a pull request to the project you wanted to make a change for. 

Guides for github desktop: https://docs.github.com/en/desktop

## Requisition.inc 

this file is the file to adjust what players can buy and the cost of each item

typing // infront of an item will "remove" it from the buy list.

example: //class B_UGV_02_Demining_F	

The ID for all vanilla assets can be found here: 
https://community.bistudio.com/wiki/Arma_3:_CfgVehicles_WEST

requirements section can restrict the zone something will be able to spawn in. Added new zone settings can be done in the editor by clicking on the zone.

example: requirements[]={"H"}; 

"H" is the ID in zone setting for helipad

Current zone IDs in default Warlords: H = helipad, A = Airfield, W = Harbor

Current zone ID as of writing in Miller Edition: H = helipad, A = Airfield, W = Harbor, S = Sea/naval zone, F/E = Long Range Fire(Arty/MLRS), M = Mid range Fire, B = Bluefor Armor, G = Indy Armor, T = OPFOR Armor


offset. This is only needed for items spawned in the defense menu it makes sure the item doesn't land on the player and kill them.

example: offset[]={0, 6, 0}; First value is left/right, 2nd value in forward back, last value is up/down. So that example code spawns the item 6 meters in front of the player.  

Warlords Redux: Miller Edition example file: https://github.com/korbelz/WarlordsReduxMe.altis/blob/main/requisitions.inc

Open Warlords example file: https://github.com/korbelz/OWLKorb/blob/main/requisitions.hpp

Warlords 2(redux) example file: https://github.com/Gamer-Dad/warlordsredux.altis/blob/master-altis/requisitions.hpp

## Warlords_constants.inc 

this is the main adjustment file that has the mission specific settings.

Most of these settings I've documented in the file itself. I've also copy/pasted it to a page on this wiki.

Warlords Redux: Miller Edition example file: https://github.com/korbelz/WarlordsReduxMe.altis/blob/main/Functions/warlords_constants.inc

Open Warlords example file: https://github.com/korbelz/OWLKorb/blob/main/owl_constants.hpp

Warlords 2(redux) example: https://github.com/Gamer-Dad/warlordsredux.altis/blob/master-altis/Functions/warlords_constants.inc

## WL2_loadfactioncclasses 

this file is the file to adjust the AI spawn tables for enemy towns.

The numbers listed in this file are not a % chance of them spawning. Its a weighted table of possible items, think of it like buying lottery tickets. The item with more lottery tickets has a better chance of winning the lotto and getting picked to spawn in. Buying 100 lottery tickets will not guarantee that you win the lotto.(unless no one else buys a ticket) 

You can remove items from this list by type // in front of them. 

If you make a change and get an error in game. Check your commas, every item in the list needs a comma at the end EXCEPT the last item on the list. No comma after the last item on the list. 

Warlords Redux: Miller Edition example file: https://github.com/korbelz/WarlordsReduxMe.altis/blob/main/Functions/server/WL2_loadFactionClasses.sqf

Open Warlords example files: https://github.com/korbelz/OWLKorb/blob/main/Server/sectorSpawnUnits.sqf