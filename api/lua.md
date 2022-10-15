This is an automatically generated listing of the Lua map scripting API for version dev-20221510 of OpenRA.

OpenRA allows custom maps and missions to be scripted using Lua 5.1.
These scripts run in a sandbox that prevents access to unsafe functions (e.g. OS or file access), and limits the memory and CPU usage of the scripts.

You can access this interface by adding the [LuaScript](../traits/#luascript) trait to the world actor in your map rules (note, you must replace the spaces in the snippet below with a single tab for each level of indentation):
```
Rules:
	World:
		LuaScript:
			Scripts: myscript.lua
```

Map scripts can interact with the game engine in three ways:

* Global tables provide functions for interacting with the global world state, or performing general helper tasks.
They exist in the global namespace, and can be called directly using ```<table name>.<function name>```.
* Individual actors expose a collection of properties and commands that query information or modify their state.
  * Some commands, marked as <em>queued activity</em>, are asynchronous. Activities are queued on the actor, and will run in sequence until the queue is empty or the Stop command is called. Actors that are not performing an activity are Idle (actor.IsIdle will return true). The properties and commands available on each actor depends on the traits that the actor specifies in its rule definitions.
* Individual players expose a collection of properties and commands that query information or modify their state.
The properties and commands available on each actor depends on the traits that the actor specifies in its rule definitions.

For a basic guide about map scripts see the [`Map Scripting` wiki page](https://github.com/OpenRA/OpenRA/wiki/Map-scripting).

## Global Tables

### Actor

| Function | Description |
|---------:|-------------|
| **int BuildTime(string type, string queue = nil)** | Returns the build time (in ticks) of the requested unit type.<br />An optional second value can be used to exactly specify the producing queue type. |
| **int Cost(string type)** |  |
| **Actor Create(string type, bool addToWorld, LuaTable initTable)** | Create a new actor. initTable specifies a list of key-value pairs that defines the initial parameters for the actor's traits. |
| **int CruiseAltitude(string type)** | Returns the cruise altitude of the requested unit type (zero if it is ground-based). |

### Angle

| Function | Description |
|---------:|-------------|
| **WAngle East { get; }** |  |
| **WAngle New(int a)** | Create an arbitrary angle. |
| **WAngle North { get; }** |  |
| **WAngle NorthEast { get; }** |  |
| **WAngle NorthWest { get; }** |  |
| **WAngle South { get; }** |  |
| **WAngle SouthEast { get; }** |  |
| **WAngle SouthWest { get; }** |  |
| **WAngle West { get; }** |  |

### Beacon

| Function | Description |
|---------:|-------------|
| **void New(Player owner, WPos position, int duration = 750, bool showRadarPings = True)** | Creates a new beacon that stays for the specified time at the specified WPos. Does not remove player set beacons, nor gets removed by placing them. Requires the 'PlaceBeacon' trait on the player actor. |

### Camera

| Function | Description |
|---------:|-------------|
| **WPos Position { get; set; }** | The center of the visible viewport. |

### HSLColor

| Function | Description |
|---------:|-------------|
| **Color Aqua { get; }** |  |
| **Color Black { get; }** |  |
| **Color Blue { get; }** |  |
| **Color Brown { get; }** |  |
| **Color Cyan { get; }** |  |
| **Color DarkBlue { get; }** |  |
| **Color DarkCyan { get; }** |  |
| **Color DarkGray { get; }** |  |
| **Color DarkGreen { get; }** |  |
| **Color DarkOrange { get; }** |  |
| **Color DarkRed { get; }** |  |
| **Color FromHex(string value)** | Create a new color with the specified red/green/blue/[alpha] hex string (rrggbb[aa]). |
| **Color FromRGB(int red, int green, int blue, int alpha = 255)** | Create a new color with the specified red/green/blue/[alpha] values. |
| **Color Fuchsia { get; }** |  |
| **Color Gold { get; }** |  |
| **Color Gray { get; }** |  |
| **Color Green { get; }** |  |
| **Color LawnGreen { get; }** |  |
| **Color LightBlue { get; }** |  |
| **Color LightCyan { get; }** |  |
| **Color LightGray { get; }** |  |
| **Color LightGreen { get; }** |  |
| **Color LightYellow { get; }** |  |
| **Color Lime { get; }** |  |
| **Color LimeGreen { get; }** |  |
| **Color Magenta { get; }** |  |
| **Color Maroon { get; }** |  |
| **Color Navy { get; }** |  |
| **Color New(int hue, int saturation, int luminosity)** | Create a new color with the specified hue/saturation/luminosity. |
| **Color Olive { get; }** |  |
| **Color Orange { get; }** |  |
| **Color OrangeRed { get; }** |  |
| **Color Purple { get; }** |  |
| **Color Red { get; }** |  |
| **Color Salmon { get; }** |  |
| **Color SkyBlue { get; }** |  |
| **Color Teal { get; }** |  |
| **Color White { get; }** |  |
| **Color Yellow { get; }** |  |

### CPos

| Function | Description |
|---------:|-------------|
| **CPos New(int x, int y)** | Create a new CPos with the specified coordinates. |
| **CPos Zero { get; }** | The cell coordinate origin. |

### CVec

| Function | Description |
|---------:|-------------|
| **CVec New(int x, int y)** | Create a new CVec with the specified coordinates. |
| **CVec Zero { get; }** | The cell zero-vector. |

### DateTime

| Function | Description |
|---------:|-------------|
| **int GameTime { get; }** | Get the current game time (in ticks). |
| **bool IsHalloween { get; }** | True on the 31st of October. |
| **int Minutes(int minutes)** | Converts the number of minutes into game time (ticks). |
| **int Seconds(int seconds)** | Converts the number of seconds into game time (ticks). |
| **int TimeLimit { get; set; }** | Return or set the time limit (in ticks). When setting, the time limit will count from now. Setting the time limit to 0 will disable it. |
| **string TimeLimitNotification { get; set; }** | The notification string used for custom time limit warnings. See the TimeLimitManager trait documentation for details. |

### Lighting

| Function | Description |
|---------:|-------------|
| **Double Ambient { get; set; }** |  |
| **Double Blue { get; set; }** |  |
| **void Flash(string type = nil, int ticks = -1)** | Controls the `FlashPaletteEffect` trait. |
| **Double Green { get; set; }** |  |
| **Double Red { get; set; }** |  |

### Map

| Function | Description |
|---------:|-------------|
| **Actor[] ActorsInBox(WPos topLeft, WPos bottomRight, LuaFunction filter = nil)** | Returns a table of all actors within the requested rectangle, filtered using the specified function. |
| **Actor[] ActorsInCircle(WPos location, WDist radius, LuaFunction filter = nil)** | Returns a table of all actors within the requested region, filtered using the specified function. |
| **Actor[] ActorsInWorld { get; }** | Returns a table of all the actors that are currently on the map/in the world. |
| **Actor[] ActorsWithTag(string tag)** | Returns a table of all actors tagged with the given string. |
| **WPos BottomRight { get; }** | Returns the location of the bottom-right corner of the map (assuming zero terrain height). |
| **WPos CenterOfCell(CPos cell)** | Returns the center of a cell in world coordinates. |
| **CPos ClosestEdgeCell(CPos givenCell)** | Returns the closest cell on the visible border of the map from the given cell. |
| **CPos ClosestMatchingEdgeCell(CPos givenCell, LuaFunction filter)** | Returns the first cell on the visible border of the map from the given cell,<br />matching the filter function called as function(CPos cell). |
| **bool IsNamedActor(Actor actor)** | Returns true if actor was originally specified in the map file. |
| **bool IsPausedShellmap { get; }** | Returns true if this is a shellmap and the player has paused animations. |
| **bool IsSinglePlayer { get; }** | Returns true if there is only one human player. |
| **LuaValue LobbyOption(string id)** | Returns the value of a `ScriptLobbyDropdown` selected in the game lobby. |
| **Actor NamedActor(string actorName)** | Returns the actor that was specified with a given name in the map file (or nil, if the actor is dead or not found). |
| **Actor[] NamedActors { get; }** | Returns a table of all the actors that were specified in the map file. |
| **CPos RandomCell()** | Returns a random cell inside the visible region of the map. |
| **CPos RandomEdgeCell()** | Returns a random cell on the visible border of the map. |
| **string TerrainType(CPos cell)** | Returns the type of the terrain at the target cell. |
| **WPos TopLeft { get; }** | Returns the location of the top-left corner of the map (assuming zero terrain height). |

### Media

| Function | Description |
|---------:|-------------|
| **void Debug(string text)** | Displays a debug message to the player, if "Show Map Debug Messages" is checked in the settings. |
| **void DisplayMessage(string text, string prefix = Mission, Color? color = nil)** | Display a text message to the player. |
| **void DisplaySystemMessage(string text, string prefix = nil)** | Display a system message to the player. If 'prefix' is nil the default system prefix is used. |
| **void FloatingText(string text, WPos position, int duration = 30, Color? color = nil)** | Display a text message at the specified location. |
| **void PlayMovieFullscreen(string movie, LuaFunction func = nil)** | Play a VQA video fullscreen. File name has to include the file extension. |
| **bool PlayMovieInRadar(string movie, LuaFunction playComplete = nil)** | Play a VQA video in the radar window. File name has to include the file extension. Returns true on success, if the movie wasn't found the function returns false and the callback is executed. |
| **void PlayMusic(string track = nil, LuaFunction func = nil)** | Play track defined in music.yaml or map.yaml, or keep track empty for playing a random song. |
| **void PlaySound(string file)** | Play a sound file |
| **void PlaySoundNotification(Player player, string notification)** | Play a sound listed in notifications.yaml |
| **void PlaySpeechNotification(Player player, string notification)** | Play an announcer voice listed in notifications.yaml |
| **void SetBackgroundMusic(string track = nil)** | Play track defined in music.yaml or map.yaml as background music. If music is already playing use Media.StopMusic() to stop it and the background music will start automatically. Keep the track empty to disable background music. |
| **void StopMusic()** | Stop the current song. |

### Player

| Function | Description |
|---------:|-------------|
| **Player GetPlayer(string name)** | Returns the player with the specified internal name, or nil if a match is not found. |
| **Player[] GetPlayers(LuaFunction filter)** | Returns a table of players filtered by the specified function. |

### Radar

| Function | Description |
|---------:|-------------|
| **void Ping(Player player, WPos position, Color color, int duration = 750)** | Creates a new radar ping that stays for the specified time at the specified WPos. |

### Reinforcements

| Function | Description |
|---------:|-------------|
| **Actor[] Reinforce(Player owner, String[] actorTypes, CPos[] entryPath, int interval = 25, LuaFunction actionFunc = nil)** | Send reinforcements consisting of multiple units. Supports ground-based, naval and air units. The first member of the entryPath array will be the units' spawnpoint, while the last one will be their destination. If actionFunc is given, it will be executed once a unit has reached its destination. actionFunc will be called as actionFunc(Actor actor). Returns a table containing the deployed units. |
| **LuaTable ReinforceWithTransport(Player owner, string actorType, String[] cargoTypes, CPos[] entryPath, CPos[] exitPath = nil, LuaFunction actionFunc = nil, LuaFunction exitFunc = nil, int dropRange = 3)** | Send reinforcements in a transport. A transport can be a ground unit (APC etc.), ships and aircraft. The first member of the entryPath array will be the spawnpoint for the transport, while the last one will be its destination. The last member of the exitPath array is be the place where the transport will be removed from the game. When the transport has reached the destination, it will unload its cargo unless a custom actionFunc has been supplied. Afterwards, the transport will follow the exitPath and leave the map, unless a custom exitFunc has been supplied. actionFunc will be called as actionFunc(Actor transport, Actor[] cargo). exitFunc will be called as exitFunc(Actor transport). dropRange determines how many cells away the transport will try to land if the actual destination is blocked (if the transport is an aircraft). Returns a table in which the first value is the transport, and the second a table containing the deployed units. |

### Trigger

| Function | Description |
|---------:|-------------|
| **void AfterDelay(int delay, LuaFunction func)** | Call a function after a specified delay. The callback function will be called as func(). |
| **void Clear(Actor a, string triggerName)** | Removes the specified trigger from this actor. Note that the removal will only take effect at the end of a tick, so you must not add new triggers at the same time that you are calling this function. |
| **void ClearAll(Actor a)** | Removes all triggers from this actor. Note that the removal will only take effect at the end of a tick, so you must not add new triggers at the same time that you are calling this function. |
| **void OnAddedToWorld(Actor a, LuaFunction func)** | Call a function when this actor is added to the world. The callback function will be called as func(Actor self). |
| **void OnAllKilled(Actor[] actors, LuaFunction func)** | Call a function when all of the actors in a group are killed. The callback function will be called as func(). |
| **void OnAllKilledOrCaptured(Actor[] actors, LuaFunction func)** | Call a function when all of the actors in a group have been killed or captured. The callback function will be called as func(). |
| **void OnAllRemovedFromWorld(Actor[] actors, LuaFunction func)** | Call a function when all of the actors in a group have been removed from the world. The callback function will be called as func(). |
| **void OnAnyKilled(Actor[] actors, LuaFunction func)** | Call a function when one of the actors in a group is killed. The callback function will be called as func(Actor killed). |
| **void OnAnyProduction(LuaFunction func)** | Call a function when any actor produces another actor. The callback function will be called as func(Actor producer, Actor produced, string productionType). |
| **void OnCapture(Actor a, LuaFunction func)** | Call a function when this actor is captured. The callback function will be called as func(Actor self, Actor captor, Player oldOwner, Player newOwner). |
| **void OnDamaged(Actor a, LuaFunction func)** | Call a function when the actor is damaged. The callback function will be called as func(Actor self, Actor attacker, int damage). |
| **void OnDiscovered(Actor a, LuaFunction func)** | Call a function when this actor is discovered by an enemy or a player with a Neutral stance. The callback function will be called as func(Actor discovered, Player discoverer). The player actor needs the 'EnemyWatcher' trait. The actors to discover need the 'AnnounceOnSeen' trait. |
| **int OnEnteredFootprint(CPos[] cells, LuaFunction func)** | Call a function when a ground-based actor enters this cell footprint. Returns the trigger id for later removal using RemoveFootprintTrigger(int id). The callback function will be called as func(Actor a, int id). |
| **int OnEnteredProximityTrigger(WPos pos, WDist range, LuaFunction func)** | Call a function when an actor enters this range. Returns the trigger id for later removal using RemoveProximityTrigger(int id). The callback function will be called as func(Actor a, int id). |
| **int OnExitedFootprint(CPos[] cells, LuaFunction func)** | Call a function when a ground-based actor leaves this cell footprint. Returns the trigger id for later removal using RemoveFootprintTrigger(int id). The callback function will be called as func(Actor a, int id). |
| **int OnExitedProximityTrigger(WPos pos, WDist range, LuaFunction func)** | Call a function when an actor leaves this range. Returns the trigger id for later removal using RemoveProximityTrigger(int id). The callback function will be called as func(Actor a, int id). |
| **void OnIdle(Actor a, LuaFunction func)** | Call a function each tick that the actor is idle. The callback function will be called as func(Actor self). |
| **void OnInfiltrated(Actor a, LuaFunction func)** | Call a function when this actor is infiltrated. The callback function will be called as func(Actor self, Actor infiltrator). |
| **void OnKilled(Actor a, LuaFunction func)** | Call a function when the actor is killed. The callback function will be called as func(Actor self, Actor killer). |
| **void OnKilledOrCaptured(Actor a, LuaFunction func)** | Call a function when this actor is killed or captured. The callback function will be called as func(). |
| **void OnObjectiveAdded(Player player, LuaFunction func)** | Call a function when this player is assigned a new objective. The callback function will be called as func(Player player, int objectiveID). |
| **void OnObjectiveCompleted(Player player, LuaFunction func)** | Call a function when this player completes an objective. The callback function will be called as func(Player player, int objectiveID). |
| **void OnObjectiveFailed(Player player, LuaFunction func)** | Call a function when this player fails an objective. The callback function will be called as func(Player player, int objectiveID). |
| **void OnPassengerEntered(Actor a, LuaFunction func)** | Call a function for each passenger when it enters a transport. The callback function will be called as func(Actor transport, Actor passenger). |
| **void OnPassengerExited(Actor a, LuaFunction func)** | Call a function for each passenger when it exits a transport. The callback function will be called as func(Actor transport, Actor passenger). |
| **void OnPlayerDiscovered(Player discovered, LuaFunction func)** | Call a function when this player is discovered by an enemy or neutral player. The callback function will be called as func(Player discovered, Player discoverer, Actor discoveredActor).The player actor needs the 'EnemyWatcher' trait. The actors to discover need the 'AnnounceOnSeen' trait. |
| **void OnPlayerLost(Player player, LuaFunction func)** | Call a function when this player fails any primary objective. The callback function will be called as func(Player player). |
| **void OnPlayerWon(Player player, LuaFunction func)** | Call a function when this player completes all primary objectives. The callback function will be called as func(Player player). |
| **void OnProduction(Actor a, LuaFunction func)** | Call a function when this actor produces another actor. The callback function will be called as func(Actor producer, Actor produced). |
| **void OnRemovedFromWorld(Actor a, LuaFunction func)** | Call a function when this actor is removed from the world. The callback function will be called as func(Actor self). |
| **void OnSold(Actor a, LuaFunction func)** | Call a function when this actor is sold. The callback function will be called as func(Actor self). |
| **void OnTimerExpired(LuaFunction func)** | Call a function when the game timer expires. The callback function will be called as func(). |
| **void RemoveFootprintTrigger(int id)** | Removes a previously created footprint trigger. |
| **void RemoveProximityTrigger(int id)** | Removes a previously created proximity trigger. |

### UserInterface

| Function | Description |
|---------:|-------------|
| **void SetMissionText(string text, Color? color = nil)** | Displays a text message at the top center of the screen. |
| **string Translate(string text)** |  |

### Utils

| Function | Description |
|---------:|-------------|
| **bool All(LuaValue[] collection, LuaFunction func)** | Returns true if func returns true for all elements in a collection. |
| **bool Any(LuaValue[] collection, LuaFunction func)** | Returns true if func returns true for any element in a collection. |
| **void Do(LuaValue[] collection, LuaFunction func)** | Calls a function on every element in a collection. |
| **CPos[] ExpandFootprint(CPos[] footprint, bool allowDiagonal)** | Expands the given footprint one step along the coordinate axes, and (if requested) diagonals. |
| **string FormatTime(int ticks, bool leadingMinuteZero = True)** | Returns the ticks formatted to HH:MM:SS. |
| **LuaValue Random(LuaValue[] collection)** | Returns a random value from a collection. |
| **int RandomInteger(int low, int high)** | Returns a random integer x in the range low &lt;= x &lt; high. |
| **LuaValue[] Shuffle(LuaValue[] collection)** | Returns the collection in a random order. |
| **LuaTable Skip(LuaTable table, int numElements)** | Skips over the first numElements members of a table and return the rest. |
| **LuaValue[] Take(int n, LuaValue[] source)** | Returns the first n values from a collection. |
| **LuaTable Where(LuaValue[] collection, LuaFunction func)** | Returns the original collection filtered with the func. |

### WDist

| Function | Description |
|---------:|-------------|
| **WDist FromCells(int numCells)** | Create a new WDist by cell distance. |
| **WDist New(int r)** | Create a new WDist. |

### WPos

| Function | Description |
|---------:|-------------|
| **WPos New(int x, int y, int z)** | Create a new WPos with the specified coordinates. |
| **WPos Zero { get; }** | The world coordinate origin. |

### WVec

| Function | Description |
|---------:|-------------|
| **WVec New(int x, int y, int z)** | Create a new WVec with the specified coordinates. |
| **WVec Zero { get; }** | The world zero-vector. |

## Actor Properties / Commands

### Ability

| Function | Description |
|---------:|-------------|
| **void Capture(Actor target)** | Captures the target actor.<br />**Requires Trait:** CaptureManager |
| **void DeliverCarryable(CPos target)**<br />*Queued Activity* | Drop the actor being carried at the target location.<br />**Requires Trait:** Carryall |
| **void DeliverCash(Actor target)**<br />*Queued Activity* | Deliver cash to the target actor.<br />**Requires Traits:** IMove, DeliversCash |
| **void DeliverExperience(Actor target)**<br />*Queued Activity* | Deliver experience to the target actor.<br />**Requires Traits:** IMove, DeliversExperience |
| **void DisguiseAs(Actor target)** | Disguises as the target actor.<br />**Requires Trait:** Disguise |
| **void DisguiseAsType(string actorType, Player newOwner)** | Disguises as the target type with the specified owner.<br />**Requires Trait:** Disguise |
| **void Infiltrate(Actor target)** | Infiltrate the target actor.<br />**Requires Trait:** Infiltrates |
| **void PickupCarryable(Actor target)**<br />*Queued Activity* | Pick up the target actor.<br />**Requires Trait:** Carryall |

### AmmoPool

| Function | Description |
|---------:|-------------|
| **int AmmoCount(string poolName = primary)** | Returns the count of the actor's specified ammopool.<br />**Requires Trait:** AmmoPool |
| **int MaximumAmmoCount(string poolName = primary)** | Returns the maximum count of ammo the actor can load.<br />**Requires Trait:** AmmoPool |
| **void Reload(string poolName = primary, int amount = 1)** | Adds the specified amount of ammo to the specified ammopool.<br />(Use a negative amount to remove ammo.)<br />**Requires Trait:** AmmoPool |

### Cloak

| Function | Description |
|---------:|-------------|
| **bool IsCloaked { get; }** | Returns true if the actor is cloaked.<br />**Requires Trait:** Cloak |

### Combat

| Function | Description |
|---------:|-------------|
| **void Attack(Actor targetActor, bool allowMove = True, bool forceAttack = False)** | Attack the target actor. The target actor needs to be visible.<br />**Requires Trait:** AttackBase |
| **void AttackMove(CPos cell, int closeEnough = 0)**<br />*Queued Activity* | Move to a cell, but stop and attack anything within range on the way. closeEnough defines an optional range (in cells) that will be considered close enough to complete the activity.<br />**Requires Traits:** AttackBase, IMove |
| **bool CanTarget(Actor targetActor)** | Checks if the targeted actor is a valid target for this actor.<br />**Requires Trait:** AttackBase |
| **void Demolish(Actor target)**<br />*Queued Activity* | Demolish the target actor.<br />**Requires Traits:** IMove, Demolition |
| **void Guard(Actor targetActor)**<br />*Queued Activity* | Guard the target actor.<br />**Requires Traits:** Guard, IMove |
| **void Hunt()**<br />*Queued Activity* | Seek out and attack nearby targets.<br />**Requires Traits:** AttackBase, IMove |
| **void Patrol(CPos[] waypoints, bool loop = True, int wait = 0)**<br />*Queued Activity* | Patrol along a set of given waypoints. The action is repeated by default, and the actor will wait for `wait` ticks at each waypoint.<br />**Requires Traits:** AttackBase, IMove |
| **void PatrolUntil(CPos[] waypoints, LuaFunction func, int wait = 0)**<br />*Queued Activity* | Patrol along a set of given waypoints until a condition becomes true. The actor will wait for `wait` ticks at each waypoint.<br />**Requires Traits:** AttackBase, IMove |

### Experience

| Function | Description |
|---------:|-------------|
| **bool CanGainLevel { get; }** | Returns true if the actor can gain a level.<br />**Requires Trait:** GainsExperience |
| **int Experience { get; }** | The actor's amount of experience.<br />**Requires Trait:** GainsExperience |
| **void GiveExperience(int amount, bool silent = False)** | Gives the actor experience. If 'silent' is true, no animation or sound will be played if the actor levels up.<br />**Requires Trait:** GainsExperience |
| **void GiveLevels(int numLevels, bool silent = False)** | Gives the actor level(s). If 'silent' is true, no animation or sound will be played.<br />**Requires Trait:** GainsExperience |
| **int Level { get; }** | The actor's level.<br />**Requires Trait:** GainsExperience |
| **int MaxLevel { get; }** | The actor's maximum possible level.<br />**Requires Trait:** GainsExperience |

### General

| Function | Description |
|---------:|-------------|
| **bool AcceptsCondition(string condition)** | Check whether this actor accepts a specific external condition.<br />**Requires Trait:** ExternalCondition |
| **bool AddTag(string tag)** | Add a tag to the actor. Returns true on success, false otherwise (for example the actor may already have the given tag). |
| **void CallFunc(LuaFunction func)**<br />*Queued Activity* | Run an arbitrary Lua function. |
| **WPos CenterPosition { get; }** | The actor position in world coordinates. |
| **void Deploy()**<br />*Queued Activity* | Queue a new transformation.<br />**Requires Trait:** Transforms |
| **void Destroy()**<br />*Queued Activity* | Remove the actor from the game, without triggering any death notification. |
| **Player EffectiveOwner { get; }** | The effective owner of the actor. |
| **WAngle Facing { get; }** | The direction that the actor is facing. |
| **void Flash(Color color, int count = 2, int interval = 2, int delay = 0)** | Render a target flash on the actor. |
| **int GrantCondition(string condition, int duration = 0)** | Grant an external condition on this actor and return the revocation token.<br />Conditions must be defined on an ExternalConditions trait on the actor.<br />If duration > 0 the condition will be automatically revoked after the defined number of ticks.<br />**Requires Trait:** ExternalCondition |
| **bool HasProperty(string name)** | Test whether an actor has a specific property. |
| **bool HasTag(string tag)** | Specifies whether or not the actor has a particular tag. |
| **int Health { get; set; }** | Current health of the actor.<br />**Requires Trait:** IHealth |
| **bool IsDead { get; }** | Specifies whether the actor is alive or dead. |
| **bool IsIdle { get; }** | Specifies whether the actor is idle (not performing any activities). |
| **bool IsInWorld { get; set; }** | Specifies whether the actor is in the world. |
| **bool IsTaggable { get; }** | Specifies whether or not the actor supports 'tags'. |
| **void Kill(Object damageTypes = nil)** | Kill the actor. damageTypes may be omitted, specified as a string, or as table of strings.<br />**Requires Trait:** IHealth |
| **CPos Location { get; }** | The actor position in cell coordinates. |
| **int MaxHealth { get; }** | Maximum health of the actor.<br />**Requires Trait:** IHealth |
| **Player Owner { get; set; }** | The player that owns the actor. |
| **bool RemoveTag(string tag)** | Remove a tag from the actor. Returns true on success, false otherwise (tag was not present). |
| **void RevokeCondition(int token)** | Revoke a condition using the token returned by GrantCondition.<br />**Requires Trait:** ExternalCondition |
| **void Sell()** | Start selling the actor.<br />**Requires Trait:** Sellable |
| **string Stance { get; set; }** | Current actor stance. Returns nil if this actor doesn't support stances. |
| **void StartBuildingRepairs(Player repairer = nil)** | Start repairs on this building. `repairer` can be an allied player.<br />**Requires Trait:** RepairableBuilding |
| **void Stop()** | Attempt to cancel any active activities. |
| **void StopBuildingRepairs(Player repairer = nil)** | Stop repairs on this building. `repairer` can be an allied player.<br />**Requires Trait:** RepairableBuilding |
| **void Teleport(CPos cell)**<br />*Queued Activity* | Instantly moves the actor to the specified cell. |
| **string TooltipName { get; }** | The actor's tooltip name. Returns nil if the actor has no tooltip. |
| **string Type { get; }** | The type of the actor (e.g. "e1"). |
| **void Wait(int ticks)**<br />*Queued Activity* | Wait for a specified number of game ticks (25 ticks = 1 second). |

### Movement

| Function | Description |
|---------:|-------------|
| **void EnterTransport(Actor transport)**<br />*Queued Activity* | Move to and enter the transport.<br />**Requires Trait:** Mobile |
| **void FindResources()**<br />*Queued Activity* | Search for nearby resources and begin harvesting.<br />**Requires Trait:** Harvester |
| **bool IsMobile { get; }** | Whether the actor can move (false if immobilized).<br />**Requires Trait:** Mobile |
| **void Land(Actor landOn)**<br />*Queued Activity* | Queues a landing activity on the specified actor.<br />**Requires Trait:** Aircraft |
| **void Move(CPos cell)**<br />*Queued Activity* | Fly within the cell grid.<br />**Requires Trait:** Aircraft |
| **void Move(CPos cell, int closeEnough = 0)**<br />*Queued Activity* | Moves within the cell grid. closeEnough defines an optional range (in cells) that will be considered close enough to complete the activity.<br />**Requires Trait:** Mobile |
| **void MoveIntoWorld(CPos cell)**<br />*Queued Activity* | Moves from outside the world into the cell grid.<br />**Requires Trait:** Mobile |
| **void Panic()**<br />*Queued Activity* | Makes the unit automatically run around and become faster.<br />**Requires Trait:** ScaredyCat |
| **void Resupply()**<br />*Queued Activity* | Starts the resupplying activity when being on a host building.<br />**Requires Trait:** Aircraft |
| **void ReturnToBase(Actor destination = nil)**<br />*Queued Activity* | Return to the base, which is either the destination given, or an auto-selected one otherwise.<br />**Requires Trait:** Aircraft |
| **void Scatter()**<br />*Queued Activity* | Leave the current position in a random direction.<br />**Requires Trait:** Mobile |
| **void ScriptedMove(CPos cell)**<br />*Queued Activity* | Moves within the cell grid, ignoring lane biases.<br />**Requires Trait:** Mobile |

### Power

| Function | Description |
|---------:|-------------|
| **int Power { get; }** | Returns the power drained/provided by this actor.<br />**Requires Trait:** Power |

### Production

| Function | Description |
|---------:|-------------|
| **bool Build(String[] actorTypes, LuaFunction actionFunc = nil)** | Build the specified set of actors using a TD-style (per building) production queue. The function will return true if production could be started, false otherwise. If an actionFunc is given, it will be called as actionFunc(Actor[] actors) once production of all actors has been completed.  The actors array is guaranteed to only contain alive actors.<br />**Requires Traits:** ProductionQueue, ScriptTriggers |
| **bool IsPrimaryBuilding { get; set; }** | Query or set the factory's primary building status.<br />**Requires Trait:** PrimaryBuilding |
| **bool IsProducing(string actorType)** | Check whether the factory's production queue that builds this type of actor is currently busy. Note: it does not check whether this particular type of actor is being produced.<br />**Requires Traits:** ProductionQueue, ScriptTriggers |
| **void Produce(string actorType, string factionVariant = nil, string productionType = nil)**<br />*Queued Activity* | Build a unit, ignoring the production queue. The activity will wait if the exit is blocked.<br />If productionType is nil or unavailable, then an exit will be selected based on 'Buildable.BuildAtProductionType'.<br />If 'Buildable.BuildAtProductionType' is not set either, a random exit will be selected.<br />**Requires Trait:** Production |
| **CPos RallyPoint { get; set; }** | Query or set a factory's rally point.<br />**Requires Trait:** RallyPoint |

### Support Powers

| Function | Description |
|---------:|-------------|
| **void ActivateIonCannon(CPos target)** | Activate the actor's IonCannonPower.<br />**Requires Trait:** IonCannonPower |
| **void ActivateNukePower(CPos target)** | Activate the actor's NukePower.<br />**Requires Trait:** NukePower |
| **void Chronoshift(LuaTable unitLocationPairs, int duration = 0, bool killCargo = False)** | Chronoshift a group of actors. A duration of 0 will teleport the actors permanently.<br />**Requires Trait:** ChronoshiftPower |
| **Actor[] TargetAirstrike(WPos target, WAngle? facing = nil)** | Activate the actor's Airstrike Power. Returns the aircraft that will attack.<br />**Requires Trait:** AirstrikePower |
| **Actor[] TargetParatroopers(WPos target, WAngle? facing = nil)** | Activate the actor's Paratroopers Power. Returns the aircraft that will drop the reinforcements.<br />**Requires Trait:** ParatroopersPower |

### Transports

| Function | Description |
|---------:|-------------|
| **bool HasPassengers { get; }** | Specifies whether transport has any passengers.<br />**Requires Trait:** Cargo |
| **void LoadPassenger(Actor a)** | Teleport an existing actor inside this transport.<br />**Requires Trait:** Cargo |
| **void Paradrop(CPos cell)**<br />*Queued Activity* | Command transport to paradrop passengers near the target cell.<br />**Requires Traits:** Cargo, ParaDrop |
| **int PassengerCount { get; }** | Specifies the amount of passengers.<br />**Requires Trait:** Cargo |
| **Actor[] Passengers { get; }** | Returns references to passengers inside the transport.<br />**Requires Trait:** Cargo |
| **Actor UnloadPassenger(Actor a = nil)** | Remove an existing actor (or first actor if none specified) from the transport.  This actor is not added to the world.<br />**Requires Trait:** Cargo |
| **void UnloadPassengers(CPos? cell = nil, int unloadRange = 5)**<br />*Queued Activity* | Command transport to unload passengers.<br />**Requires Trait:** Cargo |

## Player Properties / Commands

### Diplomacy

| Function | Description |
|---------:|-------------|
| **bool IsAlliedWith(Player targetPlayer)** | Returns true if the player is allied with the other player. |


### MissionObjectives

| Function | Description |
|---------:|-------------|
| **int AddObjective(string description, string type = Primary, bool required = True)**<br />*Queued Activity* | Add a mission objective for this player. The function returns the ID of the newly created objective, so that it can be referred to later.<br />**Requires Trait:** MissionObjectives |
| **int AddPrimaryObjective(string description)**<br />*Queued Activity* | Add a primary mission objective for this player. The function returns the ID of the newly created objective, so that it can be referred to later.<br />**Requires Trait:** MissionObjectives |
| **int AddSecondaryObjective(string description)**<br />*Queued Activity* | Add a secondary mission objective for this player. The function returns the ID of the newly created objective, so that it can be referred to later.<br />**Requires Trait:** MissionObjectives |
| **string GetObjectiveDescription(int id)**<br />*Queued Activity* | Returns the description of an objective.<br />**Requires Trait:** MissionObjectives |
| **string GetObjectiveType(int id)**<br />*Queued Activity* | Returns the type of an objective.<br />**Requires Trait:** MissionObjectives |
| **bool HasNoRequiredUnits()**<br />*Queued Activity* | Returns true if this player has lost all units/actors that have the MustBeDestroyed trait (according to the short game option).<br />**Requires Trait:** MissionObjectives |
| **bool IsObjectiveCompleted(int id)**<br />*Queued Activity* | Returns true if the objective has been successfully completed, false otherwise.<br />**Requires Trait:** MissionObjectives |
| **bool IsObjectiveFailed(int id)**<br />*Queued Activity* | Returns true if the objective has been failed, false otherwise.<br />**Requires Trait:** MissionObjectives |
| **void MarkCompletedObjective(int id)**<br />*Queued Activity* | Mark an objective as completed.  This needs the objective ID returned by AddObjective as argument.  When this player has completed all primary objectives, (s)he has won the game.<br />**Requires Trait:** MissionObjectives |
| **void MarkFailedObjective(int id)**<br />*Queued Activity* | Mark an objective as failed.  This needs the objective ID returned by AddObjective as argument.  Secondary objectives do not have any influence whatsoever on the outcome of the game.<br />**Requires Trait:** MissionObjectives |


### Player

| Function | Description |
|---------:|-------------|
| **bool AcceptsCondition(string condition)** | Check whether this player actor accepts a specific external condition. |
| **int BuildingsKilled { get; }** | The total number of buildings killed by this player.<br />**Requires Trait:** PlayerStatistics |
| **int BuildingsLost { get; }** | The total number of buildings lost by this player.<br />**Requires Trait:** PlayerStatistics |
| **Color Color { get; }** | The player's color. |
| **int DeathsCost { get; }** | The combined value of all units lost by this player.<br />**Requires Trait:** PlayerStatistics |
| **int Experience { get; set; }** | **Requires Trait:** PlayerExperience |
| **string Faction { get; }** | The player's faction. |
| **Actor[] GetActors()** | Returns all living actors staying inside the world for this player. |
| **Actor[] GetActorsByType(string type)** | Returns all living actors of the specified type of this player. |
| **Actor[] GetActorsByTypes(String[] types)** | Returns all living actors of the specified types of this player. |
| **Actor[] GetGroundAttackers()** | Returns an array of actors representing all ground attack units of this player. |
| **int GrantCondition(string condition, int duration = 0)** | Grant an external condition on the player actor and return the revocation token.<br />Conditions must be defined on an ExternalConditions trait on the player actor.<br />If duration > 0 the condition will be automatically revoked after the defined number of ticks. |
| **int Handicap { get; }** | The player's handicap level. |
| **bool HasPrerequisites(String[] type)** | Check if the player has these prerequisites available. |
| **CPos HomeLocation { get; }** | The player's home/starting location. |
| **string InternalName { get; }** | The player's internal name. |
| **bool IsBot { get; }** | Returns true if the player is a bot. |
| **bool IsLocalPlayer { get; }** | Returns true if the player is the local player. |
| **bool IsNonCombatant { get; }** | Returns true if the player is non combatant. |
| **int KillsCost { get; }** | The combined value of units killed by this player.<br />**Requires Trait:** PlayerStatistics |
| **string Name { get; }** | The player's name. |
| **void RevokeCondition(int token)** | Revoke a condition using the token returned by GrantCondition. |
| **int Spawn { get; }** | The player's spawnpoint ID. |
| **int Team { get; }** | The player's team ID. |
| **int UnitsKilled { get; }** | The total number of units killed by this player.<br />**Requires Trait:** PlayerStatistics |
| **int UnitsLost { get; }** | The total number of units lost by this player.<br />**Requires Trait:** PlayerStatistics |


### Power

| Function | Description |
|---------:|-------------|
| **int PowerDrained { get; }** | Returns the power used by the player.<br />**Requires Trait:** PowerManager |
| **int PowerProvided { get; }** | Returns the total of the power the player has.<br />**Requires Trait:** PowerManager |
| **string PowerState { get; }** | Returns the player's power state ("Normal", "Low" or "Critical").<br />**Requires Trait:** PowerManager |
| **void TriggerPowerOutage(int ticks)** | Triggers low power for the chosen amount of ticks.<br />**Requires Trait:** PowerManager |


### Production

| Function | Description |
|---------:|-------------|
| **bool Build(String[] actorTypes, LuaFunction actionFunc = nil)** | Build the specified set of actors using classic (RA-style) production queues. The function will return true if production could be started, false otherwise. If an actionFunc is given, it will be called as actionFunc(Actor[] actors) once production of all actors has been completed. The actors array is guaranteed to only contain alive actors. Note: This function will fail to work when called during the first tick.<br />**Requires Traits:** ClassicProductionQueue, ScriptTriggers |
| **bool IsProducing(string actorType)** | Check whether the production queue that builds this type of actor is currently busy. Note: it does not check whether this particular type of actor is being produced.<br />**Requires Traits:** ClassicProductionQueue, ScriptTriggers |


### Resources

| Function | Description |
|---------:|-------------|
| **int Cash { get; set; }** | The amount of cash held by the player.<br />**Requires Trait:** PlayerResources |
| **int ResourceCapacity { get; }** | The maximum resource storage of the player.<br />**Requires Trait:** PlayerResources |
| **int Resources { get; set; }** | The amount of harvestable resources held by the player.<br />**Requires Trait:** PlayerResources |

