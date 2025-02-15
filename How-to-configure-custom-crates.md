This is a Warlords Redux: Miller Edition system

Navigate to this file: 
Functions/server/WL2_processClientRequest.sqf


at the very top of the file has a labeled area where you can add/remove items from each of the various crates. 


useful links to help you find class names of gear:
https://community.bistudio.com/wiki/Arma_3:_CfgWeapons_Weapons

Here is more information from the wiki on how it works:
https://community.bistudio.com/wiki/addItemCargoGlobal


## How to get current loadout
Here is how you can get your current loadout if you want to convert a current loadout quickly into a custom crate: 

if anyone good loadout and knows how to equip it in the editor you can put the following command in the debug console to get a print out of the entire loadout. 

 getUnitLoadout player; 
 

you can then click the print out, press ctrl+A then ctrl+c to copy the entire string of gear. 
or if print to the rpt file is easier for you this command will print your loadout to the log file.

 diag_log getUnitLoadout player; 

## example code: 
https://github.com/korbelz/WarlordsReduxMe.altis/blob/main/Functions/server/WL2_processClientRequest.sqf#L10