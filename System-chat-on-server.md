# How to send a system chat message on server that includes variables

setup a variable that uses the format command to convert the variables you want to pass into a string. Then have remoteExec call the string you have created.

private _infotext = format ["Current mission is %1 server: %2 map: %3 ,  **Discord %4**", missionName, serverName, worldName, _serverdiscord];

[_infotext] remoteExec ["systemChat"];

2nd example:

[[format ["Current mission is %1 server: %2 map: %3 ,  **Discord %4**", missionName, serverName, worldName, _serverdiscord]]] remoteExec ["systemChat"];


below is how to send a formatted message straight to the RPT file

diag_log format ["Current mission is %1 on server %2", missionName, serverName];

## example code
https://github.com/korbelz/OWLKorb/blob/main/Server/sectorSpawnUnits.sqf#L9
