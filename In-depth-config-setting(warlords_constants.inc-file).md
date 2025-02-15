This values are found in the warlords_constants.inc file which contains most of the values that can be edited quickly.

These values are from Warlords Redux: Miller edition 

### #define WL_RESPAWN_MARKERS_CNT 20

Unknown what this does

### #define WL_ZONE_RESTRICTION_KILL_TIMEOUT_INFANTRY 5

 Time before Inf will die when entering a No Go zone

### #define WL_ZONE_RESTRICTION_KILL_TIMEOUT_VEHICLES 15

 Time before Vehicles will die when entering a No Go zone

### #define WL_ZONE_RESTRICTION_KILL_TIMEOUT_AIRCRAFT 5

 Time before Aircraft will die when entering a No Go zone

### #define WL_MAX_SEIZING_HEIGHT 38 

 //this is AGL, default value 150, actual cap height = this/2-ish. 50 gives a cap height of 35?

### #define WL_TIMEOUT_MIN 0.055 

 //25, 55 = 20 FPS + 3 MS + 2ms(for slop) to safely run scripts at 20 fps.

### #define WL_TIMEOUT_SHORT 0.25

 Don't touch any of these Timeout commands

### #define WL_TIMEOUT_MEDIUM 0.5

### #define WL_TIMEOUT_STANDARD 1

### #define WL_TIMEOUT_LONG 5

### #define WL_TIMEOUT_MAX 30

### #define WL_CONNECTING_LINE_AXIS 20

Dont touch these connecting line commands

### #define WL_CONNECTING_LINE_ALPHA_MIN 0.2

### #define WL_CONNECTING_LINE_ALPHA_MAX 0.5

### #define WL_MAP_PULSE_FREQ 1

 no touch

### #define WL_MAP_PULSE_ICON_SIZE 1.5

 no touch

### #define WL_BASE_ICON_SIZE 1.5

 no touch

### #define WL_ANNOUNCER_PAUSE 0.5

 no touch

### #define WL_SECTOR_CAPTURE_REWARD_MULTIPLIER 30 //default value 10

  adjusts the CP reward when capping a town inside this script: WL2_changeSectorOwnership.sqf

 ex: a 10 cp value town will be 10 * 30 = 300 cp reward when it is capped.

 This only applies to green towns(i.e. not bluefor or OPFOR)

  
### #define WL_SECTOR_PAYOFF_PERIOD 75 

//default value 60

 How many seconds between "passive" CP payout for towns owned. 

 Increasing this value will decrease "afk" money that players get for doing nothing. 

 Making this value too high may cause gridlock mid-game if both teams rush mid and don't do any backcapping.

### #define WL_SPAWN_GRID_SIZE 60 

//default value 40

 No sure what this does, think it makes randomness of spawn when attacking towns bigger

### #define WL_PLAYER_ICON_RANGE 75

 in meters

### #define WL_BASE_DANGER_SPAWN_RANGE 200

 Haven't tested this 

### #define WL_ID_SELECTION_NONE 0

 dont touch the ID_SELECTION stuff

### #define WL_ID_SELECTION_VOTING 1

### #define WL_ID_SELECTION_VOTED 2

### #define WL_ID_SELECTION_FAST_TRAVEL 3

### #define WL_ID_SELECTION_ORDERING_NAVAL 4

### #define WL_ID_SELECTION_ORDERING_AIRCRAFT 5

### #define WL_ID_SELECTION_ORDERING_AIRDROP 6

### #define WL_ID_SELECTION_SCAN 7

### #define WL_ID_SELECTION_FAST_TRAVEL_CONTESTED 8

### #define WL_ID_SELECTION_DEPLOYING_DEFENCE 9

### #define WL_SEIZING_TIMEOUT_MIN 15

 Not fully tested

### #define WL_SEIZING_TIMEOUT_MAX 90

not fully tested 

### #define WL_FAST_TRAVEL_OFFSET 100

 not fully tested

### #define WL_FAST_TRAVEL_RANGE_AXIS 50

 not fully tested

### #define WL_FAST_TRAVEL_TEAM_RADIUS 200

 not fully tested

### #define WL_TARGET_RESET_ZONE_RESTRICTION_TOLERANCE 30

 not fully tested

### #define WL_SCAN_DURATION 30

 How long in seconds that the sector will work

### #define WL_MAP_FONT_SIZE 0.0375

### #define WL_SCENE_FONT_SIZE 0.03

### #define WL_ASSET_REMOVAL_SAFEZONE 0 //100

//default value 100

 Leave this number at 0

 Any number above 0 will basically turn off clean up script and cause bodies to stack up at spawn

### #define WL_RESPAWN_PROTECTION_DURATION 240

 in seconds, should be how long before you can be teamkilled at base

### #define WL_ASSET_PROTECTION_DURATION 240

 not fully tested

### #define WL_ASSET_SCENE_ICON_DURATION 90

 not fully tested

### #define WL_FRIENDLY_FIRE_RECORD_DURATION 1200

 how long in seconds that redux "watches" to see if you go over the FRIENDLY_FIRE_THRESHOLD

### #define WL_FRIENDLY_FIRE_THRESHOLD 3

 Number of friendly fire kills before you end up with black screen

### #define WL_FRIENDLY_FIRE_PENALTY 180

 I don't think this does much of anything

### #define WL_FRIENDLY_FIRE_PENALTY_MAX 600

 How long you will have a black screen for after killing friendlies

### #define WL_MAINTENANCE_RADIUS 50

 In meters, how close you need to be for repair/re-arm

### #define WL_MAINTENANCE_COOLDOWN_REPAIR 900 

//default value 300

 How long in seconds before you can repair again 

### #define WL_MAINTENANCE_COOLDOWN_REARM 900  
 
//default value 300

 How long in seconds before you can re-arm again

### #define WL_MAINTENANCE_COOLDOWN_REARM_Helicopter 600
 
//not in .57 

### #define WL_MAINTENANCE_COOLDOWN_REARM_Jets 1200 
 
//not in .57

### #define WL_MAINTENANCE_COOLDOWN_REARM_Artillery 1800 

//not in .57

### #define WL_LOSING_SECTOR_WARN_FREQ 30

 time in seconds for the warning

### #define WL_MUSIC_VOLUME 0.1

 ? not tested

### #define WL_GARRISON_GROUP_SIZE_MIN 4

 Value used in WL2_populate sector.sqf

// Adjust RD_GARRISON_SIZE_MOD in warlords_constants for more AI INF per town(I think)

// Adjust GROUP_SIZE_MIN up to help smaller sectors without turning telos in to 1 FPS hell

### #define WL_GARRISON_GROUP_SIZE_MAX 5

 Value used in WL2_populate sector.sqf

// Adjust RD_GARRISON_SIZE_MOD in warlords_constants for more AI INF per town(I think)

// Adjust GROUP_SIZE_MIN up to help smaller sectors without turning telos in to 1 FPS hell

### #define WL_ASSET_IRRELEVANT_RANGE 1000

 how far away players need to be for AI vics will blow up automatically

### #define WL_TARGET_RESET_VOTING_TIME 60

 time in seconds

### #define KORB_KILL_REWARD_MOD 4444 
 
//Original value 10,000

 This controls kill rewards

 Lower value = Higher rewards

### #define KORB_GARRISON_SIZE_MOD 3  
 
//Original value 2; adjust this to increase total INF spawning in an AI sector.

 Value used in WL2_populate sector.sqf

// Adjust KORB_GARRISON_SIZE_MOD in warlords_constants for more AI INF per town(I think)

// Adjust GROUP_SIZE_MIN up to help smaller sectors without turning telos in to 1 FPS hell

### #define KORB_MINECOUNT_DELETE_THRESHOLD 400 

//Original value 400; Total # of mines allowed on server anymore will be delete when any sector is capped

### #define KORB_UAVCOUNT_DELETE_THRESHOLD 24 

//Original value 50;

### #define KORB_VIC_MIN_HEIGHT -125
  
//default is roughly 135 AGL, -125 = roughly 10 meters. 0 = roughly 135 AGL

### #define KORB_VIC_RANDOM_HEIGHT 125 
 
//Bell curve model, 125 = avg of 75 height + Min Height value. Game deafults to roughly 135 AGL

### #define KORB_VIC_RANDOM_AI_SPAWNS 4

//Random number of AI vics that can spawn in a zone 0 to <value given>; default 4

### #define KORB_AIR_RANDOM_AI_SPAWNS 4  

//Random number of AI Air that can spawn in a zone 0 to <value given>; default 4


### #define KORB_NAVY_RANDOM_AI_SPAWNS 4  

//Random number of AI Navy that can spawn in a zone 0 to <value given>; default 4


### #define KORB_DIVER_RANDOM_AI_SPAWNS 4  

//Random number of AI Divers that can spawn in a zone 0 to <value given>; default 4


### #define KORB_TEAM_BALANCE_SPLIT 3  

//Number of player split between teams before CP bonus payouts to lesser team; default 3


### #define KORB_BASE_VALUE_ADJUSTMENT 10000  

//default 10,000; Lower number equals more CP value for a sector; see also WL_SECTOR_CAPTURE_REWARD_MULTIPLIER


### #define KORB_AIR_RADAR_ACTIVE 1  

//default 1; 1 = radar off, datalink only; 2 = radar active + datalink


### #define KORB_JET_IR_ACTIVE 1  

//default 1; 1 = IR off; 2 = IR active


### #define KORB_HELI_IR_ACTIVE 1  

//default 1; 1 = IR off; 2 = IR active


### #define KORB_TANK_IR_ACTIVE 1  

//default 1; 1 = IR off; 2 = IR active


### #define KORB_INDY_BOATS_ACTIVE 1  

//default 1; 1 = INDY boats will spawn; 2 = Indy boats will not spawn


### #define KORB_INDY_DIVERS_ACTIVE 1  

//default 1; 1 = INDY Divers will spawn; 2 = Indy Divers will not spawn

#define KORB_CUSTOM_SECTOR_NAMES 1

//default 1; 1 = Sectors will have custom names; 2 = Sectors will have no custom names


#define KORB_DISABLE_TEAM_SWITCHING 1  

//default 1; 1 = Team switching disabled; 2 = Team switching enabled


### #define KORB_EAST_WEST_TANKAIR_DEFENDERS 1  

//default 1; 1 = Tanks and aircraft will spawn at Bluefor/OPFOR zones; 2 = Tanks and aircraft will NOT spawn at Bluefor/OPFOR zones


### #define KORB_HIGH_LOW_PLAYER_COUNT 60  

//default 60; This is the number of players at which the dynamic AI buddy system swaps from high AI count to low AI count.


### #define KORB_LOW_AI_BUDDY_COUNT 1  

//default 1; number of friendly AI player can have during high player count


### #define KORB_HIGH_AI_BUDDY_COUNT 2  

//default 2; number of friendly AI player can have during low player count


### #define KORB_TRANSITION_ALT 4000  

//default 4000; AGL altitude. Aircraft above this height will not be effected by zone restrictions around sectors


### #define KORB_BONUS_LOADOUT_ACTIVE 1  

//default 1; 1 = Bonus loadouts on; 2 = No bonus loadouts


### #define KORB_VISUAL_ID_ACTIVE 1  

//default 1; 1 = GIGACHAD visual ID system on; 2 = No GIGACHAD visual ID system


### # #define KORB_REMOVE_DATALINK_ACTIVE 1  

//default 1; 1 = Removed Datalink; 2 = Datalinks work normally
