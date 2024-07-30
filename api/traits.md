# Traits

This documentation is aimed at modders and has been automatically generated for version `bleed` of OpenRA. Please do not edit it directly, but instead add new `[Desc("String")]` tags to the source code.

Listed below are all traits with their properties and their default values plus developer commentary.
Related types with their possible values are listed [at the bottom](#related-value-types-enums).

## OpenRA.Mods.Cnc.Traits

### AttackLeap
**Move onto the target then execute the attack.**

> Inherits from: [`AttackFrontal`](#attackfrontal), `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Mobile`](#mobile).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Speed | 0c426 | 1D World Distance | Leap speed (in WDist units/tick). |
| LeapCondition | attacking | String | Conditions that last from start of the leap until the attack. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackOrderPower

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CircleColor | FF0000 | Color (RRGGBB[AA] notation) | Range circle color. |
| CircleWidth | 1 | Real Number | Range circle line width. |
| CircleBorderColor | 00000060 | Color (RRGGBB[AA] notation) | Range circle border color. |
| CircleBorderWidth | 3 | Real Number | Range circle border width. |
| SupportPowerTargetingCondition | support-targeting | String | Condition set to the unit that will execute the attack while the support power is in targeting mode. |
| SupportPowerAttackingCondition | support-attacking | String | Condition set to the unit is executing the attack while the support power attack is in progress. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | AttackOrderPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackPopupTurreted
**Actor's turret rises from the ground before attacking.**

> Inherits from: [`AttackTurreted`](#attackturreted), [`AttackFollow`](#attackfollow), `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Building`](#building), [`Turreted`](#turreted), [`WithEmbeddedTurretSpriteBody`](#withembeddedturretspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CloseDelay | 125 | Integer | How many game ticks should pass before closing the actor's turret. |
| DefaultFacing | 0 | 1D World Angle |  |
| ClosedDamageMultiplier | 50 | Integer | The percentage of damage that is received while this actor is closed. |
| OpeningSequence | opening | String | Sequence to play when opening. |
| ClosingSequence | closing | String | Sequence to play when closing. |
| ClosedIdleSequence | closed-idle | String | Idle sequence to play when closed. |
| Body | body | String | Which sprite body to play the animation on. |
| Turrets | primary | Collection of String | Turret names |
| OpportunityFire | True | Boolean | Automatically acquire and fire on targets of opportunity when not actively attacking. |
| PersistentTargeting | True | Boolean | Keep firing on targets even after attack order is cancelled |
| RangeMargin | 1c0 | 1D World Distance | Range to stay away from min and max ranges to give some leeway if the target starts moving. |
| AbortOnResupply | True | Boolean | Does this actor cancel its attack activity when it needs to resupply? Setting this to 'false' will make the actor resume attack after reloading. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackTDGunboatTurreted
**Actor has a visual turret used to attack.**

> Inherits from: [`AttackTurreted`](#attackturreted), [`AttackFollow`](#attackfollow), `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`TDGunboat`](#tdgunboat), [`Turreted`](#turreted).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Turrets | primary | Collection of String | Turret names |
| OpportunityFire | True | Boolean | Automatically acquire and fire on targets of opportunity when not actively attacking. |
| PersistentTargeting | True | Boolean | Keep firing on targets even after attack order is cancelled |
| RangeMargin | 1c0 | 1D World Distance | Range to stay away from min and max ranges to give some leeway if the target starts moving. |
| AbortOnResupply | True | Boolean | Does this actor cancel its attack activity when it needs to resupply? Setting this to 'false' will make the actor resume attack after reloading. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackTesla
**Implements the charge-then-burst attack logic specific to the RA tesla coil.**

> Inherits from: `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MaxCharges | 1 | Integer | How many charges this actor has to attack with, once charged. |
| ReloadDelay | 120 | Integer | Reload time for all charges (in ticks). |
| InitialChargeDelay | 22 | Integer | Delay for initial charge attack (in ticks). |
| ChargeDelay | 3 | Integer | Delay between charge attacks (in ticks). |
| ChargeAudio |  | String | Sound to play when actor charges. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Chronoshiftable
**Can be teleported via Chronoshift power.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ExplodeInstead | False | Boolean | Should the actor die instead of being teleported? |
| DamageTypes |  | Collection of DamageType | Types of damage that this trait causes to self when 'ExplodeInstead' is true or the return-to-origin is blocked. Leave empty for no damage types. |
| ChronoshiftSound | chrono2.aud | String |  |
| ReturnToOrigin | True | Boolean | Should the actor return to its previous location after the chronoshift wore out? |
| TimeBarColor | FFFFFF | Color (RRGGBB[AA] notation) | The color the bar of the 'return-to-origin' logic has. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ChronoshiftPostProcessEffect
**Apply palette full screen rotations during chronoshifts. Add this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ChronoEffectLength | 60 | Integer | Measured in ticks. |

### ChronoshiftPower

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Dimensions | 0,0 | 2D Cell Vector | Size of the footprint of the affected area. |
| Footprint | *(required)* | String | Actual footprint. Cells marked as x will be affected. |
| Duration | 750 | Integer | Ticks until returning after teleportation. |
| TargetOverlayPalette | terrain | String |  |
| FootprintImage | overlay | String |  |
| ValidFootprintSequence | target-valid | String |  |
| InvalidFootprintSequence | target-invalid | String |  |
| SourceFootprintSequence | target-select | String |  |
| KillCargo | True | Boolean |  |
| SelectionCursor | chrono-select | String | Cursor to display when selecting targets for the chronoshift. |
| TargetCursor | chrono-target | String | Cursor to display when targeting an area for the chronoshift. |
| TargetBlockedCursor | move-blocked | String | Cursor to display when the targeted area is blocked. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | ChronoshiftPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ChronoVortexRenderer
**Render chrono vortex**

### ClassicFacingBodyOrientation
**Fudge the coordinate system angles like the early games (for sprite sequences that use classic facing fudge).**

> Inherits from: [`BodyOrientation`](#bodyorientation).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| QuantizedFacings | -1 | Integer | Number of facings for gameplay calculations. -1 indicates auto-detection from another trait. |
| CameraPitch | 113 | 1D World Angle | Camera pitch for rotation calculations. |
| UseClassicPerspectiveFudge | True | Boolean | Fudge the coordinate system angles to simulate non-top-down perspective in mods with square cells. |

### Cloneable
**Actors with the "ClonesProducedUnits" trait will produce a free duplicate of me.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types | *(required)* | Collection of CloneableType | This unit's cloneable type is: |

### ClonesProducedUnits
**Creates a free duplicate of produced units.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Exit`](#exit), [`Production`](#production).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CloneableTypes | *(required)* | Collection of CloneableType | Uses the "Cloneable" trait to determine whether or not we should clone a produced unit. |
| ProductionType | *(required)* | String | e.g. Infantry, Vehicles, Aircraft, Buildings |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ConyardChronoReturn
**Implements the special case handling for the Chronoshiftable return on a construction yard. If ReturnOriginalActorOnCondition evaluates true and the actor is not being sold then OriginalActor will be returned to the origin. Otherwise, a vortex animation is played and damage is dealt each tick, ignoring modifiers.**

> Requires trait(s): [`Health`](#health), [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition |  | String | Condition to grant while the vortex animation plays. |
| Damage | 1000 | Integer | Amount of damage to apply each tick while the vortex animation plays. |
| DamageTypes |  | Collection of DamageType | Apply the damage using these damagetypes. |
| ReturnOriginalActorOnCondition |  | BooleanExpression | Boolean expression defining the condition under which to teleport a replacement actor instead of triggering the vortex. |
| OriginalActor | mcv | String | Replacement actor to create when ReturnOriginalActorOnCondition evaluates true. |
| Facing | 384 | 1D World Angle | Facing of the returned actor. |
| ChronoshiftSound | chrono2.aud | String |  |
| TimeBarColor | FFFFFF | Color (RRGGBB[AA] notation) | The color the bar of the 'return-to-origin' logic has. |

### Disguise
**Provides access to the disguise command, which makes the actor appear to be another player's actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Voice | Action | String |  |
| DisguisedCondition |  | String | The condition to grant to self while disguised. |
| ValidRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships the owner of the disguise target needs. |
| TargetTypes | Disguise | Collection of TargetableType | Target types of actors that this actor disguise as. |
| RevealDisguiseOn | Attack | [`RevealDisguiseType`](#revealdisguisetype) | Triggers which cause the actor to drop it's disguise. Possible values: None, Attack, Damaged, Unload, Infiltrate, Demolish, Move. |
| DisguisedAsConditions |  | Dictionary with Key: String, Value: String | Conditions to grant when disguised as specified actor. A dictionary of [actor id]: [condition]. |
| Cursor | ability | String | Cursor to display when hovering over a valid actor to disguise as. |

### DisguiseTooltip
**Overrides the default Tooltip when this actor is disguised (aids in deceiving enemy players).**

> Inherits from: [`Tooltip`](#tooltip), `TooltipInfoBase`, `ConditionalTrait`.

> Requires trait(s): [`Disguise`](#disguise).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| GenericName |  | String | An optional generic name (i.e. "Soldier" or "Structure")to be shown to chosen players. |
| GenericStancePrefix | True | Boolean | Prefix generic tooltip name with 'Ally/Neutral/EnemyPrefix'. |
| AllyPrefix | label-tooltip-prefix.ally | String | Prefix to display in the tooltip for allied units. |
| NeutralPrefix |  | String | Prefix to display in the tooltip for neutral units. |
| EnemyPrefix | label-tooltip-prefix.enemy | String | Prefix to display in the tooltip for enemy units. |
| GenericVisibility | None | [`PlayerRelationship`](#playerrelationship) | Player stances that the generic name should be shown to. |
| ShowOwnerRow | True | Boolean | Show the actor's owner and their faction flag |
| Name | *(required)* | String |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DrainPrerequisitePowerOnDamage
**Converts damage to a charge level of a GrantPrerequisiteChargeDrainPower.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| OrderName | GrantPrerequisiteChargeDrainPowerInfoOrder | String | The OrderName of the GrantPrerequisiteChargeDrainPower to drain. |
| DamageMultiplier | 1 | Integer | Damage is multiplied by this number when converting damage to drain ticks. |
| DamageDivisor | 600 | Integer | Damage is divided by this number when converting damage to drain ticks. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DropPodsPower

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UnitTypes | *(required)* | Collection of String | Drop pod unit |
| Drops | 5,8 | 2D Integer | Number of drop pods spawned. |
| PodFacing | 128 | 1D World Angle | Sets the approach direction. |
| PodScatter | 3 | Integer | Maximum offset from targetLocation |
| EntryEffect | podring | String | Effect sequence sprite image |
| EntryEffectSequence | idle | String | Effect sequence to display in the air. |
| EntryEffectPalette | effect | String |  |
| CameraActor |  | String | Actor to spawn when the attack starts |
| CameraRemoveDelay | 25 | Integer | Number of ticks to keep the camera alive |
| Weapon | Vulcan2 | String | Which weapon to fire |
| WeaponDelay | 0 | Integer | Apply the weapon impact this many ticks into the effect |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | DropPodsPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### EdibleByLeap
**Allows this actor to be the target of an attack leap.**

### EnergyWall
**Will open and be passable for actors that appear friendly when there are no enemies in range.**

> Inherits from: [`Building`](#building).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Weapon | *(required)* | String | The weapon to attack units on top of the wall with when activated. |
| ActiveCondition |  | BooleanExpression | Boolean expression defining the condition to activate this trait. |
| TerrainTypes |  | Set of String | Where you are allowed to place the building (Water, Clear, ...) |
| Footprint |  | Dictionary with Key: 2D Cell Vector, Value: FootprintCellType (enum) | x means cell is blocked, capital X means blocked but not counting as targetable,  = means part of the footprint but passable, _ means completely empty. |
| Dimensions | 1,1 | 2D Cell Vector |  |
| LocalCenterOffset | 0,0,0 | 3D World Vector | Shift center of the actor by this offset. |
| RequiresBaseProvider | False | Boolean |  |
| AllowInvalidPlacement | False | Boolean |  |
| AllowPlacementOnResources | False | Boolean |  |
| RemoveSmudgesOnBuild | True | Boolean | Clear smudges from underneath the building footprint. |
| RemoveSmudgesOnSell | True | Boolean | Clear smudges from underneath the building footprint on sell. |
| RemoveSmudgesOnTransform | True | Boolean | Clear smudges from underneath the building footprint on transform. |
| BuildSounds |  | Collection of String |  |
| UndeploySounds |  | Collection of String |  |

### FrozenUnderFogUpdatedByGps
**Updates frozen actors of actors that change owners, are sold or die whilst having an active GPS power.**

> Requires trait(s): [`FrozenUnderFog`](#frozenunderfog).

### GpsDot
**Show an indicator revealing the actor underneath the fog when a GPSWatcher is activated.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image | gpsdot | String | Sprite collection for symbols. |
| String | Infantry | String | Sprite used for this actor. |
| IndicatorPalettePrefix | player | String |  |

### GpsPower
**Requires `GpsWatcher` on the player actor.**

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RevealDelay | 0 | Integer | Delay in ticks between launching and revealing the map. |
| DoorImage | atek | String |  |
| DoorSequence | active | String |  |
| DoorPalette | player | String | Palette to use for rendering the launch animation |
| DoorPaletteIsPlayerPalette | True | Boolean | Custom palette is a player palette BaseName |
| SatelliteImage | sputnik | String |  |
| SatelliteSequence | idle | String |  |
| SatellitePalette | player | String | Palette to use for rendering the satellite projectile |
| SatellitePaletteIsPlayerPalette | True | Boolean | Custom palette is a player palette BaseName |
| RequiresActiveRadar | True | Boolean | Requires an actor with an online `ProvidesRadar` to show GPS dots. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | GpsPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GpsWatcher
**Required for `GpsPower`. Attach this to the player actor.**

### GrantConditionOnJumpjetLayer

> Inherits from: `GrantConditionOnLayer`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to grant to self when changing to specific custom layer. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantPrerequisiteChargeDrainPower
**Grants a prerequisite while discharging at a configurable rate.**

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DischargeModifier | 300 | Integer | Rate at which the power discharges compared to charging |
| Prerequisite | *(required)* | String | The prerequisite type that this provides. |
| ActiveText | ACTIVE | String | Label to display over the support power icon and in its tooltip while the power is active. |
| AvailableText | READY | String | Label to display over the support power icon and in its tooltip while the power is available but not active. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | GrantPrerequisiteChargeDrainPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### HarvesterHuskModifier

> Requires trait(s): [`Harvester`](#harvester).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| FullHuskActor |  | String |  |
| FullnessThreshold | 50 | Integer |  |

### InfiltrateForCash
**Funds are transferred from the owner to the infiltrator.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Collection of TargetableType | The `TargetTypes` from `Targetable` that are allowed to enter. |
| Percentage | 100 | Integer | Percentage of the victim's resources that will be stolen. |
| Minimum | -1 | Integer | Amount of guaranteed funds to claim when the victim does not have enough resources. When negative, the production price of the infiltrating actor will be used instead. |
| Maximum | 2147483647 | Integer | Maximum amount of funds which will be stolen. |
| PlayerExperience | 0 | Integer | Experience to grant to the infiltrating player. |
| PlayerExperiencePercentage | 0 | Integer | Experience to grant to the infiltrating player based on cash stolen. |
| InfiltratedNotification |  | String | Sound the victim will hear when they get robbed. |
| InfiltratedTextNotification |  | String | Text notification the victim will see when they get robbed. |
| InfiltrationNotification |  | String | Sound the perpetrator will hear after successful infiltration. |
| InfiltrationTextNotification |  | String | Text notification the perpetrator will see after successful infiltration. |
| ShowTicks | True | Boolean | Whether to show the cash tick indicators rising from the actor. |

### InfiltrateForDecoration
**Reveals a decoration sprite to the indicated players when infiltrated.**

> Inherits from: [`WithDecoration`](#withdecoration), `WithDecorationBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Collection of TargetableType | The `TargetTypes` from `Targetable` that are allowed to enter. |
| PlayerExperience | 0 | Integer | Experience to grant to the infiltrating player. |
| Image |  | String | Image used for this decoration. Defaults to the actor's type. |
| Sequence | *(required)* | String | Sequence used for this decoration (can be animated). |
| Palette | chrome | String | Palette to render the sprite in. Reference the world actor's PaletteFrom* traits. |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### InfiltrateForExploration
**Steal and reset the owner's exploration.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Collection of TargetableType | The `TargetTypes` from `Targetable` that are allowed to enter. |
| PlayerExperience | 0 | Integer | Experience to grant to the infiltrating player. |
| InfiltratedNotification |  | String | Sound the victim will hear when they get sabotaged. |
| InfiltratedTextNotification |  | String | Text notification the victim will see when they get sabotaged. |
| InfiltrationNotification |  | String | Sound the perpetrator will hear after successful infiltration. |
| InfiltrationTextNotification |  | String | Text notification the perpetrator will see after successful infiltration. |

### InfiltrateForPowerOutage

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Collection of TargetableType | The `TargetTypes` from `Targetable` that are allowed to enter. |
| Duration | 500 | Integer | Measured in ticks. |
| PlayerExperience | 0 | Integer | Experience to grant to the infiltrating player. |
| InfiltratedNotification |  | String | Sound the victim will hear when they get sabotaged. |
| InfiltratedTextNotification |  | String | Text notification the victim will see when they get sabotaged. |
| InfiltrationNotification |  | String | Sound the perpetrator will hear after successful infiltration. |
| InfiltrationTextNotification |  | String | Text notification the perpetrator will see after successful infiltration. |

### InfiltrateForSupportPower

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Proxy | *(required)* | String |  |
| Types |  | Collection of TargetableType | The `TargetTypes` from `Targetable` that are allowed to enter. |
| PlayerExperience | 0 | Integer | Experience to grant to the infiltrating player. |
| InfiltratedNotification |  | String | Sound the victim will hear when technology gets stolen. |
| InfiltratedTextNotification |  | String | Text notification the victim will see when technology gets stolen. |
| InfiltrationNotification |  | String | Sound the perpetrator will hear after successful infiltration. |
| InfiltrationTextNotification |  | String | Text notification the perpetrator will see after successful infiltration. |

### InfiltrateForSupportPowerReset

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Collection of TargetableType | The `TargetTypes` from `Targetable` that are allowed to enter. |
| InfiltratedNotification |  | String | Sound the victim will hear when they get sabotaged. |
| PlayerExperience | 0 | Integer | Experience to grant to the infiltrating player. |
| InfiltratedTextNotification |  | String | Text notification the victim will see when they get sabotaged. |
| InfiltrationNotification |  | String | Sound the perpetrator will hear after successful infiltration. |
| InfiltrationTextNotification |  | String | Text notification the perpetrator will see after successful infiltration. |

### InfiltrateForTransform
**Transform into a different actor type.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IntoActor | *(required)* | String |  |
| ForceHealthPercentage | 0 | Integer |  |
| SkipMakeAnims | True | Boolean |  |
| PlayerExperience | 0 | Integer | Experience to grant to the infiltrating player. |
| Types |  | Collection of TargetableType | The `TargetTypes` from `Targetable` that are allowed to enter. |

### Infiltrates

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Collection of TargetableType | The `TargetTypes` from `Targetable` that are allowed to enter. |
| Voice | Action | String |  |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| ValidRelationships | Enemy, Neutral | [`PlayerRelationship`](#playerrelationship) | Player relationships the owner of the infiltration target needs. |
| EnterBehaviour | Dispose | [`EnterBehaviour`](#enterbehaviour) | Behaviour when entering the target. Possible values are Exit, Suicide, Dispose. |
| Notification |  | String | Notification to play when a target is infiltrated. |
| TextNotification |  | String | Text notification to display when a target is infiltrated. |
| EnterCursor | enter | String | Cursor to display when able to infiltrate the target actor. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### IonCannonPower

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CameraActor |  | String | Actor to spawn when the attack starts |
| CameraRemoveDelay | 25 | Integer | Number of ticks to keep the camera alive |
| Effect | ionsfx | String | Effect sequence sprite image |
| EffectSequence | idle | String | Effect sequence to display |
| EffectPalette | effect | String |  |
| Weapon | IonCannon | String | Which weapon to fire |
| WeaponDelay | 7 | Integer | Apply the weapon impact this many ticks into the effect |
| OnFireSound |  | String | Sound to instantly play at the targeted area. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | IonCannonPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### JumpjetActorLayer

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TerrainType | Jumpjet | String | Terrain type of the airborne layer. |
| HeightOffset | 3c920 | 1D World Distance | Height offset relative to the smoothed terrain for movement. |
| SmoothingRadius | 2 | Integer | Cell radius for smoothing adjacent cell heights. |

### JumpjetLocomotor
**Used by Mobile. Required for jumpjet actors. Attach these to the world actor. You can have multiple variants by adding @suffixes.**

> Inherits from: [`Locomotor`](#locomotor).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| JumpjetTransitionCost | 0 | Int16 | Pathfinding cost for taking off or landing. |
| JumpjetTransitionTerrainTypes |  | Set of String | The terrain types that this actor can transition on. Leave empty to allow any. |
| JumpjetTransitionOnRamps | True | Boolean | Can this actor transition on slopes? |
| Name | default | String | Locomotor ID. |
| WaitAverage | 40 | Integer |  |
| WaitSpread | 10 | Integer |  |
| SharesCell | False | Boolean | Allow multiple (infantry) units in one cell. |
| MoveIntoShroud | True | Boolean | Can the actor be ordered to move in to shroud? |
| Crushes |  | Collection of CrushClass | e.g. crate, wall, infantry |
| CrushDamageTypes |  | Collection of DamageType | Types of damage that are caused while crushing. Leave empty for no damage types. |
| TerrainSpeeds |  | Dictionary with Key: String, Value: TerrainInfo | Lower the value on rough terrain. Leave out entries for impassable terrain. |

### LightPaletteRotator
**Palette effect used for blinking "animations" on actors.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ExcludePalettes |  | Set of String | Palettes this effect should not apply to. |
| TimeStep | 0.5 | Real Number | 'Speed' at which the effect cycles through palette indices. |
| ModifyIndex | 103 | Integer | Palette index to map to rotating color indices. |
| RotationIndices | 230, 231, 232, 233, 234, 235, 236, 237, 238, 239, 238, 237, 236, 235, 234, 233, 232, 231 | Collection of Integer | Palette indices to rotate through. |

### MadTank

> Requires trait(s): [`Explodes`](#explodes), [`WithFacingSpriteBody`](#withfacingspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ThumpSequence | piston | String |  |
| ThumpInterval | 8 | Integer |  |
| ThumpDamageWeapon | MADTankThump | String |  |
| ChargeDelay | 96 | Integer | Measured in ticks. |
| ChargeSound | madchrg2.aud | String |  |
| DetonationDelay | 42 | Integer | Measured in ticks. |
| DetonationSound | madexplo.aud | String |  |
| DetonationWeapon | MADTankDetonate | String |  |
| DriverActor | e1 | String |  |
| Voice | Action | String |  |
| DeployedCondition |  | String | The condition to grant to self while deployed. |
| DamageTypes |  | Collection of DamageType | Types of damage that this trait causes to self while self-destructing. Leave empty for no damage types. |
| AttackCursor | attack | String | Cursor to display when targeting. |
| DeployCursor | deploy | String | Cursor to display when able to set up the detonation sequence. |

### ModelRenderer
**Render voxels**

### PortableChrono

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ChargeDelay | 500 | Integer | Cooldown in ticks until the unit can teleport. |
| HasDistanceLimit | True | Boolean | Can the unit teleport only a certain distance? |
| MaxDistance | 12 | Integer | The maximum distance in cells this unit can teleport (only used if HasDistanceLimit = true). |
| ChronoshiftSound | chrotnk1.aud | String | Sound to play when teleporting. |
| DeployCursor | deploy | String | Cursor to display when able to deploy the actor. |
| DeployBlockedCursor | deploy-blocked | String | Cursor to display when unable to deploy the actor. |
| TargetCursor | chrono-target | String | Cursor to display when targeting a teleport location. |
| TargetBlockedCursor | move-blocked | String | Cursor to display when the targeted location is blocked. |
| KillCargo | True | Boolean | Kill cargo on teleporting. |
| FlashScreen | False | Boolean | Flash the screen on teleporting. |
| Voice | Action | String |  |
| CircleColor | 7CFC0080 | Color (RRGGBB[AA] notation) | Range circle color. |
| CircleWidth | 1 | Real Number | Range circle line width. |
| CircleBorderColor | 00000060 | Color (RRGGBB[AA] notation) | Range circle border color. |
| CircleBorderWidth | 3 | Real Number | Range circle border width. |
| TargetLineColor | 7CFC00 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ResourcePurifier
**Gives additional cash when resources are delivered to refineries.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 0 | Integer | Percentage value of the resource to grant as cash. |
| ShowTicks | True | Boolean | Whether to show the cash tick indicators rising from the actor. |
| TickLifetime | 30 | Integer | How long the cash ticks stay on the screen. |
| TickRate | 10 | Integer | How often the cash ticks can appear. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ShroudPalette
**Adds the hard-coded shroud palette to the game**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | shroud | String | Internal palette name |
| Fog | False | Boolean | Palette type |

### TDGunboat

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Speed | 28 | Integer |  |
| InitialFacing | 256 | 1D World Angle | Facing to use when actor spawns. Only 256 and 768 supported. |
| PreviewFacing | 256 | 1D World Angle | Facing to use for actor previews (map editor, color picker, etc). Only 256 and 768 supported. |

### TransferTimedExternalConditionOnTransform
**A special case trait that re-grants a timed external condition when this actor transforms. This trait does not work with permanently granted external conditions. This trait changes the external condition source, so cannot be used for conditions that may later be revoked**

> Requires trait(s): [`Transforms`](#transforms).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | External condition to transfer |

### TransformsNearResources
**Replace with another actor when a resource spawns adjacent.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IntoActor | *(required)* | String |  |
| Offset | 0,0 | 2D Cell Vector |  |
| SkipMakeAnims | False | Boolean | Don't render the make animation. |
| Type | *(required)* | String | Resource type which triggers the transformation. |
| Density | 1 | Integer | Resource density threshold which is required. |
| Adjacency | 1 | Integer | This many adjacent resource tiles are required. |
| Delay | 1000, 3000 | Collection of Integer | The range of time (in ticks) until the transformation starts. |

### TSEditorResourceLayer

> Inherits from: [`EditorResourceLayer`](#editorresourcelayer).

> Requires trait(s): [`EditorActorLayer`](#editoractorlayer).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| VeinType | Veins | String |  |
| VeinholeActors |  | Set of String | Actor types that should be treated as veins for adjacency. |
| ResourceTypes |  | Dictionary with Key: String, Value: ResourceTypeInfo |  |
| RecalculateResourceDensity | False | Boolean | Override the density saved in maps with values calculated based on the number of neighbouring resource cells. |

### TSResourceLayer

> Inherits from: [`ResourceLayer`](#resourcelayer).

> Requires trait(s): [`BuildingInfluence`](#buildinginfluence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| VeinType | Veins | String |  |
| VeinholeActors |  | Set of String | Actor types that should be treated as veins for adjacency. |
| ResourceTypes |  | Dictionary with Key: String, Value: ResourceTypeInfo |  |
| RecalculateResourceDensity | False | Boolean | Override the density saved in maps with values calculated based on the number of neighbouring resource cells. |

### TSShroudPalette
**Adds the hard-coded shroud palette to the game**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | shroud | String | Internal palette name |

### TSTiberiumRenderer
**Renders the Tiberian Sun Tiberium resources. Attach this to the world actor**

> Inherits from: [`ResourceRenderer`](#resourcerenderer).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Ramp1Sequences |  | Dictionary with Key: String, Value: Collection of String | Sequences to use for ramp type 1. Dictionary of [resource type]: [list of sequences]. |
| Ramp2Sequences |  | Dictionary with Key: String, Value: Collection of String | Sequences to use for ramp type 2. Dictionary of [resource type]: [list of sequences]. |
| Ramp3Sequences |  | Dictionary with Key: String, Value: Collection of String | Sequences to use for ramp type 3. Dictionary of [resource type]: [list of sequences]. |
| Ramp4Sequences |  | Dictionary with Key: String, Value: Collection of String | Sequences to use for ramp type 4. Dictionary of [resource type]: [list of sequences]. |
| ResourceTypes |  | Dictionary with Key: String, Value: ResourceTypeInfo |  |

### TSVeinsRenderer
**Renders the Tiberian Sun Vein resources. Attach this to the world actor**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ResourceType | *(required)* | String | Resource type used for veins. |
| Image | resources | String | Sequence image that holds the different variants. |
| Sequence | veins | String | Vein sequence name. |
| Palette | terrain | String | Palette used for rendering the resource sprites. |
| Name | *(required)* | String | Resource name used by tooltips. |
| VeinholeActors |  | Set of String | Actor types that should be treated as veins for adjacency. |

### VoxelCache
**Loads voxel models.**

### VoxelNormalsPalette

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | normals | String |  |
| Type | TiberianSun | [`NormalType`](#normaltype) | Can be TiberianSun or RedAlert2 |

### WithBuildingBib

> Requires trait(s): [`Building`](#building), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | bib | String |  |
| Palette | terrain | String |  |
| HasMinibib | False | Boolean |  |

### WithResourceAnimation
**Allows to play animations on resources. Attach this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types | *(required)* | Set of String | Resource types to animate. |
| Ratio | 1, 10 | Collection of Integer | The percentage of resource cells to play the animation on. Use two values to randomize between them. |
| Interval | 200, 500 | Collection of Integer | Tick interval between two animation spawning. Use two values to randomize between them. |
| Image | *(required)* | String | Animation image. |
| Sequences | idle | Collection of String | Randomly select one of these sequences to render. |
| Palette |  | String | Animation palette. |

## OpenRA.Mods.Cnc.Traits.Render

### RenderVoxels

> Requires trait(s): [`BodyOrientation`](#bodyorientation).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image |  | String | Defaults to the actor name. |
| Palette |  | String | Custom palette name |
| PlayerPalette | player | String | Custom PlayerColorPalette: BaseName |
| NormalsPalette | normals | String |  |
| ShadowPalette | shadow | String |  |
| Scale | 12 | Real Number | Change the image size. |
| LightPitch | 142 | 1D World Angle |  |
| LightYaw | 682 | 1D World Angle |  |
| LightAmbientColor | 0.6, 0.6, 0.6 | Collection of Real Number |  |
| LightDiffuseColor | 0.4, 0.4, 0.4 | Collection of Real Number |  |

### WithCargo
**Renders the cargo loaded into the unit.**

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`Cargo`](#cargo).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| LocalOffset | 0,0,0 | Collection of 3D World Vector | Cargo position relative to turret or body in (forward, right, up) triples. The default offset should be in the middle of the list. |
| DisplayTypes |  | Set of String | Passenger CargoType to display. |

### WithDisguisingInfantryBody

> Inherits from: [`WithInfantryBody`](#withinfantrybody), `ConditionalTrait`.

> Requires trait(s): [`Disguise`](#disguise), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MinIdleDelay | 30 | Integer |  |
| MaxIdleDelay | 110 | Integer |  |
| MoveSequence | run | String |  |
| DefaultAttackSequence |  | String |  |
| AttackSequences |  | Dictionary with Key: String, Value: Collection of String | Attack sequence to use for each armament. A dictionary of [armament name]: [sequence name(s)]. Multiple sequence names can be defined to specify per-burst animations. |
| IdleSequences |  | Collection of String |  |
| StandSequences | stand | Collection of String |  |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithEmbeddedTurretSpriteBody
**This actor has turret art with facings baked into the sprite.**

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites), [`Turreted`](#turreted).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| QuantizedFacings | -1 | Integer | Number of facings for gameplay calculations. -1 indicates auto-detection from the sequence. |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithGunboatBody

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites), [`Turreted`](#turreted).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Turret | primary | String | Turreted 'Turret' key to display |
| LeftSequence | left | String |  |
| RightSequence | right | String |  |
| WakeLeftSequence | wake-left | String |  |
| WakeRightSequence | wake-right | String |  |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithHarvesterSpriteBody

> Inherits from: [`WithFacingSpriteBody`](#withfacingspritebody), [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`Harvester`](#harvester), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ImageByFullness |  | Collection of String | Images switched between depending on fullness of harvester. Overrides RenderSprites.Image. |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithLandingCraftAnimation

> Requires trait(s): [`Cargo`](#cargo), [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| OpenTerrainTypes | Clear | Set of String |  |
| OpenSequence | open | String |  |
| CloseSequence | close | String |  |
| UnloadSequence | unload | String |  |
| Body | body | String | Which sprite body to play the animation on. |

### WithSplitAttackPaletteInfantryBody

> Inherits from: [`WithInfantryBody`](#withinfantrybody), `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SplitAttackPalette |  | String | Palette to use for the split attack rendering. |
| SplitAttackSuffix | muzzle | String | Sequence suffix to use. |
| MinIdleDelay | 30 | Integer |  |
| MaxIdleDelay | 110 | Integer |  |
| MoveSequence | run | String |  |
| DefaultAttackSequence |  | String |  |
| AttackSequences |  | Dictionary with Key: String, Value: Collection of String | Attack sequence to use for each armament. A dictionary of [armament name]: [sequence name(s)]. Multiple sequence names can be defined to specify per-burst animations. |
| IdleSequences |  | Collection of String |  |
| StandSequences | stand | Collection of String |  |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithTeslaChargeAnimation
**This actor displays a charge-up animation before firing.**

> Requires trait(s): [`RenderSprites`](#rendersprites), [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ChargeSequence | active | String | Sequence to use for charge animation. |
| Body | body | String | Which sprite body to play the animation on. |

### WithTeslaChargeOverlay
**Rendered together with AttackCharge.**

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | active | String | Sequence name to use |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |

### WithVoxelBarrel

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Armament`](#armament), [`RenderVoxels`](#rendervoxels), [`Turreted`](#turreted).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | barrel | String | Voxel sequence name to use |
| Armament | primary | String | Armament to use for recoil |
| LocalOffset | 0,0,0 | 3D World Vector | Visual offset |
| LocalOrientation | 0,0,0 | 3D World Rotation | Rotate the barrel relative to the body |
| ShowShadow | True | Boolean | Defines if the Voxel should have a shadow. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithVoxelBody
**Also returns a default selection size that is calculated automatically from the voxel dimensions.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`RenderVoxels`](#rendervoxels).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | idle | String |  |
| Offset | 0,0,0 | 3D World Vector |  |
| ShowShadow | True | Boolean | Defines if the Voxel should have a shadow. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithVoxelTurret

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`RenderVoxels`](#rendervoxels), [`Turreted`](#turreted).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | turret | String | Voxel sequence name to use |
| Turret | primary | String | Turreted 'Turret' key to display |
| ShowShadow | True | Boolean | Defines if the Voxel should have a shadow. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithVoxelUnloadBody

> Requires trait(s): [`RenderVoxels`](#rendervoxels).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UnloadSequence | unload | String | Voxel sequence name to use when docked to a refinery. |
| IdleSequence | idle | String | Voxel sequence name to use when undocked from a refinery. |
| ShowShadow | True | Boolean | Defines if the Voxel should have a shadow. |

### WithVoxelWalkerBody

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`RenderVoxels`](#rendervoxels).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | idle | String |  |
| TickRate | 5 | Integer | The speed of the walker's legs. |
| ShowShadow | True | Boolean | Defines if the Voxel should have a shadow. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

## OpenRA.Mods.Common.Commands

### ChatCommands
**Enables commands triggered by typing them into the chatbox. Attach this to the world actor.**

### DebugVisualizationCommands
**Enables visualization commands via the chatbox. Attach this to the world actor.**

### DevCommands
**Enables developer cheats via the chatbox. Attach this to the world actor.**

### HelpCommand
**Shows a list of available commands in the chatbox. Attach this to the world actor.**

### PlayerCommands
**Allows the player to pause or surrender the game via the chatbox. Attach this to the world actor.**

## OpenRA.Mods.Common.Scripting

### LuaScript
**Part of the new Lua API.**

> Requires trait(s): [`SpawnMapActors`](#spawnmapactors).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Scripts |  | Set of String | File names with location relative to the map. |

### ScriptTriggers
**Allows map scripts to attach triggers to this actor via the Triggers global.**

## OpenRA.Mods.Common.Traits

### AcceptsDeliveredCash
**Tag trait for actors with `DeliversCash`.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValidTypes |  | Set of String | Accepted `DeliversCash` types. Leave empty to accept all types. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships the owner of the delivering actor needs. |
| Sounds |  | Collection of String | Play a randomly selected sound from this list when accepting cash. |

### AcceptsDeliveredExperience
**Tag trait for actors with `DeliversExperience`.**

> Requires trait(s): [`GainsExperience`](#gainsexperience).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValidTypes |  | Set of String | Accepted `DeliversExperience` types. Leave empty to accept all types. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships the owner of the delivering actor needs. |

### ActorMap

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BinSize | 10 | Integer | Size of partition bins (cells) |

### ActorPreviewPlaceBuildingPreview
**Creates a building placement preview based on the map editor actor preview.**

> Inherits from: [`FootprintPlaceBuildingPreview`](#footprintplacebuildingpreview).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Animated | True | Boolean | Enable the building's idle animation. |
| PreviewAlpha | 1 | Real Number | Custom opacity to apply to the actor preview. |
| FootprintUnderPreview | Valid, LineBuild | [`PlaceBuildingCellType`](#placebuildingcelltype) | Footprint types to draw underneath the actor preview. |
| FootprintOverPreview | Invalid | [`PlaceBuildingCellType`](#placebuildingcelltype) | Footprint types to draw above the actor preview. |
| ZOffset | 0 | Integer | Custom ZOffset of the rendered building preview. |
| Palette | terrain | String | Palette to use for rendering the placement sprite. |
| FootprintAlpha | 1 | Real Number | Custom opacity to apply to the placement sprite. |
| LineBuildFootprintAlpha | 1 | Real Number | Custom opacity to apply to the line-build placement sprite. |

### ActorSpawner
**An actor with this trait indicates a valid spawn point for actors of ActorSpawnManager.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Set of String | Type of ActorSpawner with which it connects. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ActorSpawnManager
**Controls the spawning of specified actor types. Attach this to the world actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`MapCreeps`](#mapcreeps).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Minimum | 0 | Integer | Minimum number of actors. |
| Maximum | 4 | Integer | Maximum number of actors. |
| InitialDelay | 0 | Integer | Initial delay before first actor is spawn |
| SpawnInterval | 6000 | Collection of Integer | Time (in ticks) between actor spawn. Supports 1 or 2 values. If 2 values are provided they are used as a range from which a value is randomly selected. |
| Actors | *(required)* | Collection of String | Name of the actor that will be randomly picked to spawn. |
| Owner | Creeps | String |  |
| Types |  | Set of String | Type of ActorSpawner with which it connects. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AffectedByPowerOutage
**Disables the actor when a power outage is triggered (see `InfiltrateForPowerOutage` for more information).**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition |  | String | The condition to grant while there is a power outage. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Aircraft

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IdleBehavior | None | [`IdleBehaviorType`](#idlebehaviortype) | Behavior when aircraft becomes idle. Options are Land, ReturnToBase, LeaveMap, and None. 'Land' will behave like 'None' (hover or circle) if a suitable landing site is not available. |
| CruiseAltitude | 1c256 | 1D World Distance |  |
| Repulsable | True | Boolean | Whether the aircraft can be repulsed. |
| IdealSeparation | 1c682 | 1D World Distance | The distance it tries to maintain from other aircraft if repulsable. |
| RepulsionSpeed | -1 | Integer | The speed at which the aircraft is repulsed from other aircraft. Specify -1 for normal movement speed. |
| InitialFacing | 0 | 1D World Angle |  |
| TurnSpeed | 512 | 1D World Angle | Speed at which the actor turns. |
| IdleTurnSpeed |  | 1D World Angle (optional) | Turn speed to apply when aircraft flies in circles while idle. Defaults to TurnSpeed if undefined. |
| TurnDeadzone | 2 | 1D World Angle | When flying if the difference between current facing and desired facing is less than this value, don't turn. This prevents visual jitter. |
| Speed | 1 | Integer | Maximum flight speed when cruising. |
| IdleSpeed | -1 | Integer | If non-negative, force the aircraft to move in circles at this speed when idle (a speed of 0 means don't move), ignoring CanHover. |
| Pitch | 0 | 1D World Angle | Body pitch when flying forwards. Only relevant for voxel aircraft. |
| PitchSpeed | 0 | 1D World Angle | Pitch steps to apply each tick when starting/stopping. |
| Roll | 0 | 1D World Angle | Body roll when turning. Only relevant for voxel aircraft. |
| IdleRoll |  | 1D World Angle (optional) | Body roll to apply when aircraft flies in circles while idle. Defaults to Roll if undefined. Only relevant for voxel aircraft. |
| RollSpeed | 0 | 1D World Angle | Roll steps to apply each tick when turning. |
| MinAirborneAltitude | 1 | Integer | Minimum altitude where this aircraft is considered airborne. |
| LandableTerrainTypes |  | Set of String |  |
| MoveIntoShroud | True | Boolean | Can the actor be ordered to move in to shroud? |
| Crushes |  | Collection of CrushClass | e.g. crate, wall, infantry |
| CrushDamageTypes |  | Collection of DamageType | Types of damage that are caused while crushing. Leave empty for no damage types. |
| Voice | Action | String |  |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line for regular move orders. |
| AirborneCondition |  | String | The condition to grant to self while airborne. |
| CruisingCondition |  | String | The condition to grant to self while at cruise altitude. |
| CanHover | False | Boolean | Can the actor hover in place mid-air? If not, then the actor will have to remain in motion (circle around). |
| CanSlide | False | Boolean | Can the actor immediately change direction without turning first (doesn't need to fly in a curve)? |
| VTOL | False | Boolean | Does the actor land and take off vertically? |
| TurnToLand | False | Boolean | Does this VTOL actor need to turn before landing (on terrain)? |
| TakeOffOnResupply | False | Boolean | Does this actor automatically take off after resupplying? |
| TakeOffOnCreation | True | Boolean | Does this actor automatically take off after creation? |
| CanForceLand | True | Boolean | Can this actor be given an explicit land order using the force-move modifier? |
| LandAltitude | 0c0 | 1D World Distance | Altitude at which the aircraft considers itself landed. |
| LandRange | 5c0 | 1D World Distance | Range to search for an alternative landing location if the ordered cell is blocked. |
| MaximumPitch | 28 | 1D World Angle | How fast this actor ascends or descends during horizontal movement. |
| AltitudeVelocity | 0c43 | 1D World Distance | How fast this actor ascends or descends when moving vertically only (vertical take off/landing or hovering towards CruiseAltitude). |
| TakeoffSounds |  | Collection of String | Sounds to play when the actor is taking off. |
| LandingSounds |  | Collection of String | Sounds to play when the actor is landing. |
| WaitDistanceFromResupplyBase | 3c0 | 1D World Distance | The distance of the resupply base that the aircraft will wait for its turn. |
| NumberOfTicksToVerifyAvailableAirport | 150 | Integer | The number of ticks that a airplane will wait to make a new search for an available airport. |
| PreviewFacing | 384 | 1D World Angle | Facing to use for actor previews (map editor, color picker, etc) |
| EditorFacingDisplayOrder | 3 | Integer | Display order for the facing slider in the map editor |
| RequireForceMoveCondition |  | BooleanExpression | Boolean expression defining the condition under which the regular (non-force) move cursor is disabled. |
| Cursor | move | String | Cursor to display when a move order can be issued at target location. |
| BlockedCursor | move-blocked | String | Cursor to display when a move order cannot be issued at target location. |
| EnterCursor | enter | String | Cursor to display when able to land at target building. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to land at target building. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AirstrikePower

> Inherits from: `DirectionalSupportPower`, `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UnitType | badr.bomber | String |  |
| SquadSize | 1 | Integer |  |
| SquadOffset | -1536,1536,0 | 3D World Vector |  |
| QuantizedFacings | 32 | Integer |  |
| Cordon | 5c0 | 1D World Distance |  |
| CameraActor |  | String | Actor to spawn when the aircraft start attacking |
| CameraRemoveDelay | 25 | Integer | Amount of time to keep the camera alive after the aircraft have finished attacking |
| BeaconDistanceOffset | 6c0 | 1D World Distance | Weapon range offset to apply during the beacon clock calculation |
| UseDirectionalTarget | False | Boolean | Enables the player directional targeting |
| Arrows | arrow-t, arrow-tl, arrow-l, arrow-bl, arrow-b, arrow-br, arrow-r, arrow-tr | Collection of String |  |
| DirectionArrowAnimation |  | String | Animation used to render the direction arrows. |
| DirectionArrowPalette | chrome | String | Palette for direction cursor animation. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | AirstrikePowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AllyRepair
**Attach this to the player actor to allow building repair by team mates.**

### AlwaysVisible
**The actor is always considered visible for targeting and rendering purposes.**

### AmmoPool
**Actor has a limited amount of ammo, after using it all the actor must reload in some way.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | primary | String | Name of this ammo pool, used to link reload traits to this pool. |
| Armaments | primary, secondary | Collection of String | Name(s) of armament(s) that use this pool. |
| Ammo | 1 | Integer | How much ammo does this pool contain when fully loaded. |
| InitialAmmo | -1 | Integer | Initial ammo the actor is created with. Defaults to Ammo. |
| ReloadCount | 1 | Integer | How much ammo is reloaded after a certain period. |
| RearmSound |  | String | Sound to play for each reloaded ammo magazine. |
| ReloadDelay | 50 | Integer | Time to reload per ReloadCount on airfield etc. |
| AmmoCondition |  | String | The condition to grant to self for each ammo point in this pool. |

### AppearsOnMapPreview
**Render this actor when creating the minimap while saving the map.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Color | 00000000 | Color (RRGGBB[AA] notation) | Use this color to render the actor, instead of owner player color. |
| Terrain |  | String | Use this terrain color to render the actor, instead of owner player color. Overrides `Color` if both set. |

### Armament
**Allows you to attach weapons to the unit (use @IdentifierSuffix for > 1)**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | primary | String |  |
| Weapon | *(required)* | String | Has to be defined in weapons.yaml as well. |
| Turret | primary | String | Which turret (if present) should this armament be assigned to. |
| FireDelay | 0 | Integer | Time (in frames) until the weapon can fire again. |
| LocalOffset |  | Collection of 3D World Vector | Muzzle position relative to turret or body, (forward, right, up) triples. If weapon Burst = 1, it cycles through all listed offsets, otherwise the offset corresponding to current burst is used. |
| LocalYaw |  | Collection of 1D World Angle | Muzzle yaw relative to turret or body. |
| Recoil | 0c0 | 1D World Distance | Move the turret backwards when firing. |
| RecoilRecovery | 0c9 | 1D World Distance | Recoil recovery per-frame |
| MuzzleSequence |  | String | Muzzle flash sequence to render |
| MuzzlePalette | effect | String | Palette to render Muzzle flash sequence in |
| ReloadingCondition |  | String | Condition to grant while reloading. |
| TargetRelationships | Enemy | [`PlayerRelationship`](#playerrelationship) |  |
| ForceTargetRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) |  |
| Cursor | attack | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor | attackoutsiderange | String | Cursor to display when hovering over a valid target that is outside of range. |
| AmmoUsage | 1 | Integer | Ammo the weapon consumes per shot. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Armor
**Used to define weapon efficiency modifiers with different percentages per Type.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type |  | String |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackAircraft

> Inherits from: [`AttackFollow`](#attackfollow), `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Aircraft`](#aircraft).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AttackType | Default | [`AirAttackType`](#airattacktype) | Attack behavior. Currently supported types are: Default: Attack while following the default movement rules. Hover: Hover, even if the Aircraft can't hover while idle. Strafe: Perform a fixed-length attack run on the target. |
| StrafeRunLength | 0c0 | 1D World Distance | Distance the strafing aircraft makes to a target before turning for another pass. When set to WDist.Zero this defaults to the maximum armament range. |
| OpportunityFire | True | Boolean | Automatically acquire and fire on targets of opportunity when not actively attacking. |
| PersistentTargeting | True | Boolean | Keep firing on targets even after attack order is cancelled |
| RangeMargin | 1c0 | 1D World Distance | Range to stay away from min and max ranges to give some leeway if the target starts moving. |
| AbortOnResupply | True | Boolean | Does this actor cancel its attack activity when it needs to resupply? Setting this to 'false' will make the actor resume attack after reloading. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackBomber
**Trait used for scripted actors or actors spawned by a support power.**

> Inherits from: `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackCharges
**Actor must charge up its armaments before firing.**

> Inherits from: [`AttackOmni`](#attackomni), `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ChargeLevel | 25 | Integer | Amount of charge required to attack. |
| ChargeRate | 1 | Integer | Amount to increase the charge level each tick with a valid target. |
| DischargeRate | 1 | Integer | Amount to decrease the charge level each tick without a valid target. |
| ChargingCondition |  | String | The condition to grant to self while the charge level is greater than zero. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackFollow
**Actor will follow units until in range to attack them.**

> Inherits from: `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| OpportunityFire | True | Boolean | Automatically acquire and fire on targets of opportunity when not actively attacking. |
| PersistentTargeting | True | Boolean | Keep firing on targets even after attack order is cancelled |
| RangeMargin | 1c0 | 1D World Distance | Range to stay away from min and max ranges to give some leeway if the target starts moving. |
| AbortOnResupply | True | Boolean | Does this actor cancel its attack activity when it needs to resupply? Setting this to 'false' will make the actor resume attack after reloading. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackFrontal
**Unit got to face the target**

> Inherits from: `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackGarrisoned
**Cargo can fire their weapons out of fire ports.**

> Inherits from: [`AttackFollow`](#attackfollow), `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Cargo`](#cargo).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PortOffsets | *(required)* | Collection of 3D World Vector | Fire port offsets in local coordinates. |
| PortYaws | *(required)* | Collection of 1D World Angle | Fire port yaw angles. |
| PortCones | *(required)* | Collection of 1D World Angle | Fire port yaw cone angle. |
| MuzzlePalette | effect | String |  |
| OpportunityFire | True | Boolean | Automatically acquire and fire on targets of opportunity when not actively attacking. |
| PersistentTargeting | True | Boolean | Keep firing on targets even after attack order is cancelled |
| RangeMargin | 1c0 | 1D World Distance | Range to stay away from min and max ranges to give some leeway if the target starts moving. |
| AbortOnResupply | True | Boolean | Does this actor cancel its attack activity when it needs to resupply? Setting this to 'false' will make the actor resume attack after reloading. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackMove
**Provides access to the attack-move command, which will make the actor automatically engage viable targets while moving to the destination.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Voice | Action | String |  |
| TargetLineColor | FF4500 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackMoveCondition |  | String | The condition to grant to self while an attack-move is active. |
| AssaultMoveCondition |  | String | The condition to grant to self while an assault-move is active. |
| MoveIntoShroud | True | Boolean | Can the actor be ordered to move in to shroud? |
| AttackMoveCursor | attackmove | String |  |
| AttackMoveBlockedCursor | attackmove-blocked | String |  |
| AssaultMoveCursor | assaultmove | String |  |
| AssaultMoveBlockedCursor | assaultmove-blocked | String |  |

### AttackOmni

> Inherits from: `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackTurreted
**Actor has a visual turret used to attack.**

> Inherits from: [`AttackFollow`](#attackfollow), `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Turreted`](#turreted).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Turrets | primary | Collection of String | Turret names |
| OpportunityFire | True | Boolean | Automatically acquire and fire on targets of opportunity when not actively attacking. |
| PersistentTargeting | True | Boolean | Keep firing on targets even after attack order is cancelled |
| RangeMargin | 1c0 | 1D World Distance | Range to stay away from min and max ranges to give some leeway if the target starts moving. |
| AbortOnResupply | True | Boolean | Does this actor cancel its attack activity when it needs to resupply? Setting this to 'false' will make the actor resume attack after reloading. |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttackWander
**Will AttackMove to a random location within MoveRadius when idle. This conflicts with player orders and should only be added to animal creeps.**

> Inherits from: [`Wanders`](#wanders), `ConditionalTrait`.

> Requires trait(s): [`AttackMove`](#attackmove).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| WanderMoveRadius | 1 | Integer |  |
| ReduceMoveRadiusDelay | 5 | Integer | Number of ticks to wait before decreasing the effective move radius. |
| MinMoveDelay | 0 | Integer | Minimum amount of ticks the actor will sit idly before starting to wander. |
| MaxMoveDelay | 0 | Integer | Maximum amount of ticks the actor will sit idly before starting to wander. |
| AvoidTerrainTypes |  | Set of String | The terrain types that this actor should avoid wandering on to. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AutoCarryable
**Can be carried by units with the trait `Carryall`.**

> Inherits from: [`Carryable`](#carryable), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MinDistance | 6c0 | 1D World Distance | Required distance away from destination before requesting a pickup. Default is 6 cells. |
| ReservedCondition |  | String | The condition to grant to self while a carryall has been reserved. |
| CarriedCondition |  | String | The condition to grant to self while being carried. |
| LockedCondition |  | String | The condition to grant to self while being locked for carry. |
| LocalOffset | 0,0,0 | 3D World Vector | Carryall attachment point relative to body. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AutoCarryall
**Automatically transports harvesters with the AutoCarryable and CarryableHarvester between resource fields and refineries.**

> Inherits from: [`Carryall`](#carryall), `ConditionalTrait`.

> Requires trait(s): [`Aircraft`](#aircraft), [`BodyOrientation`](#bodyorientation).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AutoCarryCondition |  | BooleanExpression | Boolean expression defining the condition under which the auto carry behavior is enabled. Enabled by default. |
| InitialActor |  | String | Actor type that is initially spawned into this actor. |
| BeforeLoadDelay | 0 | Integer | Delay (in ticks) on the ground while attaching an actor to the carryall. |
| BeforeUnloadDelay | 0 | Integer | Delay (in ticks) on the ground while detaching an actor from the carryall. |
| LocalOffset | 0,0,0 | 3D World Vector | Carryable attachment point relative to body. |
| DropRange | 5c0 | 1D World Distance | Radius around the target drop location that are considered if the target tile is blocked. |
| UnloadCursor | deploy | String | Cursor to display when able to unload the passengers. |
| UnloadBlockedCursor | deploy-blocked | String | Cursor to display when unable to unload the passengers. |
| AllowDropOff | False | Boolean | Allow moving and unloading with one order using force-move |
| DropOffCursor | ability | String | Cursor to display when able to drop off the passengers at location. |
| DropOffBlockedCursor | move-blocked | String | Cursor to display when unable to drop off the passengers at location. |
| PickUpCursor | ability | String | Cursor to display when picking up the passengers. |
| CarryCondition |  | String | Condition to grant to the Carryall while it is carrying something. |
| CarryableConditions |  | Dictionary with Key: String, Value: String | Conditions to grant when a specified actor is being carried. A dictionary of [actor name]: [condition]. |
| Voice | Action | String |  |
| TargetLineColor | FFFF00 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AutoCrusher

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ScanRadius | 5c0 | 1D World Distance | Maximum range to scan for targets. |
| MinimumScanTimeInterval | 10 | Integer | The minimal amount of ticks to wait between scanning for targets. |
| MaximumScanTimeInterval | 15 | Integer | The maximal amount of ticks to wait between scanning for targets. |
| CrushClasses |  | Collection of CrushClass | The crush class(es) that can be automatically crushed. |
| TargetRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships the owner of the actor needs to get targeted. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AutoTarget
**The actor will automatically engage the enemy when it is in range.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AllowMovement | True | Boolean | It will try to hunt down the enemy if it is set to AttackAnything. |
| AllowTurning | True | Boolean | It will try to pivot to face the enemy if stance is not HoldFire. |
| ScanOnIdle | True | Boolean | Scan for new targets when idle. |
| ScanRadius | -1 | Integer | Set to a value >1 to override weapons maximum range for this. |
| InitialStanceAI | AttackAnything | [`UnitStance`](#unitstance) | Possible values are HoldFire, ReturnFire, Defend and AttackAnything. Used for computer-controlled players, both Lua-scripted and regular Skirmish AI alike. |
| InitialStance | Defend | [`UnitStance`](#unitstance) | Possible values are HoldFire, ReturnFire, Defend and AttackAnything. Used for human players. |
| HoldFireCondition |  | String | The condition to grant to self while in the HoldFire stance. |
| ReturnFireCondition |  | String | The condition to grant to self while in the ReturnFire stance. |
| DefendCondition |  | String | The condition to grant to self while in the Defend stance. |
| AttackAnythingCondition |  | String | The condition to grant to self while in the AttackAnything stance. |
| EnableStances | True | Boolean | Allow the player to change the unit stance. |
| MinimumScanTimeInterval | 3 | Integer | Ticks to wait until next AutoTarget: attempt. |
| MaximumScanTimeInterval | 8 | Integer | Ticks to wait until next AutoTarget: attempt. |
| EditorStanceDisplayOrder | 1 | Integer | Display order for the stance dropdown in the map editor |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AutoTargetPriority
**Specifies the target types and relative priority used by AutoTarget to decide what to target.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`AutoTarget`](#autotarget).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValidTargets | Ground, Water, Air | Collection of TargetableType | Target types that can be AutoTargeted. |
| InvalidTargets |  | Collection of TargetableType | Target types that can't be AutoTargeted. Overrules ValidTargets. |
| ValidRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | Relationships between actor's and target's owner needed for AutoTargeting. |
| Priority | 1 | Integer | ValidTargets with larger priorities will be AutoTargeted before lower priorities. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### BaseAttackNotifier
**Plays an audio notification and shows a radar ping when a building is attacked. Attach this to the player actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| NotifyInterval | 30000 | Integer | Minimum duration (in milliseconds) between notification events. |
| RadarPingColor | FF0000 | Color (RRGGBB[AA] notation) |  |
| RadarPingDuration | 250 | Integer | Length of time (in ticks) to display a location ping in the minimap. |
| Notification | BaseAttack | String | Speech notification type to play. |
| TextNotification |  | String | Text notification to display. |
| AllyNotification |  | String | Speech notification to play to allies when under attack. Won't play a notification to allies if this is null. |
| AllyTextNotification |  | String | Text notification to display to allies when under attack. |

### BaseBuilderBotModule
**Manages AI base construction.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ConstructionYardTypes |  | Set of String | Tells the AI what building types are considered construction yards. |
| VehiclesFactoryTypes |  | Set of String | Tells the AI what building types are considered vehicle production facilities. |
| RefineryTypes |  | Set of String | Tells the AI what building types are considered refineries. |
| PowerTypes |  | Set of String | Tells the AI what building types are considered power plants. |
| BarracksTypes |  | Set of String | Tells the AI what building types are considered infantry production facilities. |
| ProductionTypes |  | Set of String | Tells the AI what building types are considered production facilities. |
| NavalProductionTypes |  | Set of String | Tells the AI what building types are considered naval production facilities. |
| SiloTypes |  | Set of String | Tells the AI what building types are considered silos (resource storage). |
| DefenseTypes |  | Set of String | Tells the AI what building types are considered defenses. |
| BuildingQueues | Building | Set of String | Production queues AI uses for buildings. |
| DefenseQueues | Defense | Set of String | Production queues AI uses for defenses. |
| MinBaseRadius | 2 | Integer | Minimum distance in cells from center of the base when checking for building placement. |
| MaxBaseRadius | 20 | Integer | Radius in cells around the center of the base to expand. |
| MinimumExcessPower | 0 | Integer | Minimum excess power the AI should try to maintain. |
| MaximumExcessPower | 0 | Integer | The targeted excess power the AI tries to maintain cannot rise above this. |
| ExcessPowerIncrement | 0 | Integer | Increase maintained excess power by this amount for every ExcessPowerIncreaseThreshold of base buildings. |
| ExcessPowerIncreaseThreshold | 1 | Integer | Increase maintained excess power by ExcessPowerIncrement for every N base buildings. |
| InititalMinimumRefineryCount | 1 | Integer | Number of refineries to build before building a barracks. |
| AdditionalMinimumRefineryCount | 1 | Integer | Number of refineries to build additionally after building a barracks. |
| StructureProductionInactiveDelay | 125 | Integer | Additional delay (in ticks) between structure production checks when there is no active production. StructureProductionRandomBonusDelay is added to this. |
| StructureProductionActiveDelay | 25 | Integer | Additional delay (in ticks) added between structure production checks when actively building things. Note: this should be at least as large as the typical order latency to avoid duplicated build choices. |
| StructureProductionRandomBonusDelay | 10 | Integer | A random delay (in ticks) of up to this is added to active/inactive production delays. |
| StructureProductionResumeDelay | 1500 | Integer | Delay (in ticks) until retrying to build structure after the last 3 consecutive attempts failed. |
| MaximumFailedPlacementAttempts | 3 | Integer | After how many failed attempts to place a structure should AI give up and wait for StructureProductionResumeDelay before retrying. |
| MaxResourceCellsToCheck | 3 | Integer | How many randomly chosen cells with resources to check when deciding refinery placement. |
| CheckForNewBasesDelay | 1500 | Integer | Delay (in ticks) until rechecking for new BaseProviders. |
| PlaceDefenseTowardsEnemyChance | 100 | Integer | Chance that the AI will place the defenses in the direction of the closest enemy building. |
| MinimumDefenseRadius | 5 | Integer | Minimum range at which to build defensive structures near a combat hotspot. |
| MaximumDefenseRadius | 20 | Integer | Maximum range at which to build defensive structures near a combat hotspot. |
| NewProductionCashThreshold | 5000 | Integer | Try to build another production building if there is too much cash. |
| RallyPointScanRadius | 8 | Integer | Radius in cells around a factory scanned for rally points by the AI. |
| CheckForWaterRadius | 8 | Integer | Radius in cells around each building with ProvideBuildableArea to check for a 3x3 area of water where naval structures can be built. Should match maximum adjacency of naval structures. |
| WaterTerrainTypes | Water | Set of String | Terrain types which are considered water for base building purposes. |
| BuildingFractions |  | Dictionary with Key: String, Value: Integer | What buildings to the AI should build. What integer percentage of the total base must be this type of building. |
| BuildingLimits |  | Dictionary with Key: String, Value: Integer | What buildings should the AI have a maximum limit to build. |
| BuildingDelays |  | Dictionary with Key: String, Value: Integer | When should the AI start building specific buildings. |
| ProductionMinCashRequirement | 500 | Integer | Only queue construction of a new structure when above this requirement. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### BaseBuilding
**Tag trait for construction yard and MCVs. Used by the cycle bases hotkey to identify actors.**

### BaseProvider
**Limits the zone where buildings can be constructed to a radius around this actor.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Range | 10c0 | 1D World Distance |  |
| Cooldown | 0 | Integer |  |
| InitialDelay | 0 | Integer |  |
| CircleReadyColor | FFFFFF80 | Color (RRGGBB[AA] notation) | Range circle color when operational. |
| CircleBlockedColor | FF000080 | Color (RRGGBB[AA] notation) | Range circle color when inactive. |
| CircleWidth | 1 | Real Number | Range circle line width. |
| CircleBorderColor | 00000060 | Color (RRGGBB[AA] notation) | Range circle border color. |
| CircleBorderWidth | 3 | Real Number | Range circle border width. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### BlocksProjectiles
**This actor blocks bullets and missiles with 'Blockable' property.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Height | 1c0 | 1D World Distance |  |
| ValidRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | Determines what projectiles to block based on their allegiance to the wall owner. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### BodyOrientation

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| QuantizedFacings | -1 | Integer | Number of facings for gameplay calculations. -1 indicates auto-detection from another trait. |
| CameraPitch | 113 | 1D World Angle | Camera pitch for rotation calculations. |
| UseClassicPerspectiveFudge | True | Boolean | Fudge the coordinate system angles to simulate non-top-down perspective in mods with square cells. |

### BridgeHut
**Allows bridges to be targeted for demolition and repair.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types | GroundLevelBridge | Collection of String | Bridge types to act on |
| NeighbourOffsets |  | Collection of 2D Cell Vector | Offsets to look for adjacent bridges to act on |
| RepairPropagationDelay | 20 | Integer | Delay between each segment repair step |
| DemolishPropagationDelay | 5 | Integer | Delay between each segment demolish step |
| RequireForceAttackForHeal | False | Boolean | Hide the repair cursor if the bridge is only damaged (not destroyed) |

### Bridge

> Requires trait(s): [`Building`](#building), [`Health`](#health).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Long | False | Boolean |  |
| RepairPropagationDelay | 20 | Integer | Delay (in ticks) between repairing adjacent spans in long bridges |
| Template | 0 | UInt16 |  |
| DamagedTemplate | 0 | UInt16 |  |
| DestroyedTemplate | 0 | UInt16 |  |
| DestroyedPlusNorthTemplate | 0 | UInt16 |  |
| DestroyedPlusSouthTemplate | 0 | UInt16 |  |
| DestroyedPlusBothTemplate | 0 | UInt16 |  |
| ShorePieces | br1, br2 | Collection of String |  |
| NorthOffset |  | Collection of Integer |  |
| SouthOffset |  | Collection of Integer |  |
| DemolishWeapon | Demolish | String | The name of the weapon to use when demolishing the bridge |
| DamageTypes |  | Collection of DamageType | Types of damage that this bridge causes to units over/in path of it while being destroyed/repaired. Leave empty for no damage types. |

### BridgeLayer

### BridgePlaceholder
**Placeholder actor used for dead segments and bridge end ramps.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | GroundLevelBridge | String |  |
| DamageState | Undamaged | [`DamageState`](#damagestate) |  |
| ReplaceWithActor |  | String | Actor type to replace with on repair. |
| NeighbourOffsets |  | Collection of 2D Cell Vector |  |

### Buildable

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Prerequisites |  | Collection of String | The prerequisite names that must be available before this can be built. This can be prefixed with ! to invert the prerequisite (disabling production if the prerequisite is available) and/or ~ to hide the actor from the production palette if the prerequisite is not available. Prerequisites are granted by actors with the ProvidesPrerequisite trait. |
| Queue |  | Set of String | Production queue(s) that can produce this. |
| BuildAtProductionType |  | String | Override the production structure type (from the Production Produces list) that this unit should be built at. |
| BuildLimit | 0 | Integer | Disable production when there are more than this many of this actor on the battlefield. Set to 0 to disable. |
| ForceFaction |  | String | Force a specific faction variant, overriding the faction of the producing actor. |
| Icon | icon | String | Sequence of the actor that contains the icon. |
| IconPalette | chrome | String | Palette used for the production icon. |
| IconPaletteIsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| BuildDuration | -1 | Integer | Base build time in frames (-1 indicates to use the unit's Value). |
| BuildDurationModifier | 60 | Integer | Percentage modifier to apply to the build duration. |
| BuildPaletteOrder | 9999 | Integer | Sort order for the production palette. Smaller numbers are presented earlier. |
| Description |  | String | Text shown in the production tooltip. |

### BuildableTerrainOverlay

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AllowedTerrainTypes | *(required)* | Set of String |  |
| Palette | terrain | String | Palette to use for rendering the sprite. |
| Image | overlay | String | Sprite definition. |
| Sequence | build-invalid | String | Sequence to use for unbuildable area. |
| Alpha | 1 | Real Number | Custom opacity to apply to the overlay sprite. |

### BuildingInfluence
**A dictionary of buildings placed on the map. Attach this to the world actor.**

### Building

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TerrainTypes |  | Set of String | Where you are allowed to place the building (Water, Clear, ...) |
| Footprint |  | Dictionary with Key: 2D Cell Vector, Value: FootprintCellType (enum) | x means cell is blocked, capital X means blocked but not counting as targetable,  = means part of the footprint but passable, _ means completely empty. |
| Dimensions | 1,1 | 2D Cell Vector |  |
| LocalCenterOffset | 0,0,0 | 3D World Vector | Shift center of the actor by this offset. |
| RequiresBaseProvider | False | Boolean |  |
| AllowInvalidPlacement | False | Boolean |  |
| AllowPlacementOnResources | False | Boolean |  |
| RemoveSmudgesOnBuild | True | Boolean | Clear smudges from underneath the building footprint. |
| RemoveSmudgesOnSell | True | Boolean | Clear smudges from underneath the building footprint on sell. |
| RemoveSmudgesOnTransform | True | Boolean | Clear smudges from underneath the building footprint on transform. |
| BuildSounds |  | Collection of String |  |
| UndeploySounds |  | Collection of String |  |

### BuildingRepairBotModule
**Manages AI repairing base buildings.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Capturable
**This actor can be captured by a unit with Captures: trait. This trait should not be disabled if the actor also uses FrozenUnderFog.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`CaptureManager`](#capturemanager).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types | *(required)* | Collection of CaptureType | CaptureTypes (from the Captures trait) that are able to capture this. |
| CancelActivity | False | Boolean | Cancel the actor's current activity when getting captured. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CapturableProgressBar
**Visualize capture progress.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Capturable`](#capturable).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Color | FFA500 | Color (RRGGBB[AA] notation) |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CapturableProgressBlink
**Blinks the actor and captor when it is being captured.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Capturable`](#capturable).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Interval | 50 | Integer | Number of ticks to wait between repeating blinks. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CaptureManagerBotModule
**Manages AI capturing logic.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CapturingActorTypes |  | Set of String | Actor types that can capture other actors (via `Captures`). Leave this empty to disable capturing. |
| CapturableActorTypes |  | Set of String | Actor types that can be targeted for capturing. Leave this empty to include all actors. |
| MinimumCaptureDelay | 375 | Integer | Minimum delay (in ticks) between trying to capture with CapturingActorTypes. |
| MaximumCaptureTargetOptions | 10 | Integer | Maximum number of options to consider for capturing. If a value less than 1 is given 1 will be used instead. |
| CheckCaptureTargetsForVisibility | True | Boolean | Should visibility (Shroud, Fog, Cloak, etc) be considered when searching for capturable targets? |
| CapturableRelationships | Enemy, Neutral | [`PlayerRelationship`](#playerrelationship) | Player relationships that capturers should attempt to target. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CaptureManager
**Manages Captures and Capturable traits on an actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CapturingCondition |  | String | Condition granted when capturing an actor. |
| BeingCapturedCondition |  | String | Condition granted when being captured by another actor. |
| PreventsAutoTarget | True | Boolean | Should units friendly to the capturing actor auto-target this actor while it is being captured? |

### CaptureProgressBar
**Visualize the progress of this actor being captured.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Captures`](#captures).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Color | FFA500 | Color (RRGGBB[AA] notation) |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Captures
**This actor can capture other actors which have the Capturable: trait.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`CaptureManager`](#capturemanager).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CaptureTypes | *(required)* | Collection of CaptureType | Types of actors that it can capture, as long as the type also exists in the Capturable Type: trait. |
| SabotageThreshold | 0 | Integer | Targets with health above this percentage will be sabotaged instead of captured. Set to 0 to disable sabotaging. |
| SabotageHPRemoval | 50 | Integer | Sabotage damage expressed as a percentage of maximum target health. |
| SabotageDamageTypes |  | Collection of DamageType | Damage types that applied with the sabotage damage. |
| CaptureDelay | 0 | Integer | Delay (in ticks) that to wait next to the target before initiating the capture. |
| ConsumedByCapture | True | Boolean | Enter the target actor and be consumed by the capture. |
| PlayerExperience | 0 | Integer | Experience granted to the capturing player. |
| ValidRelationships | Enemy, Neutral | [`PlayerRelationship`](#playerrelationship) | What player relationships the target's owner needs to be captured by this actor. |
| PlayerExperienceRelationships | Enemy | [`PlayerRelationship`](#playerrelationship) | Relationships that the structure's previous owner needs to have for the capturing player to receive Experience. |
| SabotageCursor | capture | String | Cursor to display when the health of the target actor is above the sabotage threshold. |
| EnterCursor | enter | String | Cursor to display when able to capture the target actor. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to capture the target actor. |
| Voice | Action | String |  |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Cargo
**This actor can transport Passenger actors.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MaxWeight | 0 | Integer | The maximum sum of Passenger.Weight that this actor can support. |
| Types |  | Set of String | `Passenger.CargoType`s that can be loaded into this actor. |
| InitialUnits |  | Collection of String | A list of actor types that are initially spawned into this actor. |
| EjectOnSell | True | Boolean | When this actor is sold should all of its passengers be unloaded? |
| EjectOnDeath | False | Boolean | When this actor dies should all of its passengers be unloaded? |
| UnloadTerrainTypes |  | Set of String | Terrain types that this actor is allowed to eject actors onto. Leave empty for all terrain types. |
| UnloadVoice | Action | String | Voice to play when ordered to unload the passengers. |
| LoadRange | 5c0 | 1D World Distance | Radius to search for a load/unload location if the ordered cell is blocked. |
| PassengerFacing | 512 | 1D World Angle | Which direction the passenger will face (relative to the transport) when unloading. |
| AfterLoadDelay | 8 | Integer | Delay (in ticks) before continuing after loading a passenger. |
| BeforeUnloadDelay | 8 | Integer | Delay (in ticks) before unloading the first passenger. |
| AfterUnloadDelay | 25 | Integer | Delay (in ticks) before continuing after unloading a passenger. |
| UnloadCursor | deploy | String | Cursor to display when able to unload the passengers. |
| UnloadBlockedCursor | deploy-blocked | String | Cursor to display when unable to unload the passengers. |
| LoadingCondition |  | String | The condition to grant to self while waiting for cargo to load. |
| LoadedCondition |  | String | The condition to grant to self while passengers are loaded. Condition can stack with multiple passengers. |
| PassengerConditions |  | Dictionary with Key: String, Value: String | Conditions to grant when specified actors are loaded inside the transport. A dictionary of [actor name]: [condition]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CarryableHarvester

### Carryable
**Can be carried by actors with the `Carryall` trait.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ReservedCondition |  | String | The condition to grant to self while a carryall has been reserved. |
| CarriedCondition |  | String | The condition to grant to self while being carried. |
| LockedCondition |  | String | The condition to grant to self while being locked for carry. |
| LocalOffset | 0,0,0 | 3D World Vector | Carryall attachment point relative to body. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Carryall
**Transports actors with the `Carryable` trait.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Aircraft`](#aircraft), [`BodyOrientation`](#bodyorientation).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| InitialActor |  | String | Actor type that is initially spawned into this actor. |
| BeforeLoadDelay | 0 | Integer | Delay (in ticks) on the ground while attaching an actor to the carryall. |
| BeforeUnloadDelay | 0 | Integer | Delay (in ticks) on the ground while detaching an actor from the carryall. |
| LocalOffset | 0,0,0 | 3D World Vector | Carryable attachment point relative to body. |
| DropRange | 5c0 | 1D World Distance | Radius around the target drop location that are considered if the target tile is blocked. |
| UnloadCursor | deploy | String | Cursor to display when able to unload the passengers. |
| UnloadBlockedCursor | deploy-blocked | String | Cursor to display when unable to unload the passengers. |
| AllowDropOff | False | Boolean | Allow moving and unloading with one order using force-move |
| DropOffCursor | ability | String | Cursor to display when able to drop off the passengers at location. |
| DropOffBlockedCursor | move-blocked | String | Cursor to display when unable to drop off the passengers at location. |
| PickUpCursor | ability | String | Cursor to display when picking up the passengers. |
| CarryCondition |  | String | Condition to grant to the Carryall while it is carrying something. |
| CarryableConditions |  | Dictionary with Key: String, Value: String | Conditions to grant when a specified actor is being carried. A dictionary of [actor name]: [condition]. |
| Voice | Action | String |  |
| TargetLineColor | FFFF00 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CashTrickler
**Lets the actor generate cash in a set periodic time.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Interval | 50 | Integer | Number of ticks to wait between giving money. |
| InitialDelay | 0 | Integer | Number of ticks to wait before giving first money. |
| Amount | 15 | Integer | Amount of money to give each time. |
| ShowTicks | True | Boolean | Whether to show the cash tick indicators rising from the actor. |
| DisplayDuration | 30 | Integer | How long to show the cash tick indicator when enabled. |
| UseResourceStorage | False | Boolean | Use resource storage for cash granted. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CashTricklerMultiplier
**Modifies the cash given by cash tricker traits of this actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`CashTrickler`](#cashtrickler).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CellTriggerOverlay
**Renders a debug overlay showing the script triggers. Attach this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Font | BigBold | String |  |
| Color | FF0000 | Color (RRGGBB[AA] notation) |  |

### ChangesHealth
**Attach this to actors which should regenerate or lose health points over time.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Step | 5 | Integer | Absolute amount of health points added in each step. Use negative values to apply damage. |
| PercentageStep | 0 | Integer | Relative percentages of health added in each step. Use negative values to apply damage. When both values are defined, their summary will be applied. |
| Delay | 5 | Integer | Time in ticks to wait between each health modification. |
| StartIfBelow | 50 | Integer | Heal if current health is below this percentage of full health. |
| DamageCooldown | 0 | Integer | Time in ticks to wait after taking damage. |
| DamageTypes |  | Collection of DamageType | Apply the health change when encountering these damage types. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ChangesTerrain
**Modifies the terrain type underneath the actors location.**

> Requires trait(s): [`Immobile`](#immobile).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TerrainType | *(required)* | String |  |

### ClassicParallelProductionQueue
**Attach this to the player actor (not a building!) to define a new shared build queue. Will only work together with the Production: trait on the actor that actually does the production. You will also want to add PrimaryBuildings: to let the user choose where new units should exit. The production speed depends on the number of production buildings and units queued at the same time.**

> Inherits from: [`ProductionQueue`](#productionqueue).

> Requires trait(s): [`PlayerResources`](#playerresources), [`TechTree`](#techtree).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SpeedUp | False | Boolean | If you build more actors of the same type, the same queue will get its build time lowered for every actor produced there. |
| BuildingCountBuildTimeMultipliers | 100, 86, 75, 67, 60, 55, 50 | Collection of Integer | Every time another production building of the same queue is constructed, the build times of all actors in the queue modified by a percentage of the original time. |
| ParallelPenaltyBuildTimeMultipliers | 100, 116, 133, 150, 166, 183, 200, 216, 233, 250 | Collection of Integer | Build time modifier multiplied by the number of parallel production for producing different actors at the same time. |
| Type | *(required)* | String | What kind of production will be added (e.g. Building, Infantry, Vehicle, ...) |
| DisplayOrder | 0 | Integer | The value used when ordering this for display (e.g. in the Spectator UI). |
| Group |  | String | Group queues from separate buildings together into the same tab. |
| Factions |  | Set of String | Only enable this queue for certain factions. |
| Sticky | True | Boolean | Should the prerequisite remain enabled if the owner changes? |
| PayUpFront | False | Boolean | Player must pay for item upfront |
| DisallowPaused | False | Boolean | Should right clicking on the icon instantly cancel the production instead of putting it on hold? |
| BuildDurationModifier | 100 | Integer | This percentage value is multiplied with actor cost to translate into build time (lower means faster). |
| ItemLimit | 999 | Integer | Maximum number of a single actor type that can be queued (0 = infinite). |
| QueueLimit | 0 | Integer | Maximum number of items that can be queued across all actor types (0 = infinite). |
| LowPowerModifier | 100 | Integer | The build time is multiplied with this percentage on low power. |
| InfiniteBuildLimit | -1 | Integer | Production items that have more than this many items in the queue will be produced in a loop. |
| ReadyAudio |  | String | Notification played when production is complete. The filename of the audio is defined per faction in notifications.yaml. |
| ReadyTextNotification |  | String | Notification displayed when production is complete. |
| BlockedAudio |  | String | Notification played when you can't train another actor when the build limit exceeded or the exit is jammed. The filename of the audio is defined per faction in notifications.yaml. |
| BlockedTextNotification |  | String | Notification displayed when you can't train another actor when the build limit exceeded or the exit is jammed. |
| LimitedAudio |  | String | Notification played when you can't queue another actor when the queue length limit is exceeded. The filename of the audio is defined per faction in notifications.yaml. |
| LimitedTextNotification |  | String | Notification displayed when you can't queue another actor when the queue length limit is exceeded. |
| CannotPlaceAudio |  | String | Notification played when you can't place a building. Overrides PlaceBuilding.CannotPlaceNotification for this queue. The filename of the audio is defined per faction in notifications.yaml. |
| QueuedAudio |  | String | Notification played when user clicks on the build palette icon. The filename of the audio is defined per faction in notifications.yaml. |
| QueuedTextNotification |  | String | Notification displayed when user clicks on the build palette icon. |
| OnHoldAudio |  | String | Notification played when player right-clicks on the build palette icon. The filename of the audio is defined per faction in notifications.yaml. |
| OnHoldTextNotification |  | String | Notification displayed when player right-clicks on the build palette icon. |
| CancelledAudio |  | String | Notification played when player right-clicks on a build palette icon that is already on hold. The filename of the audio is defined per faction in notifications.yaml. |
| CancelledTextNotification |  | String | Notification displayed when player right-clicks on a build palette icon that is already on hold. |

### ClassicProductionQueue
**Attach this to the player actor (not a building!) to define a new shared build queue. Will only work together with the Production: trait on the actor that actually does the production. You will also want to add PrimaryBuildings: to let the user choose where new units should exit.**

> Inherits from: [`ProductionQueue`](#productionqueue).

> Requires trait(s): [`PlayerResources`](#playerresources), [`TechTree`](#techtree).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SpeedUp | False | Boolean | If you build more actors of the same type, the same queue will get its build time lowered for every actor produced there. |
| BuildTimeSpeedReduction | 100, 86, 75, 67, 60, 55, 50 | Collection of Integer | Every time another production building of the same queue is constructed, the build times of all actors in the queue decreased by a percentage of the original time. |
| Type | *(required)* | String | What kind of production will be added (e.g. Building, Infantry, Vehicle, ...) |
| DisplayOrder | 0 | Integer | The value used when ordering this for display (e.g. in the Spectator UI). |
| Group |  | String | Group queues from separate buildings together into the same tab. |
| Factions |  | Set of String | Only enable this queue for certain factions. |
| Sticky | True | Boolean | Should the prerequisite remain enabled if the owner changes? |
| PayUpFront | False | Boolean | Player must pay for item upfront |
| DisallowPaused | False | Boolean | Should right clicking on the icon instantly cancel the production instead of putting it on hold? |
| BuildDurationModifier | 100 | Integer | This percentage value is multiplied with actor cost to translate into build time (lower means faster). |
| ItemLimit | 999 | Integer | Maximum number of a single actor type that can be queued (0 = infinite). |
| QueueLimit | 0 | Integer | Maximum number of items that can be queued across all actor types (0 = infinite). |
| LowPowerModifier | 100 | Integer | The build time is multiplied with this percentage on low power. |
| InfiniteBuildLimit | -1 | Integer | Production items that have more than this many items in the queue will be produced in a loop. |
| ReadyAudio |  | String | Notification played when production is complete. The filename of the audio is defined per faction in notifications.yaml. |
| ReadyTextNotification |  | String | Notification displayed when production is complete. |
| BlockedAudio |  | String | Notification played when you can't train another actor when the build limit exceeded or the exit is jammed. The filename of the audio is defined per faction in notifications.yaml. |
| BlockedTextNotification |  | String | Notification displayed when you can't train another actor when the build limit exceeded or the exit is jammed. |
| LimitedAudio |  | String | Notification played when you can't queue another actor when the queue length limit is exceeded. The filename of the audio is defined per faction in notifications.yaml. |
| LimitedTextNotification |  | String | Notification displayed when you can't queue another actor when the queue length limit is exceeded. |
| CannotPlaceAudio |  | String | Notification played when you can't place a building. Overrides PlaceBuilding.CannotPlaceNotification for this queue. The filename of the audio is defined per faction in notifications.yaml. |
| QueuedAudio |  | String | Notification played when user clicks on the build palette icon. The filename of the audio is defined per faction in notifications.yaml. |
| QueuedTextNotification |  | String | Notification displayed when user clicks on the build palette icon. |
| OnHoldAudio |  | String | Notification played when player right-clicks on the build palette icon. The filename of the audio is defined per faction in notifications.yaml. |
| OnHoldTextNotification |  | String | Notification displayed when player right-clicks on the build palette icon. |
| CancelledAudio |  | String | Notification played when player right-clicks on a build palette icon that is already on hold. The filename of the audio is defined per faction in notifications.yaml. |
| CancelledTextNotification |  | String | Notification displayed when player right-clicks on a build palette icon that is already on hold. |

### CliffBackImpassabilityLayer
**Sets a custom terrain type for cells that are obscured by back-facing cliffs. This trait replicates the default CliffBackImpassability=2 behaviour from the TS/RA2 rules.ini.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TerrainType | Impassable | String |  |

### Cloak
**This unit can cloak and uncloak in specific situations.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| InitialDelay | 10 | Integer | Measured in game ticks. |
| CloakDelay | 30 | Integer | Measured in game ticks. |
| UncloakOn | Attack, Unload, Infiltrate, Demolish, Dock | [`UncloakType`](#uncloaktype) | Events leading to the actor getting uncloaked. Possible values are: Attack, Move, Unload, Infiltrate, Demolish, Dock, Damage, Heal, SelfHeal and SupportPower. 'Dock' is triggered when docking to a refinery or resupplying. 'SupportPower' is triggered when using a support power. |
| CloakSound |  | String |  |
| UncloakSound |  | String |  |
| DetectionTypes | Cloak | Collection of DetectionType |  |
| CloakedCondition |  | String | The condition to grant to self while cloaked. |
| CloakType |  | String | The type of cloak. Same type of cloaks won't trigger cloaking and uncloaking sound and effect. |
| CloakStyle | Alpha | [`CloakStyle`](#cloakstyle) | Render effect to use when cloaked. |
| CloakedAlpha | 0.55 | Real Number | The alpha level to use when cloaked when using Alpha CloakStyle. |
| CloakedColor | 0000008C | Color (RRGGBB[AA] notation) | The color to use when cloaked when using Color CloakStyle. |
| CloakedPalette |  | String | The palette to use when cloaked when using Palette CloakStyle. |
| IsPlayerPalette | False | Boolean | Indicates that CloakedPalette is a player palette when using Palette CloakStyle. |
| EffectImage |  | String | Which image to use for the effect played when cloaking or uncloaking. |
| CloakEffectSequence |  | String | Which effect sequence to play when cloaking. |
| UncloakEffectSequence |  | String | Which effect sequence to play when uncloaking. |
| EffectPalette | effect | String |  |
| EffectPaletteIsPlayerPalette | False | Boolean |  |
| EffectOffset | 0,0,0 | 3D World Vector | Offset for the effect played when cloaking or uncloaking. |
| EffectTracksActor | True | Boolean | Should the effect track the actor. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CloakPaletteEffect

### ColorPickerColorShift
**Create a color picker palette from another palette.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BasePalette | *(required)* | String | The name of the palette to base off. |
| MinHue | 0.29 | Real Number | Hues between this and MaxHue will be shifted. |
| MaxHue | 0.37 | Real Number | Hues between MinHue and this will be shifted. |
| ReferenceHue | 0.33 | Real Number | Hue reference for the color shift. |
| ReferenceSaturation | 0.925 | Real Number | Saturation reference for the color shift. |
| ReferenceValue | 0.95 | Real Number | Value reference for the color shift. |

### ColorPickerManager
**Configuration options for the lobby player color picker. Attach this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| HsvSaturationRange | 0.3, 0.95 | Collection of Real Number | Minimum and maximum saturation levels that are valid for use. |
| HsvValueRange | 0.3, 0.95 | Collection of Real Number | Minimum and maximum value levels that are valid for use. |
| SimilarityThreshold | 80 | Integer | Perceptual color threshold for determining whether two colors are too similar. |
| PresetColors |  | Collection of Color (RRGGBB[AA] notation) | List of colors to be displayed in the palette tab. |
| PreviewActor |  | String | Actor type to show in the color picker. This can be overridden for specific factions with FactionPreviewActors. |
| FactionPreviewActors |  | Dictionary with Key: String, Value: String | Actor type to show in the color picker for specific factions. Overrides PreviewActor. A dictionary of [faction name]: [actor name]. |

### ColorPickerPalette
**Create a color picker palette from another palette.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Internal palette name. |
| BasePalette | *(required)* | String | The name of the palette to base off. |
| RemapIndex |  | Collection of Integer | Remap these indices to player colors. |
| AllowModifiers | True | Boolean | Allow palette modifiers to change the palette. |

### CombatDebugOverlay
**Displays fireports, muzzle offsets, and hit areas in developer mode.**

### CommandBarBlacklist
**Blacklist certain order types to disable on the command bar when this unit is selected.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DisableStop | True | Boolean | Disable the 'Stop' button for this actor. |
| DisableWaypointMode | True | Boolean | Disable the 'Waypoint Mode' button for this actor. |

### ConquestVictoryConditions

> Requires trait(s): [`MissionObjectives`](#missionobjectives).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| NotificationDelay | 1500 | Integer | Delay for the end game notification in milliseconds. |
| Objective | Destroy all opposition! | String | Description of the objective. |
| SuppressNotifications | False | Boolean | Disable the win/loss messages and audio notifications? |

### Contrail
**Draw a colored contrail behind this actor when they move.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| ZOffset | 0 | Integer | Equivalent to sequence ZOffset. Controls Z sorting. |
| TrailLength | 25 | Integer | When set, display a line behind the actor. Length is measured in ticks after appearing. |
| TrailDelay | 0 | Integer | Time (in ticks) after which the line should appear. Controls the distance to the actor. |
| StartWidth | 0c64 | 1D World Distance | Thickness of the emitted line at the start of the contrail. |
| EndWidth |  | 1D World Distance (optional) | Thickness of the emitted line at the end of the contrail. Will default to StartWidth if left undefined |
| StartColor | FFFFFF | Color (RRGGBB[AA] notation) | RGB color at the contrail start. |
| StartColorUsePlayerColor | True | Boolean | Use player remap color instead of a custom color at the contrail the start. |
| StartColorAlpha | 255 | Integer | The alpha value [from 0 to 255] of color at the contrail the start. |
| EndColor |  | Color (RRGGBB[AA] notation) (optional) | RGB color at the contrail end. Will default to StartColor if left undefined |
| EndColorUsePlayerColor | False | Boolean | Use player remap color instead of a custom color at the contrail end. |
| EndColorAlpha | 0 | Integer | The alpha value [from 0 to 255] of color at the contrail end. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ControlGroups

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Groups | 1, 2, 3, 4, 5, 6, 7, 8, 9, 0 | Collection of String |  |

### CrateAction

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Crate

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Duration | 0 | Integer | Length of time (in ticks) until the crate gets removed automatically. A value of zero disables auto-removal. |
| TerrainTypes |  | Set of String | Allowed to land on. |
| CrushClass | crate | String | Define actors that can collect crates by setting this into the Crushes field from the Mobile trait. |

### CrateSpawner

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CheckboxLabel | checkbox-crates.label | String | Descriptive label for the crates checkbox in the lobby. |
| CheckboxDescription | checkbox-crates.description | String | Tooltip description for the crates checkbox in the lobby. |
| CheckboxEnabled | True | Boolean | Default value of the crates checkbox in the lobby. |
| CheckboxLocked | False | Boolean | Prevent the crates state from being changed in the lobby. |
| CheckboxVisible | True | Boolean | Whether to display the crates checkbox in the lobby. |
| CheckboxDisplayOrder | 0 | Integer | Display order for the crates checkbox in the lobby. |
| Minimum | 1 | Integer | Minimum number of crates. |
| Maximum | 255 | Integer | Maximum number of crates. |
| SpawnInterval | 4500 | Integer | Average time (ticks) between crate spawn. |
| InitialSpawnDelay | 0 | Integer | Delay (in ticks) before the first crate spawns. |
| ValidGround | Clear, Rough, Road, Ore, Beach | Set of String | Which terrain types can we drop on? |
| ValidWater | Water | Set of String | Which terrain types count as water? |
| WaterChance | 20 | Integer | Chance of generating a water crate instead of a land crate. |
| CrateActors | crate | Collection of String | Crate actors to drop. |
| CrateActorShares | 10 | Collection of Integer | Chance of each crate actor spawning. |
| DeliveryAircraft |  | String | If a DeliveryAircraft: is specified, then this actor will deliver crates. |
| QuantizedFacings | 32 | Integer | Number of facings that the delivery aircraft may approach from. |
| Cordon | 5c0 | 1D World Distance | Spawn and remove the plane this far outside the map. |

### CreateMapPlayers
**Attach this to the world actor.**

### CreatesShroud

> Inherits from: `AffectsShroud`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValidRelationships | Enemy, Neutral | [`PlayerRelationship`](#playerrelationship) | Relationship the watching player needs to see the generated shroud. |
| MinRange | 0c0 | 1D World Distance |  |
| Range | 0c0 | 1D World Distance |  |
| MaxHeightDelta | -1 | Integer | If >= 0, prevent cells that are this much higher than the actor from being revealed. |
| MoveRecalculationThreshold | 0c256 | 1D World Distance | If > 0, force visibility to be recalculated if the unit moves within a cell by more than this distance. |
| Type | Footprint | [`VisibilityType`](#visibilitytype) | Possible values are CenterPosition (measure range from the center) and  Footprint (measure range from the footprint) |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CreatesShroudMultiplier
**Modifies the shroud range created by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Crushable
**This actor is crushable.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CrushSound |  | String | Sound to play when being crushed. |
| CrushClasses | infantry | Collection of CrushClass | Which crush classes does this actor belong to. |
| WarnProbability | 75 | Integer | Probability of mobile actors noticing and evading a crush attempt. |
| CrushedByFriendlies | False | Boolean | Will friendly units just crush me instead of pathing around. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CustomSellValue
**Allow a non-standard sell/repair value to avoid buy-sell exploits.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Value | 0 | Integer |  |

### CustomTerrainDebugOverlay
**Displays custom terrain types.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Font | TinyBold | String |  |

### DamagedByTerrain
**This actor receives damage from the given weapon when on the specified terrain type.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Damage | 0 | Integer | Amount of damage received per DamageInterval ticks. |
| DamageInterval | 0 | Integer | Delay between receiving damage. |
| DamageTypes |  | Collection of DamageType | Apply the damage using these damagetypes. |
| Terrain | *(required)* | Collection of String | Terrain types where the actor will take damage. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DamageMultiplier
**Modifies the damage applied to this actor. Use 0 to make actor invulnerable.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DeliversCash
**Donate money to actors with the `AcceptsDeliveredCash` trait.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Payload | 500 | Integer | The amount of cash the owner receives. |
| PlayerExperience | 0 | Integer | The amount of experience the donating player receives. |
| Type |  | String | Identifier checked against AcceptsDeliveredCash.ValidTypes. Only needed if the latter is not empty. |
| Sounds |  | Collection of String | Sound to play when delivering cash |
| Cursor | enter | String | Cursor to display when hovering over a valid actor to deliver cash to. |
| Voice | Action | String |  |
| TargetLineColor | FFFF00 | Color (RRGGBB[AA] notation) | Color to use for the target line. |

### DeliversExperience
**This actor can grant experience levels equal to it's own current level via entering to other actors with the `AcceptsDeliveredExperience` trait.**

> Requires trait(s): [`GainsExperience`](#gainsexperience).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PlayerExperience | 0 | Integer | The amount of experience the donating player receives. |
| Type |  | String | Identifier checked against AcceptsDeliveredExperience.ValidTypes. Only needed if the latter is not empty. |
| Cursor | enter | String | Cursor to display when hovering over a valid actor to deliver experience to. |
| Voice | Action | String |  |
| TargetLineColor | FFFF00 | Color (RRGGBB[AA] notation) | Color to use for the target line. |

### Demolishable
**Handle demolitions from C4 explosives.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition |  | String | Condition to grant during demolition countdown. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Demolition

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DetonationDelay | 45 | Integer | Delay to demolish the target once the explosive device is planted. Measured in game ticks. Default is 1.8 seconds. |
| Flashes | 3 | Integer | Number of times to flash the target. |
| FlashesDelay | 4 | Integer | Delay before the flashing starts. |
| FlashInterval | 4 | Integer | Interval between each flash. |
| EnterBehaviour | Exit | [`EnterBehaviour`](#enterbehaviour) | Behaviour when entering the structure. Possible values are Exit, Suicide, Dispose. |
| DamageTypes |  | Collection of DamageType | Types of damage that this trait causes. Leave empty for no damage types. |
| Voice | Action | String | Voice string when planting explosive charges. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| TargetRelationships | Enemy, Neutral | [`PlayerRelationship`](#playerrelationship) |  |
| ForceTargetRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) |  |
| Cursor | c4 | String | Cursor to display when hovering over a demolishable target. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DetectCloaked
**Actor can reveal Cloak actors in a specified range.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DetectionTypes | Cloak | Collection of DetectionType | Specific cloak classifications I can reveal. |
| Range | 5c0 | 1D World Distance |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DetectCloakedMultiplier
**Modifies the cloak detection range of this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DeveloperMode
**Attach this to the player actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CheckboxLabel | checkbox-debug-menu.label | String | Descriptive label for the developer mode checkbox in the lobby. |
| CheckboxDescription | checkbox-debug-menu.description | String | Tooltip description for the developer mode checkbox in the lobby. |
| CheckboxEnabled | False | Boolean | Default value of the developer mode checkbox in the lobby. |
| CheckboxLocked | False | Boolean | Prevent the developer mode state from being changed in the lobby. |
| CheckboxVisible | True | Boolean | Whether to display the developer mode checkbox in the lobby. |
| CheckboxDisplayOrder | 0 | Integer | Display order for the developer mode checkbox in the lobby. |
| Cash | 20000 | Integer | Default cash bonus granted by the give cash cheat. |
| ResourceGrowth | 100 | Integer | Growth steps triggered by the grow resources button. |
| FastBuild | False | Boolean | Enable the fast build cheat by default. |
| FastCharge | False | Boolean | Enable the fast support powers cheat by default. |
| DisableShroud | False | Boolean | Enable the disable visibility cheat by default. |
| UnlimitedPower | False | Boolean | Enable the unlimited power cheat by default. |
| BuildAnywhere | False | Boolean | Enable the build anywhere cheat by default. |
| PathDebug | False | Boolean | Enable the path debug overlay by default. |

### DockClientManager
**Manages DockClients on the actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SearchForDockDelay | 125 | Integer | How long (in ticks) to wait until (re-)checking for a nearby available DockHost. |
| OccupancyCostModifier | 12 | Integer | The pathfinding cost penalty applied for each dock client waiting to unload at a DockHost. |
| EnterCursor | enter | String | Cursor to display when able to dock at target actor. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to dock at target actor. |
| Voice | Action | String | Voice to be played when ordered to dock. |
| DockLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line of docking orders. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DockHost
**A generic dock that services DockClients.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type |  | Collection of DockType | Docking type. |
| MaxQueueLength | 3 | Integer | How many clients can this dock be reserved for? |
| DockWait | 10 | Integer | How long should the client wait before starting the docking sequence. |
| DockAngle | 0 | 1D World Angle | Actual client facing when docking. |
| DockOffset | 0,0,0 | 3D World Vector | Docking cell relative to the centre of the actor. |
| IsDragRequired | False | Boolean | Does client need to be dragged in? |
| DragOffset | 0,0,0 | 3D World Vector | Vector by which the client will be dragged when docking. |
| DragLength | 0 | Integer | In how many steps to perform the dragging? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### DrawLineToTarget
**Renders target lines between order waypoints.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Delay | 2400 | Integer | Delay (in milliseconds) before the target lines disappear. |
| LineWidth | 1 | Integer | Width (in pixels) of the target lines. |
| QueuedLineWidth | 1 | Integer | Width (in pixels) of the queued target lines. |
| MarkerWidth | 2 | Integer | Width (in pixels) of the end node markers. |
| QueuedMarkerWidth | 2 | Integer | Width (in pixels) of the queued end node markers. |
| Palette | terrain | String | Palette used for rendering sprites. |

### DummyBot
**A placeholder bot that doesn't do anything.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | Unnamed Bot | String | Human-readable name this bot uses. |
| Type | *(required)* | String | Internal id for this bot. |

### DuplicateUnitCrateAction
**Creates duplicates of the actor that collects the crate.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MaxAmount | 2 | Integer | The maximum number of duplicates to make. |
| MinAmount | 1 | Integer | The minimum number of duplicates to make. Overrules MaxDuplicatesWorth. |
| MaxDuplicateValue | -1 | Integer | The maximum total value allowed for the duplicates. Duplication stops if the total worth will exceed this number. -1 = no limit |
| MaxRadius | 4 | Integer | The maximum radius (in cells) that duplicates can be spawned. |
| ValidTargets | Ground, Water | Collection of TargetableType | The list of unit target types we are allowed to duplicate. |
| ValidFactions |  | Set of String | Which factions this crate action can occur for. |
| Owner |  | String | Is the new duplicates given to a specific owner, regardless of whom collected it? |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### EditorActionManager

### EditorActorLayer
**Required for the map editor to work. Attach this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BinSize | 250 | Integer | Size of partition bins (world pixels) |

### EditorCursorLayer
**Required for the map editor to work. Attach this to the world actor.**

> Requires trait(s): [`EditorActorLayer`](#editoractorlayer).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PreviewFacing | 384 | 1D World Angle |  |

### EditorOnlyTooltip
**Shown in map editor.**

> Inherits from: `TooltipInfoBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### EditorResourceLayer
**Required for the map editor to work. Attach this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ResourceTypes |  | Dictionary with Key: String, Value: ResourceTypeInfo |  |
| RecalculateResourceDensity | False | Boolean | Override the density saved in maps with values calculated based on the number of neighbouring resource cells. |

### EditorSelectionLayer
**Renders the selection grid in the editor.**

> Requires trait(s): [`LoadWidgetAtGameStart`](#loadwidgetatgamestart).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MainColor | FFFFFF | Color (RRGGBB[AA] notation) | Main color of the selection grid. |
| AltColor | 000000 | Color (RRGGBB[AA] notation) | Alternate color of the selection grid. |
| PasteColor | 4CFF00 | Color (RRGGBB[AA] notation) | Main color of the paste grid. |
| LineThickness | 1 | Integer | Thickness of the selection grid lines. |
| AltPixelOffset | 1,1 | 2D Integer | Render offset of the secondary grid lines. |

### EjectOnDeath
**Eject a ground soldier or a paratrooper while in the air.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PilotActor | E1 | String | Name of the unit to eject. This actor type needs to have the Parachutable trait defined. |
| SuccessRate | 50 | Integer | Probability that the aircraft's pilot gets ejected once the aircraft is destroyed. |
| ChuteSound |  | String | Sound to play when ejecting the pilot from the aircraft. |
| EjectInAir | False | Boolean | Can a destroyed aircraft eject its pilot while it has not yet fallen to ground level? |
| EjectOnGround | False | Boolean | Can a destroyed aircraft eject its pilot when it falls to ground level? |
| AllowUnsuitableCell | False | Boolean | Risks stuck units when they don't have the Paratrooper trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ElevatedBridgeLayer

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ImpassableTerrainType | Impassable | String | Terrain type used by cells outside any elevated bridge footprint. |

### ElevatedBridgePlaceholder
**Placeholder to make static elevated bridges work. Define individual trait instances for each elevated bridge footprint in the map.**

> Requires trait(s): [`ElevatedBridgeLayer`](#elevatedbridgelayer).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Location | 0,0 | 2D Cell Position | Location of the bridge |
| Orientation | X | [`ElevatedBridgePlaceholderOrientation`](#elevatedbridgeplaceholderorientation) | Orientation of the bridge. |
| Length | 0 | Integer | Length of the bridge |
| Height | 0 | Byte | Height of the bridge in map height steps. |
| TerrainType | Road | String | Terrain type of the bridge. |

### Encyclopedia

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Description |  | String | Explains the purpose in the in-game encyclopedia. |
| Order | 0 | Integer | Number for ordering the list. |
| Category |  | String | Group under this heading. |

### EnemyWatcher
**Tracks neutral and enemy actors' visibility and notifies the player. Attach this to the player actor. The actors to track need the 'AnnounceOnSeen' trait.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ScanInterval | 25 | Integer | Interval in ticks between scanning for enemies. |
| NotificationInterval | 750 | Integer | Minimal ticks in-between notifications. |

### EntersTunnels
**This actor can interact with TunnelEntrances to move through TerrainTunnels.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| EnterCursor | enter | String | Cursor to display when able to enter target tunnel. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to enter target tunnel. |
| Voice | Action | String |  |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line while in tunnels. |
| RequireForceMoveCondition |  | BooleanExpression | Boolean expression defining the condition under which the regular (non-force) enter cursor is disabled. |

### Exit
**Where the unit should leave the building. Multiples are allowed if IDs are added: Exit@2, ...**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SpawnOffset | 0,0,0 | 3D World Vector | Offset at which that the exiting actor is spawned relative to the center of the producing actor. |
| ExitCell | 0,0 | 2D Cell Vector | Cell offset where the exiting actor enters the ActorMap relative to the topleft cell of the producing actor. |
| Facing |  | 1D World Angle (optional) |  |
| ProductionTypes |  | Set of String | Type tags on this exit. |
| ExitDelay | 0 | Integer | Number of ticks to wait before moving into the world. |
| Priority | 1 | Integer | Exits with larger priorities will be used before lower priorities. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ExitsDebugOverlay
**Displays `Exit` data for factories.**

> Requires trait(s): [`Exit`](#exit).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DrawPerimiterCellVectors | True | Boolean | Should cell vectors be drawn for each perimeter cell? |
| DrawExitCellVectors | True | Boolean | Should cell vectors be drawn for each exit cell? |
| DrawSpawnOffsetLines | True | Boolean | Should lines be drawn for each exit (from spawn offset to the center of the exit cell)? |

### ExitsDebugOverlayManager

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Font | TinyBold | String | The font used to draw cell vectors. Should match the value as-is in the Fonts section of the mod manifest (do not convert to lowercase). |

### ExperienceTrickler
**Lets the actor gain experience in a set periodic time.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`GainsExperience`](#gainsexperience).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Interval | 50 | Integer | Number of ticks to wait between giving experience. |
| InitialDelay | 0 | Integer | Number of ticks to wait before giving first experience. |
| Amount | 15 | Integer | Amount of experience to give each time. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ExplodeCrateAction
**Fires a weapon at the location when collected.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Weapon | *(required)* | String | The weapon to fire upon collection. |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Explodes
**This actor explodes when killed.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Weapon | *(required)* | String | Default weapon to use for explosion if ammo/payload is loaded. |
| EmptyWeapon | UnitExplode | String | Fallback weapon to use for explosion if empty (no ammo/payload). |
| LoadedChance | 100 | Integer | Chance that the explosion will use Weapon instead of EmptyWeapon when exploding, provided the actor has ammo/payload. |
| Chance | 100 | Integer | Chance that this actor will explode at all. |
| DamageThreshold | 0 | Integer | Health level at which actor will explode. |
| DeathTypes |  | Collection of DamageType | DeathType(s) that trigger the explosion. Leave empty to always trigger an explosion. |
| DamageSource | Self | [`DamageSource`](#damagesource) | Who is counted as source of damage for explosion. Possible values are Self and Killer. |
| Type | CenterPosition | [`ExplosionType`](#explosiontype) | Possible values are CenterPosition (explosion at the actors' center) and  Footprint (explosion on each occupied cell). |
| Offset | 0,0,0 | 3D World Vector | Offset of the explosion from the center of the exploding actor (or cell). |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ExplosionOnDamageTransition
**This actor triggers an explosion on itself when transitioning to a specific damage state.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Weapon | *(required)* | String | Weapon to use for explosion. |
| DamageState | Heavy | [`DamageState`](#damagestate) | At which damage state explosion will trigger. |
| TriggerOnlyOnce | False | Boolean | Should the explosion only be triggered once? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ExternalCondition
**Allows a condition to be granted from an external source (Lua, warheads, etc).**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String |  |
| SourceCap | 0 | Integer | If > 0, restrict the number of times that this condition can be granted by a single source. |
| TotalCap | 0 | Integer | If > 0, restrict the number of times that this condition can be granted by any source. |

### FallsToEarth
**Causes aircraft husks that are spawned in the air to crash to the ground.**

> Requires trait(s): [`Aircraft`](#aircraft).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Explosion | UnitExplode | String | Explosion weapon that triggers when hitting ground. |
| MaximumSpinSpeed |  | 1D World Angle (optional) | Limit the maximum spin (in angle units per tick) that can be achieved while crashing. 0 disables spinning. Leave undefined for no limit. |
| Moves | False | Boolean | Does the aircraft (husk) move forward at aircraft speed? |
| Velocity | 0c43 | 1D World Distance | Velocity (per tick) at which aircraft falls to ground. |

### FirepowerMultiplier
**Modifies the damage applied by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### FireWarheads
**Detonate defined warheads at the current location at a set interval.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Weapons | *(required)* | Collection of String | Weapons to fire. |
| StartCooldown | 0 | Integer | How long (in ticks) to wait before the first detonation. |
| Interval | 1 | Integer | How long (in ticks) to wait after a detonation. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### FixedColorPalette
**Add this to the World actor definition.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Base | terrain | String | The name of the palette to base off. |
| Name | resources | String | The name of the resulting palette |
| RemapIndex |  | Collection of Integer | Remap these indices to pre-defined colors. |
| Color | 00000000 | Color (RRGGBB[AA] notation) | The fixed color to remap. |
| AllowModifiers | True | Boolean | Allow palette modifiers to change the palette. |

### FixedPlayerColorShift
**Add fixed color shifts to player palettes. Use to add RGBA compatibility to IndexedPlayerPalette.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BasePalette | *(required)* | String | The name of the palette to base off. |
| PlayerIndex |  | Dictionary with Key: String, Value: Collection of Real Number |  |

### FlashPostProcessEffect
**Used for bursted one-colored whole screen effects. Add this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Length | 20 | Integer | Measured in ticks. |
| Color | FFFFFF | Color (RRGGBB[AA] notation) |  |
| Type |  | String | Set this when using multiple independent flash effects. |

### FloatingSpriteEmitter
**Spawns moving sprite effects.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Lifetime | *(required)* | Collection of Integer | The time between individual particle creation. Two values mean actual lifetime will vary between them. |
| Duration | -1 | Integer | The time in ticks until stop spawning. -1 means forever. |
| Offset | 0,0,0 | Collection of 3D World Vector | Randomised offset for the particle emitter. |
| Speed | 0c0 | Collection of 1D World Distance | Randomized particle forward movement. |
| Gravity | 0c0 | Collection of 1D World Distance | Randomized particle gravity. |
| RandomFacing | True | Boolean | Randomize particle facing. |
| TurnRate | 0 | Integer | Randomize particle turnrate. |
| RandomRate | 4 | Integer | The rate at which particle movement properties are reset. |
| SpawnFrequency | 1 | Collection of Integer | How many particles should spawn. Two values for a random range. |
| Image | smoke | String | Which image to use. |
| Sequences | particles | Collection of String | Which sequence to use. |
| Palette | effect | String | Which palette to use. |
| IsPlayerPalette | False | Boolean |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### FootprintPlaceBuildingPreview
**Creates a building placement preview showing only the building footprint.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Palette | terrain | String | Palette to use for rendering the placement sprite. |
| FootprintAlpha | 1 | Real Number | Custom opacity to apply to the placement sprite. |
| LineBuildFootprintAlpha | 1 | Real Number | Custom opacity to apply to the line-build placement sprite. |

### FreeActor
**Player receives a unit for free once the building is placed. This also works for structures. If you want more than one unit to appear copy this section and assign IDs like FreeActor@2, ...**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Actor | *(required)* | String | Name of the actor. |
| SpawnOffset | 0,0 | 2D Cell Vector | Offset relative to the top-left cell of the building. |
| Facing | 0 | 1D World Angle | Which direction the unit should face. |
| AllowRespawn | False | Boolean | Whether another actor should spawn upon re-enabling the trait. |
| EditorFreeActorDisplayOrder | 4 | Integer | Display order for the free actor checkbox in the map editor |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### FreeActorWithDelivery
**Player receives a unit for free once the building is placed. If you want more than one unit to be delivered, copy this section and assign IDs like FreeActorWithDelivery@2, ...**

> Inherits from: [`FreeActor`](#freeactor), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DeliveringActor | *(required)* | String | Name of the delivering actor. This actor must have the `Carryall` trait |
| SpawnLocation | 0,0 | 2D Cell Position | Cell coordinates for spawning the delivering actor. If left blank, the closest edge cell will be chosen. |
| DeliveryOffset | 0,0 | 2D Cell Vector | Offset relative to the top-left cell of the building. |
| DeliveryRange | 0c0 | 1D World Distance | Range to search for an alternative delivery location if the DeliveryOffset cell is blocked. |
| Actor | *(required)* | String | Name of the actor. |
| SpawnOffset | 0,0 | 2D Cell Vector | Offset relative to the top-left cell of the building. |
| Facing | 0 | 1D World Angle | Which direction the unit should face. |
| AllowRespawn | False | Boolean | Whether another actor should spawn upon re-enabling the trait. |
| EditorFreeActorDisplayOrder | 4 | Integer | Display order for the free actor checkbox in the map editor |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### FrozenUnderFog
**This actor will remain visible (but not updated visually) under fog, once discovered.**

> Requires trait(s): [`Building`](#building).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AlwaysVisibleRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Players with these relationships can always see the actor. |

### GainsExperience
**This actor's experience increases when it has killed a GivesExperience actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Conditions | *(required)* | Dictionary with Key: Integer, Value: String | Condition to grant at each level. Key is the XP requirements for each level as a percentage of our own value. Value is the condition to grant. |
| LevelUpImage |  | String | Image for the level up sprite. |
| LevelUpSequence | levelup | String | Sequence for the level up sprite. Needs to be present on LevelUpImage. |
| LevelUpPalette | effect | String | Palette for the level up sprite. |
| ExperienceModifier | -1 | Integer | Multiplier to apply to the Conditions keys. Defaults to the actor's value. |
| SuppressLevelupAnimation | True | Boolean | Should the level-up animation be suppressed when actor is created? |
| LevelUpNotification |  | String |  |
| LevelUpTextNotification |  | String |  |

### GainsExperienceMultiplier
**Modifies the experience gathered by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GameSaveViewportManager

### Gate
**Will open and be passable for actors that appear friendly when there are no enemies in range.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Building`](#building).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| OpeningSound |  | String |  |
| ClosingSound |  | String |  |
| CloseDelay | 150 | Integer | Ticks until the gate closes. |
| TransitionDelay | 33 | Integer | Ticks until the gate is considered open. |
| BlocksProjectilesHeight | 0c640 | 1D World Distance | Blocks bullets scaled to open value. |
| BlocksProjectilesValidRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | Determines what projectiles to block based on their allegiance to the gate owner. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GiveBaseBuilderCrateAction
**Spawns units when collected. Adjust selection shares when player has no base.**

> Inherits from: [`GiveUnitCrateAction`](#giveunitcrateaction), [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| NoBaseSelectionShares | 1000 | Integer | The selection shares to use if the collector has no actor with `BaseBuilding. |
| Units | *(required)* | Collection of String | The list of units to spawn. |
| ValidFactions |  | Set of String | Factions that are allowed to trigger this action. |
| Owner |  | String | Override the owner of the newly spawned unit: e.g. Creeps or Neutral |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GiveCashCrateAction
**Gives cash to the collector.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Amount | 2000 | Integer | Amount of cash to give. |
| UseCashTick | False | Boolean | Should the collected amount be displayed as a cash tick? |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GivesBounty
**When killed, this actor causes the attacking player to receive money.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Percentage | 10 | Integer | Percentage of the killed actor's Cost or CustomSellValue to be given. |
| ValidRelationships | Enemy, Neutral | [`PlayerRelationship`](#playerrelationship) | Player relationships the attacking player needs to receive the bounty. |
| ShowBounty | True | Boolean | Whether to show a floating text announcing the won bounty. |
| DeathTypes |  | Collection of DamageType | DeathTypes for which a bounty should be granted. Use an empty list (the default) to allow all DeathTypes. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GivesBuildableArea
**This actor allows placement of other actors with 'RequiresBuildableArea' trait around it.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AreaTypes | *(required)* | Set of String | Types of buildable area this actor gives. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GivesCashOnCapture
**Lets the actor grant cash when captured.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ShowTicks | True | Boolean | Whether to show the cash tick indicators rising from the actor. |
| DisplayDuration | 30 | Integer | How long to show the Amount tick indicator when enabled. |
| Amount | 0 | Integer | Amount of money awarded for capturing the actor. |
| CaptureTypes |  | Collection of CaptureType | Award cash only if the capturer's CaptureTypes overlap with these types. Leave empty to allow all types. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GivesExperience
**This actor gives experience to a GainsExperience actor when they are killed.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Experience | -1 | Integer | If -1, use the value of the unit cost. |
| ValidRelationships | Enemy, Neutral | [`PlayerRelationship`](#playerrelationship) | Player relationships the attacking player needs to receive the experience. |
| ActorExperienceModifier | 10000 | Integer | Percentage of the `Experience` value that is being granted to the killing actor. |
| PlayerExperienceModifier | 0 | Integer | Percentage of the `Experience` value that is being granted to the player owning the killing actor. |

### GivesExperienceMultiplier
**Modifies the experience given by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GiveUnitCrateAction
**Spawns units when collected.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Units | *(required)* | Collection of String | The list of units to spawn. |
| ValidFactions |  | Set of String | Factions that are allowed to trigger this action. |
| Owner |  | String | Override the owner of the newly spawned unit: e.g. Creeps or Neutral |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantCondition
**Grants a condition while the trait is active.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| GrantPermanently | False | Boolean | Is the condition irrevocable once it has been activated? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnAttack

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition type to grant. |
| ArmamentNames | primary | Set of String | Name of the armaments that grant this condition. |
| RequiredShotsPerInstance | 1 | Collection of Integer | Shots required to apply an instance of the condition. If there are more instances of the condition granted than values listed, the last value is used for all following instances beyond the defined range. |
| MaximumInstances | 1 | Integer | Maximum instances of the condition to grant. |
| IsCyclic | False | Boolean | Should all instances reset if the actor passes the final stage? |
| RevokeDelay | 15 | Integer | Amount of ticks required to pass without firing to revoke an instance. |
| RevokeOnNewTarget | False | Boolean | Should an instance be revoked if the actor changes target? |
| RevokeAll | False | Boolean | Should all instances be revoked instead of only one? |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnBotOwner
**Grants a condition to this actor when it is owned by an AI bot.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| Bots | *(required)* | Collection of String | Bot types that trigger the condition. |

### GrantConditionOnClientDock

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to grant to self |
| AfterDockDuration | 0 | Integer | How long condition is applied even after undock. Use -1 for infinite. |
| DockHostNames |  | Set of String | Host actor type(s) leading to the condition being granted. Leave empty for allowing all hosts by default. |

### GrantConditionOnCombatantOwner
**Grants a condition if the owner is a combatant.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to grant. |

### GrantConditionOnDamageState
**Applies a condition to the actor at specified damage states.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| EnabledSounds |  | Collection of String | Play a random sound from this list when enabled. |
| DisabledSounds |  | Collection of String | Play a random sound from this list when disabled. |
| ValidDamageStates | Heavy, Critical | [`DamageState`](#damagestate) | Levels of damage at which to grant the condition. |
| GrantPermanently | False | Boolean | Is the condition irrevocable once it has been activated? |

### GrantConditionOnDeploy
**Grants a condition when a deploy order is issued.Can be paused with the granted condition to disable undeploying.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UndeployedCondition |  | String | The condition to grant while the actor is undeployed. |
| DeployedCondition | *(required)* | String | The condition to grant after deploying and revoke before undeploying. |
| AllowedTerrainTypes |  | Set of String | The terrain types that this actor can deploy on. Leave empty to allow any. |
| CanDeployOnRamps | False | Boolean | Can this actor deploy on slopes? |
| DeployCursor | deploy | String | Cursor to display when able to (un)deploy the actor. |
| DeployBlockedCursor | deploy-blocked | String | Cursor to display when unable to (un)deploy the actor. |
| Facing |  | 1D World Angle (optional) | Facing that the actor must face before deploying. Leave undefined to deploy regardless of facing. |
| DeploySounds |  | Collection of String | Play a randomly selected sound from this list when deploying. |
| UndeploySounds |  | Collection of String | Play a randomly selected sound from this list when undeploying. |
| SkipMakeAnimation | False | Boolean | Skip make/deploy animation? |
| UndeployOnMove | False | Boolean | Undeploy before the actor tries to move? |
| UndeployOnPickup | False | Boolean | Undeploy before the actor is picked up by a Carryall? |
| Voice | Action | String |  |
| EditorDeployedDisplayOrder | 4 | Integer | Display order for the deployed checkbox in the map editor |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnDeployWithCharge
**Allow deploying on specified charge to grant a condition for a specified duration.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DeployedCondition | *(required)* | String | The condition to grant after deploying. |
| ChargedCondition |  | String | The condition to grant when charge is above ChargeThreshhold. |
| InitialCharge | -1 | Integer | Charge to start with. If set to -1 the unit will start with full charge. |
| ChargeDuration | 500 | Integer | Cooldown (in ticks) to reach full charge. |
| ChargeThreshhold | -1 | Integer | The amount of charge that needs to be present for deploy to be issued. If set to -1, threshold is set to full charge. If activated without full charge ConditionDuration is percentally smaller. |
| ConditionDuration | 1 | Integer | How long (in ticks) should the condition stay active? |
| CanCancelCondition | False | Boolean | Can DeployedCondition be canceled by followup deploy order? |
| DeployCursor | deploy | String | Cursor to display when able to (un)deploy the actor. |
| DeployBlockedCursor | deploy-blocked | String | Cursor to display when unable to (un)deploy the actor. |
| DeploySounds |  | Collection of String | Play a randomly selected sound from this list when deploying. |
| UndeploySounds |  | Collection of String | Play a randomly selected sound from this list when undeploying. |
| Voice | Action | String |  |
| ChargingColor | FF00FF | Color (RRGGBB[AA] notation) |  |
| DeployedColor | 8B008B | Color (RRGGBB[AA] notation) |  |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnFaction
**Grants a condition while the trait is active.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| Factions |  | Set of String | Only grant this condition for certain factions. |
| ResetOnOwnerChange | False | Boolean | Should it recheck everything when it is captured? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnHealth
**Applies a condition to the actor at when its health is between 2 specific values.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| EnabledSounds |  | Collection of String | Play a random sound from this list when enabled. |
| DisabledSounds |  | Collection of String | Play a random sound from this list when disabled. |
| MinHP | 0 | Integer | Minimum level of health at which to grant the condition. |
| MaxHP | 0 | Integer | Maximum level of health at which to grant the condition. Non-positive values will make it use Health.HP. |
| GrantPermanently | False | Boolean | Is the condition irrevocable once it has been granted? |

### GrantConditionOnHostDock

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to grant to self |
| AfterDockDuration | 0 | Integer | How long condition is applied even after undock. Use -1 for infinite. |
| DockClientNames |  | Set of String | Client actor type(s) leading to the condition being granted. Leave empty for allowing all clients by default. |

### GrantConditionOnLineBuildDirection

> Requires trait(s): [`LineBuild`](#linebuild).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| Direction | X | [`LineBuildDirection`](#linebuilddirection) | Line build direction to trigger the condition. |

### GrantConditionOnMinelaying

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Minelayer`](#minelayer).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnMovement

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| ValidMovementTypes | Horizontal | [`MovementType`](#movementtype) | Apply condition on listed movement types. Available options are: None, Horizontal, Vertical, Turn. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnPlayerResources
**Grants a condition to this actor when the player has stored resources.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| Threshold | 0 | Integer | Enable condition when the amount of stored resources is greater than this. |

### GrantConditionOnPowerState
**Grants condition as long as a valid power state is maintained.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| ValidPowerStates | Low, Critical | [`PowerState`](#powerstate) | PowerStates at which the condition is granted. Options are Normal, Low and Critical. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnPrerequisite
**Grants a condition to the actor this is attached to when prerequisites are available.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to grant. |
| Prerequisites | *(required)* | Collection of String | List of required prerequisites. |

### GrantConditionOnPrerequisiteManager
**Attach this to the player actor.**

> Requires trait(s): [`TechTree`](#techtree).

### GrantConditionOnProduction
**Grants a condition when this actor produces a specific actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to grant |
| Actors |  | Set of String | The actors to grant condition for. If empty condition will be granted for all actors. |
| Duration | -1 | Integer | How long condition is applies for. Use -1 for infinite. |
| ShowSelectionBar | True | Boolean | Show a selection bar while condition is applied if it has a duration. |
| SelectionBarColor | FF00FF | Color (RRGGBB[AA] notation) |  |

### GrantConditionOnSubterraneanLayer
**Grants Condition on subterranean layer. Also plays transition audio-visuals.**

> Inherits from: `GrantConditionOnLayer`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SubterraneanTransitionImage |  | String | Dig animation image to play when transitioning. |
| SubterraneanTransitionSequence |  | String | Dig animation sequence to play when transitioning. |
| SubterraneanTransitionPalette | effect | String |  |
| SubterraneanTransitionSound |  | String | Dig sound to play when transitioning. |
| Condition | *(required)* | String | The condition to grant to self when changing to specific custom layer. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionOnTerrain

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| TerrainTypes | *(required)* | Collection of String | Terrain names to trigger the condition. |

### GrantConditionOnTileSet

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| TileSets | *(required)* | Collection of String | Tile set IDs to trigger the condition. |

### GrantConditionOnTunnelLayer

> Inherits from: `GrantConditionOnLayer`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to grant to self when changing to specific custom layer. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantConditionWhileAiming

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to grant while aiming. |

### GrantExternalConditionCrateAction
**Grants a condition to the collector and nearby units.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to apply. Must be included in the target actor's ExternalConditions list. |
| Levels | 1 | Integer | How many times to grant the condition. |
| Duration | 0 | Integer | Duration of the condition (in ticks). Set to 0 for a permanent condition. |
| Range | 0c3 | 1D World Distance | The range to search for extra collectors in. Extra collectors will also be granted the crate action. |
| MaxExtraCollectors | 4 | Integer | The maximum number of extra collectors to grant the crate action to. -1 = no limit |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantExternalConditionPower

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to apply. Must be included in the target actor's ExternalConditions list. |
| Duration | 0 | Integer | Duration of the condition (in ticks). Set to 0 for a permanent condition. |
| Dimensions | 0,0 | 2D Cell Vector | Size of the footprint of the affected area. |
| Footprint | *(required)* | String | Actual footprint. Cells marked as x will be affected. |
| OnFireSound |  | String | Sound to instantly play at the targeted area. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships which condition can be applied to. |
| Sequence | active | String | Sequence to play for granting actor when activated. This requires the actor to have the WithSpriteBody trait or one of its derivatives. |
| FootprintImage | overlay | String |  |
| FootprintSequence | target-select | String |  |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | GrantExternalConditionPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GrantExternalConditionToCrusher
**Grant a condition to the crushing actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| WarnCrushCondition |  | String | The condition to apply on a crush attempt. Must be included among the crusher actor's ExternalCondition traits. |
| WarnCrushDuration | 0 | Integer | Duration of the condition applied on a crush attempt (in ticks). Set to 0 for a permanent condition. |
| OnCrushCondition |  | String | The condition to apply on a successful crush. Must be included among the crusher actor's ExternalCondition traits. |
| OnCrushDuration | 0 | Integer | Duration of the condition applied on a successful crush (in ticks). Set to 0 for a permanent condition. |

### GrantExternalConditionToProduced
**Grants a condition to actors produced by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to apply. Must be included in the produced actor's ExternalConditions list. |
| Duration | 0 | Integer | Duration of the condition (in ticks). Set to 0 for a permanent condition. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### GroundLevelBridge
**Bridge actor that can't be passed underneath.**

> Requires trait(s): [`Building`](#building).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TerrainType | Bridge | String |  |
| Type | GroundLevelBridge | String |  |
| NeighbourOffsets |  | Collection of 2D Cell Vector |  |
| DemolishWeapon | Demolish | String | The name of the weapon to use when demolishing the bridge |
| DamageTypes |  | Collection of DamageType | Types of damage that this bridge causes to units over/in path of it while being destroyed/repaired. Leave empty for no damage types. |

### Guardable
**This unit can be guarded (followed and protected) by a Guard unit.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Range | 2c0 | 1D World Distance | Maximum range that guarding actors will maintain. |

### Guard
**The player can give this unit the order to follow and protect friendly units with the Guardable trait.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Voice | Action | String |  |
| TargetLineColor | FF4500 | Color (RRGGBB[AA] notation) | Color to use for the target line. |

### HandicapDamageMultiplier
**Modifies the damage applied to this actor based on the owner's handicap.**

### HandicapFirepowerMultiplier
**Modifies the damage applied by this actor based on the owner's handicap.**

### HandicapProductionTimeMultiplier
**Modifies the production time of this actor based on the producer's handicap.**

### HarvesterAttackNotifier
**Plays an audio notification and shows a radar ping when a harvester is attacked. Attach this to the player actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| NotifyInterval | 30000 | Integer | Minimum duration (in milliseconds) between notification events. |
| RadarPingColor | FF0000 | Color (RRGGBB[AA] notation) |  |
| RadarPingDuration | 250 | Integer | Length of time (in ticks) to display a location ping in the minimap. |
| ExcludeDamageTypes |  | Collection of DamageType | Exclude damage types (defined on the warheads) that trigger Notification. |
| Notification | HarvesterAttack | String | Speech notification type to play. |
| TextNotification |  | String | Text notification to display. |

### HarvesterBotModule
**Put this on the Player actor. Manages bot harvesters to ensure they always continue harvesting as long as there are resources on the map.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| HarvesterTypes |  | Set of String | Actor types that are considered harvesters. If harvester count drops below RefineryTypes count, a new harvester is built. Leave empty to disable harvester replacement. Currently only needed by harvester replacement system. |
| RefineryTypes |  | Set of String | Actor types that are counted as refineries. Currently only needed by harvester replacement system. |
| ScanForIdleHarvestersInterval | 50 | Integer | Interval (in ticks) between giving out orders to idle harvesters. |
| HarvesterEnemyAvoidanceRadius | 8c0 | 1D World Distance | Avoid enemy actors nearby when searching for a new resource patch. Should be somewhere near the max weapon range. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Harvester

> Inherits from: `DockClientBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | Unload | Collection of DockType | Docking type |
| UnblockCell | 0,4 | 2D Cell Vector | Cell to move to when automatically unblocking DeliveryBuilding. |
| BaleLoadDelay | 4 | Integer |  |
| BaleUnloadDelay | 4 | Integer | How fast it can dump its bales. |
| BaleUnloadAmount | 1 | Integer | How many bales can it dump at once. |
| HarvestFacings | 0 | Integer |  |
| Resources |  | Collection of String | Which resources it can harvest. |
| FullyLoadedSpeed | 85 | Integer | Percentage of maximum speed when fully loaded. |
| SearchOnCreation | True | Boolean | Automatically scan for resources when created. |
| SearchFromProcRadius | 24 | Integer | Initial search radius (in cells) from the refinery that created us. |
| SearchFromHarvesterRadius | 12 | Integer | Search radius (in cells) from the last harvest order location to find more resources. |
| WaitDuration | 25 | Integer | Interval to wait between searches when there are no resources nearby. |
| ResourceRefineryDirectionPenalty | 200 | Integer | The pathfinding cost penalty applied for cells directly away from the refinery. |
| QueueFullLoad | False | Boolean | Does the unit queue harvesting runs instead of individual harvest actions? |
| EmptyCondition |  | String | Condition to grant while empty. |
| HarvestVoice | Action | String |  |
| HarvestLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line of harvest orders. |
| HarvestCursor | harvest | String | Cursor to display when ordering to harvest resources. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### HealActorsCrateAction
**Heals all actors that belong to the owner of the collector.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TargetTypes |  | Collection of TargetableType | The target type(s) of the actors this crate action will heal. Leave empty to heal all actors. |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Health

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| HP | 0 | Integer | HitPoints |
| NotifyAppliedDamage | True | Boolean | Trigger interfaces such as AnnounceOnKill? |
| EditorHealthDisplayOrder | 2 | Integer | Display order for the health slider in the map editor |

### HiddenUnderFog
**The actor stays invisible under fog of war.**

> Inherits from: [`HiddenUnderShroud`](#hiddenundershroud).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AlwaysVisibleRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Players with these relationships can always see the actor. |
| Type | Footprint | [`VisibilityType`](#visibilitytype) | Possible values are CenterPosition (reveal when the center is visible) and  Footprint (reveal when any footprint cell is visible). |

### HiddenUnderShroud
**The actor stays invisible under the shroud.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AlwaysVisibleRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Players with these relationships can always see the actor. |
| Type | Footprint | [`VisibilityType`](#visibilitytype) | Possible values are CenterPosition (reveal when the center is visible) and  Footprint (reveal when any footprint cell is visible). |

### HideMapCrateAction
**Hides the entire map in shroud.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IncludeAllies | False | Boolean | Should the map also be hidden for the allies of the collector's owner? |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### HierarchicalPathFinderOverlay
**Renders a debug overlay showing the abstract graph of the hierarchical pathfinder. Attach this to the world actor.**

> Requires trait(s): [`PathFinder`](#pathfinder).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Font | TinyBold | String |  |
| GroundLayerColor | FF8C00 | Color (RRGGBB[AA] notation) |  |
| CustomLayerColor | 0000FF | Color (RRGGBB[AA] notation) |  |
| GroundToCustomLayerColor | 800080 | Color (RRGGBB[AA] notation) |  |
| AbstractNodeColor | FF0000 | Color (RRGGBB[AA] notation) |  |

### HitShape
**Shape of actor for targeting and damage calculations.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Turret |  | String | Name of turret this shape is linked to. Leave empty to link shape to body. |
| TargetableOffsets | 0,0,0 | Collection of 3D World Vector | Create a targetable position for each offset listed here (relative to CenterPosition). |
| UseTargetableCellsOffsets | False | Boolean | Create a targetable position at the center of each occupied cell. Stacks with TargetableOffsets. |
| ArmorTypes |  | Collection of ArmorType | Defines which Armor types apply when the actor receives damage to this HitShape. If none specified, all armor types the actor has are valid. |
| Type |  | IHitShape | Engine comes with support for `Circle`, `Capsule`, `Polygon` and `Rectangle`. Defaults to `Circle` when left empty. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Huntable
**This actor can be targeted by the Hunt activity.**

### Husk
**Spawns remains of a husk actor with the correct facing.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AllowedTerrain |  | Set of String |  |
| PreviewFacing | 384 | 1D World Angle | Facing to use for actor previews (map editor, color picker, etc) |
| Locomotor |  | String | Used to define crushes. Locomotor must be defined on the World actor. |

### IgnoresCloak
**This actor does not care about any type of cloak its targets might have, regardless of distance.**

### IgnoresDisguise
**Allows automatic targeting of disguised actors.**

### Immobile

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| OccupiesSpace | True | Boolean |  |

### InaccuracyMultiplier
**Modifies the inaccuracy of weapons fired by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### IndexedPalette
**Define a palette by swapping palette indices.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Internal palette name |
| BasePalette |  | String | The name of the palette to base off. |
| Index | *(required)* | Collection of Integer | Indices from BasePalette to be swapped with ReplaceIndex. |
| ReplaceIndex | *(required)* | Collection of Integer | Indices from BasePalette to replace from Index. |
| AllowModifiers | True | Boolean | Allow palette modifiers to change the palette. |

### IndexedPlayerPalette
**Define a player palette by swapping palette indices.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BasePalette |  | String | The name of the palette to base off. |
| BaseName | player | String | The prefix for the resulting player palettes |
| RemapIndex |  | Collection of Integer | Remap these indices to player colors. |
| AllowModifiers | True | Boolean | Allow palette modifiers to change the palette. |
| PlayerIndex |  | Dictionary with Key: String, Value: Collection of Integer |  |

### InstantlyRepairable
**Eligible for instant repair.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Collection of InstantlyRepairType | Actors with these Types under EngineerRepair trait can repair me. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### InstantlyRepairs
**Can instantly repair other actors, but gets consumed afterwards.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types |  | Collection of InstantlyRepairType | Uses the InstantlyRepairable trait to determine repairability. |
| Voice | Action | String |  |
| TargetLineColor | FFFF00 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| EnterBehaviour | Dispose | [`EnterBehaviour`](#enterbehaviour) | Behaviour when entering the structure. Possible values are Exit, Suicide, Dispose. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | What player relationship the target's owner needs to be repaired by this actor. |
| RepairSound |  | String | Sound to play when repairing is done. |
| Cursor | goldwrench | String | Cursor to display when hovering over a valid actor to repair. |
| RepairBlockedCursor | goldwrench-blocked | String | Cursor to display when target actor has full health so it can't be repaired. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Interactable
**Used to enable mouse interaction on actors that are not Selectable.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Bounds |  | Collection of 1D World Distance | Defines a custom rectangle for mouse interaction with the actor. If null, the engine will guess an appropriate size based on the With*Body trait. The first two numbers define the width and height of the rectangle as a world distance. The (optional) second two numbers define an x and y offset from the actor center. |
| DecorationBounds |  | Collection of 1D World Distance | Defines a custom rectangle for Decorations (e.g. the selection box). If null, Bounds will be used instead |

### IsometricSelectable
**This actor is selectable. Defines bounds of selectable area, selection class, selection priority and selection priority modifiers.**

> Requires trait(s): [`Building`](#building).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Bounds |  | Collection of Integer | Defines a custom rectangle for mouse interaction with the actor. If null, the engine will guess an appropriate size based on the building's footprint. The first two numbers define the width and depth of the footprint rectangle. The (optional) second two numbers define an x and y offset from the actor center. |
| Height | 24 | Integer | Height above the footprint for the top of the interaction rectangle. |
| DecorationBounds |  | Collection of Integer | Defines a custom rectangle for Decorations (e.g. the selection box). If null, Bounds will be used instead. |
| DecorationHeight | -1 | Integer | Defines a custom height for Decorations (e.g. the selection box). If < 0, Height will be used instead. If Height is 0, this must be defined with a value greater than 0. |
| Priority | 10 | Integer |  |
| PriorityModifiers | None | [`SelectionPriorityModifiers`](#selectionprioritymodifiers) | Allow selection priority to be modified using a hotkey. Valid values are None (priority is not affected by modifiers) Ctrl (priority is raised when Ctrl pressed) and Alt (priority is raised when Alt pressed). |
| Class |  | String | All units having the same selection class specified will be selected with select-by-type commands (e.g. double-click).  Defaults to the actor name when not defined or inherited. |
| Voice | Select | String |  |

### JamsMissiles
**This actor deflects missiles.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Range | 0c0 | 1D World Distance | Range of the deflection. |
| DeflectionRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | What player relationships are affected. |
| Chance | 100 | Integer | Chance of deflecting missiles. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### KillsSelf

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RemoveInstead | False | Boolean | Remove the actor from the world (and destroy it) instead of killing it. |
| Delay | 0 | Collection of Integer | The amount of time (in ticks) before the actor dies. Two values indicate a range between which a random value is chosen. |
| DamageTypes |  | Collection of DamageType | Types of damage that this trait causes. Leave empty for no damage types. |
| GrantsCondition |  | String | The condition to grant moments before suiciding. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### LegacyBridgeHut
**Allows bridges to be targeted for demolition and repair.**

### LegacyBridgeLayer

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Bridges | bridge1, bridge2 | Collection of String |  |

### LevelUpCrateAction
**Gives experience levels to the collector.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Levels | 1 | Integer | Number of experience levels to give. |
| Range | 0c3 | 1D World Distance | The range to search for extra collectors in. Extra collectors will also be granted the crate action. |
| MaxExtraCollectors | 4 | Integer | The maximum number of extra collectors to grant the crate action to. |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### LineBuild
**Place the second actor in line to build more of the same at once (used for walls).**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Range | 5 | Integer | The maximum allowed length of the line. |
| NodeTypes | wall | Set of String | LineBuildNode 'Types' to attach to. |
| SegmentType |  | String | Actor type for line-built segments (defaults to same actor). |
| SegmentsRequireNode | False | Boolean | Delete generated segments when destroyed or sold. |

### LineBuildNode
**LineBuild actors attach to LineBuildNodes.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types | wall | Set of String | This actor is of LineBuild 'NodeType'... |
| Connections | 1,0, 0,1, -1,0, 0,-1 | Collection of 2D Cell Vector | Cells (outside the footprint) that contain cells that can connect to this actor. |

### LineBuildSegmentExternalCondition
**Applies a condition to connected line build segments.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`LineBuild`](#linebuild).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to apply. Must be included in the target actor's ExternalConditions list. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### LoadWidgetAtGameStart

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ShellmapRoot | MAINMENU | String | The widget tree to open when a shellmap is loaded (i.e. the main menu). |
| IngameRoot | INGAME_ROOT | String | The widget tree to open when a regular map is loaded (i.e. the ingame UI). |
| EditorRoot | EDITOR_ROOT | String | The widget tree to open when the map editor is loaded. |
| GameSaveLoadingRoot | GAMESAVE_LOADING_SCREEN | String | The widget tree to open (in addition to INGAME_ROOT) while loading a saved game. |
| ClearRoot | True | Boolean | Remove any existing UI when a map is loaded. |

### LobbyPrerequisiteCheckbox
**Enables defined prerequisites at game start for all players if the checkbox is enabled.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ID | *(required)* | String | Internal id for this checkbox. |
| Label | *(required)* | String | Display name for this checkbox. |
| Description |  | String | Description name for this checkbox. |
| Enabled | False | Boolean | Default value of the checkbox in the lobby. |
| Locked | False | Boolean | Prevent the checkbox from being changed from its default value. |
| Visible | True | Boolean | Display the checkbox in the lobby. |
| DisplayOrder | 0 | Integer | Display order for the checkbox in the lobby. |
| Prerequisites | *(required)* | Set of String | Prerequisites to grant when this checkbox is enabled. |

### Locomotor
**Used by Mobile. Attach these to the world actor. You can have multiple variants by adding @suffixes.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | default | String | Locomotor ID. |
| WaitAverage | 40 | Integer |  |
| WaitSpread | 10 | Integer |  |
| SharesCell | False | Boolean | Allow multiple (infantry) units in one cell. |
| MoveIntoShroud | True | Boolean | Can the actor be ordered to move in to shroud? |
| Crushes |  | Collection of CrushClass | e.g. crate, wall, infantry |
| CrushDamageTypes |  | Collection of DamageType | Types of damage that are caused while crushing. Leave empty for no damage types. |
| TerrainSpeeds |  | Dictionary with Key: String, Value: TerrainInfo | Lower the value on rough terrain. Leave out entries for impassable terrain. |

### MapBuildRadius
**Controls the build radius checkboxes in the lobby options.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AllyBuildRadiusCheckboxLabel | checkbox-ally-build-radius.label | String | Descriptive label for the ally build radius checkbox in the lobby. |
| AllyBuildRadiusCheckboxDescription | checkbox-ally-build-radius.description | String | Tooltip description for the ally build radius checkbox in the lobby. |
| AllyBuildRadiusCheckboxEnabled | True | Boolean | Default value of the ally build radius checkbox in the lobby. |
| AllyBuildRadiusCheckboxLocked | False | Boolean | Prevent the ally build radius state from being changed in the lobby. |
| AllyBuildRadiusCheckboxVisible | True | Boolean | Whether to display the ally build radius checkbox in the lobby. |
| AllyBuildRadiusCheckboxDisplayOrder | 0 | Integer | Display order for the ally build radius checkbox in the lobby. |
| BuildRadiusCheckboxLabel | checkbox-build-radius.label | String | Tooltip description for the build radius checkbox in the lobby. |
| BuildRadiusCheckboxDescription | checkbox-build-radius.description | String | Tooltip description for the build radius checkbox in the lobby. |
| BuildRadiusCheckboxEnabled | True | Boolean | Default value of the build radius checkbox in the lobby. |
| BuildRadiusCheckboxLocked | False | Boolean | Prevent the build radius state from being changed in the lobby. |
| BuildRadiusCheckboxVisible | True | Boolean | Display the build radius checkbox in the lobby. |
| BuildRadiusCheckboxDisplayOrder | 0 | Integer | Display order for the build radius checkbox in the lobby. |

### MapCreeps
**Controls the 'Creeps' checkbox in the lobby options.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CheckboxLabel | dropdown-map-creeps.label | String | Descriptive label for the creeps checkbox in the lobby. |
| CheckboxDescription | dropdown-map-creeps.description | String | Tooltip description for the creeps checkbox in the lobby. |
| CheckboxEnabled | True | Boolean | Default value of the creeps checkbox in the lobby. |
| CheckboxLocked | False | Boolean | Prevent the creeps state from being changed in the lobby. |
| CheckboxVisible | True | Boolean | Whether to display the creeps checkbox in the lobby. |
| CheckboxDisplayOrder | 0 | Integer | Display order for the creeps checkbox in the lobby. |

### MapEditorData

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RequireTilesets |  | Set of String |  |
| ExcludeTilesets |  | Set of String |  |
| Categories |  | Collection of String |  |

### MapOptions
**Controls the game speed, tech level, and short game lobby options.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ShortGameCheckboxLabel | checkbox-short-game.label | String | Descriptive label for the short game checkbox in the lobby. |
| ShortGameCheckboxDescription | checkbox-short-game.description | String | Tooltip description for the short game checkbox in the lobby. |
| ShortGameCheckboxEnabled | True | Boolean | Default value of the short game checkbox in the lobby. |
| ShortGameCheckboxLocked | False | Boolean | Prevent the short game enabled state from being changed in the lobby. |
| ShortGameCheckboxVisible | True | Boolean | Whether to display the short game checkbox in the lobby. |
| ShortGameCheckboxDisplayOrder | 0 | Integer | Display order for the short game checkbox in the lobby. |
| TechLevelDropdownLabel | dropdown-tech-level.label | String | Descriptive label for the tech level option in the lobby. |
| TechLevelDropdownDescription | dropdown-tech-level.description | String | Tooltip description for the tech level option in the lobby. |
| TechLevel | unrestricted | String | Default tech level. |
| TechLevelDropdownLocked | False | Boolean | Prevent the tech level from being changed in the lobby. |
| TechLevelDropdownVisible | True | Boolean | Display the tech level option in the lobby. |
| TechLevelDropdownDisplayOrder | 0 | Integer | Display order for the tech level option in the lobby. |
| GameSpeedDropdownLabel | dropdown-game-speed.label | String | Tooltip description for the game speed option in the lobby. |
| GameSpeedDropdownDescription | dropdown-game-speed.description | String | Description of the game speed option in the lobby. |
| GameSpeed |  | String | Default game speed (leave empty to use the default defined in mod.yaml). |
| GameSpeedDropdownLocked | False | Boolean | Prevent the game speed from being changed in the lobby. |
| GameSpeedDropdownVisible | True | Boolean | Display the game speed option in the lobby. |
| GameSpeedDropdownDisplayOrder | 0 | Integer | Display order for the game speed option in the lobby. |

### MapStartingLocations
**Allows the map to have working spawnpoints. Also controls the 'Separate Team Spawns' checkbox in the lobby options.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| InitialExploreRange | 5c0 | 1D World Distance |  |
| SeparateTeamSpawnsCheckboxLabel | checkbox-separate-team-spawns.label | String | Descriptive label for the spawn positions checkbox in the lobby. |
| SeparateTeamSpawnsCheckboxDescription | checkbox-separate-team-spawns.description | String | Tooltip description for the spawn positions checkbox in the lobby. |
| SeparateTeamSpawnsCheckboxEnabled | True | Boolean | Default value of the spawn positions checkbox in the lobby. |
| SeparateTeamSpawnsCheckboxLocked | False | Boolean | Prevent the spawn positions state from being changed in the lobby. |
| SeparateTeamSpawnsCheckboxVisible | True | Boolean | Whether to display the spawn positions checkbox in the lobby. |
| SeparateTeamSpawnsCheckboxDisplayOrder | 0 | Integer | Display order for the spawn positions checkbox in the lobby. |

### MarkerLayerOverlay

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Colors | FF0000, FF7F00, FFEE46, 00FF21, 00FFFF, 002AFF, A500FF, FF00DC | Collection of Color (RRGGBB[AA] notation) | A list of colors to be used for drawing. |
| Alpha | 85 | Integer | Default alpha blend. |
| AxisAngleColor | DC143C | Color (RRGGBB[AA] notation) | Color of the axis angle display. |

### McvManagerBotModule
**Manages AI MCVs.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| McvTypes |  | Set of String | Actor types that are considered MCVs (deploy into base builders). |
| ConstructionYardTypes |  | Set of String | Actor types that are considered construction yards (base builders). |
| McvFactoryTypes |  | Set of String | Actor types that are able to produce MCVs. |
| MinimumConstructionYardCount | 1 | Integer | Try to maintain at least this many ConstructionYardTypes, build an MCV if number is below this. |
| ScanForNewMcvInterval | 20 | Integer | Delay (in ticks) between looking for and giving out orders to new MCVs. |
| MinBaseRadius | 2 | Integer | Minimum distance in cells from center of the base when checking for MCV deployment location. |
| MaxBaseRadius | 20 | Integer | Maximum distance in cells from center of the base when checking for MCV deployment location. Only applies if RestrictMCVDeploymentFallbackToBase is enabled and there's at least one construction yard. |
| RestrictMCVDeploymentFallbackToBase | True | Boolean | Should deployment of additional MCVs be restricted to MaxBaseRadius if explicit deploy locations are missing or occupied? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### MenuPostProcessEffect
**Fades the world from/to black at the start/end of the game, and can (optionally) desaturate the world**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| FadeLength | 10 | Integer | Time (in ticks) to fade between states |
| Effect | None | [`EffectType`](#effecttype) | Effect style to fade to during gameplay. Accepts values of None or Desaturated. |
| MenuEffect | None | [`EffectType`](#effecttype) | Effect style to fade to when opening the in-game menu. Accepts values of None, Black or Desaturated. |

### MineImmune
**Tag trait for stuff that should not trigger mines.**

### Mine

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CrushClasses |  | Collection of CrushClass |  |
| AvoidFriendly | True | Boolean |  |
| BlockFriendly | True | Boolean |  |
| DetonateClasses |  | Collection of CrushClass |  |

### MinelayerBotModule
**Manages AI minelayer unit related with Minelayer traits. When enemy damage AI's actors, the location of conflict will be recorded, If a location is a valid spot, it will add/merge to favorite location for usage later**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IgnoredEnemyTargetTypes |  | Collection of TargetableType | Enemy target types to ignore when add the minefield location to conflict location. |
| UseEnemyLocationTargetTypes |  | Collection of TargetableType | Victim target types that considering conflict location as enemy location instead of victim location. |
| MinelayingActorTypes |  | Set of String | Actors with Minelayertrait. |
| MaxPerAssign | 1 | Integer | Find this amount of suitable actors and lay mine to a location. |
| ScanTick | 320 | Integer | Scan suitable actors and target in this interval. |
| MineFieldRadius | 1 | Integer | Radius per mine laying order. |
| AwayFromAlliedTargetTypes |  | Collection of TargetableType | Minefield location is cancelled if those whose target type belong to allied nearby. |
| AwayFromEnemyTargetTypes |  | Collection of TargetableType | Minefield location is cancelled if those whose target type belong to enemy nearby. |
| AwayFromCellDistance | 9 | Integer | Minefield location check distance to AwayFromAlliedTargettype and AwayFromEnemyTargettype. In addition, if any emeny actor within this range and minefield location is not cancelled, minelayer will try lay mines at the 3/4 path to minefield location |
| FavoritePositionDistance | 6 | Integer | Merge conflict point minefield position to a favorite minefield position if within this range and closest. If favorite minefield positions is at the max of 5, we always merge it to closest regardless of this |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Minelayer

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Mine | minv | String |  |
| AmmoPoolName | primary | String |  |
| MinefieldDepth | 1c512 | 1D World Distance |  |
| Voice | Action | String | Voice to use when ordered to lay a minefield. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line when laying mines. |
| TileValidName | build-valid | String | Sprite overlay to use for valid minefield cells. |
| TileInvalidName | build-invalid | String | Sprite overlay to use for invalid minefield cells. |
| TileUnknownName | build-unknown | String | Sprite overlay to use for minefield cells hidden behind fog or shroud. |
| TerrainTypes |  | Set of String | Only allow laying mines on listed terrain types. Leave empty to allow all terrain types. |
| DeployCursor | deploy | String | Cursor to display when able to lay a mine. |
| DeployBlockedCursor | deploy-blocked | String | Cursor to display when unable to lay a mine. |
| AbilityCursor | ability | String | Cursor to display when able to lay a mine. |
| AmmoUsage | 1 | Integer | Ammo the minelayer consumes per mine. |
| PreLayDelay | 0 | Integer | Number of ticks it takes to lay a mine. |
| AfterLayingDelay | 20 | Integer | Number of ticks for the minelayer to wait after laying a mine. The wait can be interrupted by a player order. |

### MissionData
**Defines the FMVs that can be played by missions.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Briefing |  | String | Briefing text displayed in the mission browser. |
| BackgroundVideo |  | String | Played by the "Background Info" button in the mission browser. |
| BriefingVideo |  | String | Played by the "Briefing" button in the mission browser. |
| StartVideo |  | String | Automatically played before starting the mission. |
| WinVideo |  | String | Automatically played when the player wins the mission. |
| LossVideo |  | String | Automatically played when the player loses the mission. |

### MissionObjectives

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Cooperative | False | Boolean | Set this to true if multiple cooperative players have a distinct set of objectives that each of them has to complete to win the game. This is mainly useful for multiplayer coop missions. Do not use this for skirmish team games. |
| EarlyGameOver | False | Boolean | If set to true, this setting causes the game to end immediately once the first player (or team of cooperative players) fails or completes his objectives.  If set to false, players that fail their objectives will stick around and become observers. |
| GameOverDelay | 1500 | Integer | Delay between the game over condition being met, and the game actually ending, in milliseconds. |
| WinNotification |  | String |  |
| WinTextNotification |  | String |  |
| LoseNotification |  | String |  |
| LoseTextNotification |  | String |  |
| LeaveNotification |  | String |  |
| LeaveTextNotification |  | String |  |

### Mobile
**Unit is able to move.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Locomotor | *(required)* | String | Which Locomotor does this trait use. Must be defined on the World actor. |
| InitialFacing | 0 | 1D World Angle |  |
| TurnSpeed | 512 | 1D World Angle | Speed at which the actor turns. |
| Speed | 1 | Integer |  |
| AlwaysTurnInPlace | False | Boolean | If set to true, this unit will always turn in place instead of following a curved trajectory (like infantry). |
| TurnsWhileMoving | False | Boolean | If set to true, this unit won't stop to turn, it will turn while moving instead. |
| Cursor | move | String | Cursor to display when a move order can be issued at target location. |
| TerrainCursors |  | Dictionary with Key: String, Value: String | Cursor overrides to display for specific terrain types. A dictionary of [terrain type]: [cursor name]. |
| BlockedCursor | move-blocked | String | Cursor to display when a move order cannot be issued at target location. |
| Voice | Action | String |  |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line for regular move orders. |
| PreviewFacing | 384 | 1D World Angle | Facing to use for actor previews (map editor, color picker, etc) |
| EditorFacingDisplayOrder | 3 | Integer | Display order for the facing slider in the map editor |
| CanMoveBackward | False | Boolean | Can move backward if possible |
| BackwardDuration | 40 | Integer | After how many ticks the actor will turn forward during backoff. If set to -1 the unit will be allowed to move backwards without time limit. |
| MaxBackwardCells | 15 | Integer | Actor will only try to move backwards when the path (in cells) is shorter than this value. If set to -1 the unit will be allowed to move backwards without range limit. |
| RequireForceMoveCondition |  | BooleanExpression | Boolean expression defining the condition under which the regular (non-force) move cursor is disabled. |
| ImmovableCondition |  | BooleanExpression | Boolean expression defining the condition under which this actor cannot be nudged by other actors. |
| TerrainOrientationAdjustmentMargin | -0c1 | 1D World Distance | The distance from the edge of a cell over which the actor will adjust its tilt when moving between cells with different ramp types. -1 means that the actor does not tilt on slopes. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ModularBot
**Bot that uses BotModules.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | *(required)* | String | Internal id for this bot. |
| Name | Unnamed Bot | String | Human-readable name this bot uses. |
| MinOrderQuotientPerTick | 5 | Integer | Minimum portion of pending orders to issue each tick (e.g. 5 issues at least 1/5th of all pending orders). Excess orders remain queued for subsequent ticks. |

### MusicPlaylist
**Trait for music handling. Attach this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| StartingMusic |  | String | Music to play when the map starts. Plays the first song on the playlist when undefined. |
| VictoryMusic |  | String | Music to play when the game has been won. |
| DefeatMusic |  | String | Music to play when the game has been lost. |
| BackgroundMusic |  | String | This track is played when no other music is playing. It cannot be paused, but can be overridden by selecting a new track. |
| AllowMuteBackgroundMusic | False | Boolean | Allow the background music to be muted by the player. |
| DisableWorldSounds | False | Boolean | Disable all world sounds (combat etc). |

### MustBeDestroyed
**Actors with this trait must be destroyed for a game to end.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RequiredForShortGame | False | Boolean | In a short game only actors that have this value set to true need to be destroyed. |

### NukePower

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MissileWeapon | *(required)* | String | Weapon to use for the impact. |
| MissileDelay | 0 | Integer | Delay (in ticks) after launch until the missile is spawned. |
| MissileImage |  | String | Image to use for the missile. |
| MissileUp | up | String | Sprite sequence for the ascending missile. |
| MissileDown | down | String | Sprite sequence for the descending missile. |
| SpawnOffset | 0,0,0 | 3D World Vector | Offset from the actor the missile spawns on. |
| DetonationAltitude | 0c0 | 1D World Distance | Altitude offset from the target position at which the warhead should detonate. |
| RemoveMissileOnDetonation | True | Boolean | Should nuke missile projectile be removed on detonation above ground. 'False' will make the missile continue until it hits the ground and disappears (without triggering another explosion). |
| MissilePalette | effect | String | Palette to use for the missile weapon image. |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName. |
| TrailImage |  | String | Trail animation. |
| TrailSequences |  | Collection of String | Loop a randomly chosen sequence of TrailImage from this list while this projectile is moving. |
| TrailInterval | 1 | Integer | Interval in ticks between each spawned Trail animation. |
| TrailDelay | 1 | Integer | Delay in ticks until trail animation is spawned. |
| TrailPalette | effect | String | Palette used to render the trail sequence. |
| TrailUsePlayerPalette | False | Boolean | Use the Player Palette to render the trail sequence. |
| FlightDelay | 400 | Integer | Travel time - split equally between ascent and descent. |
| FlightVelocity | 0c512 | 1D World Distance | Visual ascent velocity in WDist / tick. |
| SkipAscent | False | Boolean | Descend immediately on the target. |
| BeaconRemoveAdvance | 25 | Integer | Amount of time before detonation to remove the beacon. |
| CameraRange | 0c0 | 1D World Distance | Range of cells the camera should reveal around target cell. |
| RevealGeneratedShroud | True | Boolean | Can the camera reveal shroud generated by the `CreatesShroud` trait? |
| CameraRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Reveal cells to players with these relationships only. |
| CameraSpawnAdvance | 25 | Integer | Amount of time before detonation to spawn the camera. |
| CameraRemoveDelay | 25 | Integer | Amount of time after detonation to remove the camera. |
| CircleColor | FF000080 | Color (RRGGBB[AA] notation) | Range circle color. |
| CircleWidth | 1 | Real Number | Range circle width in pixel. |
| CircleBorderColor | FF000040 | Color (RRGGBB[AA] notation) | Range circle border color. |
| CircleBorderWidth | 3 | Real Number | Range circle border width in pixel. |
| CircleRanges |  | Collection of 1D World Distance | Render circles based on these distance ranges while targeting. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | NukePowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ObjectivesPanel
**Provides game mode progress information for players. Goes on WorldActor - observers don't have a player it can live on. Current options for PanelName are 'SKIRMISH_STATS' and 'MISSION_OBJECTIVES'.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PanelName |  | String |  |
| ExitDelay | 1400 | Integer | in ms |

### OrderEffects
**Renders an effect at the order target locations.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TerrainFlashImage | *(required)* | String | The image to use. |
| TerrainFlashSequence | *(required)* | String | The sequence to use. |
| TerrainFlashPalette |  | String | The palette to use. |
| ActorFlashType | Overlay | [`ActorFlashType`](#actorflashtype) | The type of effect to apply to targeted (frozen) actors. Accepts values Overlay and Tint. |
| ActorFlashOverlayColor | FFFFFF | Color (RRGGBB[AA] notation) | The overlay color to display when ActorFlashType is Overlay. |
| ActorFlashOverlayAlpha | 0.5 | Real Number | The overlay transparency to display when ActorFlashType is Overlay. |
| ActorFlashTint | 1.4,1.4,1.4 | float3 | The tint to apply when ActorFlashType is Tint. |
| ActorFlashCount | 2 | Integer | Number of times to flash (frozen) actors. |
| ActorFlashInterval | 2 | Integer | Number of ticks between (frozen) actor flashes. |

### OwnerLostAction
**Perform an action when the actor's owner is defeated.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Action | Kill | [`OwnerLostActionType`](#ownerlostactiontype) | What does this unit do when its owner loses. Allowed values are 'ChangeOwner', 'Dispose', 'Kill' |
| Owner | Neutral | String | Map player to use when 'Action' is 'ChangeOwner'. |
| DeathTypes |  | Collection of DamageType | The deathtypes used when 'Action' is 'Kill'. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### PaletteFromEmbeddedSpritePalette

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Internal palette name |
| Filename | *(required)* | String | Filename of sprite that contains the palette definition. |
| Frame | 0 | Integer | Image frame associated with the palette definition, if relevant. |
| AllowModifiers | True | Boolean | Allow palette modifiers to change the palette. |
| CursorPalette | False | Boolean | Whether this palette is available for cursors. |

### PaletteFromFile
**Load VGA palette (.pal) registers.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Internal palette name |
| Tileset |  | String | If defined, load the palette only for this tileset. |
| Filename | *(required)* | String | filename to load |
| TransparentIndex | 0 | Collection of Integer | Map listed indices to transparent. Ignores previous color. |
| ShadowIndex |  | Collection of Integer | Map listed indices to shadow. Ignores previous color. |
| AllowModifiers | True | Boolean |  |
| CursorPalette | False | Boolean | Whether this palette is available for cursors. |

### PaletteFromGimpOrJascFile
**Load a GIMP .gpl or JASC .pal palette file. Supports per-color alpha.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Palette name used internally. |
| Tilesets |  | Set of String | Defines for which tileset IDs this palette should be loaded. If none specified, it applies to all tileset IDs not explicitly excluded. |
| ExcludeTilesets |  | Set of String | Don't load palette for these tileset IDs. |
| Filename | *(required)* | String | Name of the file to load. |
| Premultiply | True | Boolean | Premultiply colors with their alpha values. |
| AllowModifiers | True | Boolean |  |
| TransparentIndex | 0 | Integer | Index set to be fully transparent/invisible. |
| CursorPalette | False | Boolean | Whether this palette is available for cursors. |

### PaletteFromGrayscale
**Creates a greyscale palette without any base palette file.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Internal palette name |
| Tileset |  | String | If defined, load the palette only for this tileset. |
| AllowModifiers | True | Boolean |  |
| TransparentIndex | 0 | Integer | Index set to be fully transparent/invisible. |

### PaletteFromPaletteWithAlpha
**Create a palette by applying alpha transparency to another palette.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Internal palette name |
| BasePalette | *(required)* | String | The name of the palette to base off. |
| AllowModifiers | True | Boolean | Allow palette modifiers to change the palette. |
| Alpha | 1 | Real Number | Alpha component that is applied to the base palette. |
| Premultiply | True | Boolean | Premultiply color by the alpha component. |

### PaletteFromPlayerPaletteWithAlpha
**Create player palettes by applying alpha transparency to another player palette.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BaseName | *(required)* | String | The prefix for the resulting player palettes |
| BasePalette | *(required)* | String | The name of the player palette to base off. |
| AllowModifiers | True | Boolean | Allow palette modifiers to change the palette. |
| Alpha | 1 | Real Number | Alpha component that is applied to the base palette. |
| Premultiply | True | Boolean | Premultiply color by the alpha component. |

### PaletteFromPng
**Load a PNG and use its embedded palette.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Internal palette name |
| Tileset |  | String | If defined, load the palette only for this tileset. |
| Filename | *(required)* | String | Filename to load |
| ShadowIndex |  | Collection of Integer | Map listed indices to shadow. Ignores previous color. |
| AllowModifiers | True | Boolean |  |
| CursorPalette | False | Boolean | Whether this palette is available for cursors. |

### PaletteFromRGBA
**Creates a single color palette without any base palette file.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name | *(required)* | String | Internal palette name |
| Tileset |  | String | If defined, load the palette only for this tileset. |
| R | 0 | Integer | red color component |
| G | 0 | Integer | green color component |
| B | 0 | Integer | blue color component |
| A | 255 | Integer | alpha channel (transparency) |
| AllowModifiers | True | Boolean |  |
| TransparentIndex | 0 | Integer | Index set to be fully transparent/invisible. |

### Parachutable
**Can be paradropped by a ParaDrop actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| KilledOnImpassableTerrain | True | Boolean | If we land on invalid terrain for my actor type should we be killed? |
| DamageTypes |  | Collection of DamageType | Types of damage that this trait causes to self when 'KilledOnImpassableTerrain' is true. Leave empty for no damage types. |
| Image | explosion | String | Image where Ground/WaterCorpseSequence is looked up. |
| GroundCorpseSequence |  | String |  |
| GroundCorpsePalette | effect | String |  |
| GroundImpactSound |  | String |  |
| WaterCorpseSequence |  | String |  |
| WaterCorpsePalette | effect | String |  |
| WaterTerrainTypes | Water | Set of String | Terrain types on which to display WaterCorpseSequence. |
| WaterImpactSound |  | String |  |
| FallRate | 13 | Integer |  |
| ParachutingCondition |  | String | The condition to grant to self while parachuting. |

### ParaDrop
**This unit can spawn and eject other actors while flying.**

> Requires trait(s): [`Cargo`](#cargo).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DropRange | 4c0 | 1D World Distance | Distance around the drop-point to unload troops. |
| DropInterval | 5 | Integer | Wait at least this many ticks between each drop. |
| ChuteSound |  | String | Sound to play when dropping. |

### ParallelProductionQueue

> Inherits from: [`ProductionQueue`](#productionqueue).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | *(required)* | String | What kind of production will be added (e.g. Building, Infantry, Vehicle, ...) |
| DisplayOrder | 0 | Integer | The value used when ordering this for display (e.g. in the Spectator UI). |
| Group |  | String | Group queues from separate buildings together into the same tab. |
| Factions |  | Set of String | Only enable this queue for certain factions. |
| Sticky | True | Boolean | Should the prerequisite remain enabled if the owner changes? |
| PayUpFront | False | Boolean | Player must pay for item upfront |
| DisallowPaused | False | Boolean | Should right clicking on the icon instantly cancel the production instead of putting it on hold? |
| BuildDurationModifier | 100 | Integer | This percentage value is multiplied with actor cost to translate into build time (lower means faster). |
| ItemLimit | 999 | Integer | Maximum number of a single actor type that can be queued (0 = infinite). |
| QueueLimit | 0 | Integer | Maximum number of items that can be queued across all actor types (0 = infinite). |
| LowPowerModifier | 100 | Integer | The build time is multiplied with this percentage on low power. |
| InfiniteBuildLimit | -1 | Integer | Production items that have more than this many items in the queue will be produced in a loop. |
| ReadyAudio |  | String | Notification played when production is complete. The filename of the audio is defined per faction in notifications.yaml. |
| ReadyTextNotification |  | String | Notification displayed when production is complete. |
| BlockedAudio |  | String | Notification played when you can't train another actor when the build limit exceeded or the exit is jammed. The filename of the audio is defined per faction in notifications.yaml. |
| BlockedTextNotification |  | String | Notification displayed when you can't train another actor when the build limit exceeded or the exit is jammed. |
| LimitedAudio |  | String | Notification played when you can't queue another actor when the queue length limit is exceeded. The filename of the audio is defined per faction in notifications.yaml. |
| LimitedTextNotification |  | String | Notification displayed when you can't queue another actor when the queue length limit is exceeded. |
| CannotPlaceAudio |  | String | Notification played when you can't place a building. Overrides PlaceBuilding.CannotPlaceNotification for this queue. The filename of the audio is defined per faction in notifications.yaml. |
| QueuedAudio |  | String | Notification played when user clicks on the build palette icon. The filename of the audio is defined per faction in notifications.yaml. |
| QueuedTextNotification |  | String | Notification displayed when user clicks on the build palette icon. |
| OnHoldAudio |  | String | Notification played when player right-clicks on the build palette icon. The filename of the audio is defined per faction in notifications.yaml. |
| OnHoldTextNotification |  | String | Notification displayed when player right-clicks on the build palette icon. |
| CancelledAudio |  | String | Notification played when player right-clicks on a build palette icon that is already on hold. The filename of the audio is defined per faction in notifications.yaml. |
| CancelledTextNotification |  | String | Notification displayed when player right-clicks on a build palette icon that is already on hold. |

### ParatroopersPower

> Inherits from: `DirectionalSupportPower`, `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UnitType | badr | String |  |
| SquadSize | 1 | Integer |  |
| SquadOffset | -1536,1536,0 | 3D World Vector |  |
| ReinforcementsArrivedSpeechNotification |  | String | Speech notification to play when entering the drop zone. |
| ReinforcementsArrivedTextNotification |  | String | Text notification to display when entering the drop zone. |
| QuantizedFacings | 32 | Integer | Number of facings that the delivery aircraft may approach from. |
| Cordon | 5c0 | 1D World Distance | Spawn and remove the plane this far outside the map. |
| DropItems |  | Collection of String | Troops to be delivered.  They will be distributed between the planes if SquadSize > 1. |
| AllowImpassableCells | False | Boolean | Risks stuck units when they don't have the Paratrooper trait. |
| CameraActor |  | String | Actor to spawn when the paradrop starts. |
| CameraRemoveDelay | 85 | Integer | Amount of time (in ticks) to keep the camera alive while the passengers drop. |
| BeaconDistanceOffset | 4c0 | 1D World Distance | Weapon range offset to apply during the beacon clock calculation. |
| UseDirectionalTarget | False | Boolean | Enables the player directional targeting |
| Arrows | arrow-t, arrow-tl, arrow-l, arrow-bl, arrow-b, arrow-br, arrow-r, arrow-tr | Collection of String |  |
| DirectionArrowAnimation |  | String | Animation used to render the direction arrows. |
| DirectionArrowPalette | chrome | String | Palette for direction cursor animation. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | ParatroopersPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Passenger
**This actor can enter Cargo actors.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CargoType |  | String |  |
| CustomPipType |  | String | If defined, use a custom pip type defined on the transport's WithCargoPipsDecoration.CustomPipSequences list. |
| Weight | 1 | Integer |  |
| CargoCondition |  | String | The condition to grant to when this actor is loaded inside any transport. |
| CargoConditions |  | Dictionary with Key: String, Value: String | Conditions to grant when this actor is loaded inside specified transport. A dictionary of [actor name]: [condition]. |
| Voice | Action | String |  |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| RequireForceMoveCondition |  | BooleanExpression | Boolean expression defining the condition under which the regular (non-force) enter cursor is disabled. |
| EnterCursor | enter | String | Cursor to display when able to enter target actor. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to enter target actor. |

### PathFinder
**Calculates routes for mobile actors with locomotors based on the A* search algorithm.  Attach this to the world actor.**

> Requires trait(s): [`ActorMap`](#actormap), [`Locomotor`](#locomotor).

### PathFinderOverlay
**Renders a visualization overlay showing how the pathfinder searches for paths. Attach this to the world actor.**

> Requires trait(s): [`PathFinder`](#pathfinder).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Font | TinyBold | String |  |
| TargetLineColor | FF0000 | Color (RRGGBB[AA] notation) |  |
| AbstractColor1 | 00FF00 | Color (RRGGBB[AA] notation) |  |
| AbstractColor2 | 98FB98 | Color (RRGGBB[AA] notation) |  |
| LocalColor1 | FFFF00 | Color (RRGGBB[AA] notation) |  |
| LocalColor2 | FFFFE0 | Color (RRGGBB[AA] notation) |  |
| ShowCosts | True | Boolean |  |

### PlaceBeacon
**A beacon that is constructed from a circle sprite that is animated once and a moving arrow sprite.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Duration | 750 | Integer |  |
| NotificationType | Sounds | String |  |
| Notification | Beacon | String |  |
| IsPlayerPalette | True | Boolean |  |
| Palette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence | arrow | String |  |
| CircleSequence | circles | String |  |

### PlaceBuilding
**Allows the player to execute build orders.  Attach this to the player actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| NewOptionsNotificationDelay | 10 | Integer | Play NewOptionsNotification this many ticks after building placement. |
| NewOptionsNotification |  | String | Speech notification to play after building placement if new construction options are available. |
| NewOptionsTextNotification |  | String | Text notification to display after building placement if new construction options are available. |
| CannotPlaceNotification |  | String | Speech notification to play if building placement is not possible. |
| CannotPlaceTextNotification |  | String | Text notification to display if building placement is not possible. |
| ToggleVariantKey | OpenRA.HotkeyReference | HotkeyReference | Hotkey to toggle between PlaceBuildingVariants when placing a structure. |

### PlaceBuildingVariants
**Place a different building when PlaceBuilding's ToggleVariantKey hotkey is pressed while the PlaceBuildingOrderGenerator is active.**

> Requires trait(s): [`Buildable`](#buildable), [`Building`](#building).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Actors | *(required)* | Collection of String | Variant actors that can be cycled between when placing a structure. |
| Facings |  | Collection of 1D World Angle | Facing of the non-variant actor, followed by facings for each variant actor. The length equals the length of Actors + 1. |

### PlayerColorPalette
**Add this to the World actor definition.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BasePalette |  | String | The name of the palette to base off. |
| BaseName | player | String | The prefix for the resulting player palettes |
| RemapIndex |  | Collection of Integer | Remap these indices to player colors. |
| AllowModifiers | True | Boolean | Allow palette modifiers to change the palette. |

### PlayerColorShift
**Add color shifts to player palettes. Use to add RGBA compatibility to PlayerColorPalette.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BasePalette | *(required)* | String | The name of the palette to base off. |
| MinHue | 0.29 | Real Number | Hues between this and MaxHue will be shifted. |
| MaxHue | 0.37 | Real Number | Hues between MinHue and this will be shifted. |
| ReferenceHue | 0.33 | Real Number | Hue reference for the color shift. |
| ReferenceSaturation | 0.925 | Real Number | Saturation reference for the color shift. |
| ReferenceValue | 0.95 | Real Number | Value reference for the color shift. |

### PlayerExperience
**This trait can be used to track player experience based on units killed with the `GivesExperience` trait. It can also be used as a point score system in scripted maps, for example. Attach this to the player actor.**

### PlayerRadarTerrain

> Requires trait(s): [`Shroud`](#shroud).

### PlayerResources

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DefaultCashDropdownLabel | Starting Cash | String | Descriptive label for the starting cash option in the lobby. |
| DefaultCashDropdownDescription | The amount of cash that players start with | String | Tooltip description for the starting cash option in the lobby. |
| SelectableCash | 2500, 5000, 10000, 20000 | Collection of Integer | Starting cash options that are available in the lobby options. |
| DefaultCash | 5000 | Integer | Default starting cash option: should be one of the SelectableCash options. |
| DefaultCashDropdownLocked | False | Boolean | Force the DefaultCash option by disabling changes in the lobby. |
| DefaultCashDropdownVisible | True | Boolean | Whether to display the DefaultCash option in the lobby. |
| DefaultCashDropdownDisplayOrder | 0 | Integer | Display order for the DefaultCash option. |
| InsufficientFundsNotification |  | String | Speech notification to play when the player does not have any funds. |
| InsufficientFundsTextNotification |  | String | Text notification to display when the player does not have any funds. |
| InsufficientFundsNotificationInterval | 30000 | Integer | Delay (in milliseconds) during which warnings will be muted. |
| CashTickUpNotification |  | String |  |
| CashTickDownNotification |  | String |  |
| ResourceValues |  | Dictionary with Key: String, Value: Integer | Monetary value of each resource type. Dictionary of [resource type]: [value per unit]. |

### PlayerStatistics
**Attach this to the player actor to collect observer stats.**

### Pluggable

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Offset | 0,0 | 2D Cell Vector | Footprint cell offset where a plug can be placed. |
| Conditions | *(required)* | Dictionary with Key: String, Value: String | Conditions to grant for each accepted plug type. Key is the plug type. Value is the condition that is granted when the plug is enabled. |
| Requirements |  | Dictionary with Key: String, Value: BooleanExpression | Requirements for accepting a plug type. Key is the plug type that the requirements applies to. Value is the condition expression defining the requirements to place the plug. |
| EditorOptions |  | Dictionary with Key: String, Value: String | Options to display in the map editor. Key is the plug type that the requirements applies to. Value is the label that is displayed in the actor editor dropdown. |
| EmptyOption | Empty | String | Label to use for an empty plug socket. |
| EditorDisplayOrder | 5 | Integer | Display order for the dropdown in the map editor |

### Plug

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | *(required)* | String | Plug type (matched against Conditions in Pluggable) |

### Power

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Amount | 0 | Integer | If negative, it will drain power. If positive, it will provide power. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### PowerManager
**Attach this to the player actor.**

> Requires trait(s): [`DeveloperMode`](#developermode).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AdviceInterval | 10000 | Integer | Interval (in milliseconds) at which to warn the player of low power. |
| SpeechNotification |  | String | The speech notification to play when the player is low power. |
| TextNotification |  | String | The text notification to display when the player is low power. |

### PowerMultiplier
**Modifies the power usage/output of this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### PowerTooltip
**Shown power info on the build palette widget.**

### PrimaryBuilding
**Used together with ClassicProductionQueue.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PrimaryCondition |  | String | The condition to grant to self while this is the primary building. |
| SelectionNotification |  | String | Speech notification to play when selecting a primary building. |
| SelectionTextNotification |  | String | Text notification to display when selecting a primary building. |
| ProductionQueues |  | Collection of String | List of production queues for which the primary flag should be set. If empty, the list given in the `Produces` property of the `Production` trait will be used. |
| Cursor | deploy | String | Cursor to display when setting the primary building. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProduceActorPower
**Produces an actor without using the standard production queue.**

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Actors | *(required)* | Collection of String | Actors to produce. |
| Type | *(required)* | String | Production queue type to use |
| ReadyAudio |  | String | Speech notification played when production is activated. The filename of the audio is defined per faction in notifications.yaml. |
| ReadyTextNotification |  | String | Text notification displayed when production is activated. |
| BlockedAudio |  | String | Speech notification played when the exit is jammed. The filename of the audio is defined per faction in notifications.yaml. |
| BlockedTextNotification |  | String | Text notification displayed when the exit is jammed. |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | ProduceActorPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProducibleWithLevel
**Actors possessing this trait should define the GainsExperience trait. When the prerequisites are fulfilled,  this trait grants a level-up to newly spawned actors.**

> Requires trait(s): [`GainsExperience`](#gainsexperience).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Prerequisites |  | Collection of String |  |
| InitialLevels | 1 | Integer | Number of levels to give to the actor on creation. |
| SuppressLevelupAnimation | True | Boolean | Should the level-up animation be suppressed when actor is created? |

### ProductionAirdrop
**Deliver the unit in production via skylift.**

> Inherits from: [`Production`](#production), `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ReadyAudio | Reinforce | String | Speech notification to play when a unit is delivered. |
| ReadyTextNotification |  | String | Text notification to display when a unit is delivered. |
| ActorType | *(required)* | String | Cargo aircraft used for delivery. Must have the `Aircraft` trait. |
| BaselineSpawn | False | Boolean | The cargo aircraft will spawn at the player baseline (map edge closest to the player spawn) |
| Facing | 256 | 1D World Angle | Direction the aircraft should face to land. |
| WaitTickBeforeProduce | 0 | Integer | Tick that aircraft should wait before producing. |
| WaitTickAfterProduce | 0 | Integer | Tick that aircraft should wait after producing. |
| LandOffset | 0,0,0 | 3D World Vector | Offset the aircraft used for landing. |
| Produces | *(required)* | Collection of String | e.g. Infantry, Vehicles, Aircraft, Buildings |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProductionCostMultiplier
**Modifies the production cost of this actor for a specific queue or when a prerequisite is granted.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Multiplier | 100 | Integer | Percentage modifier to apply. |
| Prerequisites |  | Collection of String | Only apply this cost change if owner has these prerequisites. |
| Queue |  | Set of String | Queues that this cost will apply. |

### ProductionFromMapEdge
**Produce a unit on the closest map edge cell and move into the world.**

> Inherits from: [`Production`](#production), `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Produces | *(required)* | Collection of String | e.g. Infantry, Vehicles, Aircraft, Buildings |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Production
**This unit has access to build queues.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Produces | *(required)* | Collection of String | e.g. Infantry, Vehicles, Aircraft, Buildings |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProductionParadrop
**Deliver the unit in production via paradrop.**

> Inherits from: [`Production`](#production), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Exit`](#exit).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ActorType | badr | String | Cargo aircraft used. Must have Aircraft trait. |
| ChuteSound |  | String | Sound to play when dropping the unit. |
| ReadyAudio |  | String | Speech notification to play when dropping the unit. |
| ReadyTextNotification |  | String | Text notification to display when dropping the unit. |
| Produces | *(required)* | Collection of String | e.g. Infantry, Vehicles, Aircraft, Buildings |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProductionQueueFromSelection

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ProductionTabsWidget |  | String |  |
| ProductionPaletteWidget |  | String |  |

### ProductionQueue
**Attach this to an actor (usually a building) to let it produce units or construct buildings. If one builds another actor of this type, he will get a separate queue to create two actors at the same time. Will only work together with the Production: trait.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | *(required)* | String | What kind of production will be added (e.g. Building, Infantry, Vehicle, ...) |
| DisplayOrder | 0 | Integer | The value used when ordering this for display (e.g. in the Spectator UI). |
| Group |  | String | Group queues from separate buildings together into the same tab. |
| Factions |  | Set of String | Only enable this queue for certain factions. |
| Sticky | True | Boolean | Should the prerequisite remain enabled if the owner changes? |
| PayUpFront | False | Boolean | Player must pay for item upfront |
| DisallowPaused | False | Boolean | Should right clicking on the icon instantly cancel the production instead of putting it on hold? |
| BuildDurationModifier | 100 | Integer | This percentage value is multiplied with actor cost to translate into build time (lower means faster). |
| ItemLimit | 999 | Integer | Maximum number of a single actor type that can be queued (0 = infinite). |
| QueueLimit | 0 | Integer | Maximum number of items that can be queued across all actor types (0 = infinite). |
| LowPowerModifier | 100 | Integer | The build time is multiplied with this percentage on low power. |
| InfiniteBuildLimit | -1 | Integer | Production items that have more than this many items in the queue will be produced in a loop. |
| ReadyAudio |  | String | Notification played when production is complete. The filename of the audio is defined per faction in notifications.yaml. |
| ReadyTextNotification |  | String | Notification displayed when production is complete. |
| BlockedAudio |  | String | Notification played when you can't train another actor when the build limit exceeded or the exit is jammed. The filename of the audio is defined per faction in notifications.yaml. |
| BlockedTextNotification |  | String | Notification displayed when you can't train another actor when the build limit exceeded or the exit is jammed. |
| LimitedAudio |  | String | Notification played when you can't queue another actor when the queue length limit is exceeded. The filename of the audio is defined per faction in notifications.yaml. |
| LimitedTextNotification |  | String | Notification displayed when you can't queue another actor when the queue length limit is exceeded. |
| CannotPlaceAudio |  | String | Notification played when you can't place a building. Overrides PlaceBuilding.CannotPlaceNotification for this queue. The filename of the audio is defined per faction in notifications.yaml. |
| QueuedAudio |  | String | Notification played when user clicks on the build palette icon. The filename of the audio is defined per faction in notifications.yaml. |
| QueuedTextNotification |  | String | Notification displayed when user clicks on the build palette icon. |
| OnHoldAudio |  | String | Notification played when player right-clicks on the build palette icon. The filename of the audio is defined per faction in notifications.yaml. |
| OnHoldTextNotification |  | String | Notification displayed when player right-clicks on the build palette icon. |
| CancelledAudio |  | String | Notification played when player right-clicks on a build palette icon that is already on hold. The filename of the audio is defined per faction in notifications.yaml. |
| CancelledTextNotification |  | String | Notification displayed when player right-clicks on a build palette icon that is already on hold. |

### ProductionTimeMultiplier
**Modifies the production time of this actor for a specific queue or when a prerequisite is granted.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Multiplier | 100 | Integer | Percentage modifier to apply. |
| Prerequisites |  | Collection of String | Only apply this time change if owner has these prerequisites. |
| Queue |  | Set of String | Queues that this time will apply. |

### ProvidesPrerequisite

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Prerequisite |  | String | The prerequisite type that this provides. If left empty it defaults to the actor's name. |
| RequiresPrerequisites |  | Collection of String | Only grant this prerequisite when you have these prerequisites. |
| Factions |  | Set of String | Only grant this prerequisite for certain factions. |
| ResetOnOwnerChange | False | Boolean | Should it recheck everything when it is captured? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProvidesTechPrerequisite

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Id |  | String | Internal id for this tech level. |
| Name |  | String | Name shown in the lobby options. |
| Prerequisites |  | Collection of String | Prerequisites to grant when this tech level is active. |

### ProximityCaptor
**Actor can capture ProximityCapturable actors.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types | *(required)* | Collection of CaptureType |  |

### ProximityCapturable
**Actor can be captured by units within a certain range.**

> Inherits from: `ProximityCapturableBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Range | 5c0 | 1D World Distance | Maximum range at which a ProximityCaptor actor can initiate the capture. |
| CaptorTypes | Player, Vehicle, Tank, Infantry | Collection of CaptureType | Allowed ProximityCaptor actors to capture this actor. |
| MustBeClear | False | Boolean | If set, the capturing process stops immediately after another player comes into range. |
| Sticky | False | Boolean | If set, the ownership will not revert back when the captor leaves the area. |
| Permanent | False | Boolean | If set, the actor can only be captured via this logic once. This option implies the `Sticky` behaviour as well. |
| DrawDecoration | True | Boolean | If set, will draw a border in the owner's color around the capturable area. |

### ProximityExternalCondition
**Applies a condition to actors within a specified range.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | The condition to apply. Must be included in the target actor's ExternalConditions list. |
| Range | 3c0 | 1D World Distance | The range to search for actors. |
| MaximumVerticalOffset | 0c0 | 1D World Distance | The maximum vertical range above terrain to search for actors. Ignored if 0 (actors are selected regardless of vertical distance). |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | What player relationships are affected. |
| AffectsParent | False | Boolean | Condition is applied permanently to this actor. |
| EnableSound |  | String |  |
| DisableSound |  | String |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### QuantizeFacingsFromSequence
**Derive facings from sprite body sequence.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | idle | String | Defines sequence to derive facings from. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RadarPings

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| FromRadius | 200 | Integer |  |
| ToRadius | 15 | Integer |  |
| ShrinkSpeed | 4 | Integer |  |
| RotationSpeed | 0.12 | Real Number |  |

### RallyPoint
**Used to waypoint units after production or repair is finished.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image | rallypoint | String |  |
| LineWidth | 1 | Integer | Width (in pixels) of the rallypoint line. |
| FlagSequence | flag | String |  |
| CirclesSequence | circles | String |  |
| Cursor | ability | String | Cursor to display when rally point can be set. |
| Palette | player | String | Custom indicator palette name |
| IsPlayerPalette | True | Boolean | Custom palette is a player palette BaseName |
| Path |  | Collection of 2D Cell Vector | A list of 0 or more offsets defining the initial rally point path. |
| Notification |  | String | Speech notification to play when setting a new rallypoint. |
| TextNotification |  | String | Text notification to display when setting a new rallypoint. |
| ForceSetType |  | String | Used to group equivalent actors to allow force-setting a rallypoint (e.g. for Primary production). |

### RangeMultiplier
**Modifies the range of weapons fired by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Rearmable

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RearmActors | *(required)* | Set of String | Actors that this actor can dock to and get rearmed by. |
| AmmoPools | primary | Set of String | Name(s) of AmmoPool(s) that use this trait to rearm. |

### Refinery

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UseStorage | True | Boolean | Store resources in silos. Adds cash directly without storing if set to false. |
| DiscardExcessResources | False | Boolean | Discard resources once silo capacity has been reached. |
| ShowTicks | True | Boolean |  |
| TickRate | 10 | Integer |  |

### RegionProximityCapturable
**Actor can be captured by units entering a certain set of cells.**

> Inherits from: `ProximityCapturableBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Region |  | Collection of 2D Cell Vector | Set of cell offsets (relative to the actor's Location) the ProximityCaptor needs to be in to initiate the capture.  A 'Region' ActorInit can be used to override this value per actor. If either is empty or non-existent,  the immediately neighboring cells of the actor will be used. |
| CaptorTypes | Player, Vehicle, Tank, Infantry | Collection of CaptureType | Allowed ProximityCaptor actors to capture this actor. |
| MustBeClear | False | Boolean | If set, the capturing process stops immediately after another player comes into range. |
| Sticky | False | Boolean | If set, the ownership will not revert back when the captor leaves the area. |
| Permanent | False | Boolean | If set, the actor can only be captured via this logic once. This option implies the `Sticky` behaviour as well. |
| DrawDecoration | True | Boolean | If set, will draw a border in the owner's color around the capturable area. |

### RejectsOrders
**Can be used to make a unit partly uncontrollable by the player.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Reject |  | Set of String | Explicit list of rejected orders. Leave empty to reject all minus those listed under Except. |
| Except |  | Set of String | List of orders that should *not* be rejected. Also overrides other instances of this trait's Reject fields. |
| RemoveOrders | False | Boolean | Remove current and all queued orders from the actor when this trait is enabled. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ReloadAmmoDelayMultiplier
**Modifies the reload time of ammo pools on this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ReloadAmmoPool
**Reloads an ammo pool.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AmmoPool | primary | String | Reload ammo pool with this name. |
| Delay | 50 | Integer | Reload time in ticks per Count. |
| Count | 1 | Integer | How much ammo is reloaded after Delay. |
| ResetOnFire | False | Boolean | Whether or not reload timer should be reset when ammo has been fired. |
| Sound |  | String | Play this sound each time ammo is reloaded. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ReloadDelayMultiplier
**Modifies the reload time of weapons fired by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RenderJammerCircle

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Color | FF000080 | Color (RRGGBB[AA] notation) | Range circle color. |
| Width | 1 | Real Number | Range circle line width. |
| BorderColor | 00000060 | Color (RRGGBB[AA] notation) | Range circle border color. |
| BorderWidth | 3 | Real Number | Range circle border width. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RenderShroudCircle

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Color | 00FFFF80 | Color (RRGGBB[AA] notation) | Color of the circle. |
| Width | 1 | Real Number | Range circle line width. |
| BorderColor | 00000060 | Color (RRGGBB[AA] notation) | Border color of the circle. |
| BorderWidth | 3 | Real Number | Range circle border width. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RepairableBuilding
**Building can be repaired by the repair button.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RepairPercent | 20 | Integer | Cost to fully repair the actor as a percent of its value. |
| RepairInterval | 24 | Integer | Number of ticks between each repair step. |
| RepairStep | 7 | Integer | The maximum amount of HP to repair each step. |
| RepairDamageTypes |  | Collection of DamageType | Damage types used for the repair. |
| RepairBonuses | 100, 150, 175, 200, 220, 240, 260, 280, 300 | Collection of Integer | The percentage repair bonus applied with increasing numbers of repairers. |
| CancelWhenDisabled | False | Boolean | Cancel the repair state when the trait is disabled. |
| PlayerExperience | 0 | Integer | Experience gained by a player for repairing structures of allied players. |
| RepairCondition |  | String | The condition to grant to self while being repaired. |
| RepairingNotification |  | String | Voice line to play when repairs are started. |
| RepairingTextNotification |  | String | Transient text message to display when repairs are started. |
| RepairingStoppedNotification |  | String | Speech notification to play when the repair process is aborted. |
| RepairingStoppedTextNotification |  | String | Text notification to display when the repair process is aborted. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Repairable
**This actor can be sent to a structure for repairs.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RepairActors | *(required)* | Set of String |  |
| Voice | Action | String |  |
| HpPerStep | -1 | Integer | The amount the unit will be repaired at each step. Use -1 for fallback behavior where HpPerStep from RepairsUnits trait will be used. |
| RequireForceMoveCondition |  | BooleanExpression | Boolean expression defining the condition under which the regular (non-force) enter cursor is disabled. |
| EnterCursor | enter | String | Cursor to display when able to be repaired at target actor. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to be repaired at target actor. |

### RepairableNear

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RepairActors | *(required)* | Set of String |  |
| CloseEnough | 4c0 | 1D World Distance |  |
| Voice | Action | String |  |
| RequireForceMoveCondition |  | BooleanExpression | Boolean expression defining the condition under which the regular (non-force) enter cursor is disabled. |
| EnterCursor | enter | String | Cursor to display when able to be repaired near target actor. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to be repaired near target actor. |

### RepairsBridges
**Can enter a BridgeHut or LegacyBridgeHut to trigger a repair.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Voice | Action | String |  |
| TargetLineColor | FFFF00 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| EnterBehaviour | Dispose | [`EnterBehaviour`](#enterbehaviour) | Behaviour when entering the structure. Possible values are Exit, Suicide, Dispose. |
| TargetCursor | goldwrench | String | Cursor to display when targeting an unrepaired bridge. |
| TargetBlockedCursor | goldwrench-blocked | String | Cursor to display when repairing is denied. |
| RepairNotification |  | String | Speech notification to play when a bridge is repaired. |
| RepairTextNotification |  | String | Text notification to display when a bridge is repaired. |

### RepairsUnits

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValuePercentage | 20 | Integer | Cost in % of the unit value to fully repair the unit. |
| HpPerStep | 10 | Integer |  |
| Interval | 24 | Integer | Time (in ticks) between two repair steps. |
| RepairDamageTypes |  | Collection of DamageType | Damage types used for the repair. |
| StartRepairingNotification |  | String | Speech notification played when starting to repair a unit. |
| StartRepairingTextNotification |  | String | Text notification displayed when starting to repair a unit. |
| FinishRepairingNotification |  | String | Speech notification played when repairing a unit is done. |
| FinishRepairingTextNotification |  | String | Text notification displayed when repairing a unit is done. |
| PlayerExperience | 0 | Integer | Experience gained by the player owning this actor for repairing an allied unit. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Replaceable

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types | *(required)* | Set of String | Replacement types this Replaceable actor accepts. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Replacement

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ReplaceableTypes | *(required)* | Set of String | Replacement type (matched against Types in Replaceable). |

### RequiresBuildableArea
**This actor requires another actor with 'GivesBuildableArea' trait around to be placed.**

> Requires trait(s): [`Building`](#building).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AreaTypes | *(required)* | Set of String | Types of buildable are this actor requires. |
| Adjacent | 2 | Integer | Maximum range from the actor with 'GivesBuildableArea' this can be placed at. |

### RequiresSpecificOwners
**Can be used to enforce specific owners (like 'Neutral' or 'Creeps') for this actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValidOwnerNames | *(required)* | Set of String | Only allow players listed here as owners. |

### Reservable
**Reserve landing places for aircraft.**

### ResourceClaimLayer
**Allows harvesters to coordinate their operations. Attach this to the world actor.**

### ResourceLayer
**Attach this to the world actor.**

> Requires trait(s): [`BuildingInfluence`](#buildinginfluence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ResourceTypes |  | Dictionary with Key: String, Value: ResourceTypeInfo |  |
| RecalculateResourceDensity | False | Boolean | Override the density saved in maps with values calculated based on the number of neighbouring resource cells. |

### ResourceRenderer
**Visualizes the state of the `ResourceLayer`.  Attach this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ResourceTypes |  | Dictionary with Key: String, Value: ResourceTypeInfo |  |

### ResourceStorageWarning
**Provides the player with an audible warning when their storage is nearing full.**

> Requires trait(s): [`PlayerResources`](#playerresources).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AdviceInterval | 20000 | Integer | Interval (in milliseconds) at which to check if more storage is needed. |
| Threshold | 80 | Integer | The percentage threshold above which a warning is played. |
| Notification | SilosNeeded | String | Speech to play for the warning. |
| TextNotification |  | String | Text to display for the warning. |

### ResourceValueMultiplier
**Modifies the value of resources delivered to this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RevealMapCrateAction
**Reveals the entire map.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IncludeAllies | False | Boolean | Should the map also be revealed for the allies of the collector's owner? |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RevealOnDeath
**Reveal this actor's last position when killed.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RevealForRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Relationships relative to the actors' owner that shroud will be revealed for. |
| Duration | 25 | Integer | Duration of the reveal. |
| Radius | 1c512 | 1D World Distance | Radius of the reveal around this actor. |
| RevealGeneratedShroud | True | Boolean | Can this actor be revealed through shroud generated by the `CreatesShroud` trait? |
| DeathTypes |  | Collection of DamageType | DeathTypes for which shroud will be revealed. Use an empty list (the default) to allow all DeathTypes. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RevealOnFire
**Reveal this actor to the target's owner when attacking.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ArmamentNames | primary, secondary | Collection of String | The armament types which trigger revealing. |
| RevealForRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships relative to the target player this actor will be revealed to during firing. |
| Duration | 25 | Integer | Duration of the reveal. |
| Radius | 1c512 | 1D World Distance | Radius of the reveal around this actor. |
| RevealGeneratedShroud | True | Boolean | Can this actor be revealed through shroud generated by the `CreatesShroud` trait? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RevealsMap
**Reveals shroud and fog across the whole map while active.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Relationships the watching player needs to see the shroud removed. |
| RevealGeneratedShroud | True | Boolean | Can this actor reveal shroud generated by the `CreatesShroud` trait? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RevealsShroud

> Inherits from: `AffectsShroud`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Relationships the watching player needs to see the shroud removed. |
| RevealGeneratedShroud | True | Boolean | Can this actor reveal shroud generated by the `CreatesShroud` trait? |
| MinRange | 0c0 | 1D World Distance |  |
| Range | 0c0 | 1D World Distance |  |
| MaxHeightDelta | -1 | Integer | If >= 0, prevent cells that are this much higher than the actor from being revealed. |
| MoveRecalculationThreshold | 0c256 | 1D World Distance | If > 0, force visibility to be recalculated if the unit moves within a cell by more than this distance. |
| Type | Footprint | [`VisibilityType`](#visibilitytype) | Possible values are CenterPosition (measure range from the center) and  Footprint (measure range from the footprint) |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RevealsShroudMultiplier
**Modifies the shroud range revealed by this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RotationPaletteEffect
**Palette effect used for sprinkle "animations".**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Palettes |  | Set of String | Defines to which palettes this effect should be applied to. If none specified, it applies to all palettes not explicitly excluded. |
| Tilesets |  | Set of String | Defines for which tileset IDs this effect should be loaded. If none specified, it applies to all tileset IDs not explicitly excluded. |
| ExcludePalettes |  | Set of String | Defines which palettes should be excluded from this effect. |
| ExcludeTilesets |  | Set of String | Don't apply the effect for these tileset IDs. |
| RotationBase | 96 | Integer | Palette index of first RotationRange color. |
| RotationRange | 7 | Integer | Range of colors to rotate. |
| RotationStep | 0.25 | Real Number | Step towards next color index per tick. |

### ScalePowerWithHealth
**Scale power amount with the current health.**

> Requires trait(s): [`Power`](#power).

### ScaredyCat
**Makes the unit automatically run around when taking damage.**

> Requires trait(s): [`Mobile`](#mobile).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PanicChance | 100 | Integer | Chance (out of 100) the unit has to enter panic mode when attacked. |
| PanicDuration | 250 | Integer | How long (in ticks) the actor should panic for. |
| PanicSpeedModifier | 200 | Integer | Panic movement speed as a percentage of the normal speed. |
| AttackPanicChance | 20 | Integer | Chance (out of 100) the unit has to enter panic mode when attacking. |
| AvoidTerrainTypes |  | Set of String | The terrain types that this actor should avoid running on to while panicking. |
| PanicSequencePrefix | panic- | String |  |

### ScriptLobbyDropdown
**Controls the map difficulty, tech level, and short game lobby options.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ID | *(required)* | String | Internal id for this option. |
| Label | *(required)* | String | Descriptive label for this option. |
| Description |  | String | Tooltip description for this option. |
| Default | *(required)* | String | Default option key in the `Values` list. |
| Values | *(required)* | Dictionary with Key: String, Value: String | Options to choose from. |
| Locked | False | Boolean | Prevent the option from being changed from its default value. |
| Visible | True | Boolean | Whether to display the option in the lobby. |
| DisplayOrder | 0 | Integer | Display order for the option in the lobby. |

### ScriptTags
**Allows this actor to be 'tagged' with arbitrary strings. Tags must be unique or they will be rejected.**

### SeedsResource
**Lets the actor spread resources around it in a circle.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Interval | 75 | Integer |  |
| ResourceType | Ore | String |  |
| MaxRange | 100 | Integer |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Selectable
**This actor is selectable. Defines bounds of selectable area, selection class, selection priority and selection priority modifiers.**

> Inherits from: [`Interactable`](#interactable).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Priority | 10 | Integer |  |
| PriorityModifiers | None | [`SelectionPriorityModifiers`](#selectionprioritymodifiers) | Allow selection priority to be modified using a hotkey. Valid values are None (priority is not affected by modifiers) Ctrl (priority is raised when Ctrl pressed) and Alt (priority is raised when Alt pressed). |
| Class |  | String | All units having the same selection class specified will be selected with select-by-type commands (e.g. double-click). Defaults to the actor name when not defined or inherited. |
| Voice | Select | String |  |
| Bounds |  | Collection of 1D World Distance | Defines a custom rectangle for mouse interaction with the actor. If null, the engine will guess an appropriate size based on the With*Body trait. The first two numbers define the width and height of the rectangle as a world distance. The (optional) second two numbers define an x and y offset from the actor center. |
| DecorationBounds |  | Collection of 1D World Distance | Defines a custom rectangle for Decorations (e.g. the selection box). If null, Bounds will be used instead |

### Selection

### Sellable
**Actor can be sold**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RefundPercent | 50 | Integer | Percentage of units value to give back after selling. |
| SellSounds |  | Collection of String | List of audio clips to play when the actor is being sold. |
| Notification |  | String | Speech notification to play. |
| TextNotification |  | String | Text notification to display. |
| ShowTicks | True | Boolean | Whether to show the cash tick indicators rising from the actor. |
| ShowTooltipText | True | Boolean | Whether to show the refund text on the tooltip, when actor is hovered over with sell order. |
| SkipMakeAnimation | False | Boolean | Skip playing (reversed) make animation. |
| Cursor | sell | String | Cursor to display when the sell order generator hovers over this actor. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SequencePlaceBuildingPreview
**Creates a building placement preview based on a defined sequence.**

> Inherits from: [`FootprintPlaceBuildingPreview`](#footprintplacebuildingpreview).

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | idle | String | Sequence name to use. |
| SequenceAlpha | 1 | Real Number | Custom opacity to apply to the sequence sprite. |
| FootprintUnderPreview | Valid, LineBuild | [`PlaceBuildingCellType`](#placebuildingcelltype) | Footprint types to draw underneath the actor preview. |
| FootprintOverPreview | Invalid | [`PlaceBuildingCellType`](#placebuildingcelltype) | Footprint types to draw above the actor preview. |
| Palette | terrain | String | Palette to use for rendering the placement sprite. |
| FootprintAlpha | 1 | Real Number | Custom opacity to apply to the placement sprite. |
| LineBuildFootprintAlpha | 1 | Real Number | Custom opacity to apply to the line-build placement sprite. |

### ShakeOnDeath

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DeathTypes |  | Collection of DamageType | DeathType(s) that trigger the shake. Leave empty to always trigger a shake. |
| Duration | 10 | Integer |  |
| Intensity | 1 | Integer |  |

### ShroudRenderer

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | shroud | String |  |
| ShroudVariants | shroud | Collection of String |  |
| FogVariants | fog | Collection of String |  |
| ShroudPalette | shroud | String |  |
| FogPalette | fog | String |  |
| Index | 12, 9, 8, 3, 1, 6, 4, 2, 13, 11, 7, 14 | Collection of Integer | Bitfield of shroud directions for each frame. Lower four bits are corners clockwise from TL; upper four are edges clockwise from top |
| UseExtendedIndex | False | Boolean | Use the upper four bits when calculating frame |
| OverrideFullShroud |  | String | Override for source art that doesn't define a fully shrouded tile |
| OverrideShroudIndex | 15 | Integer |  |
| OverrideFullFog |  | String | Override for source art that doesn't define a fully fogged tile |
| OverrideFogIndex | 15 | Integer |  |
| ShroudBlend | Alpha | [`BlendMode`](#blendmode) |  |

### SmudgeLayer
**Attach this to the world actor. Order of the layers defines the Z sorting.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | Scorch | String |  |
| Sequence | scorch | String | Sprite sequence name |
| SmokeChance | 0 | Integer | Chance of smoke rising from the ground |
| MaxSmokeOffsetDistance | 0c0 | 1D World Distance | By how much (in each direction) can the smoke appearance offset stray from the center of the cell? Note: Limit this to half a cell for square and 1/3 a cell for isometric cells to avoid straying into neighbour cells. |
| SmokeImage |  | String | Smoke sprite image name |
| SmokeSequences |  | Collection of String | Smoke sprite sequences randomly chosen from |
| SmokePalette | effect | String |  |
| Palette | terrain | String |  |
| InitialSmudges |  | Dictionary with Key: 2D Cell Position, Value: MapSmudge |  |

### SpawnActorOnDeath
**Spawn another actor immediately upon death.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Actor | *(required)* | String | Actor to spawn on death. |
| Probability | 100 | Integer | Probability the actor spawns. |
| OwnerType | Victim | [`OwnerType`](#ownertype) | Owner of the spawned actor. Allowed keywords:'Victim', 'Killer' and 'InternalName'. Falls back to 'InternalName' if 'Victim' is used and the victim is defeated (see 'SpawnAfterDefeat'). |
| InternalOwner | Neutral | String | Map player to use when 'InternalName' is defined on 'OwnerType'. |
| EffectiveOwnerFromOwner | False | Boolean | Changes the effective (displayed) owner of the spawned actor to the old owner (victim). |
| DeathType |  | String | DeathType that triggers the actor spawn. Leave empty to spawn an actor ignoring the DeathTypes. |
| SkipMakeAnimations | True | Boolean | Skips the spawned actor's make animations if true. |
| RequiresLobbyCreeps | False | Boolean | Should an actor only be spawned when the 'Creeps' setting is true? |
| Offset | 0,0 | 2D Cell Vector | Offset of the spawned actor relative to the dying actor's position. Warning: Spawning an actor outside the parent actor's footprint/influence might lead to unexpected behaviour. |
| SpawnAfterDefeat | True | Boolean | Should an actor spawn after the player has been defeated (e.g. after surrendering)? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SpawnActorPower
**Spawns an actor that stays for a limited amount of time.**

> Inherits from: `SupportPower`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Actor | *(required)* | String | Actor to spawn. |
| LifeTime | 250 | Integer | Amount of time to keep the actor alive in ticks. Value < 0 means this actor will not remove itself. |
| Terrain |  | Collection of String | Only allow this to be spawned on this terrain. |
| AllowUnderShroud | True | Boolean |  |
| DeploySound |  | String |  |
| EffectImage |  | String |  |
| EffectSequence |  | String |  |
| EffectPalette |  | String |  |
| ChargeInterval | 0 | Integer | Measured in ticks. |
| IconImage | icon | String |  |
| Icon |  | String | Icon sprite displayed in the support power palette. |
| IconPalette | chrome | String | Palette used for the icon. |
| Name |  | String |  |
| Description |  | String |  |
| AllowMultiple | False | Boolean | Allow multiple instances of the same support power. |
| OneShot | False | Boolean | Allow this to be used only once. |
| Cursor | ability | String | Cursor to display for using this support power. |
| BlockedCursor | generic-blocked | String | Cursor when unable to activate on this position.  |
| StartFullyCharged | False | Boolean | If set to true, the support power will be fully charged when it becomes available. Normal rules apply for subsequent charges. |
| Prerequisites |  | Collection of String |  |
| DetectedSound |  | String |  |
| DetectedSpeechNotification |  | String |  |
| DetectedTextNotification |  | String |  |
| BeginChargeSound |  | String |  |
| BeginChargeSpeechNotification |  | String |  |
| BeginChargeTextNotification |  | String |  |
| EndChargeSound |  | String |  |
| EndChargeSpeechNotification |  | String |  |
| EndChargeTextNotification |  | String |  |
| SelectTargetSound |  | String |  |
| SelectTargetSpeechNotification |  | String |  |
| SelectTargetTextNotification |  | String |  |
| InsufficientPowerSound |  | String |  |
| InsufficientPowerSpeechNotification |  | String |  |
| InsufficientPowerTextNotification |  | String |  |
| LaunchSound |  | String |  |
| LaunchSpeechNotification |  | String |  |
| LaunchTextNotification |  | String |  |
| IncomingSound |  | String |  |
| IncomingSpeechNotification |  | String |  |
| IncomingTextNotification |  | String |  |
| DisplayTimerRelationships | None | [`PlayerRelationship`](#playerrelationship) | Defines to which players the timer is shown. |
| DisplayBeacon | False | Boolean | Beacons are only supported on the Airstrike, Paratroopers, and Nuke powers |
| BeaconPaletteIsPlayerPalette | True | Boolean |  |
| BeaconPalette | player | String |  |
| BeaconImage | beacon | String |  |
| BeaconPoster |  | String |  |
| BeaconPosterPalette | chrome | String |  |
| ClockSequence |  | String |  |
| BeaconSequence |  | String |  |
| ArrowSequence |  | String |  |
| CircleSequence |  | String |  |
| BeaconDelay | 0 | Integer | Delay after launch, measured in ticks. |
| DisplayRadarPing | False | Boolean |  |
| RadarPingDuration | 125 | Integer | Measured in ticks. |
| OrderName | SpawnActorPowerInfoOrder | String |  |
| SupportPowerPaletteOrder | 9999 | Integer | Sort order for the support power palette. Smaller numbers are presented earlier. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SpawnActorsOnSell
**Spawn new actors when sold.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ValuePercent | 40 | Integer |  |
| MinHpPercent | 30 | Integer |  |
| ActorTypes | *(required)* | Collection of String | Actor types to spawn on sell, amount and type based on ValuePercent. Be sure to use lowercase. |
| GuaranteedActorTypes |  | Collection of String | Actors to spawn on sell. Be sure to use lowercase. |
| Factions |  | Set of String | Spawns actors only if the selling player's faction is in this list. Leave empty to allow all factions by default. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SpawnMapActors
**Spawns the initial units for each player upon game start.**

### SpawnStartingUnits
**Spawn base actor at the spawnpoint and support units in an annulus around the base actor. Both are defined at MPStartUnits. Attach this to the world actor.**

> Requires trait(s): [`StartingUnits`](#startingunits).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| StartingUnitsClass | none | String |  |
| DropdownLabel | dropdown-starting-units.label | String | Descriptive label for the starting units option in the lobby. |
| DropdownDescription | dropdown-starting-units.description | String | Tooltip description for the starting units option in the lobby. |
| DropdownLocked | False | Boolean | Prevent the starting units option from being changed in the lobby. |
| DropdownVisible | True | Boolean | Whether to display the starting units option in the lobby. |
| DropdownDisplayOrder | 0 | Integer | Display order for the starting units option in the lobby. |

### SpeedMultiplier
**Modifies the movement speed of this actor.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Modifier | 100 | Integer | Percentage modifier to apply. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SpreadsCondition
**Any actor with this trait enabled has a chance to affect others with this trait.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Probability | 5 | Integer | The chance this actor is going to affect an adjacent actor. |
| Range | 3c0 | 1D World Distance | How far the condition can spread from one actor to another. |
| SpreadCondition | spreading | String | Condition to grant onto another actor in range with the same trait. |
| Delay | 5 | Integer | Time in ticks to wait between spreading further. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SquadManagerBotModule
**Manages AI squads.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| NavalUnitsTypes |  | Set of String | Actor types that are valid for naval squads. |
| AirUnitsTypes |  | Set of String | Actor types that are excluded from ground attacks. |
| ExcludeFromSquadsTypes |  | Set of String | Actor types that should generally be excluded from attack squads. |
| ConstructionYardTypes |  | Set of String | Actor types that are considered construction yards (base builders). |
| NavalProductionTypes |  | Set of String | Enemy building types around which to scan for targets for naval squads. |
| ProtectionTypes |  | Set of String | Own actor types that are prioritized when defending. |
| AircraftTargetType | Air | Collection of TargetableType | Target types are used for identifying aircraft. |
| SquadSize | 8 | Integer | Minimum number of units AI must have before attacking. |
| SquadSizeRandomBonus | 30 | Integer | Random number of up to this many units is added to squad size when creating an attack squad. |
| AssignRolesInterval | 50 | Integer | Delay (in ticks) between giving out orders to units. |
| RushInterval | 600 | Integer | Delay (in ticks) between attempting rush attacks. |
| AttackForceInterval | 75 | Integer | Delay (in ticks) between updating squads. |
| MinimumAttackForceDelay | 0 | Integer | Minimum delay (in ticks) between creating squads. |
| RushAttackScanRadius | 15 | Integer | Radius in cells around enemy BaseBuilder (Construction Yard) where AI scans for targets to rush. |
| ProtectUnitScanRadius | 15 | Integer | Radius in cells around the base that should be scanned for units to be protected. |
| MaxBaseRadius | 20 | Integer | Maximum distance in cells from center of the base when checking for MCV deployment location. Only applies if RestrictMCVDeploymentFallbackToBase is enabled and there's at least one construction yard. |
| IdleScanRadius | 10 | Integer | Radius in cells that squads should scan for enemies around their position while idle. |
| DangerScanRadius | 10 | Integer | Radius in cells that squads should scan for danger around their position to make flee decisions. |
| AttackScanRadius | 12 | Integer | Radius in cells that attack squads should scan for enemies around their position when trying to attack. |
| ProtectionScanRadius | 8 | Integer | Radius in cells that protecting squads should scan for enemies around their position. |
| IgnoredEnemyTargetTypes |  | Collection of TargetableType | Enemy target types to never target. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### StartGameNotification

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Notification | StartGame | String |  |
| TextNotification |  | String |  |
| LoadedNotification | GameLoaded | String |  |
| LoadedTextNotification |  | String |  |
| SavedNotification | GameSaved | String |  |
| SavedTextNotification |  | String |  |

### StartingUnits
**Used by SpawnStartingUnits. Attach these to the world actor. You can have multiple variants by adding @suffixes.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Class | none | String | Internal class ID. |
| ClassName | Unlabeled | String | Exposed via the UI to the player. |
| Factions |  | Set of String | Only available when selecting one of these factions. Leave empty for no restrictions. |
| BaseActor |  | String | The actor at the center, usually the mobile construction vehicle. |
| BaseActorOffset | 0,0 | 2D Cell Vector | Offset from the spawn point, BaseActor will spawn at. |
| SupportActors |  | Collection of String | A group of units ready to defend or scout. |
| InnerSupportRadius | 2 | Integer | Inner radius for spawning support actors |
| OuterSupportRadius | 4 | Integer | Outer radius for spawning support actors |
| BaseActorFacing | 512 | 1D World Angle (optional) | Initial facing of BaseActor. Leave undefined for random facings. |
| SupportActorsFacing |  | 1D World Angle (optional) | Initial facing of SupportActors. Leave undefined for random facings. |

### StoresPlayerResources
**Adds capacity to a player's harvested resource limit.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Capacity | 0 | Integer |  |

### StoresResources
**Allows the storage of resources.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Capacity | 28 | Integer | The amounts of resources that can be stored. |
| Resources |  | Collection of String | Which resources can be stored. |

### StrategicPoint
**Used to mark a place that needs to be in possession for StrategicVictoryConditions.**

### StrategicVictoryConditions
**Allows King of the Hill (KotH) style gameplay.**

> Requires trait(s): [`MissionObjectives`](#missionobjectives).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| HoldDuration | 7500 | Integer | Amount of time (in game ticks) that the player has to hold all the strategic points. Defaults to 7500 ticks (5 minutes at default speed). |
| ResetOnHoldLost | True | Boolean | Should the timer reset when the player loses hold of a strategic point. |
| RatioRequired | 50 | Integer | Percentage of all strategic points the player has to hold to win. |
| NotificationDelay | 1500 | Integer | Delay for the end game notification in milliseconds. |
| Objective | Hold all the strategic positions! | String | Description of the objective |
| SuppressNotifications | False | Boolean | Disable the win/loss messages and audio notifications? |

### SubterraneanActorLayer

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TerrainType | Subterranean | String | Terrain type of the underground layer. |
| HeightOffset | -2c0 | 1D World Distance | Height offset relative to the smoothed terrain for movement. |
| SmoothingRadius | 2 | Integer | Cell radius for smoothing adjacent cell heights. |

### SubterraneanLocomotor
**Used by Mobile. Required for subterranean actors. Attach these to the world actor. You can have multiple variants by adding @suffixes.**

> Inherits from: [`Locomotor`](#locomotor).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SubterraneanTransitionCost | 0 | Int16 | Pathfinding cost for submerging or reemerging. |
| SubterraneanTransitionTerrainTypes |  | Set of String | The terrain types that this actor can transition on. Leave empty to allow any. |
| SubterraneanTransitionOnRamps | False | Boolean | Can this actor transition on slopes? |
| SubterraneanTransitionDepth | -1c0 | 1D World Distance | Depth at which the subterranean condition is applied. |
| Name | default | String | Locomotor ID. |
| WaitAverage | 40 | Integer |  |
| WaitSpread | 10 | Integer |  |
| SharesCell | False | Boolean | Allow multiple (infantry) units in one cell. |
| MoveIntoShroud | True | Boolean | Can the actor be ordered to move in to shroud? |
| Crushes |  | Collection of CrushClass | e.g. crate, wall, infantry |
| CrushDamageTypes |  | Collection of DamageType | Types of damage that are caused while crushing. Leave empty for no damage types. |
| TerrainSpeeds |  | Dictionary with Key: String, Value: TerrainInfo | Lower the value on rough terrain. Leave out entries for impassable terrain. |

### SupportPowerBotModule
**Manages bot support power handling.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`SupportPowerManager`](#supportpowermanager).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Decisions |  | Collection of SupportPowerDecision | Tells the AI how to use its support powers. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SupportPowerCrateAction
**Gives a supportpower to the collector.**

> Inherits from: [`CrateAction`](#crateaction), `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Proxy | *(required)* | String | Which proxy actor, which grants the support power, to spawn. |
| SelectionShares | 10 | Integer | Chance of getting this crate, assuming the collector is compatible. |
| Image | crate-effects | String | Image containing the crate effect animation sequence. |
| Sequence |  | String | Animation sequence played when collected. Leave empty for no effect. |
| Palette | effect | String | Palette to draw the animation in. |
| Sound |  | String | Audio clip to play when the crate is collected. |
| Notification |  | String | Speech notification to play when the crate is collected. |
| TextNotification |  | String | Text notification to display when the crate is collected. |
| TimeDelay | 0 | Integer | The earliest time (in ticks) that this crate action can occur on. |
| Prerequisites |  | Collection of String | Only allow this crate action when the collector has these prerequisites |
| ExcludedActorTypes |  | Collection of String | Actor types that this crate action will not occur for. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SupportPowerManager
**Attach this to the player actor.**

> Requires trait(s): [`DeveloperMode`](#developermode), [`TechTree`](#techtree).

### TakeCover
**Make the unit go prone when under attack, in an attempt to reduce damage.**

> Inherits from: [`Turreted`](#turreted), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Duration | 100 | Integer | How long (in ticks) the actor remains prone. Negative values mean actor remains prone permanently. |
| SpeedModifier | 50 | Integer | Prone movement speed as a percentage of the normal speed. |
| DamageTriggers |  | Collection of DamageType | Damage types that trigger prone state. Defined on the warheads. If Duration is negative (permanent), you can leave this empty to trigger prone state immediately. |
| DamageModifiers |  | Dictionary with Key: String, Value: Integer | Damage modifiers for each damage type (defined on the warheads) while the unit is prone. |
| ProneOffset | 500,0,0 | 3D World Vector | Muzzle offset modifier to apply while prone. |
| ProneSequencePrefix | prone- | String | Sequence prefix to apply while prone. |
| Turret | primary | String |  |
| TurnSpeed | 512 | 1D World Angle | Speed at which the turret turns. |
| InitialFacing | 0 | 1D World Angle |  |
| RealignDelay | 40 | Integer | Number of ticks before turret is realigned. (-1 turns off realignment) |
| Offset | 0,0,0 | 3D World Vector | Muzzle position relative to turret or body. (forward, right, up) triples |
| EditorTurretFacingDisplayOrder | 4 | Integer | Display order for the turret facing slider in the map editor |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Targetable
**Actor can be targeted.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TargetTypes |  | Collection of TargetableType | Target type. Used for filtering (in)valid targets. |
| RequiresForceFire | False | Boolean |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TechTree
**Manages build limits and pre-requisites.  Attach this to the player actor.**

### TemporaryOwnerManager
**Interacts with the ChangeOwner warhead. Displays a bar how long this actor is affected and reverts back to the old owner on temporary changes.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BarColor | FFA500 | Color (RRGGBB[AA] notation) |  |

### TerrainGeometryOverlay
**Renders a debug overlay showing the terrain cells. Attach this to the world actor.**

### TerrainLighting
**Add to the world actor to apply a global lighting tint and allow actors using the TerrainLightSource to add localised lighting.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Intensity | 1 | Real Number |  |
| HeightStep | 0 | Real Number |  |
| RedTint | 1 | Real Number |  |
| GreenTint | 1 | Real Number |  |
| BlueTint | 1 | Real Number |  |
| BinSize | 10 | Integer | Size of light source partition bins (cells) |

### TerrainLightSource
**Adds a localized circular light centered on the actor to the world's TerrainLightSource trait.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Range | 10c0 | 1D World Distance |  |
| Intensity | 0 | Real Number |  |
| RedTint | 0 | Real Number |  |
| GreenTint | 0 | Real Number |  |
| BlueTint | 0 | Real Number |  |

### TerrainModifiesDamage

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TerrainModifier | *(required)* | Dictionary with Key: String, Value: Integer | Damage percentage for specific terrain types. 120 = 120%, 80 = 80%, etc. |
| ModifyHealing | False | Boolean | Modify healing damage? For example: A friendly medic. |

### TerrainRenderer

### TerrainTunnel

> Requires trait(s): [`TerrainTunnelLayer`](#terraintunnellayer).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Location | 0,0 | 2D Cell Position | Location of the tunnel |
| Height | 0 | Byte | Height of the tunnel floor in map height steps. |
| Dimensions | 0,0 | 2D Cell Vector | Size of the tunnel footprint |
| Footprint | *(required)* | String | Tunnel footprint. _ is passable, x is blocked, and o are tunnel portals. |
| TerrainType | *(required)* | String | Terrain type of the tunnel floor. |

### TerrainTunnelLayer

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ImpassableTerrainType | Impassable | String | Terrain type used by cells outside any tunnel footprint. |

### ThrowsParticle

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Anim | *(required)* | String |  |
| Offset | 0,0,0 | 3D World Vector | Initial position relative to body |
| MinThrowRange | 0c256 | 1D World Distance | Minimum distance to throw the particle |
| MaxThrowRange | 0c768 | 1D World Distance | Maximum distance to throw the particle |
| MinThrowAngle | 85 | 1D World Angle | Minimum angle to throw the particle |
| MaxThrowAngle | 170 | 1D World Angle | Maximum angle to throw the particle |
| Velocity | 75 | Integer | Speed to throw the particle (horizontal WPos/tick) |
| TurnSpeed | 60 | 1D World Angle | Speed at which the particle turns. |

### ThrowsShrapnel
**Throws particles when the actor is destroyed that do damage on impact.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Weapons | *(required)* | Collection of String | The weapons used for shrapnel. |
| Pieces | 3, 10 | Collection of Integer | The amount of pieces of shrapnel to expel. Two values indicate a range. |
| Range | 2c0, 5c0 | Collection of 1D World Distance | The minimum and maximum distances the shrapnel may travel. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TimeLimitManager
**This trait allows setting a time limit on matches. Attach this to the World actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TimeLimitLabel | dropdown-time-limit.label | String | Label that will be shown for the time limit option in the lobby. |
| TimeLimitDescription | dropdown-time-limit.description | String | Tooltip description that will be shown for the time limit option in the lobby. |
| TimeLimitOptions | 0, 10, 20, 30, 40, 60, 90 | Collection of Integer | Time Limit options that will be shown in the lobby dropdown. Values are in minutes. |
| TimeLimitWarnings | 1: 
2: 
3: 
4: 
5: 
10: 
 | Dictionary with Key: Integer, Value: String | List of remaining minutes of game time when a text and optional speech notification should be made to players. |
| TimeLimitDefault | 0 | Integer | Default selection for the time limit option in the lobby. Needs to use one of the TimeLimitOptions. |
| TimeLimitLocked | False | Boolean | Prevent the time limit option from being changed in the lobby. |
| TimeLimitDropdownVisible | True | Boolean | Whether to display the options dropdown in the lobby. |
| TimeLimitDisplayOrder | 0 | Integer | Display order for the time limit dropdown in the lobby. |
| Notification | {0} minute{1} remaining. | String | Notification text for time limit warnings. The string '{0}' will be replaced by the remaining time in minutes, '{1}' is used for the plural form. |
| CountdownLabel |  | String | ID of the LabelWidget used to display a text ingame that will be updated every second. |
| CountdownText |  | String | Text to be shown using the CountdownLabel. The string '{0}' will be replaced by the time in hh:mm:ss format. |
| SkipTimeRemainingNotifications | False | Boolean | Will prevent showing/playing the built-in time limit warnings when set to true. |
| SkipTimerExpiredNotification | False | Boolean | Will prevent showing/playing the built-in timer expired notification when set to true. |

### TintPostProcessEffect
**Used for day/night effects.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Red | 1 | Real Number |  |
| Green | 1 | Real Number |  |
| Blue | 1 | Real Number |  |
| Ambient | 1 | Real Number |  |

### ToggleConditionOnOrder
**Toggles a condition on and off when a specified order type is received.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition to grant. |
| OrderName | *(required)* | String | Order name that toggles the condition. |
| EnabledSound |  | String |  |
| EnabledSpeech |  | String |  |
| EnabledTextNotification |  | String |  |
| DisabledSound |  | String |  |
| DisabledSpeech |  | String |  |
| DisabledTextNotification |  | String |  |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TooltipDescription
**Additional info shown in the battlefield tooltip.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Description | *(required)* | String | Text shown in tooltip. |
| ValidRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the description. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Tooltip
**Shown in the build palette widget.**

> Inherits from: `TooltipInfoBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| GenericName |  | String | An optional generic name (i.e. "Soldier" or "Structure")to be shown to chosen players. |
| GenericStancePrefix | True | Boolean | Prefix generic tooltip name with 'Ally/Neutral/EnemyPrefix'. |
| AllyPrefix | label-tooltip-prefix.ally | String | Prefix to display in the tooltip for allied units. |
| NeutralPrefix |  | String | Prefix to display in the tooltip for neutral units. |
| EnemyPrefix | label-tooltip-prefix.enemy | String | Prefix to display in the tooltip for enemy units. |
| GenericVisibility | None | [`PlayerRelationship`](#playerrelationship) | Player stances that the generic name should be shown to. |
| ShowOwnerRow | True | Boolean | Show the actor's owner and their faction flag |
| Name | *(required)* | String |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TransformCrusherOnCrush
**Put this on the actor that gets crushed to replace the crusher with a new actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IntoActor | *(required)* | String |  |
| SkipMakeAnims | True | Boolean |  |
| CrushClasses |  | Collection of CrushClass |  |

### TransformOnCapture
**Replaces the captured actor with a new one.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IntoActor | *(required)* | String |  |
| ForceHealthPercentage | 0 | Integer |  |
| SkipMakeAnims | True | Boolean |  |
| CaptureTypes |  | Collection of CaptureType | Transform only if the capturer's CaptureTypes overlap with these types. Leave empty to allow all types. |

### Transforms
**Actor becomes a specified actor type when this trait is triggered.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IntoActor | *(required)* | String | Actor to transform into. |
| Offset | 0,0 | 2D Cell Vector | Offset to spawn the transformed actor relative to the current cell. |
| Facing | 384 | 1D World Angle | Facing that the actor must face before transforming. |
| TransformSounds |  | Collection of String | Sounds to play when transforming. |
| NoTransformSounds |  | Collection of String | Sounds to play when the transformation is blocked. |
| TransformNotification |  | String | Speech notification to play when transforming. |
| TransformTextNotification |  | String | Text notification to display when transforming. |
| NoTransformNotification |  | String | Speech notification to play when the transformation is blocked. |
| NoTransformTextNotification |  | String | Text notification to display when the transformation is blocked. |
| DeployCursor | deploy | String | Cursor to display when able to (un)deploy the actor. |
| DeployBlockedCursor | deploy-blocked | String | Cursor to display when unable to (un)deploy the actor. |
| Voice | Action | String |  |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TransformsIntoAircraft
**Add to a building to expose a move cursor that triggers Transforms and issues a move order to the transformed actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Transforms`](#transforms).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MoveIntoShroud | True | Boolean | Can the actor be ordered to move in to shroud? |
| DockActors | *(required)* | Set of String |  |
| Voice | Action | String |  |
| RequiresForceMove | False | Boolean | Require the force-move modifier to display the move cursor. |
| Cursor | move | String | Cursor to display when a move order can be issued at target location. |
| BlockedCursor | move-blocked | String | Cursor to display when a move order cannot be issued at target location. |
| EnterCursor | enter | String | Cursor to display when able to land at target building. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to land at target building. |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line for regular move orders. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TransformsIntoDockClient
**Add to a building to expose a move cursor that triggers Transforms and issues a dock order to the transformed actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Transforms`](#transforms).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| EnterCursor | enter | String | Cursor to display when able to dock at target actor. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to dock at target actor. |
| Voice | Action | String | Voice. |
| DockLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line of docking orders. |
| RequiresForceMove | False | Boolean | Require the force-move modifier to display the dock cursor. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TransformsIntoEntersTunnels
**Add to a building to expose a move cursor that triggers Transforms and issues an enter tunnel order to the transformed actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Transforms`](#transforms).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| EnterCursor | enter | String | Cursor to display when able to enter target tunnel. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to enter target tunnel. |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line while in tunnels. |
| Voice | Action | String |  |
| RequiresForceMove | False | Boolean | Require the force-move modifier to display the enter cursor. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TransformsIntoMobile
**Add to a building to expose a move cursor that triggers Transforms and issues a move order to the transformed actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Transforms`](#transforms).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Locomotor | *(required)* | String | Locomotor used by the transformed actor. Must be defined on the World actor. |
| Cursor | move | String | Cursor to display when a move order can be issued at target location. |
| TerrainCursors |  | Dictionary with Key: String, Value: String | Cursor overrides to display for specific terrain types. A dictionary of [terrain type]: [cursor name]. |
| BlockedCursor | move-blocked | String | Cursor to display when a move order cannot be issued at target location. |
| Voice | Action | String |  |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line for regular move orders. |
| RequiresForceMove | False | Boolean | Require the force-move modifier to display the move cursor. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TransformsIntoPassenger
**Add to a building to expose a move cursor that triggers Transforms and issues an EnterTransport order to the transformed actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Transforms`](#transforms).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| CargoType |  | String |  |
| Weight | 1 | Integer |  |
| Voice | Action | String |  |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| RequiresForceMove | False | Boolean | Require the force-move modifier to display the enter cursor. |
| EnterCursor | enter | String | Cursor to display when able to enter target actor. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to enter target actor. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TransformsIntoRepairable
**Add to a building to expose a move cursor that triggers Transforms and issues a repair order to the transformed actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Transforms`](#transforms).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RepairActors | *(required)* | Set of String |  |
| Voice | Action | String |  |
| TargetLineColor | 008000 | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| RequiresForceMove | False | Boolean | Require the force-move modifier to display the enter cursor. |
| EnterCursor | enter | String | Cursor to display when able to be repaired at target actor. |
| EnterBlockedCursor | enter-blocked | String | Cursor to display when unable to be repaired at target actor. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TransformsIntoTransforms
**Add to a building to allow queued transform orders while undeploying.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Transforms`](#transforms).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Voice | Action | String |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TunnelEntrance
**Provides a target for players to issue orders for units to move through a TerrainTunnel. The host actor should be placed so that the Sensor position overlaps one of the TerrainTunnel portal cells.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RallyPoint | 0,0 | 2D Cell Vector | Offset to use as a staging point for actors entering or exiting the tunnel. Should be at least Margin cells away from the actual entrance. |
| Margin | 2 | Integer | Cell radius to use as a staging area around the RallyPoint. |
| Sensor | 0,0 | 2D Cell Vector | Offset to check for the corresponding TerrainTunnel portal cell(s). |

### TurnOnIdle
**Turns actor randomly when idle.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Mobile`](#mobile).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MinDelay | 400 | Integer | Minimum amount of ticks the actor will wait before the turn. |
| MaxDelay | 800 | Integer | Maximum amount of ticks the actor will wait before the turn. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Turreted

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Turret | primary | String |  |
| TurnSpeed | 512 | 1D World Angle | Speed at which the turret turns. |
| InitialFacing | 0 | 1D World Angle |  |
| RealignDelay | 40 | Integer | Number of ticks before turret is realigned. (-1 turns off realignment) |
| Offset | 0,0,0 | 3D World Vector | Muzzle position relative to turret or body. (forward, right, up) triples |
| EditorTurretFacingDisplayOrder | 4 | Integer | Display order for the turret facing slider in the map editor |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### UnitBuilderBotModule
**Controls AI unit production.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IdleBaseUnitsMaximum | -1 | Integer | If > 0, only produce units as long as there are less than this amount of units idling inside the base. Beware: if it is less than squad size, e.g. the `SquadSize` from `SquadManagerBotModule`, the bot might get stuck as there aren't enough idle units to create squad. |
| UnitQueues | Vehicle, Infantry, Plane, Ship, Aircraft | Collection of String | Production queues AI uses for producing units. |
| UnitsToBuild |  | Dictionary with Key: String, Value: Integer | What units to the AI should build. What relative share of the total army must be this type of unit. |
| UnitLimits |  | Dictionary with Key: String, Value: Integer | What units should the AI have a maximum limit to train. |
| UnitDelays |  | Dictionary with Key: String, Value: Integer | When should the AI start train specific units. |
| ProductionMinCashRequirement | 500 | Integer | Only queue construction of a new unit when above this requirement. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### UpdatesDerrickCount
**Tag trait for updating the 'Oil Derrick' count economy statistic.**

### UpdatesPlayerStatistics
**Attach this to a unit to update observer stats.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| AddToArmyValue | False | Boolean | Add to army value in statistics |
| AddToAssetsValue | True | Boolean | Add to assets value in statistics |
| OverrideActor |  | String | Count this actor as a different type in the spectator army display. |

### ValidateOrder
**Used to detect exploits. Attach this to the world actor.**

### Valued
**How much the unit is worth.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Cost | 0 | Integer | Used in production, but also for bounties so remember to set it > 0 even for NPCs. |

### Voiced
**This actor has a voice.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| VoiceSet | *(required)* | String | Which voice set to use. |
| Volume | 1 | Real Number | Multiply volume with this factor. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### Wanders
**Wanders around aimlessly while idle.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| WanderMoveRadius | 1 | Integer |  |
| ReduceMoveRadiusDelay | 5 | Integer | Number of ticks to wait before decreasing the effective move radius. |
| MinMoveDelay | 0 | Integer | Minimum amount of ticks the actor will sit idly before starting to wander. |
| MaxMoveDelay | 0 | Integer | Maximum amount of ticks the actor will sit idly before starting to wander. |
| AvoidTerrainTypes |  | Set of String | The terrain types that this actor should avoid wandering on to. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WarheadDebugOverlay
**Part of the combat overlay from `DeveloperMode`. Attach this to the world actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DisplayDuration | 25 | Integer |  |

### WeatherOverlay
**Adds a particle-based overlay.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ParticleDensityFactor | 8 | Integer | Average number of particles per 100x100 px square. |
| ChangingWindLevel | True | Boolean | Should the level of the wind change over time, or just stick to the first value of WindLevels? |
| WindLevels | -12, -7, -5, 0, 5, 7, 12 | Collection of Integer | The levels of wind intensity (particles x-axis movement in px/tick). |
| WindTick | 150, 550 | Collection of Integer | Works only if ChangingWindLevel is enabled. Min. and max. ticks needed to change the WindLevel. |
| InstantWindChanges | False | Boolean | Hard or soft fading between the WindLevels. |
| UseSquares | True | Boolean | Particles are drawn in squares when enabled, otherwise with lines. |
| ParticleSize | 1, 3 | Collection of Integer | Size / width of the particle in px. |
| ScatterDirection | -1, 1 | Collection of Integer | Scatters falling direction on the x-axis. Scatter min. and max. value in px/tick. |
| Gravity | 2.5, 5 | Collection of Real Number | Min. and max. speed at which particles fall in px/tick. |
| SwingOffset | 2.5, 3.5 | Collection of Real Number | The current offset value for the swing movement. SwingOffset min. and max. value in px/tick. |
| SwingSpeed | 0.0025, 0.06 | Collection of Real Number | The value that particles swing to the side each update. SwingSpeed min. and max. value in px/tick. |
| SwingAmplitude | 1, 1.5 | Collection of Real Number | The value range that can be swung to the left or right. SwingAmplitude min. and max. value in px/tick. |
| ParticleColors | ECECEC, E4E4E4, D0D0D0, BCBCBC | Collection of Color (RRGGBB[AA] notation) | The randomly selected rgb(a) hex colors for the particles. Use this order: rrggbb[aa], rrggbb[aa], ... |
| LineTailAlphaValue | 200 | Byte | Works only with line enabled and can be used to fade out the tail of the line like a contrail. |
| FadeOutTicks | 1000 | Integer | Time to fade out once the trait becomes disabled. |
| FadeInTicks | 1000 | Integer | Time to fade in once the trait becomes enabled. |
| InitialParticlePercentage | 100 | Integer | Percentage of the initial particle when enabled and the game start. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithColoredOverlay
**Display a colored overlay when a timed condition is active.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Color | 80000080 | Color (RRGGBB[AA] notation) | Color to overlay. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

## OpenRA.Mods.Common.Traits.Conditions

### GrantRandomCondition
**Grants a random condition from a predefined list to the actor when created.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Conditions | *(required)* | Collection of String | List of conditions to grant from. |

## OpenRA.Mods.Common.Traits.Radar

### AppearsOnRadar
**Provides a signature on the minimap.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UseLocation | False | Boolean | Use center position instead of occupied cells. |
| ValidRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view this actor on radar. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProvidesRadar
**This actor enables the radar minimap.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### RadarColorFromTerrain

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Terrain | *(required)* | String |  |

## OpenRA.Mods.Common.Traits.Render

### CashTricklerBar
**Display the time remaining until the next cash is given by actor's CashTrickler trait.**

> Requires trait(s): [`CashTrickler`](#cashtrickler).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DisplayRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Defines to which players the bar is to be shown. |
| Color | FF00FF | Color (RRGGBB[AA] notation) |  |

### Hovers
**Changes the visual Z position periodically.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BobDistance | -0c43 | 1D World Distance | Maximum visual Z axis distance relative to actual position + InitialHeight. |
| MinHoveringAltitude | 0c0 | 1D World Distance | Actual altitude of actor needs to be this or higher to enable hover effect. |
| Ticks | 6 | Integer | Amount of ticks it takes to reach BobDistance. |
| FallTicks | 10 | Integer | Amount of ticks it takes to fall to the ground from the highest point when disabled. |
| RiseTicks | 20 | Integer | Amount of ticks it takes to rise from the ground to InitialHeight. |
| InitialHeight | 0c43 | 1D World Distance | Initial Z axis modifier relative to actual position. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### IsometricSelectionDecorations

> Inherits from: `SelectionDecorationsBase`.

> Requires trait(s): [`IsometricSelectable`](#isometricselectable).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SelectionBoxColor | FFFFFF | Color (RRGGBB[AA] notation) |  |

### LeavesTrails
**Renders a sprite effect when leaving a cell.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image | *(required)* | String |  |
| Sequences | idle | Collection of String |  |
| Palette | effect | String |  |
| TerrainTypes |  | Set of String | Only leave trail on listed terrain types. Leave empty to leave trail on all terrain types. |
| Type | Cell | [`TrailType`](#trailtype) | Accepts values: Cell to draw the trail sprite in the center of the current cell, CenterPosition to draw the trail sprite at the current position. |
| VisibleThroughFog | False | Boolean | Should the trail be visible through fog. |
| TrailWhileStationary | False | Boolean | Display a trail while stationary. |
| StationaryInterval | 0 | Integer | Delay between trail updates when stationary. |
| TrailWhileMoving | True | Boolean | Display a trail while moving. |
| MovingInterval | 0 | Integer | Delay between trail updates when moving. |
| StartDelay | 0 | Integer | Delay before first trail. Use negative values for falling back to the *Interval values. |
| Offsets | 0,0,0 | Collection of 3D World Vector | Trail spawn positions relative to actor position. (forward, right, up) triples |
| SpawnAtLastPosition | True | Boolean | Should the trail spawn relative to last position or current position? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProductionBar
**Visualizes the remaining build time of actor produced here.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Production`](#production).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ProductionType | *(required)* | String | Production queue type, for actors with multiple queues. |
| Color | 87CEEB | Color (RRGGBB[AA] notation) |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### ProductionIconOverlayManager
**Attach this to the player actor. Required for WithProductionIconOverlay trait on actors to work.**

> Requires trait(s): [`TechTree`](#techtree).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | *(required)* | String | Type of the overlay. Prerequisites from WithProductionIconOverlay traits with matching types determine when this overlay will be enabled. |
| Image | *(required)* | String | Image used for the overlay. |
| Sequence |  | String | Sequence used for the overlay (cannot be animated). |
| Palette | chrome | String | Palette to render the sprite in. Reference the world actor's PaletteFrom* traits. |

### ReloadArmamentsBar
**Visualizes the minimum remaining time for reloading the armaments.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armaments | primary, secondary | Collection of String | Armament names |
| Color | FF0000 | Color (RRGGBB[AA] notation) |  |

### RenderDebugState
**Displays the actor's type and ID above the actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Font | TinyBold | String |  |

### RenderDetectionCircle

> Requires trait(s): [`DetectCloaked`](#detectcloaked).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UpdateLineTick | 1023 | 1D World Angle | WAngle the Radar update line advances per tick. |
| TrailCount | 0 | Integer | Number of trailing Radar update lines. |
| Color | 32CD3280 | Color (RRGGBB[AA] notation) | Color of the circle and scanner update line. |
| Width | 1 | Real Number | Range circle line width. |
| BorderColor | 00000060 | Color (RRGGBB[AA] notation) | Border color of the circle and scanner update line. |
| BorderWidth | 3 | Real Number | Range circle border width. |
| Visible | WhenSelected | [`DetectionCircleVisibility`](#detectioncirclevisibility) | When to show the detection circle. Valid values are `Always`, and `WhenSelected` |

### RenderRangeCircle
**Draw a circle indicating my weapon's range.**

> Requires trait(s): `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RangeCircleType |  | String |  |
| FallbackRange | 0c0 | 1D World Distance | Range to draw if no armaments are available. |
| RangeCircleMode | Maximum | [`RangeCircleMode`](#rangecirclemode) | Which circle to show. Valid values are `Maximum`, and `Minimum`. |
| Color | FFFF0080 | Color (RRGGBB[AA] notation) | Color of the circle. |
| Width | 1 | Real Number | Range circle line width. |
| BorderColor | 00000060 | Color (RRGGBB[AA] notation) | Color of the border. |
| BorderWidth | 3 | Real Number | Range circle border width. |

### RenderSpritesEditorOnly
**Invisible during games.**

> Inherits from: [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image |  | String | The sequence name that defines the actor sprites. Defaults to the actor name. |
| FactionImages |  | Dictionary with Key: String, Value: String | A dictionary of faction-specific image overrides. |
| Palette |  | String | Custom palette name |
| PlayerPalette | player | String | Custom PlayerColorPalette: BaseName |

### RenderSprites
**Render trait fundament that won't work without additional With* render traits.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image |  | String | The sequence name that defines the actor sprites. Defaults to the actor name. |
| FactionImages |  | Dictionary with Key: String, Value: String | A dictionary of faction-specific image overrides. |
| Palette |  | String | Custom palette name |
| PlayerPalette | player | String | Custom PlayerColorPalette: BaseName |

### SelectionDecorations

> Inherits from: `SelectionDecorationsBase`.

> Requires trait(s): [`Interactable`](#interactable).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SelectionBoxColor | FFFFFF | Color (RRGGBB[AA] notation) |  |

### SupportPowerChargeBar
**Display the time remaining until the super weapon attached to the actor is ready.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DisplayRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Defines to which players the bar is to be shown. |
| Color | FF00FF | Color (RRGGBB[AA] notation) |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### TimedConditionBar
**Visualizes the remaining time for a condition.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Condition | *(required)* | String | Condition that this bar corresponds to |
| Color | FF0000 | Color (RRGGBB[AA] notation) |  |

### WithAcceptDeliveredCashAnimation
**Replaces the building animation when it accepts a cash delivery unit.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | active | String | Sequence name to use |
| Body | body | String | Which sprite body to play the animation on. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithAimAnimation

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteBody`](#withspritebody), `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armament | primary | String | Armament name |
| Sequence | *(required)* | String | Displayed while targeting. |
| Body | body | String | Which sprite body to modify. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithAircraftLandingEffect
**Plays an animation on the ground position when the actor lands.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image | *(required)* | String |  |
| Sequences | idle | Collection of String |  |
| Palette | effect | String |  |
| VisibleThroughFog | False | Boolean | Should the sprite effect be visible through fog. |
| DistanceAboveTerrain | 0c756 | 1D World Distance | Height at which to play the animation when descending. |
| TerrainTypes |  | Set of String | Only play on these terrain types. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithAmmoPipsDecoration

> Inherits from: `WithDecorationBase`, `ConditionalTrait`.

> Requires trait(s): [`AmmoPool`](#ammopool).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PipCount | -1 | Integer | Number of pips to display. Defaults to the sum of the enabled AmmoPool.Ammo. |
| PipStride | 0,0 | 2D Integer | If non-zero, override the spacing between adjacent pips. |
| Image | pips | String | Image that defines the pip sequences. |
| EmptySequence | pip-empty | String | Sequence used for empty pips. |
| FullSequence | pip-green | String | Sequence used for full pips. |
| Palette | chrome | String |  |
| AmmoPools |  | Collection of String | Name(s) of AmmoPool(s) that use this decoration. Leave empty to include all pools. |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithAttackAnimation

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Armament`](#armament), [`WithSpriteBody`](#withspritebody), `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armament | primary | String | Armament name |
| Sequence |  | String | Displayed while attacking. |
| Delay | 0 | Integer | Delay in ticks before animation starts, either relative to attack preparation or attack. |
| DelayRelativeTo | Preparation | [`AttackDelayType`](#attackdelaytype) | Should the animation be delayed relative to preparation or actual attack? |
| Body | body | String | Which sprite body to modify. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithAttackOverlay
**Rendered together with an attack.**

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armament |  | String | Armament that will play the animation. Set to null to allow all armaments. |
| Sequence | *(required)* | String | Sequence name to use |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| IsDecoration | False | Boolean |  |
| Delay | 0 | Integer | Delay in ticks before overlay starts, either relative to attack preparation or attack. |
| DelayRelativeTo | Preparation | [`AttackDelayType`](#attackdelaytype) | Should the overlay be delayed relative to preparation or actual attack? |

### WithBridgeSpriteBody

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | GroundLevelBridge | String |  |
| AOffset | 0,0 | 2D Cell Vector | Offset to search for the 'A' neighbour |
| BOffset | 0,0 | 2D Cell Vector | Position to search for the 'B' neighbour |
| Sequences | idle | Collection of String | Sequences to use when both neighbours are alive. |
| ADestroyedSequences | adestroyed | Collection of String |  |
| BDestroyedSequences | bdestroyed | Collection of String |  |
| ABDestroyedSequences | abdestroyed | Collection of String |  |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithBuildingPlacedAnimation
**Changes the animation when the actor constructed a building.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | build | String | Sequence name to use |
| Body | body | String | Which sprite body to play the animation on. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithBuildingPlacedOverlay
**Rendered when the actor constructed a building.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | crane-overlay | String | Sequence name to use |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithBuildingRepairDecoration
**Displays a custom UI overlay relative to the actor's mouseover bounds.**

> Inherits from: [`WithDecoration`](#withdecoration), `WithDecorationBase`, `ConditionalTrait`.

> Requires trait(s): [`RepairableBuilding`](#repairablebuilding).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image |  | String | Image used for this decoration. Defaults to the actor's type. |
| Sequence | *(required)* | String | Sequence used for this decoration (can be animated). |
| Palette | chrome | String | Palette to render the sprite in. Reference the world actor's PaletteFrom* traits. |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithCargoPipsDecoration

> Inherits from: `WithDecorationBase`, `ConditionalTrait`.

> Requires trait(s): [`Cargo`](#cargo).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PipCount | -1 | Integer | Number of pips to display. Defaults to Cargo.MaxWeight. |
| PipStride | 0,0 | 2D Integer | If non-zero, override the spacing between adjacent pips. |
| Image | pips | String | Image that defines the pip sequences. |
| EmptySequence | pip-empty | String | Sequence used for empty pips. |
| FullSequence | pip-green | String | Sequence used for full pips that aren't defined in CustomPipSequences. |
| CustomPipSequences |  | Dictionary with Key: String, Value: String | Pip sequence to use for specific passenger actors. |
| Palette | chrome | String |  |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithChargeOverlay
**Render overlay that varies the animation frame based on the AttackCharges trait's charge level.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites), [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | active | String | Sequence to use for the charge levels. |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithChargeSpriteBody
**Render trait that varies the sprite body frame based on the AttackCharges trait's charge level.**

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`AttackCharges`](#attackcharges), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithCrateBody
**Renders crates with both water and land variants.**

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| XmasImages |  | Collection of String | Easteregg sequences to use in December. |
| WaterTerrainTypes | Water | Set of String | Terrain types on which to display WaterSequence. |
| IdleSequence | idle | String |  |
| WaterSequence |  | String |  |
| LandSequence |  | String |  |

### WithDamageOverlay
**Renders an overlay when the actor is taking heavy damage.**

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image | smoke_m | String |  |
| IdleSequence | idle | String |  |
| LoopSequence | loop | String |  |
| EndSequence | end | String |  |
| Offset | 0,0,0 | 3D World Vector | Position relative to the body orientation. |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName. |
| DamageTypes |  | Collection of DamageType | Damage types that this should be used for (defined on the warheads). Leave empty to disable all filtering. |
| MinimumDamageState | Heavy | [`DamageState`](#damagestate) | Trigger when Undamaged, Light, Medium, Heavy, Critical or Dead. |
| MaximumDamageState | Dead | [`DamageState`](#damagestate) |  |

### WithDeadBridgeSpriteBody

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| RampActors |  | Collection of String |  |
| AOffset | 0,0 | 2D Cell Vector | Offset to search for the 'A' neighbour |
| BOffset | 0,0 | 2D Cell Vector | Position to search for the 'B' neighbour |
| ARampSequences | aramp | Collection of String |  |
| BRampSequences | bramp | Collection of String |  |
| ABRampSequences | abramp | Collection of String |  |
| EditorSequence | editor | String | Placeholder sequence to use in the map editor. |
| EditorPalette | terrainalpha | String | Palette to use for the editor placeholder. |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithDeathAnimation
**This actor has a death animation.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DeathSequence | die | String | Sequence prefix to play when this actor is killed by a warhead. |
| DeathSequencePalette | player | String | The palette used for `DeathSequence`. |
| DeathPaletteIsPlayerPalette | True | Boolean | Custom death animation palette is a player palette BaseName |
| UseDeathTypeSuffix | True | Boolean | Should DeathType-specific sequences be used (sequence name = DeathSequence + DeathType). |
| CrushedSequence |  | String | Sequence to play when this actor is crushed. |
| CrushedSequencePalette | effect | String | The palette used for `CrushedSequence`. |
| CrushedPaletteIsPlayerPalette | False | Boolean | Custom crushed animation palette is a player palette BaseName |
| DeathTypes |  | Dictionary with Key: String, Value: Collection of String | Death animations to use for each damage type (defined on the warheads). Is only used if UseDeathTypeSuffix is `True`. |
| FallbackSequence |  | String | Sequence to use when the actor is killed by some non-standard means (e.g. suicide). |
| Delay | 0 | Integer | Delay the spawn of the death animation by this many ticks. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithDecoration
**Displays a custom UI overlay relative to the actor's mouseover bounds.**

> Inherits from: `WithDecorationBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image |  | String | Image used for this decoration. Defaults to the actor's type. |
| Sequence | *(required)* | String | Sequence used for this decoration (can be animated). |
| Palette | chrome | String | Palette to render the sprite in. Reference the world actor's PaletteFrom* traits. |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithDeliveryAnimation
**Building animation to play when ProductionAirdrop is used to deliver units.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ActiveSequence | active | String |  |
| Body | body | String | Which sprite body to play the animation on. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithDockedOverlay
**Rendered when a harvester is docked.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | docking-overlay | String | Sequence name to use |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithDockingAnimation

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DockSequence | dock | String | Displayed when docking to refinery. |
| DockLoopSequence | dock-loop | String | Looped while unloading at refinery. |

### WithDockingOverlay
**Rendered on the refinery when a voxel harvester is docking and undocking.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | unload-overlay | String | Sequence name to use |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithFacingSpriteBody

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithGateSpriteBody
**This actor visually connects to walls and changes appearance when actors walk through it.**

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Gate`](#gate), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| WallConnections |  | Collection of 2D Cell Vector | Cells (outside the gate footprint) that contain wall cells that can connect to the gate |
| Type | wall | String | Wall type for connections |
| OpenSequence |  | String | Override sequence to use when fully open. |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithHarvestAnimation

> Requires trait(s): [`Harvester`](#harvester), [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| HarvestSequence | harvest | String | Displayed while harvesting. |
| Body | body | String | Which sprite body to play the animation on. |

### WithHarvestOverlay
**Displays an overlay whenever resources are harvested by the actor.**

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | harvest | String | Sequence name to use |
| LocalOffset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette | effect | String |  |

### WithIdleAnimation
**Periodically plays an idle animation, replacing the default body animation.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequences | active | Collection of String | Sequence names to use. |
| Interval | 750 | Collection of Integer | The amount of time (in ticks) between animations. Two values indicate a range between which a random value is chosen. |
| Body | body | String | Which sprite body to play the animation on. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithIdleOverlay
**Renders a decorative animation on units and buildings.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image |  | String | Image used for this decoration. Defaults to the actor's type. |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle-overlay | String | Sequence name to use |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| IsDecoration | False | Boolean |  |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithInfantryBody

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MinIdleDelay | 30 | Integer |  |
| MaxIdleDelay | 110 | Integer |  |
| MoveSequence | run | String |  |
| DefaultAttackSequence |  | String |  |
| AttackSequences |  | Dictionary with Key: String, Value: Collection of String | Attack sequence to use for each armament. A dictionary of [armament name]: [sequence name(s)]. Multiple sequence names can be defined to specify per-burst animations. |
| IdleSequences |  | Collection of String |  |
| StandSequences | stand | Collection of String |  |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithMakeAnimation
**Replaces the sprite during construction/deploy/undeploy.**

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | make | String | Sequence name to use. |
| Condition |  | String | The condition to grant to self while the make animation is playing. |
| BodyNames | body | Collection of String | Apply to sprite bodies with these names. |

### WithMakeOverlay
**Draws an overlay on top of a make animation.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | *(required)* | String | Sequence name to use. |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName. |

### WithMoveAnimation

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MoveSequence | move | String | Displayed while moving. |
| Body | body | String | Which sprite body to modify. |
| ValidMovementTypes | Horizontal | [`MovementType`](#movementtype) | Apply condition on listed movement types. Available options are: None, Horizontal, Vertical, Turn. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithMuzzleOverlay
**Renders the MuzzleSequence from the Armament trait.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Armament`](#armament), [`RenderSprites`](#rendersprites), `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| IgnoreOffset | False | Boolean | Ignore the weapon position, and always draw relative to the center of the actor |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithNameTagDecoration
**Displays the player name above the unit**

> Inherits from: `WithDecorationBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MaxLength | 10 | Integer |  |
| Font | TinyBold | String |  |
| Color | FFFFFF | Color (RRGGBB[AA] notation) | Display in this color when not using the player color. |
| UsePlayerColor | False | Boolean | Use the player color of the current owner. |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithParachute
**Renders a parachute on units.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image |  | String | The image that contains the parachute sequences. |
| OpeningSequence |  | String | Parachute opening sequence. |
| Sequence |  | String | Parachute idle sequence. |
| ClosingSequence |  | String | Parachute closing sequence. Defaults to opening sequence played backwards. |
| Palette | player | String | Palette used to render the parachute. |
| IsPlayerPalette | True | Boolean |  |
| Offset | 0,0,384 | 3D World Vector | Parachute position relative to the paradropped unit. |
| ShadowImage |  | String | The image that contains the shadow sequence for the paradropped unit. |
| ShadowSequence |  | String | Paradropped unit's shadow sequence. |
| ShadowColor | 0000008C | Color (RRGGBB[AA] notation) | Color to render the paradropped unit's shadow. |
| ShadowOffset | 0,128,0 | 3D World Vector | Shadow position relative to the paradropped unit's intended landing position. |
| ShadowZOffset | 0 | Integer | Z-offset to apply on the shadow sequence. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithProductionDoorOverlay
**Play an animation when a unit exits or blocks the exit after production finished.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`Building`](#building), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | build-door | String |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithProductionIconOverlay
**Displays overlays from `ProductionIconOverlayManager` with matching types when defined prerequisites are granted.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Types | *(required)* | Collection of String |  |
| Prerequisites |  | Collection of String |  |

### WithProductionOverlay
**Renders an animation when the Production trait of the actor is activated. Works both with per player ClassicProductionQueue and per building ProductionQueue, but needs any of these.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`Production`](#production), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Queues |  | Set of String | Queues that should be producing for this overlay to render. |
| Sequence | production-overlay | String | Sequence name to use |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithRangeCircle
**Renders an arbitrary circle when selected or placing a structure**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type |  | String | Type of range circle. used to decide which circles to draw on other structures during building placement. |
| Color | FFFFFF80 | Color (RRGGBB[AA] notation) | Color of the circle |
| Width | 1 | Real Number | Border width. |
| BorderColor | 00000060 | Color (RRGGBB[AA] notation) | Color of the border. |
| BorderWidth | 3 | Real Number | Range circle border width. |
| UsePlayerColor | False | Boolean | If set, the color of the owning player will be used instead of `Color`. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships which will be able to see the circle. Valid values are combinations of `None`, `Ally`, `Enemy` and `Neutral`. |
| Visible | WhenSelected | [`RangeCircleVisibility`](#rangecirclevisibility) | When to show the range circle. Valid values are `Always`, and `WhenSelected` |
| Range | 0c0 | 1D World Distance | Range of the circle |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithRepairOverlay
**Displays an overlay when the building is being repaired by the player.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| StartSequence |  | String | Sequence to use upon repair beginning. |
| Sequence | active | String | Sequence name to play once during repair intervals or repeatedly if a start sequence is set. |
| EndSequence |  | String | Sequence to use after repairing has finished. |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithResourceLevelOverlay
**Displays the fill status of PlayerResources with an extra sprite overlay on the actor.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites), [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | resources | String | Sequence name to use |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithResourceLevelSpriteBody
**Render trait for buildings that change the sprite according to the remaining resource storage capacity across all depots.**

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Stages | 10 | Integer | Internal resource stages. Does not have to match number of sequence frames. |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithResourceStoragePipsDecoration

> Inherits from: `WithDecorationBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PipCount | 0 | Integer | Number of pips to display how filled unit is. |
| PipStride | 0,0 | 2D Integer | If non-zero, override the spacing between adjacent pips. |
| Image | pips | String | Image that defines the pip sequences. |
| EmptySequence | pip-empty | String | Sequence used for empty pips. |
| FullSequence | pip-green | String | Sequence used for full pips. |
| Palette | chrome | String |  |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithResupplyAnimation
**Replaces the default animation when actor resupplies a unit.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | active | String | Sequence name to use |
| Body | body | String | Which sprite body to play the animation on. |
| PlayAnimationOn | Rearm, Repair | [`ResupplyType`](#resupplytype) | Events leading to the animation getting played. Possible values currently are: Rearm, Repair. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithShadow
**Clones the actor sprite with another palette below it.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ShadowColor | 0000008C | Color (RRGGBB[AA] notation) | Color to draw shadow. |
| Offset | 0,0,0 | 3D World Vector | Shadow position offset relative to actor position (ground level). |
| ZOffset | -5 | Integer | Shadow Z offset relative to actor sprite. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithSpriteBarrel
**Renders barrels for units with the Turreted trait.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Armament`](#armament), [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites), [`Turreted`](#turreted).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | barrel | String | Sequence name to use. |
| Armament | primary | String | Armament to use for recoil. |
| LocalOffset | 0,0,0 | 3D World Vector | Visual offset. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithSpriteBody
**Default trait for rendering sprite-based actors.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithSpriteControlGroupDecoration
**Renders Ctrl groups using pixel art.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Palette | chrome | String |  |
| Image | pips | String |  |
| GroupSequence | groups | String | Sprite sequence used to render the control group 0-9 numbers. |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |

### WithSpriteTurret
**Renders turrets for units with the Turreted trait.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Armament`](#armament), [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites), [`Turreted`](#turreted).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | turret | String | Sequence name to use |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName |
| Turret | primary | String | Turreted 'Turret' key to display |
| Recoils | True | Boolean | Render recoil |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithStoresResourcesPipsDecoration

> Inherits from: `WithDecorationBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PipCount | 0 | Integer | Number of pips to display how filled unit is. |
| PipStride | 0,0 | 2D Integer | If non-zero, override the spacing between adjacent pips. |
| Image | pips | String | Image that defines the pip sequences. |
| EmptySequence | pip-empty | String | Sequence used for empty pips. |
| FullSequence | pip-green | String | Sequence used for full pips that aren't defined in ResourceSequences. |
| ResourceSequences |  | Dictionary with Key: String, Value: String | Pip sequence to use for specific resource types. |
| Palette | chrome | String |  |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithSupportPowerActivationAnimation
**Replaces the building animation when a support power is triggered.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteBody`](#withspritebody).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | active | String | Sequence name to use |
| Body | body | String | Which sprite body to play the animation on. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithSupportPowerActivationOverlay
**Displays an overlay when a support power is triggered.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | active | String | Sequence name to use |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithSwitchableOverlay
**Renders a decorative animation on units and buildings. Overlay switching controlled by PauseOnCondition.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Image |  | String | Image used for this decoration. Defaults to the actor's type. |
| SwitchingSequence |  | String | Animation to play when the trait is enabling and disabling. |
| EnabledSequence |  | String | Animation to play when the trait is enabled |
| DisabledSequence |  | String | Animation to play when the trait is disabled. |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| IsDecoration | False | Boolean |  |
| SwitchingLevel | 20 | Integer | How long (1 level = 1 tick) should the switching animation play? |
| SwitchingLevelOnSpawn | 20 | Integer | Levels when actor is spawned. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithTextControlGroupDecoration
**Renders Ctrl groups using typeface.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Font | TinyBold | String |  |
| Color | FFFFFF | Color (RRGGBB[AA] notation) | Display in this color when not using the player color. |
| UsePlayerColor | False | Boolean | Use the player color of the current owner. |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| Margin | 0,0 | 2D Integer | Offset text center position from the selection box edge. |

### WithTextDecoration
**Displays a text overlay relative to the selection box.**

> Inherits from: `WithDecorationBase`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Text | *(required)* | String |  |
| Font | TinyBold | String |  |
| Color | FFFFFF | Color (RRGGBB[AA] notation) | Display in this color when not using the player color. |
| UsePlayerColor | False | Boolean | Use the player color of the current owner. |
| Position | TopLeft | String | Position in the actor's selection box to draw the decoration. |
| ValidRelationships | Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can view the decoration. |
| RequiresSelection | False | Boolean | Should this be visible only when selected? |
| Margin | 0,0 | 2D Integer | Offset sprite center position from the selection box edge. |
| Offsets |  | Dictionary with Key: BooleanExpression, Value: 2D Integer | Screen-space offsets to apply when defined conditions are enabled. A dictionary of [condition string]: [x, y offset]. |
| BlinkInterval | 5 | Integer | The number of ticks that each step in the blink pattern in active. |
| BlinkPattern |  | Collection of BlinkState (enum) | A pattern of ticks (BlinkInterval long) where the decoration is visible or hidden. |
| BlinkPatterns |  | Dictionary with Key: BooleanExpression, Value: Collection of BlinkState (enum) | Override blink conditions to use when defined conditions are enabled. A dictionary of [condition string]: [pattern]. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithTurretAimAnimation

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`WithSpriteTurret`](#withspriteturret), `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armament | primary | String | Armament name |
| Turret | primary | String | Turret name |
| Sequence | *(required)* | String | Displayed while targeting. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithTurretAttackAnimation

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`Armament`](#armament), [`WithSpriteTurret`](#withspriteturret).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Armament | primary | String | Armament name |
| Turret | primary | String | Turret name |
| Sequence |  | String | Displayed while attacking. |
| Delay | 0 | Integer | Delay in ticks before animation starts, either relative to attack preparation or attack. |
| DelayRelativeTo | Preparation | [`AttackDelayType`](#attackdelaytype) | Should the animation be delayed relative to preparation or actual attack? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithWallSpriteBody
**Render trait for actors that change sprites if neighbors with the same trait are present.**

> Inherits from: [`WithSpriteBody`](#withspritebody), `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`Building`](#building), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Type | wall | String |  |
| StartSequence |  | String | Animation to play when the actor is created. |
| Sequence | idle | String | Animation to play when the actor is idle. |
| Name | body | String | Identifier used to assign modifying traits to this sprite body. |
| ForceToGround | False | Boolean | Forces sprite body to be rendered on ground regardless of actor altitude (for example for custom shadow sprites). |
| Palette |  | String | Custom palette name. |
| IsPlayerPalette | False | Boolean | Palette is a player palette BaseName. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

## OpenRA.Mods.Common.Traits.Sound

### ActorLostNotification

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Notification | UnitLost | String | Speech notification to play. |
| TextNotification |  | String | Text notification to display. |
| NotifyAll | False | Boolean |  |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AmbientSound
**Plays a looping audio file at the actor position. Attach this to the `World` actor to cover the whole map.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| SoundFiles | *(required)* | Collection of String |  |
| Delay | 0 | Collection of Integer | Initial delay (in ticks) before playing the sound for the first time. Two values indicate a random delay range. |
| Interval | 0 | Collection of Integer | Interval between playing the sound (in ticks). Two values indicate a random delay range. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AnnounceOnKill
**Play the Kill voice of this actor when eliminating enemies.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Interval | 5000 | Integer | Minimum duration (in milliseconds) between sound events. |
| Voice | Kill | String | Voice to use when killing something. |

### AnnounceOnSeen
**Players will be notified when this actor becomes visible to them. Requires the 'EnemyWatcher' trait on the player actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| PingRadar | False | Boolean | Should there be a radar ping on enemies' radar at the actor's location when they see him |
| Notification |  | String | Speech notification to play. |
| TextNotification |  | String | Text notification to display. |
| AnnounceNeutrals | False | Boolean |  |

### AttackSounds
**Played when preparing for an attack or attacking.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sounds |  | Collection of String | Play a randomly selected sound from this list when preparing for an attack or attacking. |
| Delay | 0 | Integer | Delay in ticks before sound starts, either relative to attack preparation or attack. |
| DelayRelativeTo | Preparation | [`AttackDelayType`](#attackdelaytype) | Should the sound be delayed relative to preparation or actual attack? |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### CaptureNotification

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Notification | BuildingCaptured | String | Speech notification to play to the new owner. |
| TextNotification |  | String | Text notification to display to the new owner. |
| NewOwnerVoice | True | Boolean | Specifies if Notification is played with the voice of the new owners faction. |
| LoseNotification |  | String | Speech notification to play to the old owner. |
| LoseTextNotification |  | String | Text notification to display to the old owner. |
| LoseNewOwnerVoice | False | Boolean | Specifies if LoseNotification is played with the voice of the new owners faction. |

### DeathSounds
**Sounds to play when killed.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Voice | Die | String | Death notification voice. |
| VolumeMultiplier | 1 | Real Number | Multiply volume with this factor. |
| DeathTypes |  | Collection of DamageType | Damage types that this should be used for (defined on the warheads). If empty, this will be used as the default sound for all death types. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SoundOnDamageTransition

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| DamagedSounds |  | Collection of String | Play a random sound from this list when damaged. |
| DestroyedSounds |  | Collection of String | Play a random sound from this list when destroyed. |
| DamageTypes |  | Collection of DamageType | DamageType(s) that trigger the sounds. Leave empty to always trigger a sound. |

### VoiceAnnouncement
**Plays a voice clip when the trait is enabled.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Voice | *(required)* | String | Voice to play. |
| ValidRelationships | Enemy, Neutral, Ally | [`PlayerRelationship`](#playerrelationship) | Player relationships who can hear this voice. |
| PlayToOwner | True | Boolean | Play the voice to the owning player even if Stance.Ally is not included in ValidStances. |
| OneShot | False | Boolean | Disable the announcement after it has been triggered. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

## OpenRA.Mods.D2k.Traits

### AttackSwallow
**Sandworms use this attack model.**

> Inherits from: [`AttackFrontal`](#attackfrontal), `AttackBase`, `PausableConditionalTrait`, `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ReturnDelay | 60 | Integer | The number of ticks it takes to return underground. |
| AttackDelay | 30 | Integer | The number of ticks it takes to get in place under the target to attack. |
| AttackingCondition |  | String | The condition to grant to self while attacking. |
| WormAttackSound | WORM.WAV | String |  |
| WormAttackNotification | WormAttack | String |  |
| WormAttackTextNotification | notification-worm-attack | String |  |
| Armaments | primary, secondary | Collection of String | Armament names |
| Cursor |  | String | Cursor to display when hovering over a valid target. |
| OutsideRangeCursor |  | String | Cursor to display when hovering over a valid target that is outside of range. |
| TargetLineColor | DC143C | Color (RRGGBB[AA] notation) | Color to use for the target line. |
| AttackRequiresEnteringCell | False | Boolean | Does the attack type require the attacker to enter the target's cell? |
| TargetFrozenActors | False | Boolean | Allow firing into the fog to target frozen actors without requiring force-fire. |
| ForceFireIgnoresActors | False | Boolean | Force-fire mode ignores actors and targets the ground instead. |
| OutsideRangeRequiresForceFire | False | Boolean | Force-fire mode is required to enable targeting against targets outside of range. |
| Voice | Action | String |  |
| FacingTolerance | 512 | 1D World Angle | Tolerance for attack angle. Range [0, 512], 512 covers 360 degrees. |
| TargetTerrainWithoutForceFire | False | Boolean | When enabled, show the target cursor on terrain cells even without force-fire. |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### AttractsWorms
**This actor makes noise, which causes them to be targeted by actors with the Sandworm trait.**

> Inherits from: `ConditionalTrait`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Intensity | 0 | Integer | How much noise this actor produces. |
| Falloff | 100, 100, 25, 11, 6, 4, 3, 2, 1, 0 | Collection of Integer | Noise percentage at Range step away from the actor. |
| Spread | 3c0 | 1D World Distance | Range between falloff steps. |
| Range |  | Collection of 1D World Distance | Ranges at which each Falloff step is defined. Overrides Spread. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### BuildableTerrainLayer
**Attach this to the world actor. Required for LaysTerrain to work.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Palette | terrain | String | Palette to render the layer sprites in. |
| MaxStrength | 9000 | Integer | The hitpoints, which can be reduced by the DamagesConcreteWarhead. |

### D2kActorPreviewPlaceBuildingPreview
**Creates a building placement preview based on the map editor actor preview.**

> Inherits from: [`ActorPreviewPlaceBuildingPreview`](#actorpreviewplacebuildingpreview), [`FootprintPlaceBuildingPreview`](#footprintplacebuildingpreview).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UnsafeTerrainTypes | Rock | Set of String | Terrain types that should show the 'unsafe' footprint tile. |
| RequiresPrerequisites |  | Collection of String | Only check for 'unsafe' footprint tiles when you have these prerequisites. |
| Image | overlay | String | Sprite image to use for the overlay. |
| TileValidName | build-valid | String | Sprite overlay to use for valid cells. |
| TileInvalidName | build-invalid | String | Sprite overlay to use for invalid cells. |
| TileUnsafeName | build-unsafe | String | Sprite overlay to use for blocked cells. |
| Animated | True | Boolean | Enable the building's idle animation. |
| PreviewAlpha | 1 | Real Number | Custom opacity to apply to the actor preview. |
| FootprintUnderPreview | Valid, LineBuild | [`PlaceBuildingCellType`](#placebuildingcelltype) | Footprint types to draw underneath the actor preview. |
| FootprintOverPreview | Invalid | [`PlaceBuildingCellType`](#placebuildingcelltype) | Footprint types to draw above the actor preview. |
| ZOffset | 0 | Integer | Custom ZOffset of the rendered building preview. |
| Palette | terrain | String | Palette to use for rendering the placement sprite. |
| FootprintAlpha | 1 | Real Number | Custom opacity to apply to the placement sprite. |
| LineBuildFootprintAlpha | 1 | Real Number | Custom opacity to apply to the line-build placement sprite. |

### D2kResourceRenderer
**Used to render spice with round borders. Attach this to the world actor**

> Inherits from: [`ResourceRenderer`](#resourcerenderer).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| ResourceTypes |  | Dictionary with Key: String, Value: ResourceTypeInfo |  |

### HarvesterInsurance
**A player with this trait will receive a free harvester when his last one gets eaten by a sandworm, provided he has at least one refinery.**

### Sandworm

> Inherits from: [`Wanders`](#wanders), `ConditionalTrait`.

> Requires trait(s): [`Mobile`](#mobile), `AttackBase`.

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TargetRescanInterval | 125 | Integer | Time between rescanning for targets (in ticks). |
| MaxSearchRadius | 20c0 | 1D World Distance | The radius in which the worm "searches" for targets. |
| IgnoreNoiseAttackRange | 3c0 | 1D World Distance | The range at which the worm launches an attack regardless of noise levels. |
| ChanceToDisappear | 100 | Integer | The chance this actor has of disappearing after it attacks (in %). |
| WanderMoveRadius | 1 | Integer |  |
| ReduceMoveRadiusDelay | 5 | Integer | Number of ticks to wait before decreasing the effective move radius. |
| MinMoveDelay | 0 | Integer | Minimum amount of ticks the actor will sit idly before starting to wander. |
| MaxMoveDelay | 0 | Integer | Maximum amount of ticks the actor will sit idly before starting to wander. |
| AvoidTerrainTypes |  | Set of String | The terrain types that this actor should avoid wandering on to. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### SpiceBloom
**Seeds resources by explosive eruptions after accumulation times.**

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| GrowthSequences | grow1, grow2, grow3 | Collection of String |  |
| SpurtSequence | spurt | String |  |
| Lifetime | 2000, 3000 | Collection of Integer | The range of time (in ticks) that the spicebloom will take to grow until it blows up. |
| ResourceType | Spice | String |  |
| GrowthTerrainTypes |  | Set of String | Spice blooms only grow on these terrain types. |
| Weapon |  | String | The weapon to use for spice creation. |
| Bursts | 4, 12 | Collection of Integer | The number of times to fire Weapon at the minimum and maximum actor age. |
| Range | 3, 5 | Collection of Integer | The minimum and maximum distance in cells that spice may be expelled. |
| BurstInterval | 1 | Integer | Delay between each burst. (in Ticks) |

## OpenRA.Mods.D2k.Traits.Buildings

### D2kBuilding

> Inherits from: [`Building`](#building).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Damage | 500 | Integer | Amount of damage received per DamageInterval ticks. |
| DamageInterval | 100 | Integer | Delay between receiving damage. |
| DamageTypes |  | Collection of DamageType | Apply the damage using these damagetypes. |
| DamageTerrainTypes | Rock | Collection of String | Terrain types where the actor will take damage. |
| DamageThreshold | 50 | Integer | Percentage health below which the actor will not receive further damage. |
| StartOnThreshold | True | Boolean | Inflict damage down to the DamageThreshold when the actor gets created on damaging terrain. |
| ConcreteTemplate | 88 | UInt16 | The terrain template to place when adding a concrete foundation. If the template is PickAny, then the actor footprint will be filled with this tile. |
| ConcretePrerequisites |  | Collection of String | List of required prerequisites to place a terrain template. |
| TerrainTypes |  | Set of String | Where you are allowed to place the building (Water, Clear, ...) |
| Footprint |  | Dictionary with Key: 2D Cell Vector, Value: FootprintCellType (enum) | x means cell is blocked, capital X means blocked but not counting as targetable,  = means part of the footprint but passable, _ means completely empty. |
| Dimensions | 1,1 | 2D Cell Vector |  |
| LocalCenterOffset | 0,0,0 | 3D World Vector | Shift center of the actor by this offset. |
| RequiresBaseProvider | False | Boolean |  |
| AllowInvalidPlacement | False | Boolean |  |
| AllowPlacementOnResources | False | Boolean |  |
| RemoveSmudgesOnBuild | True | Boolean | Clear smudges from underneath the building footprint. |
| RemoveSmudgesOnSell | True | Boolean | Clear smudges from underneath the building footprint on sell. |
| RemoveSmudgesOnTransform | True | Boolean | Clear smudges from underneath the building footprint on transform. |
| BuildSounds |  | Collection of String |  |
| UndeploySounds |  | Collection of String |  |

## OpenRA.Mods.D2k.Traits.Render

### WithCrumbleOverlay
**Rendered together with the "make" animation.**

> Inherits from: `ConditionalTrait`.

> Requires trait(s): [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | crumble-overlay | String | Sequence name to use |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

### WithDeliveryOverlay
**Rendered when ProductionAirdrop is in progress.**

> Inherits from: `PausableConditionalTrait`, `ConditionalTrait`.

> Requires trait(s): [`BodyOrientation`](#bodyorientation), [`RenderSprites`](#rendersprites).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Sequence | active | String | Sequence name to use |
| Offset | 0,0,0 | 3D World Vector | Position relative to body |
| Palette |  | String | Custom palette name |
| IsPlayerPalette | False | Boolean | Custom palette is a player palette BaseName |
| PauseOnCondition |  | BooleanExpression | Boolean expression defining the condition to pause this trait. |
| RequiresCondition |  | BooleanExpression | Boolean expression defining the condition to enable this trait. |

## OpenRA.Mods.Mobius.Traits

### FixedColorShift
**Apply a fixed color shift to a palette. Use this to add RGBA compatibility to FixedColorPalette.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BasePalette | *(required)* | String | The name of the palette to base off. |
| Color | 00000000 | Color (RRGGBB[AA] notation) | The fixed color to remap. |
| MinHue | 0.29 | Real Number | Hues between this and MaxHue will be shifted. |
| MaxHue | 0.37 | Real Number | Hues between MinHue and this will be shifted. |
| ReferenceHue | 0.33 | Real Number | Hue reference for the color shift. |
| ReferenceSaturation | 0.925 | Real Number | Saturation reference for the color shift. |
| ReferenceValue | 0.95 | Real Number | Value reference for the color shift. |

## OpenRA.Traits

### DebugPauseState
**Checks for pause related desyncs. Attach this to the world actor.**

### DebugVisualizations
**Enables visualization commands. Attach this to the world actor.**

### Faction
**Attach this to the `World` actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Name |  | String | This is the name exposed to the players. |
| InternalName |  | String | This is the internal name for owner checks. |
| RandomFactionMembers |  | Set of String | Pick a random faction as the player's faction out of this list. |
| Side |  | String | The side that the faction belongs to. For example, England belongs to the 'Allies' side. |
| Description |  | String | This is shown in the lobby as a tooltip. |
| Selectable | True | Boolean |  |

### FrozenActorLayer
**Required for FrozenUnderFog to work. Attach this to the player actor.**

> Requires trait(s): [`Shroud`](#shroud).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BinSize | 10 | Integer | Size of partition bins (cells) |

### ScreenMap

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| BinSize | 250 | Integer | Size of partition bins (world pixels) |

### ScreenShaker

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| MinMultiplier | -3,-3 | 2D Real Number |  |
| MaxMultiplier | 3,3 | 2D Real Number |  |

### Shroud
**Required for shroud and fog visibility checks. Add this to the player actor.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| FogCheckboxLabel | checkbox-fog-of-war.label | String | Descriptive label for the fog checkbox in the lobby. |
| FogCheckboxDescription | checkbox-fog-of-war.description | String | Tooltip description for the fog checkbox in the lobby. |
| FogCheckboxEnabled | True | Boolean | Default value of the fog checkbox in the lobby. |
| FogCheckboxLocked | False | Boolean | Prevent the fog enabled state from being changed in the lobby. |
| FogCheckboxVisible | True | Boolean | Whether to display the fog checkbox in the lobby. |
| FogCheckboxDisplayOrder | 0 | Integer | Display order for the fog checkbox in the lobby. |
| ExploredMapCheckboxLabel | checkbox-explored-map.label | String | Descriptive label for the explored map checkbox in the lobby. |
| ExploredMapCheckboxDescription | checkbox-explored-map.description | String | Tooltip description for the explored map checkbox in the lobby. |
| ExploredMapCheckboxEnabled | False | Boolean | Default value of the explore map checkbox in the lobby. |
| ExploredMapCheckboxLocked | False | Boolean | Prevent the explore map enabled state from being changed in the lobby. |
| ExploredMapCheckboxVisible | True | Boolean | Whether to display the explore map checkbox in the lobby. |
| ExploredMapCheckboxDisplayOrder | 0 | Integer | Display order for the explore map checkbox in the lobby. |

# Related value types (enums):

### ActorFlashType
Possible values: `Overlay`, `Tint`

Referenced by: [`OrderEffects`](#ordereffects)

### AirAttackType
Possible values: `Default`, `Hover`, `Strafe`

Referenced by: [`AttackAircraft`](#attackaircraft)

### AttackDelayType
Possible values: `Preparation`, `Attack`

Referenced by: [`AttackSounds`](#attacksounds), [`WithAttackAnimation`](#withattackanimation), [`WithAttackOverlay`](#withattackoverlay), [`WithTurretAttackAnimation`](#withturretattackanimation)

### BlendMode
Possible values: `None`, `Alpha`, `Additive`, `Subtractive`, `Multiply`, `Multiplicative`, `DoubleMultiplicative`, `LowAdditive`, `Screen`, `Translucent`

Referenced by: [`ShroudRenderer`](#shroudrenderer)

### CloakStyle
Possible values: `None`, `Alpha`, `Color`, `Palette`

Referenced by: [`Cloak`](#cloak)

### DamageSource
Possible values: `Self`, `Killer`

Referenced by: [`Explodes`](#explodes)

### DamageState
Possible values: `Undamaged`, `Light`, `Medium`, `Heavy`, `Critical`, `Dead`

Referenced by: [`BridgePlaceholder`](#bridgeplaceholder), [`ExplosionOnDamageTransition`](#explosionondamagetransition), [`GrantConditionOnDamageState`](#grantconditionondamagestate), [`WithDamageOverlay`](#withdamageoverlay)

### DetectionCircleVisibility
Possible values: `Always`, `WhenSelected`

Referenced by: [`RenderDetectionCircle`](#renderdetectioncircle)

### EffectType
Possible values: `None`, `Black`, `Desaturated`

Referenced by: [`MenuPostProcessEffect`](#menupostprocesseffect)

### ElevatedBridgePlaceholderOrientation
Possible values: `X`, `Y`

Referenced by: [`ElevatedBridgePlaceholder`](#elevatedbridgeplaceholder)

### EnterBehaviour
Possible values: `Exit`, `Suicide`, `Dispose`

Referenced by: [`Demolition`](#demolition), [`Infiltrates`](#infiltrates), [`InstantlyRepairs`](#instantlyrepairs), [`RepairsBridges`](#repairsbridges)

### ExplosionType
Possible values: `Footprint`, `CenterPosition`

Referenced by: [`Explodes`](#explodes)

### IdleBehaviorType
Possible values: `None`, `Land`, `ReturnToBase`, `LeaveMap`, `LeaveMapAtClosestEdge`

Referenced by: [`Aircraft`](#aircraft)

### LineBuildDirection
Possible values: `Unset`, `X`, `Y`

Referenced by: [`GrantConditionOnLineBuildDirection`](#grantconditiononlinebuilddirection)

### MovementType
Possible values: `None`, `Horizontal`, `Vertical`, `Turn`

Referenced by: [`GrantConditionOnMovement`](#grantconditiononmovement), [`WithMoveAnimation`](#withmoveanimation)

### NormalType
Possible values: `TiberianSun`, `RedAlert2`

Referenced by: [`VoxelNormalsPalette`](#voxelnormalspalette)

### OwnerLostActionType
Possible values: `ChangeOwner`, `Dispose`, `Kill`

Referenced by: [`OwnerLostAction`](#ownerlostaction)

### OwnerType
Possible values: `Victim`, `Killer`, `InternalName`

Referenced by: [`SpawnActorOnDeath`](#spawnactorondeath)

### PlaceBuildingCellType
Possible values: `None`, `Valid`, `Invalid`, `LineBuild`

Referenced by: [`ActorPreviewPlaceBuildingPreview`](#actorpreviewplacebuildingpreview), [`D2kActorPreviewPlaceBuildingPreview`](#d2kactorpreviewplacebuildingpreview), [`SequencePlaceBuildingPreview`](#sequenceplacebuildingpreview)

### PlayerRelationship
Possible values: `None`, `Enemy`, `Neutral`, `Ally`

Referenced by: [`AcceptsDeliveredCash`](#acceptsdeliveredcash), [`AcceptsDeliveredExperience`](#acceptsdeliveredexperience), [`AirstrikePower`](#airstrikepower), [`AppearsOnRadar`](#appearsonradar), [`Armament`](#armament), [`AttackOrderPower`](#attackorderpower), [`AutoCrusher`](#autocrusher), [`AutoTargetPriority`](#autotargetpriority), [`BlocksProjectiles`](#blocksprojectiles), [`CaptureManagerBotModule`](#capturemanagerbotmodule), [`Captures`](#captures), [`CashTricklerBar`](#cashtricklerbar), [`ChronoshiftPower`](#chronoshiftpower), [`CreatesShroud`](#createsshroud), [`Demolition`](#demolition), [`Disguise`](#disguise), [`DisguiseTooltip`](#disguisetooltip), [`DropPodsPower`](#droppodspower), [`FrozenUnderFog`](#frozenunderfog), [`Gate`](#gate), [`GivesBounty`](#givesbounty), [`GivesExperience`](#givesexperience), [`GpsPower`](#gpspower), [`GrantExternalConditionPower`](#grantexternalconditionpower), [`GrantPrerequisiteChargeDrainPower`](#grantprerequisitechargedrainpower), [`HiddenUnderFog`](#hiddenunderfog), [`HiddenUnderShroud`](#hiddenundershroud), [`InfiltrateForDecoration`](#infiltratefordecoration), [`Infiltrates`](#infiltrates), [`InstantlyRepairs`](#instantlyrepairs), [`IonCannonPower`](#ioncannonpower), [`JamsMissiles`](#jamsmissiles), [`NukePower`](#nukepower), [`ParatroopersPower`](#paratrooperspower), [`ProduceActorPower`](#produceactorpower), [`ProximityExternalCondition`](#proximityexternalcondition), [`RevealOnDeath`](#revealondeath), [`RevealOnFire`](#revealonfire), [`RevealsMap`](#revealsmap), [`RevealsShroud`](#revealsshroud), [`SpawnActorPower`](#spawnactorpower), [`SupportPowerChargeBar`](#supportpowerchargebar), [`Tooltip`](#tooltip), [`TooltipDescription`](#tooltipdescription), [`VoiceAnnouncement`](#voiceannouncement), [`WithAmmoPipsDecoration`](#withammopipsdecoration), [`WithBuildingRepairDecoration`](#withbuildingrepairdecoration), [`WithCargoPipsDecoration`](#withcargopipsdecoration), [`WithDecoration`](#withdecoration), [`WithNameTagDecoration`](#withnametagdecoration), [`WithRangeCircle`](#withrangecircle), [`WithResourceStoragePipsDecoration`](#withresourcestoragepipsdecoration), [`WithStoresResourcesPipsDecoration`](#withstoresresourcespipsdecoration), [`WithTextDecoration`](#withtextdecoration)

### PowerState
Possible values: `Normal`, `Low`, `Critical`

Referenced by: [`GrantConditionOnPowerState`](#grantconditiononpowerstate)

### RangeCircleMode
Possible values: `Maximum`, `Minimum`

Referenced by: [`RenderRangeCircle`](#renderrangecircle)

### RangeCircleVisibility
Possible values: `Always`, `WhenSelected`

Referenced by: [`WithRangeCircle`](#withrangecircle)

### ResupplyType
Possible values: `None`, `Rearm`, `Repair`

Referenced by: [`WithResupplyAnimation`](#withresupplyanimation)

### RevealDisguiseType
Possible values: `None`, `Attack`, `Damaged`, `Load`, `Unload`, `Infiltrate`, `Demolish`, `Move`

Referenced by: [`Disguise`](#disguise)

### SelectionPriorityModifiers
Possible values: `None`, `Ctrl`, `Alt`

Referenced by: [`IsometricSelectable`](#isometricselectable), [`Selectable`](#selectable)

### TrailType
Possible values: `Cell`, `CenterPosition`

Referenced by: [`LeavesTrails`](#leavestrails)

### UncloakType
Possible values: `None`, `Attack`, `Move`, `Load`, `Unload`, `Infiltrate`, `Demolish`, `Damage`, `Heal`, `SelfHeal`, `Dock`, `SupportPower`

Referenced by: [`Cloak`](#cloak)

### UnitStance
Possible values: `HoldFire`, `ReturnFire`, `Defend`, `AttackAnything`

Referenced by: [`AutoTarget`](#autotarget)

### VisibilityType
Possible values: `Footprint`, `CenterPosition`, `GroundPosition`

Referenced by: [`CreatesShroud`](#createsshroud), [`HiddenUnderFog`](#hiddenunderfog), [`HiddenUnderShroud`](#hiddenundershroud), [`RevealsShroud`](#revealsshroud)

