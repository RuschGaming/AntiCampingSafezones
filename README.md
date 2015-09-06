Anti Camping Safezones By GR8
=============

Made to prevent campers shooting people going in and out of safezones. There is a timer to protect your from any harm and give you enough time to get to safety. People cannot follow others outside a safezone becuase they will not be able to shoot. This is highly configurable and still a WIP.

Installation (per-machine)
--------------------------

1. Download [`AntiCampingSafezones`](https://github.com/Gr8z/AntiCampingSafezones/archive/master.zip),
2. Move the `safezone` folder into your Mission PBO.
3. Open your `initPlayerLocal.sqf`.
4. add `[] execVM "safzones\init.sqf";` to the very top.
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

8. Youre Done. 