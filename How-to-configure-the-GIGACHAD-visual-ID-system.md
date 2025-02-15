# the Global Independent Ground/Air Camouflage in High A** Definition (GIGACHAD) visual identification system

Navigate to this file: Functions/server/WL2_processClientRequest.sqf

useful links to help you:https://dev.arma3.com/post/oprep-vehicle-customization

Open up the editor < virtual arsenal. On the right hand menu select the vehicle you want a custom look for and place it in the editor. Then select the vehicle and visual menu(right click aircraft and select at the bottom) . Set the look you would like to add to warlords. Press the EXPORT button on the bottom of the screen. 

Paste the new visual code into the processclientrequest file. visual code goes between the [   ] call BIS_fnc_initVehicle; section. 

Remember to set the class name and side you want the new visual look to work for.

## example code

//blue mora 
```
 if (_className == "I_APC_tracked_03_cannon_F" && side _sender == WEST) then {

 	if (KORB_VISUAL_ID_ACTIVE == 1) then {

 	    [

     	     _asset, ["EAF_01",1],
  
 	     ["showBags",1,"showBags2",1,"showCamonetHull",0,"showCamonetTurret",0,"showTools",1,"showSLATHull",1,"showSLATTurret",1]

 	     ] call BIS_fnc_initVehicle;

 };

 }; 
```

## Example code
https://github.com/korbelz/WarlordsReduxMe.altis/blob/main/Functions/server/WL2_processClientRequest.sqf#L572