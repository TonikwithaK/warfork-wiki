---
title: Gametype Scripting
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Gametype_Scripting
aliases:
- Gametype_Scripting
---

Eternally incorrect and incomplete. Please refer to the [warfork source](https://github.com/TeamForbiddenLLC/warfork-qfusion) whenever possible.

## Utility Types

### Vec3

#### Constructors

| Constructor | Description |
|----|----|
| Vec3() | Initializes x,y,z to zero. |
| Vec3(float v) | Initializes x,y,z to v. |
| Vec3(float x, float y, float z) | Initializes x,y,z with the given values for each. |
| Vec3(Vec3) | Copy constructor. Initializes x,y,z to the values on the supplied Vec3. |

#### Properties

| Property | Description                    | R/W |
|----------|--------------------------------|-----|
| float x  | The x component of the vector. | RW  |
| float y  | The y component of the vector. | RW  |
| float z  | The z component of the vector. | RW  |

#### Methods

| Method | Description |
|----|----|
| void set(float x, float y, float z) | Sets the x,y,z components on the vector to the supplied values. |
| float length() | Returns the magnitude of the vector. |
| float normalize() | Normalizes the vector and returns the magnitude pre-normalization. |
| float distance(Vec3) | Returns the distance between the tips of this vector and the supplied vector. |
| void angleVectors(Vec3 forward, Vec3 right, Vec3 up) | Sets the provided vectors as rotations about the forward, right, and up axes (?) |
| Vec3 toAngles() | Returns a vector representing the current vector as a rotation. |
| Vec3 perpendicular() | Returns the vector perpendicular to this vector. |
| void makeNormalVectors(Vec3 right, Vec3 up) | Returns the normal and binormal vector of the current vector (assumed to be the tangent/forward). |

#### Operators

| Operator | Description                                                  |
|----------|--------------------------------------------------------------|
| \+ Vec3  | Vector addition                                              |
| \- Vec3  | Vector subtraction                                           |
| \* Vec3  | [Dot product](https://en.wikipedia.org/wiki/Dot_product)     |
| ^ Vec3   | [Cross product](https://en.wikipedia.org/wiki/Cross_product) |
| \* int   | Scalar multiplication                                        |
| \* float | Scalar multiplication                                        |

oh yeah and the assign versions work too

### String

### Array

### Dictionary

### Time

## Game Types

### Trace

### Match

### Gametype

### Team

#### Constructors

Not constructable.

#### Properties

| Property | Description | R/W |
|----|----|----|
| Stats stats | Cumulative team stats | RW |
| int numPlayers | The number of players on the team (wow) | R |
| int ping | Average ping | R |
| bool hasCoach | Is any player on the team a coach | R |
| String@ name | The display name of the team | RW |
| String@ defaultName | The default name (SPECTATOR, PLAYERS, FORBIDDEN, ICY) | R |

#### Methods

| Method | Description |
|----|----|
| Entity@ ent(int n) | Returns the entity of the n-th player on the team |
| bool isLocked() | Returns the locked state of the team, which controls whether players can join |
| bool lock() | Locks the team, preventing players from joining. Returns true if the team was previously unlocked |
| bool unlock() | Unlocks the team, allowing players to join. Returns true if the team was previously locked |
| void clearInvites() | ?????? |
| int team() | Returns the enum value of the team, see below |

#### Enums

##### Team Enum

| Enum Value     | Description                              |
|----------------|------------------------------------------|
| TEAM_SPECTATOR | Spectators team                          |
| TEAM_PLAYERS   | Players team, used in non-team gametypes |
| TEAM_ALPHA     | Forbidden                                |
| TEAM_BETA      | Icy                                      |

### Stats

#### Constructors

Not constructable.

#### Properties

| Property | Description | R/W |
|----|----|----|
| int score | The current score of this player/team | R |
| int deaths | The number of deaths, including deaths by suicide | R |
| int frags | The number of frags, including teamfrags | R |
| int suicides | The number of deaths by suicide | R |
| int teamFrags | The number of frags on teammates | R |
| int awards | The total number of awards recieved by this player/team | R |
| int totalDamageGiven | The total amount of damage given to others, including damage given to teammates | R |
| int totalDamageRecieved | The total amount of damage recieved from others, including damage recieved from teammates | R |
| int totalTeamDamageGiven | The total amount of damage given to teammates | R |
| int totalTeamDamageRecieved | The total amount of damage recieved from teammates | R |
| int healthTaken | The total amount of health recieved from pickups | R |
| int armorTaken | The total amount of armor recieved from pickups | R |
| int numrounds | The number of rounds played | R |
| int ga_taken | The number of green armor pickups | R |
| int ya_taken | The number of yellow armor pickups | R |
| int ra_taken | The number of red armor pickups | R |
| int mh_taken | The number of mega health pickups | R |
| int uh_taken | The number of ultra health pickups | R |
| int quad_taken | The number of quad damage pickups | R |
| int shells_taken | The number of warshell pickups | R |
| int regens_taken | The number of regen pickups | R |
| int bombs_planted | The number of bombs planted | R |
| int bombs_defused | The number of bombs defused | R |
| int flags_capped | The number of successful flag captures | R |
| int fairplay_count | The number of fair play awards | R |
| bool had_playtime | Did the player play during this round? | R |

#### Methods

| Method | Description |
|----|----|
| void setScore(int newscore) | Sets the score on this Stats object to newscore |
| void addScore(int score) | Adds to the current score |
| void addRound() | Increments round counter |
| void clear() | Resets all stats |
| int accuracyShots(int ammo) | Returns the number of shots fired of a given ammo tag |
| int accuracyHits(int ammo) | Returns the number of shots hit with a given ammo |
| int accuracyHitsDirect(int ammo) | Returns the number of direct hits with a given ammo (no RL splash, etc.) |
| int accuracyHitsAir(int ammo) | Returns the number of shots hit on aerial targets with a given ammo |
| int accuracyDamage(int ammo) | Returns the amount of damage dealt with the given ammo |

### Bot

#### Constructors

Not constructable.

#### Properties

| Parameter | Description | R/W |
|----|----|----|
| float reactionTime | The reaction time associated with this bot's personality | R |
| float offensiveness | The offensiveness associated with this bot's personality | R |
| float campiness | The campiness associated with this bot's personality | R |
| float firerate | The firerate associated with this bot's personality | R |

#### Methods

| Method | Description |
|----|----|
| void clearGoalWeights() | ?????? |
| void resetGoalWeights() | ?????? |
| void setGoalWeight(int i, float weight) | ?????? |
| float getItemWeight(Item @item) | Get the affinity the bot has for the given weapon |

### Client

#### Constructors

Not constructable.

#### Properties

| Property | Description | R/W |
|----|----|----|
| Stats stats | Stats object for this client | RW |
| bool connecting | Is this client connecting to the server? | R |
| bool multiview | ?????? | R |
| bool tv | Is viewing on tv | R |
| int team | Team number | RW |
| int hand | Client's hand in use | R |
| bool isOperator | Is client an oper | R |
| int queueTimeStamp | Timestamp (ms) of when the client joined challengers queue | R |
| int muted | & 1 = chat disabled, & 2 = vsay disabled | R |
| float armor | Client's armor amount | RW |
| bool chaseActive | Is Client spectating | R |
| int chaseTarget | Number of player entity that client is spectating | RW |
| bool chaseTeamonly | Is spectating locked to client's teammates | RW |
| int chaseFollowMode | 0 = freefly, 1 = ineyes (first person), 2 = thirdperson | RW |
| bool coach | Is client a coach (??) | R |
| int ping | Latency in ms | R |
| int16 weapon | Equipped weapon? | R |
| int16 pendingWeapon | Weapon to switch to after cooldown | R |
| bool takeStun | player is stunned, possibly unused | RW |
| uint lastActivity | Timestamp (ms) of last interaction | R |
| uint uCmdTimeStamp | Timestamp (ms) of last command received from client | R |
| int playerNum | Internal ID (entity number - 1) | R |
| String@ name | Client's display name | R |
| String@ clanName | Client's clan name | R |
| uint pmoveFeatures | Bitmask describing player move features, see below | RW |
| float pmoveMaxSpeed | Client's walking speed | RW |
| float pmoveJumpSpeed | Client's jumping speed | RW |
| float pmoveDashSpeed | Client's dash speed | RW |
| uint pressedKeys | Bitmask describing currently pressed keys, format ??? | R |
| bool chaseActive | ?????? | RW |

#### Methods

| Method | Description |
|----|----|
| bool isReady() | Returns the ready state of this client, as in F4 |
| bool isBot() | Returns the human status of the client |
| Bot@ getBot() | If this client is a bot, returns the corresponding Bot object |
| int state() | Returns the client state, as a client state enum. See below |
| void respawn(bool ghost) | Respawn this client, optionally as a ghost 👻👻👻 |
| void clearPlayerStateEvents() | ?????? todo wtf are player state events |
| String@ getMMLogin() | Returns the value of cl_mm_login for this client |
| Entity@ getEnt() | Returns the corresponding Entity object for this client |
| int inventoryCount(int tag) | Returns the amount of the given item (addressed by tag, see Item) in this client's inventory |
| void inventorySetCount(int tag, int count) | Sets the amount of the given item (addressed by tag) in this client's inventory |
| void inventoryGiveItem(int tag, int count) | Adds the amount of the given item (addressed by tag) in this client's inventory |
| void inventoryGiveItem(int tag) | Add default quantity of the given item (addressed by tag) to this client |
| void inventoryClear() | Delete all items from the client's inventory |
| bool canSelectWeapon(int tag) | Returns whether the given weapon (addressed by tag) may be switched to, as determined by ammo |
| void selectWeapon(int tag) | Make the client switch to the given weapon (addressed by tag) |
| void addAward(String award) | Adds the specified award and displays it |
| void addMetaAward(String award) | Evil hacker awards, not displayed, only sent to matchmaker |
| void execGameCommand(String command) | Sends the given server command to this client |
| void setHUDStat(int stat, int value) | ;-; |
| int getHUDStat(int stat) | ;-; |
| String@ getUserInfoKey(String) | Returns the value associated with the given key in userinfo |
| void printMessage(String) | Sends the user a chat message with the given text |
| void chaseCam(String@ name, bool teamOnly) | Makes the client follow the teammate with the given name (or none at all to reset), and optionally locks spectating to teammates |
| void newRaceRun(int numSectors) | ?????? racemod stuff is hard :p |
| void setRaceTime(int sector, uint time) | ?????? racemod stuff is hard :p |
| void setHelpMessage(uint msg) | sets the specified mapmsg to display? |
| void setQuickMenuItems(String) | Set voice com quick commands |

#### Enums

##### Client State

should be called connection state LOL

| Enum Value | Description |
|----|----|
| CS_FREE | This connection can be reused/is inactive |
| CS_ZOMBIE | The client associated with this connection recently disconnected, don't reuse yet |
| CS_CONNECTING | This client is waiting for configstrings |
| CS_CONNECTED | A client object has been created, but is not in game yet |
| CS_SPAWNED | The client is in game |

### Cvar

#### Constructors

| Constructor | Description |
|----|----|
| Cvar(String name, String value, uint flags) | Creates the cvar "name" if it does not exist, with the given value and flags. If the cvar exists, the value is unused, and the supplied flags are set if they are not already set on the cvar. |
| Cvar(Cvar) | Copy constructor. |

#### Properties

| Property | Description | R/W |
|----|----|----|
| bool modified | Set each time the cvar is changed | RW |
| bool boolean | The value of the cvar as a bool | R |
| int integer | The value of the cvar as an int | R |
| float value | The value of the cvar as a float | R |
| String@ name | The name of cvar | R |
| String@ string | The value of the cvar as a string | R |
| String@ defaultString | The default value of the cvar | R |
| String@ latchedString | If the cvar has CVAR_LATCH or a variant, the value after a map/video restart | R |

#### Methods

| Method | Description |
|----|----|
| void reset() | Resets the value of the cvar to its default value. |
| void set(String &value) | Sets the value of the cvar to the supplied string. |
| void set(float value) | Sets the value of the cvar to the supplied float. |
| void set(int value) | Sets the value of the cvar to the supplied integer. Note: cast to float internally |
| void set(double value) | Sets the value of the cvar to the supplied double. Note: cast to float internally |

#### Enums

##### Cvar flag

| Enum Value | Description |
|----|----|
| CVAR_ARCHIVE | Saved to config |
| CVAR_USERINFO | Added to userinfo when changed |
| CVAR_SERVERINFO | Added to serverinfo when changed |
| CVAR_NOSET | Only settable from command line |
| CVAR_LATCH | Save changes until a map restart |
| CVAR_LATCH_VIDEO | Save changes until a video restart |
| CVAR_LATCH_AUDIO | Save changes until a sound restart |
| CVAR_CHEAT | Reset to default unless cheats are enabled |
| CVAR_READONLY | not user-changeable |
| \[Not present in angelscript\] CVAR_DEVELOPER | only visible/changeable in dev builds |

### Entity

#### Constructors

Not constructable. New instances can be spawned, see@ G_SpawnEntity.

#### Properties

| Property | Description | R/W |
|----|----|----|
| Client@ client | The associated client (nullable) | RW |
| Item@ item | ?????? (for bonus items) | RW |
| Entity@ groundEntity | ?????? | RW |
| Entity@ owner | ?????? | RW |
| Entity@ enemy | ?????? | RW |
| Entity@ activator | ?????? | RW |
| int type | Entity type enum (see below) | RW |
| int modelindex | ?????? | RW |
| int modelindex2 | ?????? | RW |
| int frame | Frame of animation OR ET_SPRITE radius, ... | RW |
| int ownerNum | ?????? | RW |
| int counterNum | ?????? | RW |
| int skinNum | ?????? | RW |
| int colorRGBA | ?????? | RW |
| int weapon | ?????? | RW |
| bool teleported | ?????? | RW |
| uint effects | ?????? | RW |
| int sound | ?????? | RW |
| int team | ?????? | RW |
| int light | ?????? | RW |
| bool inuse | ?????? | R |
| uint svflags | ?????? | RW |
| int solid | ?????? | RW |
| int clipMask | ?????? | RW |
| int spawnFlags | ?????? | RW |
| int style | ?????? | RW |
| int moveType | ?????? | RW |
| uint nextThink | ?????? | RW |
| float health | ?????? | RW |
| int maxHealth | ?????? | RW |
| int viewHeight | ?????? | RW |
| int takeDamage | ?????? | RW |
| int damage | ?????? | RW |
| int projectileMaxDamage | ?????? | RW |
| int projectileMinDamage | ?????? | RW |
| int projectileMaxKnockback | ?????? | RW |
| int projectileMinKnockback | ?????? | RW |
| float projectileSplashRadius | ?????? | RW |
| int count | ?????? | RW |
| float wait | ?????? | RW |
| float delay | ?????? | RW |
| float random | ?????? | RW |
| int waterLevel | ?????? | RW |
| float attenuation | ?????? | RW |
| int mass | ?????? | RW |
| uint timeStamp | ?????? | RW |
| entThink@ think | Think callback | RW |
| entTouch@ touch | Touch callback | RW |
| entUse@ use | Use callback | RW |
| entPain@ pain | Pain callback | RW |
| entDie@ die | Die callback | RW |
| entStop@ stop | Stop callback | RW |
| Vec3 velocity | The velocity vector of the entity | RW |
| Vec3 avelocity | The angular velocity vector of the entity | RW |
| Vec3 origin | Position vector | RW |
| Vec3 origin2 | Position vector (but different than origin) | RW |
| Vec3 angles | The direction the entity is facing | RW |
| Vec3 movedir | Movement vector (separate from current velocity) | RW |
| int entNum | ?????? | R |
| int playerNum | ?????? | R |
| String@ model | ?????? | R |
| String@ model2 | ?????? | R |
| String@ classname | Name of the entity | RW |
| String@ targetname | ?????? | RW |
| String@ target | ?????? | RW |
| String@ map | ?????? | RW |
| int particlesSpeed | ?????? only used on ET_PARTICLES entities | RW |
| int particlesShaderIndex | ?????? only used on ET_PARTICLES entities | RW |
| int particlesSpread | ?????? only used on ET_PARTICLES entities | RW |
| int particlesSize | ?????? only used on ET_PARTICLES entities | RW |
| int particlesTime | ?????? only used on ET_PARTICLES entities | RW |
| int particlesFrequency | ?????? only used on ET_PARTICLES entities | RW |
| bool particlesSpherical | ?????? only used on ET_PARTICLES entities | RW |
| bool particlesBounce | ?????? only used on ET_PARTICLES entities | RW |
| bool particlesGravity | ?????? only used on ET_PARTICLES entities | RW |
| bool particlesExpandEffect | ?????? only used on ET_PARTICLES entities | RW |
| bool particlesShrinkEffect | ?????? only used on ET_PARTICLES entities | RW |

#### Methods

#### Enums

##### Entity Type

| Enum Value           | Description                                  |
|----------------------|----------------------------------------------|
| ET_GENERIC           | Generic entity?                              |
| ET_PLAYER            | Player entity                                |
| ET_CORPSE            | Corpse entity                                |
| ET_BEAM              | Map beams                                    |
| ET_PORTALSURFACE     | Portal surface, used for misc_portal_surface |
| ET_PUSH_TRIGGER      | Push trigger entity, another weird map thing |
| ET_GIB               | Gib entity that leaves a trail               |
| ET_BLASTER           | Gunblade projectile?                         |
| ET_ELECTRO_WEAK      | EB projectile                                |
| ET_ROCKET            | Rocket projectile                            |
| ET_GRENADE           | Grenade projectile                           |
| ET_PLASMA            | Plasma gun projectile                        |
| ET_SPRITE            | 2d Sprite entity                             |
| ET_ITEM              | Item entity, like those created by SpawnItem |
| ET_LASERBEAM         | Lasergun projectile?                         |
| ET_CURVELASERBEAM    | Weak laser beam, unused                      |
| ET_FLAG_BASE         | ??? used for the flag base in CTF            |
| ET_MINIMAP_ICON      | HUD Minimap                                  |
| ET_DECAL             | Decal sprites                                |
| ET_ITEM_TIMER        | ??? (for specs only)                         |
| ET_PARTICLES         | misc_particles                               |
| ET_SPAWN_INDICATOR   | Shows spawn locations                        |
| ET_VIDEO_SPEAKER     | misc_video_speaker                           |
| ET_RADAR             | ET_SPRITE minus the depth test               |
| ET_EVENT \[96\]      | Used for effects, last 1 frame               |
| ET_SOUNDEVENT \[97\] | Used for effects, last 1 frame               |

#### Callbacks

| Callback signature | Description |
|----|----|
| void entThink(Entity@ ent) | Think function. Called every frame(?) |
| void entTouch(Entity@ ent, Entity@ other, Vec3 planeNormal, int surfFlags) | Called when the entity touches another entity. planeNormal, surfFlags ??? |
| void entUse(Entity@ ent, Entity@ other, Entity@ activator) | ?????? |
| void entPain(Entity@ ent, Entity@ other, float kick, float damage) | Called when the entity is damaged by another entity. kick ????? |
| void entDie(Entity@ ent, Entity@ inflicter, Entity@ attacker) | Called on entity death. inflictor, attacker ?????? |
| void entStop(Entity@ ent) | ?????? |

### Item

Weapons & weapon, ammo, armor, health, powerup pickups

#### Constructors

Not constructable.

#### Properties

| Property            | Description                         | R/W |
|---------------------|-------------------------------------|-----|
| int tag             | More specific type, see enums       | R   |
| uint type           | Category, see relevant enum         | R   |
| int flags           | Item flags, see relevant enum       | R   |
| int quantity        | Pickup amount                       | R   |
| int inventoryMax    | Max amount that can be carried      | R   |
| int ammoTag         | Ammo type, see relevant enum        | R   |
| int weakAmmoTag     | Ammo type                           | R   |
| String@ classname   | Linked to map entity name?          | R   |
| String@ name        | Printed on pickup                   | R   |
| String@ shortName   | Name used for printing in messages  | R   |
| String@ model       | worldmodel                          | R   |
| String@ model2      | worldmodel                          | R   |
| String@ icon        | Icon displayed in HUD?              | R   |
| String@ simpleIcon  | Image used in simpleitems mode      | R   |
| String@ pickupSound | Sound played on pickup              | R   |
| String@ colorToken  | Color used for printing in messages | R   |

#### Methods

| Method            | Description                            |
|-------------------|----------------------------------------|
| bool isPickable() | Returns the state of the pickable flag |
| bool isUsable()   | Returns the state of the usable flag   |
| bool isDropable() | Returns the state of the dropable flag |

#### Enums

##### Weapon Tag

| Name                 | Description          |
|----------------------|----------------------|
| WEAP_NONE            | No weapon            |
| WEAP_GUNBLADE        | The gunblade         |
| WEAP_MACHINEGUN      | The machinegun       |
| WEAP_RIOTGUN         | The riotgun          |
| WEAP_GRENADELAUNCHER | The grenade launcher |
| WEAP_ROCKETLAUNCHER  | The rocket launcher  |
| WEAP_PLASMAGUN       | The plasmagun        |
| WEAP_LASERGUN        | The lasergun         |
| WEAP_ELECTROBOLT     | The electrobolt      |
| WEAP_INSTAGUN        | The instagun         |

##### Ammo Tag

| Name                         | Description           |
|------------------------------|-----------------------|
| AMMO_NONE                    | No ammo               |
| AMMO_GUNBLADE \[WEAP_TOTAL\] | Gunblade ammo         |
| AMMO_BULLETS                 | Machinegun ammo       |
| AMMO_SHELLS                  | Riotgun ammo          |
| AMMO_GRENADES                | Grenade Launcher ammo |
| AMMO_ROCKETS                 | Rocket Launcher ammo  |
| AMMO_PLASMA                  | Plasmagun ammo        |
| AMMO_LASER                   | Lasergun ammo         |
| AMMO_BOLTS                   | Electrobolt ammo      |
| AMMO_INSTAS                  | Instagun ammo         |
| AMMO_WEAK_GUNBLADE           | Unused in Warfork.    |
| AMMO_WEAK_BULLETS            | Unused in Warfork.    |
| AMMO_WEAK_SHELLS             | Unused in Warfork.    |
| AMMO_WEAK_GRENADES           | Unused in Warfork.    |
| AMMO_WEAK_ROCKETS            | Unused in Warfork.    |
| AMMO_WEAK_PLASMA             | Unused in Warfork.    |
| AMMO_WEAK_LASER              | Unused in Warfork.    |
| AMMO_WEAK_BOLTS              | Unused in Warfork.    |
| AMMO_WEAK_INSTAS             | Unused in Warfork.    |
|                              |                       |

##### Armor Tag

| Name                    | Description                 |
|-------------------------|-----------------------------|
| ARMOR_NONE \[0\]        | No armor                    |
| ARMOR_GA \[AMMO_TOTAL\] | Green armor, +50 up to 100  |
| ARMOR_YA                | Yellow armor, +75 up to 125 |
| ARMOR_RA                | Red armor, +100 up to 150   |
| ARMOR_SHARD             | Armor shard, +5 up to 200   |

##### Health Tag

| Name                         | Description                           |
|------------------------------|---------------------------------------|
| HEALTH_NONE \[0\]            | No health                             |
| HEALTH_SMALL \[ARMOR_TOTAL\] | Green health, 5HP pickup              |
| HEALTH_MEDIUM                | Yellow health, 25HP pickup            |
| HEALTH_LARGE                 | Orange health, 50HP pickup            |
| HEALTH_MEGA                  | Purple health, 100HP pickup, overheal |
| HEALTH_ULTRA                 | Blue health, 100HP pickup, overheal   |

##### Powerup Tag

| Name                          | Description         |
|-------------------------------|---------------------|
| POWERUP_NONE \[0\]            | No powerup          |
| POWERUP_QUAD \[HEALTH_TOTAL\] | Quad damage powerup |
| POWERUP_SHELL                 | Warshell powerup    |
| POWERUP_REGEN                 | Regen powerup       |

##### Otheritems Tag

starts at POWERUP_TOTAL

| Name             | Description          |
|------------------|----------------------|
| AMMO_PACK_WEAK   | unused?              |
| AMMO_PACK_STRONG | unused?              |
| AMMO_PACK        | Item is an ammo pack |

##### Item flags

This type is not accessible in AngelScript, but the field it describes is. Compare using the enum ordinals provided below, or the Item methods.
Bitmaskable

| Name                   | Description      |
|------------------------|------------------|
| ITFLAG_PICKABLE \[1\]  | Can be picked up |
| ITFLAG_USABLE \[2\]    | Can be used      |
| ITFLAG_DROPABLE \[4\]  | Can be dropped   |
| ITFLAG_STAY_COOP \[8\] | Unused           |

##### Item type

Bitmaskable

| Name             | Description       |
|------------------|-------------------|
| IT_WEAPON \[1\]  | Item is a weapon  |
| IT_AMMO \[2\]    | Item is ammo      |
| IT_ARMOR \[4\]   | Item is armor     |
| IT_POWERUP \[8\] | Item is a powerup |
| IT_HEALTH \[64\] | Item is health    |
