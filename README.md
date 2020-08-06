# rrrfffrrr's insurgency plugins(EOL)
#### Plugin list
* [Announcement](#Announcement)
* [Challenge](#Challenge)
* [AutoKick](#AutoKick)
* [RespawnBots](#RespawnBots)
* [CheckpointRespawn](#CheckpointRespawn)
* [Medic](#Medic)
* [SuicideBomber](#SuicideBomber)
* [Injury](#injury)
* [RSWD](#RSWD)  
* [FireSupport](#FireSupport)
* [CounterAttack](#CounterAttack)
* [RespawnBots2](#RespawnBots2)

#### Why?
[Jaredballou's plugins](https://github.com/jaredballou/insurgency-sourcemod) are don't work on my server.  
So i made this with some codes from jaredballou's.

## Announcement
Show a line that contain in [announcement.txt](announcement.txt).

#### Plugins
[announcement.smx](plugins/announcement.smx)

#### Sources
[announcement.sp](scripting/announcement.sp)

#### Cvars
```
"sm_announce_enabled"	"1"		// Enable announcement
"sm_announce_delay"		"45"	// Announcement delay
```

#### Cmds
```
"sm_announce_reload"	// Reload announce text
```

## Challenge
Show text when connect.  
I didn't change name to connect message because i'm too lazy.

#### Plugins
[Challenge.smx](plugins/Challenge.smx)

#### Sources
[Challenge.sp](scripting/Challenge.sp)

#### Cvars
```
"sm_challenge_enabled"	"0"		// Enable connect message
```

#### Cmds
```
"sm_challenge_reload"	// Reload connect message
```

## AutoKick
Kick everyone who connect.  
For maintenance.

#### Plugins
[AutoKick.smx](plugins/AutoKick.smx)

#### Sources
[AutoKick.sp](scripting/AutoKick.sp)

#### Cvars
```
"sm_autokick_enabled"	"0"		// Kick everyone who connect if it's true
```

## RespawnBots
Respawn bots which isn't alive.  
Optimized version of CheckpointRespawn.
Default cvars not correct.

#### Plugins
[RespawnBots.smx](plugins/RespawnBots.smx)

#### Sources
[RespawnBots.sp](scripting/RespawnBots.sp)

#### Dependencies
[insurgency.games.txt](gamedata/insurgency.games.txt)

#### Cvars
```
"sm_botrespawn_enabled"			"0"		// Enable respawn bots.
"sm_botrespawn_delay"			"1"		// Delay to respawn, 0 will disable respawn.
"sm_botrespawn_rp"				"5"		// Default respawn point. Bot num is (Alive bot number) + sm_botrespawn_rp + (Player number) * sm_botrespawn_rp_add
"sm_botrespawn_rp_add"			"5"		// How many respawn point increase per players
"sm_botrespawn_display"			"1"		// Enable display how many bots remain. (Include respawn number)
"sm_botrespawn_display_delay"	"1"		// Display delay
```

## CheckpointRespawn
Respawn bots which isn't alive.  
It's prototype so having problem with performance.  
Use RespawnBots instead.
Default cvars not correct.

#### Plugins
[CheckpointRespawn.smx](plugins/CheckpointRespawn.smx)

#### Sources
[CheckpointRespawn.sp](scripting/CheckpointRespawn.sp)

#### Dependencies
[insurgency.games.txt](gamedata/insurgency.games.txt)

#### Cvars
```
"sm_botrespawn_enabled"			"0"		// Enable respawn.
"sm_botrespawn_delay_ins"			"1"		// Delay to respawn bots, 0 will disable respawn.
"sm_botrespawn_rp_ins"				"5"		// Default respawn point. Bot num is (Alive bot number) + sm_botrespawn_rp + (Player number) * sm_botrespawn_rp_add
"sm_botrespawn_rp_add_ins"			"5"		// How many respawn point increase per players
"sm_botrespawn_delay_sec"			"1"		// Delay to respawn player, 0 will disable respawn.
"sm_botrespawn_rp_sec"				"5"		// Player respawn point.
"sm_botrespawn_display"			"1"		// Enable display how many respawn point remain. (0 = don't display, 1 = display teams, 2 = display all)
"sm_botrespawn_display_delay"	"1"		// Display delay
```

## Medic
Make it medic that can revive other player.

#### Plugins
[Medic.smx](plugins/Medic.smx)

#### Sources
[Medic.sp](scripting/Medic.sp)

#### Dependencies
[insurgency.games.txt](gamedata/insurgency.games.txt)

#### Cvars
```
"sm_medic_enabled"			"1"			// Enable medic.
"sm_medic_class"			"breacher"	// Class that is medic. (recon, rifleman, specialist, breacher, support, demolition, marksman, sniper, ...)
"sm_medic_delay"			"10"		// Delay to revive player. (sec)
"sm_medic_rp"				"8"			// Max revive number per object.
"sm_medic_distance"			"100"		// Max revive distance from dead position to medic.
"sm_medic_item"				"kabar"		// Revive item.
"sm_medic_score"			"50"		// Get score when revive.
```

## SuicideBomber
Make a bot suicidebomber.

#### Plugins
[SuicideBomber.smx](plugins/SuicideBomber.smx)

#### Sources
[SuicideBomber.sp](scripting/SuicideBomber.sp)

#### Cvars
```
"sm_suicide_enabled"			"1"				// Enable medic.
"sm_suicide_bomber"				"sharpshooter"	// A class that will be bomber. ("" is all bot is bomber... with "ins_bot_knives_only" "0" ... zombie...)
"sm_suicide_detonate_range"		"600"			// Max range to detonate. I recommend 125.
"sm_suicide_resist"				"20"			// Bomber health multiply. Default health is 2000...
"sm_suicide_delay"				"0.01"			// Wrong cvar... why i make this???? make sure this value is 1.
```

## Injury
Make injury effect.

#### Plugins
[injury.smx](plugins/injury.smx)

#### Sources
[injury.sp](scripting/injury.sp)

## RSWD
Reset supply token when die or spawn.

#### Plugins
[RSWD.smx](plugins/RSWD.smx)

#### Sources
[RSWD.sp](scripting/RSWD.sp)

## By the way...
Many plugins above this line should be fixed but i'm too lazy...

## FireSupport
Call artillery with command and weapon.

#### Plugins
[FireSupport.smx](plugins/FireSupport.smx)

#### Sources
[FireSupport.sp](scripting/FireSupport.sp)

#### Dependencies
[insurgency.games.txt](gamedata/insurgency.games.txt) 

#### Cvars
```
"sm_firesupport_spread"			"800.0"							"Max spread."
"sm_firesupport_shell_num"		"20.0"							"Shells to fire."
"sm_firesupport_delay"			"10.0"							"Min delay to first shell."
"sm_firesupport_delay_support"	"60.0"							"Min delay to next support."
"sm_firesupport_class"			"template_recon_security_coop"	"Set fire support specialist class."
"sm_firesupport_count"			"1"								"Count of available support per rounds(0 = disable)"
"sm_firesupport_enable_cmd"		"0"								"Player can call fire support using sm_firesupport_call."
"sm_firesupport_enable_weapon"	"1"								"Player can call fire support using weapon."
"sm_firesupport_weapon"			"p2a1"							"Weapon to call fire support."
```

#### Cmds
```
"sm_firesupport_call"    "Call fire support where you looking at."
"sm_firesupport_ad_call" "Call fire support without any restriction." ADMINCMD
```

## CounterAttack
!!! HAS BUG !!!
CustomCounterAttack: Give some functions to control custom counter attack.  
CATrigger: Use native and forward function from CustomCounterAttack to trigger custom counter attack.  
NOT FOR CONTROL DEFAULT COUNTER ATTACKS.  
CATrigger is an example to use `CustomCounterAttack.smx`.

#### Plugins
[CustomCounterAttack.smx](plugins/CustomCounterAttack.smx)  
[CATrigger.smx](plugins/CATrigger.smx)

#### Sources
[CustomCounterAttack.sp](scripting/CustomCounterAttack.sp)  
[CATrigger.sp](scripting/CATrigger.sp)  
[counterattack.inc](scripting/include/counterattack.inc)

#### Dependencies
[insurgency.games.txt](gamedata/insurgency.games.txt)  
CATrigger use CustomCounterAttack

#### Cvars
```
"sm_counterattack_persist_time"			"1"				// Restore last remain round time when custom counter attack finished.
"sm_catrigger_min"                  "6"       // Custom counter attack will be triggered in (100 / (1 + Max - Min)) %
"sm_catrigger_max"                  "10"
```

## RespawnBots2
This is remake version of RespawnBots.  
Bots will be respawn after some delay.  
And they will be respawn infinitly when counter attack. (If enabled)  
Plus, Bot will not be spawn where they can look player instantly. (If enabled)  
MUST RELOAD MAP AFTER LOAD/RELOAD THIS PLUGINS. (Or spawnzone will be broken for 1 round)

#### Plugins
[RespawnBots2.smx](plugins/RespawnBots2.smx)

#### Sources
[RespawnBots.sp](scripting/RespawnBots2.sp)

#### Dependencies
[insurgency.games.txt](gamedata/insurgency.games.txt)

#### Cvars
```
"sm_botrespawn_delay"				""1"	""How many seconds wait before spawn for insurgent, 0 is disable delay"

"sm_botrespawn_rp"					""5"	""Default bots count, 0 is infinity"
"sm_botrespawn_rp_add"				""5"	""Number of bots that each player (rp + players * rp_add)"

"sm_botrespawn_carp"				""5"	""Default bots count when counter attack"
"sm_botrespawn_carp_add"			""5"	""Number of bots that each player when counter attack (carp + players * carp_add)"
"sm_botrespawn_infinite_ca"			""1"	""Infinity spawn when counter attack"

"sm_botrespawn_display"				""1"	""Display respawn point(0 = don't display, 1 = display)"
"sm_botrespawn_display_delay"		""1"	""Display delay(sec)"

"sm_botrespawn_count_alive"			""1"	""Count only alive players when counter attack."

"sm_botrespawn_adjust"				""1"	""Adjust spawn location to where player can't see."
"sm_botrespawn_adjust_distance"		""100"	""Adjust spawn location when someone close enough (Include teams)"
```
