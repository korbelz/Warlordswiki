## Setting up object on the map 

To get started you need to place a Game Logic item. This can be found under Assets > Systems > Logic Entities. When you place this object it isn't quite center with where our runway will be ingame. 

Paste this code into the init field of your game logic
```
_dynamicAirport1 = "DynamicAirport_01_F" createVehicle position this;
_dynamicAirport1 setdir 61.5;
```

all done, now just run the mission and open the map to check the position of your newly placed airport logic for the AI. 

## Troubleshooting tips

the Dynamic airfield functions as an invisible aircraft carrier for AI to land if their aircraft is equipped with a tailhook. When placing the game logic it you'll need to take this into account. 

AI will land at the reciprocal heading + 8 degrees of the setdir heading in code. 
example: you need AI to land with a runway heading 230 degrees. (230 - 180) + 8 = 58 degrees for setdir

AI pilots seem to land short of the outline of runway on map

AI pilots/aircraft touchdown point can vary quite a bit. This is very noticeable when aircraft is damaged 

AI will approach the runway at a very shallow angle so you may need to place the hide terrain tool in the editor to clear a path for them.   

## background reading for airfields 

info on airfields
https://armadocs.gitlab.io/terrain/03project/3config/airstrips/

wiki info on how to config a dynamic airfield
https://community.bistudio.com/wiki/Arma_3:_Dynamic_Airport_Configuration 