# This is focused around the "Choose your own Warlords" mode setup. 


//

// server.cfg
//

// comments are written with "//" in front of them.

// NOTE: More parameters and details are available at http://community.bistudio.com/wiki/server.cfg

// GENERAL SETTINGS

hostname       = "Open Warlords";    // Name of the server displayed in the public server list

//password     = "1800dwarden";      // Password required to join the server (remove // at start of line to enable)

passwordAdmin  = "1800dwarden";       // Password to login as admin. Open the chat and type: #login password

serverCommandPassword = "1800dwarden";       // Password required by alternate syntax of [[serverCommand]] server-side scripting.

maxPlayers     = 10;    // Maximum amount of players, including headless clients. Anybody who joins the server is considered a player, regardless of their role or team.


// INGAME SETTINGS

persistent     = 1;     // If set to 1, missions will continue to run after all players have disconnected; required if you want to use the -autoInit 
startup parameter

disconnectTimeout = 90;     //  Server wait time before disconnecting client, default 90 seconds, range 5 to 90 seconds. (since Arma 3 update 1.56+) 
 

// VOICE CHAT

disableVoN       = 0;     // If set to 1, voice chat will be disabled

vonCodec = 1;     // If set to 1 then it uses IETF standard OPUS codec, if to 0 then it uses SPEEX codec (since Arma 3 update 1.58+) 
 
vonCodecQuality  = 10;    // Supports range 1-30; 1-10 is 8kHz (narrowband), 11-20 is 16kHz (wideband), 21-30 is 32kHz (ultrawideband); higher = better sound quality


// VOTING

voteMissionPlayers  = 1;       // Minimum number of players required before displaying the mission selection screen, if you have not already selected a mission in this config

voteThreshold       = 0.75;    // Percentage (0.00 to 1.00) of players needed to vote something into effect, for example an admin or a new mission. Set to 9999 to prevent random players being voted as admins.


allowedVoteCmds[] =

{

	{ "admin", true, true, 0.75 },					// 75% of players need to vote for the admin

	{ "missions",	true,	true, 0.75 },			// 75% players need to vote for #missions

	{ "mission",	true,	true },				// will use global {{hl|voteThreshold}}

	{ "kick",		true,	true, 0.75 },		// 

	{ "restart",	true,	true, 0.75 },			// 75% players need to vote to restart the server, this doesnt get a new mission

	{ "reassign",	false,	true, 0.75 },		// not available before mission start, I dont know what this command does

	{ "kick",		true,	true, 0.75, 0.75 }	// means kicked in case either 75% of all players

												// or 75% of players from his side (west, east, resistance, civilian) voted to kick him(2 out of 3 or 3 out of 4)

};


allowedVotedAdminCmds[] =

{

	{ "mission",	true, true },

	{ "missions",	true, true },   //voted in admin can basically only start a new mission vote

	{ "restart",	false, false }, //this is to prevent a solo player voting themselves admin then trolling the server non-stop with restarts

	{ "reassign",	false, false }, //i dont know this command does 

	{ "kick",		false, false }  //this is to prevent a solo player voting themselves admin then kicking each new player that joins

};



// WELCOME MESSAGE ("message of the day")

// It can be several lines, separated by comma

// Empty messages "" will not be displayed, but can be used to increase the delay before other messages

motd[] = 

{

    "Project in development. Press U for menu. ando#3526 if curious about project.",

	"Admins type #missions to load a new mission",

	"https://discord.gg/SBGrYUpvba"

};

motdInterval = 5;    // Number of seconds between each message


autoSelectMission = false;


// MISSIONS CYCLE

//class Missions {

//	class WarlordsCustom

//    {

//    	template = OWLKorb.Altis;

//		difficulty = "regular";

//    };

//};


class Missions {}; 


missionWhitelist[] = {

		OWLKorb.Altis,

		OWL.altis,

		Redux57.altis,

		WarlordsReduxMav.altis,

		WarlordsReduxMe.altis

		};


// LOGGING

timeStampFormat  = "short";                 // Timestamp format used in the server RPT logs. Possible values are "none" (default), "short", "full"

logFile          = "server_console.log";    // Server console output filename


class AdvancedOptions

{

    LogObjectNotFound = false;            // logging enabled

    ignoreMissionLoadErrors = true;    // do not ingore errors


};


// SECURITY

BattlEye          = 1;    // If set to 1, BattlEye Anti-Cheat will be enabled on the server (default: 1, recommended: 1)

verifySignatures  = 2;    // If set to 2, players with unknown or unsigned mods wont be allowed join (default: 0, recommended: 2)

kickDuplicate     = 1;    // If set to 1, players with an ID that is identical to another player will be kicked (recommended: 1)


// FILE EXTENSIONS

allowedLoadFileExtensions[] =       {"hpp","sqs","sqf","fsm","cpp","paa","txt","xml","inc","ext","sqm","ods","fxy","lip","csv","kb","bik","bikb","html","htm","biedi"}; // only allow files with those extensions to be loaded via loadFile command (since Arma 3 v1.19.124216) 

allowedPreprocessFileExtensions[] = {"hpp","sqs","sqf","fsm","cpp","paa","txt","xml","inc","ext","sqm","ods","fxy","lip","csv","kb","bik","bikb","html","htm","biedi"}; // only allow files with those extensions to be loaded via preprocessFile/preprocessFileLineNumber commands (since Arma 3 v1.19.124323)

allowedHTMLLoadExtensions[] =       {"htm","html","xml","txt"}; // only allow files with those extensions to be loaded via HTMLLoad command (since Arma 3 v1.27.126715)


// EVENT SCRIPTS (see http://community.bistudio.com/wiki/ArmA:_Server_Side_Scripting)

onUserConnected     = "";    // command to run when a player connects

onUserDisconnected  = "";    // command to run when a player disconnects

doubleIdDetected    = "";    // command to run if a player has the same ID as another player in the server


// SIGNATURE VERIFICATION

onUnsignedData      = "kick (_this select 0)";    // command to run if a player has unsigned files

onHackedData        = "kick (_this select 0)";    // command to run if a player has tampered files

onDifferentData = "";				// data with a valid signature, but different version than the one present on server detected

steamProtocolMaxDataSize = 4096;    //Limit for maximum Steam Query packet length. Increasing this value is dangerous as it can cause Arma 3 server to send UDP packets of a size larger than the MTU. This will cause UDP packets to be fragmented which is not supported by some older routers. But increasing this will fix the modlist length limit in Arma 3: Launcher.

// HEADLESS CLIENT

// headlessClients[]  = {};    // list of IP addresses allowed to connect using headless clients; example: {"127.0.0.1", "192.168.1.100"};

// localClient[]      = {};    // list of IP addresses to which are granted unlimited bandwidth; example: {"127.0.0.1", "192.168.1.100"};
