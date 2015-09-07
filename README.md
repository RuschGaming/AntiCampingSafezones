Anti Camping Safezones By GR8
=============

Made to prevent campers shooting people going in and out of safezones. There is a timer to protect you from any harm and give you enough time to get to safety. People cannot follow others outside a safezone becuase they will not be able to shoot. This is highly configurable and still a WIP.

Installation
--------------------------

1. Download [`AntiCampingSafezones`](https://github.com/Gr8z/AntiCampingSafezones/archive/master.zip),
2. Move the `safezone` folder into your Mission PBO.
3. Open your `initPlayerLocal.sqf`.
4. add `[] execVM "safzones\config.sqf";` to the very top.
5. Open your `config.cpp`.
6. Look for `class CfgExileCustomCode`
7. Replace the whole block with this:

```
class CfgExileCustomCode 
{
	ExileClient_object_player_event_onEnterSafezone = "safezones\GG_object_player_event_onEnterSafezone.sqf";
	ExileClient_object_player_event_onLeaveSafezone = "safezones\GG_object_player_event_onLeaveSafezone.sqf";
};
```
* NOTE : If you have any **CfgExileCustomCode** Overrides already. Make sure to keep them with this code as well. 

EXTRA STEPS
--------------------------
* NOTE : You Don't need to follow these steps if you are using `LooseRespect = false;`. You must do the follow if you have `LooseRespect = true;`.

1. open `addons\exile_server_config\CfgSettings.hpp`.
2. Look for  `bambi = -500;`.
3. Add this below `safezone = -800;		// Safezone Campers by GR8`. This is the respect the camper will loose, change it to your liking.
4. copy `ExileServer_object_player_event_onMpKilled.sqf` from the download.
5. Replace it in `addons\exile_server\code`.

