Navigate to this file: Functions/server/WL2_processClientRequest.sqf

useful links to help you: https://community.bistudio.com/wiki/Arma_3:_Vehicle_Loadouts , https://dev.arma3.com/post/oprep-vehicle-customization

Open up the editor < virtual arsenal. On the right hand menu select the aircraft you want a custom loadout for and place it in the editor. Then select the aircraft and pylon loadout menu(right click aircraft and select attributes at the bottom) . Set the pylons to the loadout you would like to add to warlords. 

Below are direction from the wiki. The top part of this wiki code is already in Warlords Redux: Miller Edition so you'll only need to worry about pasting in the new loadout you want. 

## Saving and restoring
Here's a demo on how to gather and store pylon loadouts in script form:

Open your text editor, and copy-paste the following:

[private](https://community.bistudio.com/wiki/private) _pylons [=](https://community.bistudio.com/wiki/a_=_b) /* paste your data here */;
[private](https://community.bistudio.com/wiki/private) _pylonPaths [=](https://community.bistudio.com/wiki/a_=_b) ([configProperties](https://community.bistudio.com/wiki/configProperties) [[configFile](https://community.bistudio.com/wiki/configFile) [>>](https://community.bistudio.com/wiki/config_greater_greater_name) "CfgVehicles" [>>](https://community.bistudio.com/wiki/config_greater_greater_name) [typeOf](https://community.bistudio.com/wiki/typeOf) _vehicle [>>](https://community.bistudio.com/wiki/config_greater_greater_name) "Components" [>>](https://community.bistudio.com/wiki/config_greater_greater_name) "TransportPylonsComponent" [>>](https://community.bistudio.com/wiki/config_greater_greater_name) "Pylons", "isClass _x"]) [apply](https://community.bistudio.com/wiki/apply) {[getArray](https://community.bistudio.com/wiki/getArray) ([_x](https://community.bistudio.com/wiki/Magic_Variables#x) [>>](https://community.bistudio.com/wiki/config_greater_greater_name) "turret")};
{ _vehicle [removeWeaponGlobal](https://community.bistudio.com/wiki/removeWeaponGlobal) [getText](https://community.bistudio.com/wiki/getText) ([configFile](https://community.bistudio.com/wiki/configFile) [>>](https://community.bistudio.com/wiki/config_greater_greater_name) "CfgMagazines" [>>](https://community.bistudio.com/wiki/config_greater_greater_name) [_x](https://community.bistudio.com/wiki/Magic_Variables#x) [>>](https://community.bistudio.com/wiki/config_greater_greater_name) "pylonWeapon") } [forEach](https://community.bistudio.com/wiki/forEach) [getPylonMagazines](https://community.bistudio.com/wiki/getPylonMagazines) _vehicle;
{ _vehicle [setPylonLoadout](https://community.bistudio.com/wiki/setPylonLoadout) [[_forEachIndex](https://community.bistudio.com/wiki/Magic_Variables#forEachIndex) [+](https://community.bistudio.com/wiki/+) 1, [_x](https://community.bistudio.com/wiki/Magic_Variables#x), [true](https://community.bistudio.com/wiki/true), _pylonPaths [select](https://community.bistudio.com/wiki/select) [_forEachIndex](https://community.bistudio.com/wiki/Magic_Variables#forEachIndex)] } [forEach](https://community.bistudio.com/wiki/forEach) _pylons;


Create a new scenario in the Eden editor, add your vehicle, adjust the pylon loadout, and set its "Object Init" to:
[copyToClipboard](https://community.bistudio.com/wiki/copyToClipboard) [str](https://community.bistudio.com/wiki/str) [getPylonMagazines](https://community.bistudio.com/wiki/getPylonMagazines) [this](https://community.bistudio.com/wiki/Magic_Variables#this_2)


Play scenario, wait until loaded, then pause the game and return to Eden.


Your pylon loadout is now in the clipboard; go back to your text editor, and paste the loadout in the _pylons variable.


The loadout code is ready; you must assign the target vehicle to the _vehicle variable before calling it. 


Note: if you try to manually put a weapon that the aircraft is not configured to carry it will error out. 

## example code: 
https://github.com/korbelz/WarlordsReduxMe.altis/blob/main/Functions/server/WL2_processClientRequest.sqf#L205