# Onset_IA
This package is a new Advenced AI Sytem

## How to install
- Add the "Onset_IA" folder to your server packages 

- Edit your server_config.json and add "Onset_IA" in the packages section before the files who need it

```json
"packages": [
	"Onset_IA"
],
```
- On the files who needs to use the AI, initialize the Onset_IA package using this function  
```lua
local ia = ImportPackage("Onset_IA")
```
After that you should be able to use the built-in functions

## Function
```lua
CreateIa(x, y, z, h [,clothingId, target]) -- Create new AI and Return npc Id
CreatePoint(x,y,z, mode) -- Create new Force Mode point

SetIaTarget(npc, player) -- Set new Target
SetIaClothing(npc, clothingId) -- Set Clothing of AI
SetIaSpeed(npc, speed) -- Set AI Speed
SetIaMode(npc, mode) -- Set AI Mode

GetPlayerDist(player, npc) -- Return Distance between AI and Player
GetPlayerTarget(player) -- Return all AI who we Target Player
GetIaTarget(npc) -- Return Target of AI
GetIaMode(npc) -- Return Mode of AI

DestroyAllIa() -- Destroy All AI
DestroyIa(npc) -- Destroy specify AI
```

## AI Mode
```
AI change mode automatic witch condition but if you want to force change mode

Mode 0: AI follow player
Mode 1: Force IA pass through a specific point
Mode 2: takes the same route as the player until passing through a point of type 2
```

## Exemple
```lua
local ia = ImportPackage("Onset_IA") -- Import to your Server Script Onset_IA

local npc = ia.CreateIa(0, 0, 1700, 0) -- if you don't set target the script the script will find it

ia.SetIaClothing(npc, 12) -- Change clothing of AI
ia.SetIaSpeed(npc, 300) -- Change Speed of AI
ia.SetIaMode(npc, 0) -- Change mode of AI

local Target = ia.GetIaTarget(npc)

AddPlayerChat(Target, "Your are the target of AI n°"..npc)
```

## Discord
Join Origin [Discord](https://discord.gg/MDEwtKr) server now !

## License
This project is licensed under the [MIT](https://choosealicense.com/licenses/mit/) License
