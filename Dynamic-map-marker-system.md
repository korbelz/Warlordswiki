## example of the Dynamic information map markers system, this system is designed to be used along with the "Choose your own Warlords" mode

### I place this code in the server init file, but you can place it anywhere that it will be run a single time

//dynamic map marker system


_markerone = createMarker ["markerone", [13998.892,14819.831,0]]; // Not visible yet.

_markerone setMarkerType "mil_marker"; // Visible.

_markerone setMarkerColor "ColorOrange";

_markerone setMarkerAlpha 0.30;

_markerone setMarkerText missionName; 



//add server discord to this list to have it auto populate

_serverdiscord = serverName; 

switch (_serverdiscord) do

{ 

	case "Open Warlords":

	{

    	_serverdiscord = "https://discord.gg/SBGrYUpvba"; 

	};

	case default 

	{

		_serverdiscord = "discord.gg/arma3";

	};


};


_markertwo = createMarker ["markertwo", [13991.464,14401.705,0]]; // Not visible yet.

_markertwo setMarkerType "mil_box"; // Visible.

_markertwo setMarkerColor "ColorOrange";

_markertwo setMarkerAlpha 0.30;

_markertwo setMarkerText _serverdiscord; 


_buglink = missionName; 

switch (_buglink) do

{ 

	case "OWLKorb":

	{

    	_buglink = "https://github.com/korbelz/OWLKorb/issues";
 
	};

	case "OWL":

	{

    	_buglink = "https://github.com/aaannnndd/OWL/issues"; 

	};

	case "WarlordsReduxMe":

	{

    	_buglink = "https://github.com/korbelz/WarlordsReduxMe.altis"; 

	};

	case "WarlordsReduxMav":

	{

    	_buglink = "https://github.com/korbelz/WarlordsReduxMav.altis/issues"; 

	};

	case default
 
	{

		_buglink = "discord.gg/arma3";

	};


};

_markerthree = createMarker ["markerthree", [13995.007,13756.69,0]]; // Not visible yet.

_markerthree  setMarkerType "mil_triangle"; // Visible.

_markerthree  setMarkerColor "ColorOrange";

_markerthree  setMarkerAlpha 0.30;

_markerthree  setMarkerText _buglink; 


## Link to use in a mission
https://github.com/korbelz/OWLKorb/blob/main/Server/initServer.sqf#L105