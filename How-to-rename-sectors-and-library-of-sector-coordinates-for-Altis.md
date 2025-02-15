createLocation command

https://community.bistudio.com/wiki/createLocation

# Code and where to place it
Example: 

**_location = createLocation ["NameCity", [18803.1,22363.6,0], 30, 30];** 

**_location setText "Player town";**


I currently place these new sectors at the start of WL2_sectorsInitClient.sqf. Example can be found here:

https://github.com/korbelz/WarlordsReduxMe.altis/blob/main/Functions/client/WL2_sectorsInitClient.sqf

# Method 2

This method won't give you a "city" marker on the map but is quicker to setup.

in the init field of the game logic for the sector place this code: 
' this setVariable ["BIS_WL_name",  "Korbville"]; '


# Library of coordinates for most sectors on Altis:
[2949.7,11008,0] Fire base West

[4129.08,11740.4,0] Neri

[3364.63,12608.1,0] Kavala Pier

[3550.73,12984.9,0] Kavala

[3815.92,13717,0] Aggelochori

[4218.57,15079.4,0] Power Plant

[4891.72,16184.4,0] Negadas

[4620.37,21334.1,0] Oerokastro

[2706.72,22059.1,0] Bomos

[5070.54,11285.9,0] Panichori

[7132.91,11093.2,0] Edessa

[8275.26,10904,0] Sector #58(Korbville)

[9012.78,12019.1,0] Zaros

[12291.3,8906.51,0] Vikos(southern base)

[10666.5,12271.8,0] Therisa

[11505.5,11706.5,0] AAC Airfield

[13557.9,12161.3,0] AAC island

[14246.1,13011.1,0] Sagonisi

[11012.1,13397.8,0] Poliakko

[11740.9,13686.5,0] Katalaki

[11127.9,14560,0] Alikampos

[12484.6,14374,0] Neochori

[12942.4,15036.9,0] Stavros

[12370.3,15684,0] Lakka

[12748.1,16551.3,0] Lakka Hill(military)

[14293.3,16178.3,0] Altis main airbase

[15152.6,17281.1,0] Altis airbase north ramp

[15379,16064.5,0] Power plant

[16247.1,17108.6,0] Telos

[17860.2,18097.2,0] Kalithea

[18732.9,22386.4,0] Sector #72(Nuketown)

[14487,17638.2,0] Gravia

[13990.5,18727.1,0] Athira

[14611.6,20791.2,0] Frini

[12845.8,19647,0] Ifestiona

[11767.5,18322.1,0] Koroni

[10440.3,17245.3,0] Orino

[9322.28,15926.3,0] Agios Dionysios

[7391.81,15407.8,0] Topolia

[6173.99,16233.8,0] Kore factory

[7110.73,16447.3,0] Kore

[8629,18290.1,0] Syrta

[10320,19072.1,0] Galati

[9435.24,20244.3,0] Abdera

[9209.92,21571.7,0] NE airfield(Ammolofi Airbase)

[15619.2,4537.46,0] Sector #73(USS Deathstar)

[26956.5,24745.5,0] Molos Airfield

[26990.7,23199.7,0] Molos

[28036.1,23234.6,0] Northeast Fire base

[23877.3,23727.5,0] Sideras

[26719,21227.2,0] Gatolia

[25638.9,21364,0] Sofia

[25390.7,20325.2,0] power plant

[23936,20173.6,0] Delfinaki

[23573.5,21100.6,0] Military(Nidasos base)

[21836.5,21020.8,0] Iraklia(Ghost hotel)

[23219.8,19976.8,0] Ioannina

[23140.8,18678.6,0] Almyra(Salt Flats)

[20977.1,19248.7,0] Agios Georgios(Georgios Base)

[19239.2,17558,0] Agios Petros

[18812.4,16599.1,0] Rodopoli

[16656.4,16121,0] Anthrakia

[18110.6,15240.6,0] Charkia

[20967.4,16967.3,0] Paros

[21377.1,16358,0] Kalochori

[20668.3,15684.9,0] Limni(Neri Solar plant)

[19388.3,13243.2,0] Dorida

[17424.7,13169.4,0] Pygros(Pygros Military)

[16759.9,12671.1,0] Pygros

[14982.8,11156.8,0] Faronaki

[20229.2,11668.1,0] Chalkeia

[20424.4,8854.12,0] Panagia

[21672.6,7581.34,0] Feres

[20968.2,7349.95,0] Selakano(Selakano Airbase)

[20794,6734.49,0] Selakano


