Unit
====

### Prefix: unit

### Description

Any character in game, including players, NPCs, Banks, summoned Pets and
Mounts, Vendors, and Ability Vendors

------------------------------------------------------------------------

`Enum`

CodeEnumArchetype
-----------------

-   **EliteShields**
-   **Iconic**
-   **Townie**
-   **EliteNoShields**
-   **Guard**

------------------------------------------------------------------------

`Enum`

CodeEnumCastBarType
-------------------

### Description

Represents the type of cast bar being shown

-   **None**
-   **Normal**
-   **Telegraph\_Backlash**
-   **Telegraph\_Evade**

------------------------------------------------------------------------

`Enum`

CodeEnumCCState
---------------

### Description

An enum representing the various crowd control effects, including Taunt

-   **Stun**
-   **Sleep**
-   **Root**
-   **Disarm**
-   **Silence**
-   **Polymorph**
-   **Fear**
-   **Hold**
-   **Knockdown**
-   **Vulnerability**
-   **VulnerabilityWithAct**
-   **Disorient**
-   **Disable**
-   **Taunt**
-   **Detaunt**
-   **Blind**
-   **Knockback**
-   **Pushback**
-   **Pull**
-   **PositionSwitch**
-   **Tether**
-   **Snare**
-   **Interrupt**
-   **Daze**
-   **Subdue**
-   **Grounded**
-   **DisableCinematic**
-   **AbilityRestriction**

------------------------------------------------------------------------

`Enum`

CodeEnumCCStateStunVictimGameplay
---------------------------------

-   **Forward**
-   **Backward**
-   **Left**
-   **Right**

------------------------------------------------------------------------

`Enum`

CodeEnumDiminishingReturnState
------------------------------

-   **Linear**
-   **SoftCap**
-   **HardCap**

------------------------------------------------------------------------

`Enum`

CodeEnumDisposition
-------------------

### Description

An NPC's disposition towards the player.\
Hostile: Attacks when their target is within agro range\
Neutral: Will only attack if they are attacked first Friendly: The unit
cannot attack or be attacked by the target

-   **Hostile**
-   **Neutral**
-   **Friendly**
-   **Unknown**

------------------------------------------------------------------------

`Enum`

CodeEnumEliteness
-----------------

### Description

An enum representing the estimated group size needed to kill the NPC.

-   **Solo**
-   **Group**
-   **SmallRaid**
-   **LargeRaid**

------------------------------------------------------------------------

`Enum`

CodeEnumEUnitStatType
---------------------

-   **Resources0**
-   **Resources1**
-   **Resources2**
-   **Resources3**
-   **Resources4**
-   **Resources5**
-   **Resources6**
-   **Resources7**
-   **Resources8**
-   **Resources9**
-   **Resources10**

------------------------------------------------------------------------

`Enum`

CodeEnumFaction
---------------

### Description

An enum representing the different player factions

-   **DominionPlayer**
-   **ExilesPlayer**

------------------------------------------------------------------------

`Enum`

CodeEnumFlightPathType
----------------------

### Description

An enum representing different types of flight paths\
Local: Traveling from one place to another within the same worldId\
Transfer: Traveling from one worldId to another

-   **Local**
-   **Transfer**

------------------------------------------------------------------------

`Enum`

CodeEnumGender
--------------

### Description

An enum representing a unit's gender. For the sake of this enum, Chua
are male.

-   **Male**
-   **Female**
-   **Uni**

------------------------------------------------------------------------

`Enum`

CodeEnumLevelDifferentialAttribute
----------------------------------

### Description

An enum that contains the different colors used to show level difference
between a unit and the player. These are listed in ascending order.

-   **Grey**
-   **Green**
-   **Cyan**
-   **Blue**
-   **White**
-   **Yellow**
-   **Orange**
-   **Red**
-   **Magenta**

------------------------------------------------------------------------

`Enum`

CodeEnumLootItemType
--------------------

### Description

An enum representing the different types of loot that can drop off an
NPC. StaticItem: Your typical item loot. Cash: Make money money...\
Virtual Item: Virtual items used for specific quests / challenges /
dungeons / adventures\
AdventureSpell: Drops that have an immediate effect on the player that
picks them up

-   **StaticItem**
-   **Cash**
-   **VirtualItem**
-   **AdventureSpell**
-   **AccountItem**

------------------------------------------------------------------------

`Enum`

CodeEnumProperties
------------------

### Description

An enum representing various unit properties. These properties are
generally seen on the Character and Inspect screens in the default UI

-   **Strength**
-   **Dexterity**
-   **Technology**
-   **Magic**
-   **Wisdom**
-   **BaseHealth**
-   **ManaPerFiveSeconds**
-   **HealthRegenMultiplier**
-   **ResourceMax\_0**
-   **ResourceMax\_1**
-   **ResourceMax\_2**
-   **ResourceMax\_3**
-   **ResourceMax\_4**
-   **ResourceMax\_5**
-   **ResourceMax\_6**
-   **ResourceRegenMultiplier\_0**
-   **ResourceRegenMultiplier\_1**
-   **ResourceRegenMultiplier\_2**
-   **ResourceRegenMultiplier\_3**
-   **ResourceRegenMultiplier\_4**
-   **ResourceRegenMultiplier\_5**
-   **ResourceRegenMultiplier\_6**
-   **ResistPhysical**
-   **ResistTech**
-   **ResistMagic**
-   **StalkerWoundMultiplier**
-   **KillingSpreeOutOfCombatGracePeriodMS**
-   **Rating\_AvoidReduce**
-   **Rating\_AvoidIncrease**
-   **MoveSpeedMultiplier**
-   **Rating\_CritChanceIncrease**
-   **AssaultPower**
-   **SupportPower**
-   **ResourceMax\_7**
-   **ResourceRegenMultiplier\_7**
-   **Stamina**
-   **ShieldCapacityMax**
-   **Armor**
-   **Rating\_CritChanceDecrease**
-   **InterruptArmor\_Threshold**
-   **InterruptArmor\_RechargeTime**
-   **InterruptArmor\_RechargeCount**
-   **RatingCritSeverityIncrease**
-   **BaseAvoidChance**
-   **BaseCritChance**
-   **PvPPrestigeMultiplier**
-   **PvPXPMultiplier**
-   **BreathDecay**
-   **CCPower**
-   **CriticalHitSeverityMultiplier**
-   **Health\_Total\_Multiplier**
-   **JumpHeight**
-   **GravityMultiplier**
-   **XpMultiplier**
-   **ThreatMultiplier**
-   **AutoAttackDelayMultiplier**
-   **FallingDamageMultiplier**
-   **DamageDealtMultiplierMelee**
-   **DamageDealtMultiplierRanged**
-   **DamageDealtMultiplierSpell**
-   **DamageDealtMultiplierPhysical**
-   **DamageDealtMultiplierTech**
-   **DamageDealtMultiplierMagic**
-   **DamageTakenOffsetPhysical**
-   **DamageTakenOffsetTech**
-   **DamageTakenOffsetMagic**
-   **DamageTakenMultiplierPhysical**
-   **DamageTakenMultiplierTech**
-   **DamageTakenMultiplierMagic**
-   **HealingMultiplierOutgoing**
-   **HealingMultiplierIncoming**
-   **ExecutingEnergyRateMultiplier**
-   **CCDurationModifier**
-   **ResistPhysicalMitigationMultiplier**
-   **ResistTechMitigationMultiplier**
-   **ResistMagicMitigationMultiplier**
-   **KillSpreeCCVMulitplier**
-   **ManaFinalMultiplier**
-   **ReputationMultiplier**
-   **ShieldMitigationMin**
-   **ShieldMitigationMax**
-   **ShieldRegenPct**
-   **ShieldDamageTypes**
-   **SlowFallMultiplier**
-   **PathXpMultiplier**
-   **ScientistScanBotThoroughnessMultiplier**
-   **ScientistScanBotScanTimeMultiplier**
-   **ScientistScanBotRangeMultiplier**
-   **ScientistScanBotHealthMultiplier**
-   **ScientistScanBotSpeedMultiplier**
-   **SettlerImprovementTimeMultiplier**
-   **CreatureScientistScanMultiplier**
-   **ManaBase**
-   **InterruptArmor\_AfterCCRechargeTime**
-   **InterruptArmor\_AfterCCRechargeCount**
-   **PvPOffensiveRating**
-   **PvPDefensiveRating**
-   **DamageMitigationPctOffset**
-   **BaseAvoidReduceChance**
-   **BaseAvoidCritChance**
-   **StealthDetectionModifier**
-   **ManaRegenInCombat**
-   **ManaRegenOutOfCombat**
-   **SeeThroughStealth**
-   **FrictionMax**
-   **Deprecated1**
-   **Deprecated2**
-   **RenownGainMultiplier**
-   **MoneyDropMultiplier**
-   **SpellMechanicEnergyRegenOrDecayMultiplier**
-   **SpellMechanicEnergyDecayOverdriveMultiplier**
-   **ItemArmor**
-   **ItemAssaultPower**
-   **ItemSupportPower**
-   **IgnoreArmorBase**
-   **IgnoreShieldBase**
-   **MaxThreatVsCreature**
-   **ManaCostModifier**
-   **CooldownReductionModifier**
-   **BaseLifesteal**
-   **DamageMitigationPctOffsetPhysical**
-   **DamageMitigationPctOffsetTech**
-   **DamageMitigationPctOffsetMagic**
-   **PvPOffensePctOffset**
-   **PvPDefensePctOffset**
-   **ShieldTickTime**
-   **ShieldRebootTime**
-   **ScientistScanBotHealthRegenMultiplier**
-   **ScientistScanBotCooldownMultiplier**
-   **MountSpeedMultiplier**
-   **MoneyQuestMultiplier**
-   **XpQuestMultiplier**
-   **ReputationQuestMultiplier**
-   **PrestigeQuestMultiplier**
-   **NPCSpellExecutionFreqMultiplier**
-   **ResourceMax\_8**
-   **ResourceRegenMultiplier\_8**
-   **ResourceMax\_9**
-   **ResourceRegenMultiplier\_9**
-   **ResourceMax\_10**
-   **ResourceRegenMultiplier\_10**
-   **HealToShieldConversion**
-   **BaseGlanceAmount**
-   **BaseFocusPool**
-   **RatingFocusRecovery**
-   **RatingLifesteal**
-   **RatingMultiHitChance**
-   **AssaultRating**
-   **SupportRating**
-   **RatingCriticalMitigation**
-   **RatingIntensity**
-   **RatingVigor**
-   **RatingGlanceChance**
-   **RatingArmorPierce**
-   **RatingMultiHitAmount**
-   **RatingGlanceAmount**
-   **RatingDamageReflectAmount**
-   **RatingDamageReflectChance**
-   **RatingCCResilience**
-   **BaseFocusRecoveryInCombat**
-   **BaseFocusRecoveryOutofCombat**
-   **BaseMultiHitAmount**
-   **FocusCostModifier**
-   **BaseMultiHitChance**
-   **BaseDamageReflectAmount**
-   **BaseDamageReflectChance**
-   **BaseCriticalMitigation**
-   **BaseIntensity**
-   **BaseGlanceChance**
-   **FocusFinalMultiplier**
-   **BaseVigor**

------------------------------------------------------------------------

`Enum`

CodeEnumRank
------------

### Description

An enum representing the difficulty of an NPC in relation to other NPCs
of the same level

-   **Fodder**
-   **Minion**
-   **Standard**
-   **Champion**
-   **Superior**
-   **Elite**

------------------------------------------------------------------------

`Enum`

CodeEnumResourceConversionType
------------------------------

### Description

An enum representing the various types of resource conversion.
Item2Item: One type of item for another type\
Item2Rep: One type of item for reputation with a faction\
Prereq2Rep: ???

-   **Item2Item**
-   **Item2Rep**
-   **Prereq2Rep**

------------------------------------------------------------------------

`Enum`

CodeEnumRewardInfoType
----------------------

-   **Quest**
-   **Challenge**
-   **Explorer**
-   **Scientist**
-   **Soldier**
-   **Settler**
-   **PublicEvent**
-   **Rival**
-   **Friend**
-   **ScientistSpell**
-   **TSpell**
-   **Contract**

------------------------------------------------------------------------

`Enum`

CodeEnumSpellMechanic
---------------------

### Description

An enum representing the spell mechanics of each class

-   **None**
-   **Focus**
-   **MedicCore**
-   **Empathy**
-   **SpellSurge**
-   **Kinetic**
-   **Volatility**
-   **Unused03**

------------------------------------------------------------------------

`Enum`

CreatureRisk
------------

-   **Minor**
-   **Average**
-   **Major**

------------------------------------------------------------------------

`Event`

AttackMissed
------------

### Description

An event that is fired when a unit dodges an attack from another unit

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    performed the attack
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that was
    the target of the attack
-   **eMissType** **(Integer)** - An enum that describes why the attack
    missed. Uses the\
    GameLib.CodeEnumMissType enum list

------------------------------------------------------------------------

`Event`

DamageOrHealingDone (Deprecated)
--------------------------------

### Description

An event that gets fired whenever a unit takes damage or gets healed.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who used
    the spell that caused the damage/healing
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that
    received the damage/healing
-   **eDamageType** **(Integer)** - The type of damage done to the unit.
    This enum corresponds with\
    GameLib.CodeEnumDamageType
-   **nHealth** **(Integer)** - The amount of damage or healing done to
    the target's health
-   **nShields** **(Integer)** - The amount of damage or healing done to
    the target's shields
-   **nAbsorb** **(Integer)** - The amount of damage or healing done to
    the target's absorption
-   **bIsCritical** **(Boolean)** - Whether or not the attack was a
    critical hit
-   **splUsed** **([Spell](../Classes/Spell.md))** - The spell that did
    the damage / healing to the target

------------------------------------------------------------------------

`Event`

ExperienceGained
----------------

### Description

An event fired when a unit gains experience

### Params

-   **eReason** **(Integer)**
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that
    gained the experience
-   **strText** **(String)** - A localized string containing the amount
    of XP gained and any relevant notes\
    on why the unit gained the XP. Current modiefiers include "Bonus XP"
    for\
    killing clusters of NPCs, "Explorer's XP" for discovering new areas
    for the first\
    time, and Rested XP for XP gained while the user had the Rested
    bonus.
-   **nDelay** **(Integer)** - The delay before the unit gains XP from
    the event. This is usually set for\
    some time during an NPC's death animation.

------------------------------------------------------------------------

`Event`

InteractiveUnitChanged
----------------------

### Description

This event is fired when the player targets an interactive unit, such as
vendors, quest givers, and quest objective NPCs/props.

### Params

-   **unitNewTarget** **([Unit](../Classes/Unit.md))** - The
    interactive unit that the player is now targeting
-   **strContext** **(String)** - A brief description of how the player
    can interact with the unit

------------------------------------------------------------------------

`Event`

LootedItem (Deprecated)
-----------------------

### Description

This event is fired when the player loots an item that was dropped by an
NPC

### Params

-   **itemLoot** **([Item](../Classes/Item.md))** - The item that was
    looted
-   **nCount** **(Integer)** - The number of items in the stack that was
    looted

------------------------------------------------------------------------

`Event`

LootedMoney (Deprecated)
------------------------

### Description

This event is fired when the player loots currency that was dropped by
an NPC

### Params

-   **monLoot** **([Money](../Classes/Money.md))** - The currency that
    the player looted

------------------------------------------------------------------------

`Event`

Mount
-----

### Description

An event that gets fired when the player mounts or dismounts

### Params

-   **bMounted** **(Boolean)** - A boolean that states whether the
    player is mounting or dismounting

------------------------------------------------------------------------

`Event`

SpellCastFailed
---------------

### Description

An event that fires whenever a spell is canceled by any means

### Params

-   **eMessageType** **(Integer)** - An enum representing how long it
    will be before the unit can cast again.\
    This value is currently set to ECombatMessageType, which is not
    available to\
    the Lua API at the moment.
-   **eCastResult** **(Integer)** - An enum representing why the cast
    failed. This value uses the\
    ESpell4CastResult enum, which is not available to players at the
    moment.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The target of the
    failed spell
-   **unitSource** **([Unit](../Classes/Unit.md))** - The caster of the
    failed spell
-   **strMessage** **(String)** - A string describing why the spell
    failed
-   **strSpellName** **(string)** - The name of the spell that failed

------------------------------------------------------------------------

`Event`

TargetUnitChanged
-----------------

### Description

An event that is fired whenever the player changes their target

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit's new
    target

------------------------------------------------------------------------

`Event`

UnitActivationTypeChanged
-------------------------

### Description

An event that gets fired whenever the effect that happens when you
interact with the object changes.

### Params

-   **unitChanged** **([Unit](../Classes/Unit.md))** - The unit who has
    a new activation type

### Usage/Example

```lua
    Examples of when this event is fired include:
    - When a friendly player dies and can be revived by right clicking the corpse
    - When an object becomes interactive due to a quest or some other prerequisite
    - When an NPC offers a quest when they did not have one previously.
```

------------------------------------------------------------------------

`Event`

UnitCreated
-----------

### Description

An event that is fired whenever a unit is spawned or a player enters the
world

### Params

-   **unitSpawned** **([Unit](../Classes/Unit.md))** - The newly
    created unit

------------------------------------------------------------------------

`Event`

UnitDestroyed
-------------

### Description

An event that gets fired whenever a unit is despawned or a player leaves
the game world

### Params

-   **unitDestroyed** **([Unit](../Classes/Unit.md))** - The unit that
    has left this world

------------------------------------------------------------------------

`Event`

UnitEnteredCombat
-----------------

### Description

An event that gets fired whenever a unit enters or leaves combat

### Params

-   **unitInCombat** **([Unit](../Classes/Unit.md))** - The unit that
    just entered combat
-   **bInCombat** **(Boolean)** - A boolean stating whether or not the
    unit has entered or left combat

------------------------------------------------------------------------

`Event`

UnitMiniMapMarkerChanged
------------------------

### Description

An event that is fired whenever a player whose location shows on the
map/minimap moves

### Params

-   **unitMoving** **([Unit](../Classes/Unit.md))** - The unit who has
    changed position

------------------------------------------------------------------------

`Event`

UnitNameChanged
---------------

### Description

An event that gets fired whenever the unit's name gets changed

### Params

-   **unitChanged** **([Unit](../Classes/Unit.md))** - The unit whose
    name was changed
-   **strNewName** **(String)** - The unit's new name

------------------------------------------------------------------------

`Function`

GetVitalTable()
---------------

### Description

A function that returns a list of several of the character's vital
statistics. This table is indexed by the CodeEnumVital enum.

### Params

-   **Table** - A table containing a list of the character's vitals,
    sorted by index, using the values from CodeEnumVitals as indexes
    -   **Integer** - Some of the values are integers
    -   **String** - Others are strings
    -   **Float** - And others are floats

------------------------------------------------------------------------

`Function`

is()
----

------------------------------------------------------------------------

`Method`

\_\_eq() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

AddTextBubble()
---------------

### Description

Adds a text bubble above the unit with the specified text

### Params

-   **String** - The text to put in the text bubble

------------------------------------------------------------------------

`Method`

CanBeHarvestedBy(unitPlayer)
----------------------------

### Description

Returns whether or not the player can harvest the selected unit. Returns
false if the unit is not a harvestable unit.

### Params

-   **unitPlayer** **([Unit](../Classes/Unit.md))** - The function
    checks against this unit's tradeskills to see if the calling unit
    is\
    harvestable

### Return Value

-   **Boolean** - Whether or not the unit can be harvested by the unit
    that was passed in

------------------------------------------------------------------------

`Method`

CanGrantXp()
------------

------------------------------------------------------------------------

`Method`

CanUpgradeWarplotStructure()
----------------------------

### Description

Returns whether or not a character has permissions to upgrade a warplot
structure during a match

### Return Value

-   **Boolean** - Whether or not the player has permissions to upgrade
    structures

------------------------------------------------------------------------

`Method`

ClearTargetMarker()
-------------------

### Description

Removes a target marker from the unit

### Return Value

-   **Boolean** - Whether or not the function finished successfully

------------------------------------------------------------------------

`Method`

ConvertResource(idConversion)
-----------------------------

### Description

Perform this unit's resource conversion operation if it has one

### Params

-   **idConversion** **(Integer)** - The id number for the resource
    conversion. This value will generally come\
    from unit:GetResourceConversions()

------------------------------------------------------------------------

`Method`

CreatureRisk() (Deprecated)
---------------------------

------------------------------------------------------------------------

`Method`

FloatLootText(itemLooted, nCount)
---------------------------------

### Description

Spawns a floating display for the items the character loots

### Params

-   **itemLooted** **([Item](../Classes/Item.md))** - The item that was
    looted
-   **nCount** **(Integer)** - The number of items in the stack that was
    looted

------------------------------------------------------------------------

`Method`

GetAbsorptionMax()
------------------

### Description

Returns the current maximum absorption amount for the character.\
If the character has nothing giving them absorption, this returns 0.\
If the unit has no health bar, this returns nil.

### Return Value

-   **Integer** - The character's maximum absorption amount

------------------------------------------------------------------------

`Method`

GetAbsorptionValue()
--------------------

### Description

Returns the character's current absorption value. If the unit loses
whatever effect gave them absorption, this will return any unused
absorption even\
though the max absorption value is 0.

### Return Value

-   **Integer** - The character's current absorption value.

------------------------------------------------------------------------

`Method`

GetAchievementPoints() (Deprecated)
-----------------------------------

### Description

Returns the character's achievement points.

### Return Value

-   **Integer** - The number of achievement points the character has
    earned.

------------------------------------------------------------------------

`Method`

GetActivationState()
--------------------

### Description

Passes a table with information on whether a unit can be interacted
with, as well as who can interact with them.

### Return Value

-   **Table** - This table is indexed by CUnit's s\_ActivationInfo array
    -   **bActive** **(Boolean)**
    -   **bCanInteract** **(Boolean)** - Whether or not the player can
        interact with the unit
    -   **bUseableWhenDead** **(Boolean)** - Whether or not the unit can
        be interacted with when dead. This includes\
        dead players that can be revived
    -   **bUseableWhenHostile** **(Boolean)** - Pretty self explanitory,
        really
    -   **bShowCallout** **(Boolean)** - Whether the HUDAlert should be
        shown for the unit's interaction
    -   **bClickToMove** **(Boolean)**
    -   **bIsHighlightable** **(Boolean)**
    -   **bShowOverhead** **(Boolean)**
    -   **bUsePlayerPath** **(Boolean)** - The unit can only be
        interacted with by players with the appropriate path\
        if this is set to true

------------------------------------------------------------------------

`Method`

GetAffiliationName()
--------------------

### Description

Returns the name of the faction that the character is affiliated with

### Return Value

-   **String** - The name of the faction that the unit is affiliated
    with

------------------------------------------------------------------------

`Method`

GetAlternateTarget()
--------------------

### Description

Gets the unit's current focus target

### Return Value

-   **[Unit](../Classes/Unit.md)** - The unit currently set as the
    player's focus target

------------------------------------------------------------------------

`Method`

GetArchetype()
--------------

### Description

Returns an NPC's archetype

### Return Value

-   **Table**
    -   **idArchetype** **(Integer)** - An enum representing the NPC's
        archetype
    -   **strIcon** **(String)** - The name of the icon that corresponds
        with a particular archetype

------------------------------------------------------------------------

`Method`

GetArmorPierce()
----------------

------------------------------------------------------------------------

`Method`

GetArmorPierceRating()
----------------------

------------------------------------------------------------------------

`Method`

GetArmorPierceRatingPercent()
-----------------------------

------------------------------------------------------------------------

`Method`

GetAssaultAndSupportPowerSoftcap()
----------------------------------

### Description

Returns the softcap for Assault and Support power

### Return Value

-   **Integer** - The current softcap for both Assault and Support power

------------------------------------------------------------------------

`Method`

GetAssaultPower()
-----------------

### Description

Returns the player's current Assault Power

### Return Value

-   **Integer** - The player's Assault Power

------------------------------------------------------------------------

`Method`

GetAssaultRating()
------------------

------------------------------------------------------------------------

`Method`

GetAttachmentPosition(nAttachmentIdx)
-------------------------------------

### Description

Gets the position of the selected attachment

### Params

-   **nAttachmentIdx** **(Integer)** - The attachment you want to find
    the position for

### Return Value

-   **Table**
    -   **bFound** **(Boolean)** - Whether any attachment was found on
        the unit
    -   **tLocation** **(Table)** - The location of the attachment in x,
        y, z coordinates
        -   **x** **(Float)**
        -   **y** **(Float)**
        -   **z** **(Float)**

------------------------------------------------------------------------

`Method`

GetAuctionableItems()
---------------------

### Description

Gets a list of all the items the player can throw up on the Auction
House

### Return Value

-   **Array of itemSellable** - An array of items that the player is
    able to sell on the Auction House

------------------------------------------------------------------------

`Method`

GetBankItems()
--------------

------------------------------------------------------------------------

`Method`

GetBaseLifesteal() (Deprecated)
-------------------------------

### Description

Gets the unit's base life-steal amount

### Return Value

-   **Float** - The base amount of life-steal the unit has

------------------------------------------------------------------------

`Method`

GetBasicStats()
---------------

### Description

Returns a table containing a unit's most basic information

### Return Value

-   **Table**
    -   **strName** **(String)** - The unit's name
    -   **nLevel** **(Integer)** - The unit's true level. This value may
        be nil for some units
    -   **nEffectiveLevel** **(Integer)** - The unit's effective level.
        Effective level is only used when being leveled\
        down (mentoring) or leveled up (rallying). This value will be
        nil for units\
        without a modified level.
    -   **nHealth** **(Integer)** - The unit's current health. This
        value is nil for simple units.
    -   **nMaxHealth** **(Integer)** - The unit's max health. This value
        is nil for simple units.
    -   **bShouldShowDeathPenalty** **(Boolean)** - Whether or not the
        unit is affected by a death penalty timer
    -   **nPercentageOfDeathPenaltyTimer** **(Integer)** - The percent
        of the death penalty timer that is remaining for the unit
    -   **nDeathPenaltyMinutes** **(Integer)** - The minute value of the
        unit's remaining death penalty timer
    -   **nDeathPenaltySeconds** **(Integer)** - The seconds value of
        the unit's remaining death penalty timer. This value\
        only counts the seconds and only goes from 0-59
    -   **nResource0** **(Integer)** - The unit's current amount of
        Resource0
    -   **nResource0min** **(Integer)** - The minimum amount of
        Resource0 a unit can have
    -   **nResource0max** **(Integer)** - The maximum amount of
        Resource0 a unit can have
    -   **nResource1** **(Integer)** - The unit's current amount of
        Resource1
    -   **nResource1min** **(Integer)** - The minimum amount of
        Resource1 a unit can have
    -   **nResource1max** **(Integer)** - The maximum amount of
        Resource1 a unit can have
    -   **nResource2** **(Integer)** - The unit's current amount of
        Resource2
    -   **nResource2min** **(Integer)** - The minimum amount of
        Resource2 a unit can have
    -   **nResource2max** **(Integer)** - The maximum amount of
        Resource2 a unit can have
    -   **nResource3** **(Integer)** - The unit's current amount of
        Resource3
    -   **nResource3min** **(Integer)** - The minimum amount of
        Resource3 a unit can have
    -   **nResource3max** **(Integer)** - The maximum amount of
        Resource3 a unit can have
    -   **nResource4** **(Integer)** - The unit's current amount of
        Resource4
    -   **nResource4min** **(Integer)** - The minimum amount of
        Resource4 a unit can have
    -   **nResource4max** **(Integer)** - The maximum amount of
        Resource4 a unit can have
    -   **nResource5** **(Integer)** - The unit's current amount of
        Resource5
    -   **nResource5min** **(Integer)** - The minimum amount of
        Resource5 a unit can have
    -   **nResource5max** **(Integer)** - The maximum amount of
        Resource5 a unit can have
    -   **nResource6** **(Integer)** - The unit's current amount of
        Resource6
    -   **nResource6min** **(Integer)** - The minimum amount of
        Resource6 a unit can have
    -   **nResource6max** **(Integer)** - The maximum amount of
        Resource6 a unit can have
    -   **nResource7** **(Integer)** - The unit's current amount of
        Resource7
    -   **nResource7min** **(Integer)** - The minimum amount of
        Resource7 a unit can have
    -   **nResource7max** **(Integer)** - The maximum amount of
        Resource7 a unit can have

### Remarks

Resource0 = Endurance. Endurance is the resource used while sprinting.\
\
\
Resource1 = Kinetic Energy (Warriors), Volatility (Engineers), Psi
Points (Esper), Power Cores (Medic), and is not used for stalkers\
\
Resource2 - 3 = Unused\
Resource4 = Suit Power (stalkers)\
Resource5-7 = Unused\

------------------------------------------------------------------------

`Method`

GetBindPointString()
--------------------

### Description

Returns the name of the last place the character set their bind point.

### Return Value

-   **String** - The name of the character's current bind point

------------------------------------------------------------------------

`Method`

GetBuffs()
----------

### Description

Returns a table containing all of the positive and negative buffs on the
unit

### Return Value

-   **Table** - A table containing information on all of the positive
    and negative buffs on the unit
    -   **arHarmful** **(Array of Table)** - An array containing info on
        all of the debuffs on the unit
        -   **Table**
            -   **fTimeRemaining** **(Float)** - The amount of time (in seconds) left before the buff ends.
             -   **idBuff** **(Integer)** - The id number for the buff itself. This is not to be confused with the id number of the spell containing the buff's effect.
            -   **nCount** **(Integer)** - The number of stacks of a buff that are on the unit.
            -   **splEffect** **([Spell](../Classes/Spell.md))** - The spell containing the buff's effect.
            -   **strTooltip** **(String)** - Description of the buff or debuff.
            -   **unitCaster** **([Unit](../Classes/Unit.md))** - Source of the buff. Can be nil if the caster unit got destroyed.
            -   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that received the buff/debuff.
    -   **arBeneficial** **(Array of Table)** - An array containing info
        on all of the beneficial buffs on the unit
        -   **Table**
            -   **fTimeRemaining** **(Float)** - The amount of time (in seconds) left before the buff ends.
             -   **idBuff** **(Integer)** - The id number for the buff itself. This is not to be confused with the id number of the spell containing the buff's effect.
            -   **nCount** **(Integer)** - The number of stacks of a buff that are on the unit.
            -   **splEffect** **([Spell](../Classes/Spell.md))** - The spell containing the buff's effect.
            -   **strTooltip** **(String)** - Description of the buff or debuff.
            -   **unitCaster** **([Unit](../Classes/Unit.md))** - Source of the buff. Can be nil if the caster unit got destroyed.
            -   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that received the buff/debuff.

------------------------------------------------------------------------

`Method`

GetBuybackItems()
-----------------

### Description

Returns a list with info on the items that the players can buy back from
a vendor

### Return Value

-   **Array of Table**
    -   **idUnique** **(Integer)** - The unique ID of the item. This ID
        belongs to this one instance of the item.
    -   **idItem** **(Integer)** - The ID number of the item. Every copy
        of this item has the same ID for this value.
    -   **nStackSize** **(Integer)** - The number of instances of the
        item that can be bought back
    -   **nStockCount** **(Integer)** - The number of an item that the
        vendor has on them
    -   **bMeetsPrereq** **(Boolean)** - Whether or not the character
        can use the item
    -   **tPriceInfo** **(Table)**
        -   **nAmount1** **(Integer)** - The amount of the primary
            currency used to buy back the item
        -   **eCurrencyType1** **(Integer)** - The type of the primary
            currency used to purchase an item
        -   **eAltType1** **(Integer)** - The secondary type of currency
            that can be used to purchase the item
        -   **nAmount2** **(Integer)** - The amount of the second type
            of currency used to purchase an item
        -   **eCurrencyType2** **(Integer)** - The second type of
            currency used to purchase the item
        -   **eAltType2** **(Integer)** - The alternat form of currency
            that can be used for the secondary cost of the item
    -   **itemData** **([Item](../Classes/Item.md))** - The item that
        the player can buy back
    -   **arGlyphIds** **(Array of Integer)** - An array of ID numbers
        for the glyphs on the item (if there are any)
    -   **itemGlyphData** **(item)** - The glyph slots on the item, if
        any
    -   **itemModData** **([Item](../Classes/Item.md))** -
        Modifications to the item (if any)
    -   **strIcon** **(String)** - The string containing the icon name
    -   **strMaker** **(String)** - The name of the player that made the
        item

------------------------------------------------------------------------

`Method`

GetCastBarType()
----------------

### Description

Returns the player's current cast bar type from the
Unit.CodeEnumCastBarType table

### Return Value

-   **Integer** - The type of cast bar that should be displayed when the
    unit uses an ability

------------------------------------------------------------------------

`Method`

GetCastDuration()
-----------------

### Description

Returns the cast time of the spell that the unit is currently attempting
to cast. If no spell is being cast, this returns 0.

### Return Value

-   **Integer** - The cast time of the spell that the unit is currently
    attempting to cast (in milliseconds)

------------------------------------------------------------------------

`Method`

GetCastElapsed()
----------------

### Description

Returns the amount of time since the unit began to cast an ability. If
the unit is not currently casting an ability, this returns 0.

### Return Value

-   **Integer** - The amount of time since the the unit began to cast
    the ability (in milliseconds)

------------------------------------------------------------------------

`Method`

GetCastName()
-------------

### Description

Returns the name of the spell that the unit is currently casting.
Returns an empty string if the character is not casting.

### Return Value

-   **String** - Returns the name of the spell that the unit is casting.

------------------------------------------------------------------------

`Method`

GetCastTotalPercent()
---------------------

### Description

Returns the percentage of the cast time that has elapsed for the spell
that the unit is casting

### Return Value

-   **Integer** - The percentage of the cast time that is completed

------------------------------------------------------------------------

`Method`

GetCCDurationModifier()
-----------------------

### Description

Returns any modifiers to Crowd Control duration on the player.

### Return Value

-   **Integer** - The crowd control duration modifier on the player

------------------------------------------------------------------------

`Method`

GetCCDurationRatingPercent()
----------------------------

------------------------------------------------------------------------

`Method`

GetCCResilience()
-----------------

------------------------------------------------------------------------

`Method`

GetCCStateTimeRemaining()
-------------------------

### Description

Returns the remaining time that the unit is under crowd control effects

### Return Value

-   **Integer** - The remaining time the unit has to spend in a crowd
    control state (in milliseconds)

------------------------------------------------------------------------

`Method`

GetCCStateTotalTime()
---------------------

------------------------------------------------------------------------

`Method`

GetClassId()
------------

### Description

Returns the unit's class ID

### Return Value

-   **Integer** - The unit's class ID. This value corresponds with the
    GameLib.CodeEnumClass enum.

------------------------------------------------------------------------

`Method`

GetClusterContributionValue()
-----------------------------

------------------------------------------------------------------------

`Method`

GetClusterInformation()
-----------------------

### Description

Returns information on the cluster that the unit belongs to

### Return Value

-   **Table**
    -   **eDifficulty** **(Integer)** - The cluster's difficulty. This
        corresponds with the XXX enum
    -   **nCount** **(Integer)** - The number of units in the cluster
    -   **nIconCount** **(Integer)** - The number of enemies in the
        cluster
    -   **tUnits** **(Array of [Unit](../Classes/Unit.md))** - The
        units in the cluster

------------------------------------------------------------------------

`Method`

GetClusterUnits()
-----------------

### Description

Returns a list of units in the unit's cluster

### Return Value

-   **Array of [Unit](../Classes/Unit.md)** - An array of the units in
    the cluster

------------------------------------------------------------------------

`Method`

GetCommodityItems()
-------------------

### Description

Returns list of the player's commodity items. This does not work for
NPCs

### Return Value

-   **[Item](../Classes/Item.md)** - An array of commodity items in the
    player's inventory

------------------------------------------------------------------------

`Method`

GetConColor()
-------------

### Description

Returns a color that corresponds with the unit's difficulty in relation
to the player's.

### Return Value

-   **[CColor](../Classes/CColor.md)** - The color value representing
    the level difference between the player and the unit.

------------------------------------------------------------------------

`Method`

GetConValue()
-------------

### Description

Returns the integer representing the level difference between the player
and the unit

### Return Value

-   **Integer** - The integer representing the level difference between
    the player and the unit.\
    This value corresponds with the CodeEnumLevelDifferentialAttribute
    enum

------------------------------------------------------------------------

`Method`

GetCooldownReductionModifier()
------------------------------

### Description

The modifier that the unit's cooldowns are reduced by

### Return Value

-   **Integer** - The unit's cooldowns are reduced by this amount

------------------------------------------------------------------------

`Method`

GetCraftingStationTradeskills()
-------------------------------

### Description

Returns a list of tradeskills that can be used at this crafting station.
Returns nil if the unit is not a crafting station

### Return Value

-   **Array of Table** - This array will contain info on every
    tradeskill that can be used at this station
    -   **eTradeskillId** **(Integer)** - The ID number of the
        tradeskill. This value corresponds with the\
        CraftingLib.CodeEnumTradeskill enum
    -   **strName** **(String)** - The name of the tradeskill

------------------------------------------------------------------------

`Method`

GetCreatureRisk()
-----------------

------------------------------------------------------------------------

`Method`

GetCritChance()
---------------

### Description

Returns the chance that the unit's attacks will be a critical hit

### Return Value

-   **Float** - The chance that the unit's attacks will be a critical
    hit

------------------------------------------------------------------------

`Method`

GetCriticalMitigation()
-----------------------

------------------------------------------------------------------------

`Method`

GetCriticalMitigationRating()
-----------------------------

------------------------------------------------------------------------

`Method`

GetCriticalMitigationRatingPercent()
------------------------------------

------------------------------------------------------------------------

`Method`

GetCritRating()
---------------

------------------------------------------------------------------------

`Method`

GetCritRatingPercent()
----------------------

------------------------------------------------------------------------

`Method`

GetCritSeverity()
-----------------

### Description

Returns how much extra damage is done when one of the unit's abilities
lands a critical hit

### Return Value

-   **Float** - The amount of extra damage that is done when the unit
    lands a critical hit

------------------------------------------------------------------------

`Method`

GetCritSeverityRating()
-----------------------

------------------------------------------------------------------------

`Method`

GetCritSeverityRatingPercent()
------------------------------

------------------------------------------------------------------------

`Method`

GetCurrentWarplotTier()
-----------------------

### Description

Returns the tier of a Warplot plug. If this is called for any unit other
than a Warplot plug, this returns nil.

### Return Value

-   **Integer** - The current tier of a Warplot plug

------------------------------------------------------------------------

`Method`

GetCurrentWarplotUpgradeCost()
------------------------------

### Description

Returns the number of Nanopacks needed to upgrade the selected Warplot
plug. This returns nil if called from any unit that is not a Warplot
plug.

### Return Value

-   **Integer** - The number of Nanopacks needed to upgrade the selected
    Warplot plug.

------------------------------------------------------------------------

`Method`

GetDamageReflectAmount()
------------------------

------------------------------------------------------------------------

`Method`

GetDamageReflectAmountRating()
------------------------------

------------------------------------------------------------------------

`Method`

GetDamageReflectAmountRatingPercent()
-------------------------------------

------------------------------------------------------------------------

`Method`

GetDamageReflectChance()
------------------------

------------------------------------------------------------------------

`Method`

GetDamageReflectRating()
------------------------

------------------------------------------------------------------------

`Method`

GetDamageReflectRatingPercent()
-------------------------------

------------------------------------------------------------------------

`Method`

GetDeflectChance()
------------------

### Description

Returns the unit's chance to deflect attacks

### Return Value

-   **Float** - The unit's chance to deflect attacks

------------------------------------------------------------------------

`Method`

GetDeflectCritChance()
----------------------

### Description

The unit's chance to deflect critical hits

### Return Value

-   **Float** - The unit's chance to deflect critical hits

------------------------------------------------------------------------

`Method`

GetDeflectCritRating()
----------------------

------------------------------------------------------------------------

`Method`

GetDeflectCritRatingPercent()
-----------------------------

------------------------------------------------------------------------

`Method`

GetDeflectRating()
------------------

------------------------------------------------------------------------

`Method`

GetDeflectRatingPercent()
-------------------------

------------------------------------------------------------------------

`Method`

GetDifficulty()
---------------

### Description

Returns the difficulty of the cluster

### Return Value

-   **Integer** - The cluster's difficulty.

------------------------------------------------------------------------

`Method`

GetDispositionTo()
------------------

### Description

Returns a unit's disposition to another unit

### Params

-   **[Unit](../Classes/Unit.md)** - The unit that the calling unit is
    being compared to

### Return Value

-   **Integer** - A number representing the calling unit's disposition
    to another unit. This number correlates to\
    CodeEnumDisposition.

------------------------------------------------------------------------

`Method`

GetEffectiveItemLevel()
-----------------------

------------------------------------------------------------------------

`Method`

GetEliteness()
--------------

### Description

Returns an enum representing the unit's eliteness level

### Return Value

-   **Integer** - The unit's eliteness level. This number corresponds
    with CodeEnumEliteness

------------------------------------------------------------------------

`Method`

GetEquippedItems()
------------------

### Description

Returns an array containing all of the unit's equipped items.

### Return Value

-   **Array of [Item](../Classes/Item.md)** - An array of all of the
    items the unit has equipped

------------------------------------------------------------------------

`Method`

GetFacing()
-----------

### Description

Returns the direction the unit is facing, in x,y,z coordinates.

### Return Value

-   **Table**
    -   **x** **(Float)**
    -   **y** **(Float)**
    -   **z** **(Float)**

------------------------------------------------------------------------

`Method`

GetFaction()
------------

### Description

Gets the ID for the faction that the unit belongs to

### Return Value

-   **Unit.CodeEnumFaction** - The ID for the faction that the unit
    belongs to

### Usage/Example

```lua
    It's worth noting that the player's faction changes in certain PvP match types, such as Arenas and Hold the Line.
```

------------------------------------------------------------------------

`Method`

GetFlightPaths()
----------------

### Description

Returns a list of flight paths that are available from a Taxi NPC.
Returns nil if the unit isn't a Taxi NPC

### Return Value

-   **Array of Table** - An array containing information for each of the
    Taxi's connections.
    -   **idNode** **(Integer)** - The ID number for this flight path
    -   **eType** **(Integer)** - The flight path's type. This
        corresponds with the CodeEnumFlightPathType enum
    -   **strName** **(String)** - The name of the flight path
    -   **tLocation** **(Table)** - The destination's x, y, and z
        coordinates
        -   **x** **(Float)**
        -   **y** **(Float)**
        -   **z** **(Float)**

------------------------------------------------------------------------

`Method`

GetFlightPathToPoint()
----------------------

### Description

Returns a table containing the price of the flight and each node that
the path passes through

### Return Value

-   **Table**
    -   **tPriceInfo** **(Table)** - A table containing price
        information for the flight path
        -   **nAmount1** **(Integer)** - The cost of the flight path
        -   **eCurrencyType1** **(Integer)** - The primary currency type
            used to purchase the flight path. This value corresponds
            with\
            Money.CodeEnumCurrencyType enum
        -   **eAltType1** **(Integer)** - The alternate type of currency
            used to purchase the flight path. This value\
            corresponds with the Money.CodeEnumCurrencyType enum
        -   **nAmount2** **(Integer)** - The amount of alternate
            currency used to activate the flight path
        -   **eCurrencyType2** **(Integer)** - The type of currency used
            as an alternate way to activate the flight path.\
            This value corresponds with the Money.CodeEnumCurrencyType
            enum
        -   **eAltType2** **(Integer)** - The alternate type of currency
            used for the alternate purchase cost\
            for the flight path. This corresponds with the
            Money.CodeEnumCurrencyType enum
    -   **tRoute** **(Table)** - An array of node IDs that are
        accessible from the taxi
        -   **idNode** **(Integer)** - The ID number of the flight path

------------------------------------------------------------------------

`Method`

GetFocus()
----------

------------------------------------------------------------------------

`Method`

GetFocusCostModifier()
----------------------

------------------------------------------------------------------------

`Method`

GetFocusRegenInCombat()
-----------------------

------------------------------------------------------------------------

`Method`

GetFocusRegenNonCombat()
------------------------

------------------------------------------------------------------------

`Method`

GetFocusRegenRatingPercent()
----------------------------

------------------------------------------------------------------------

`Method`

GetGender()
-----------

### Description

Returns an integer representing the unit's gender.

### Return Value

-   **Integer** - Returns an integer representing the unit's gender.
    This corresponds with the CodeEnumGender enum

------------------------------------------------------------------------

`Method`

GetGlanceAmount()
-----------------

------------------------------------------------------------------------

`Method`

GetGlanceAmountRating()
-----------------------

------------------------------------------------------------------------

`Method`

GetGlanceAmountRatingPercent()
------------------------------

------------------------------------------------------------------------

`Method`

GetGlanceChance()
-----------------

------------------------------------------------------------------------

`Method`

GetGlanceRating()
-----------------

------------------------------------------------------------------------

`Method`

GetGlanceRatingPercent()
------------------------

------------------------------------------------------------------------

`Method`

GetGroupValue()
---------------

### Description

Returns the cluster's difficulty value

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Method`

GetGuildName()
--------------

### Description

Returns the unit's guild's name. Note that this will specifically get
the guild and not other guild types such as warparties, circles, or
arena teams.

### Return Value

-   **String** - The name of the player's guild

------------------------------------------------------------------------

`Method`

GetGuildType()
--------------

### Description

Returns the unit's guild type

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Method`

GetHarvestRequiredTradeskillName()
----------------------------------

### Description

Returns the name of the tradeskill required to harvest a node. Note,
some units are labeled as "Harvestable", but do not require a tradeskill
and generally\
do not provide materials.

### Return Value

-   **String** - The name of the tradeskill required to harvest the
    node.

------------------------------------------------------------------------

`Method`

GetHarvestRequiredTradeskillTier()
----------------------------------

### Description

Returns the tier of the tradeskill required to harvest a node. Note that
there are some nodes that are labeled as "Harvest", but do not require a
tradeskill.\
These nodes do not provide mats.

### Return Value

-   **Integer** - The tradeskill tier required to harvest the node

------------------------------------------------------------------------

`Method`

GetHeading()
------------

### Description

Returns the heading of the unit

### Return Value

-   **Float** - The heading of the unit in degrees.

------------------------------------------------------------------------

`Method`

GetHealth()
-----------

### Description

Returns the unit's current HP

### Return Value

-   **Integer** - The unit's current HP

------------------------------------------------------------------------

`Method`

GetId()
-------

### Description

Returns the unit's ID

### Return Value

-   **Integer** - The unit's ID

------------------------------------------------------------------------

`Method`

GetIgnoreArmorBase() (Deprecated)
---------------------------------

### Description

Returns unit's armor penetration percent

### Return Value

-   **Float** - The unit's armor penetration percent

------------------------------------------------------------------------

`Method`

GetIgnoreShieldBase()
---------------------

### Description

Returns the unit's shield penetration percent

### Return Value

-   **Float** - The unit's shield penetration percent

------------------------------------------------------------------------

`Method`

GetInfo()
---------

------------------------------------------------------------------------

`Method`

GetInstancePortalCompletionTime()
---------------------------------

### Description

Returns the expected completion time of the instance inside an instance
portal

### Return Value

-   **Integer** - The expected completion time of the instance, in
    minutes

------------------------------------------------------------------------

`Method`

GetInstancePortalLevelRange()
-----------------------------

### Description

Returns the level range for an instance inside an instance portal.
Returns nil if the unit is not an instance portal.

### Return Value

-   **Table**
    -   **nMinLevel** **(Integer)** - The minimum level for the instance
    -   **nMaxLevel** **(Integer)** - The maximum level for the
        instance. Players above this level will be\
        scaled to this level inside the instance

------------------------------------------------------------------------

`Method`

GetInstancePortalRemainingTime()
--------------------------------

### Description

The group's remaining time to finish an instance.

### Return Value

-   **Integer** - The group's remaining time to finish an instance, in
    seconds

------------------------------------------------------------------------

`Method`

GetIntensity()
--------------

------------------------------------------------------------------------

`Method`

GetIntensityRating()
--------------------

------------------------------------------------------------------------

`Method`

GetIntensityRatingPercent()
---------------------------

------------------------------------------------------------------------

`Method`

GetInterruptArmorMax()
----------------------

### Description

Returns the maximum amount of interrupt armor the unit can have

### Return Value

-   **Integer** - The maximum amount of interrupt armor for the unit

------------------------------------------------------------------------

`Method`

GetInterruptArmorValue()
------------------------

### Description

The amount of interrupt armor currently on the unit

### Return Value

-   **Integer** - The amount of interrupt armor currently on the unit

------------------------------------------------------------------------

`Method`

GetInventoryItems()
-------------------

### Description

Returns a list of the player's inventory items. Calling this on anyone
but the current player returns an empty table.

### Return Value

-   **Array of Table** - An array containing player's items and the
    corresponding bag slot that they are found in
    -   **nBagSlot** **(Integer)** - The bag slot where the item is
        found
    -   **itemInBag** **([Item](../Classes/Item.md))** - The item in
        the player's inventory

------------------------------------------------------------------------

`Method`

GetInventorySlotsInUseCount()
-----------------------------

------------------------------------------------------------------------

`Method`

GetLevel()
----------

### Description

Returns the unit's level

### Return Value

-   **Integer** - The unit's level

------------------------------------------------------------------------

`Method`

GetLevelDifferential(unitTarget)
--------------------------------

### Description

Returns an integer representing the unit's level differential with the
specified unit

### Params

-   **unitTarget** **(unit)** - The unit that the source unit is being
    compared to

### Return Value

-   **Integer** - An integer representing the level differential between
    the source unit and the target. This value\
    corresponds with the CodeEnumLevelDifferential enum

------------------------------------------------------------------------

`Method`

GetLevelString()
----------------

### Description

Returns a localized string that includes a label and the unit's
effective level

### Return Value

-   **String** - A string containing a label ("Level: " in English) and
    the unit's effective level

------------------------------------------------------------------------

`Method`

GetLifesteal()
--------------

------------------------------------------------------------------------

`Method`

GetLifestealRating()
--------------------

------------------------------------------------------------------------

`Method`

GetLifestealRatingPercent()
---------------------------

------------------------------------------------------------------------

`Method`

GetLoot()
---------

### Description

Returns a list of dropped loot that belongs to the player

### Return Value

-   **Array of Table** - There are multiple combinations of variables
    found in the table. Each combination is dependant on which\
    type
    -   **Table** - This contains all of the variables for items that
        can be looted
        -   **nCount** **(Integer)** - The amount of items looted in
            this indivudal drop
        -   **itemLoot** **([Item](../Classes/Item.md))** - The item
            that was dropped
        -   **itemModData** **([Item](../Classes/Item.md))** - The mod
            data for the item that was dropped. Note that not every
            item\
            will have this variable
        -   **itemSigilData** **([Item](../Classes/Item.md))** - The
            sigil data for the item that was dropped. Note that not
            every item will\
            have sigil data.
    -   **Table** - This table contains all the variables for money loot
        drops
        -   **monCurrency** **([Money](../Classes/Money.md))** -
            Currency that was dropped.
    -   **Table** - This table contains all the variables for virtual
        items that are looted
        -   **strName** **(String)** - The name of the virtual item
        -   **strFlavor** **(String)** - The flavor text for the virtual
            item
        -   **nCount** **(Integer)** - The number of the virtual item
            that will be picked up in this individual drop
        -   **strIcon** **(String)** - The string name for the icon used
            for the virtual item
        -   **eType** **(Integer)** - The virtual item's type. This
            value corresponds with the &gt;&gt;&gt;&gt; enum
    -   **Table** - This table contains all the variables for spell
        effects that are dropped, such as\
        from Scientist scans.
        -   **tAbility** **(Table)** - Information on the skill that is
            picked up.
            -   **strName** **(String)** - The name of the spell
            -   **strDescription** **(String)** - The description of the
                spell
            -   **strButtonIcon** **(String)** - The string for the
                spell's icon

------------------------------------------------------------------------

`Method`

GetMagicMitigation()
--------------------

### Description

Returns the unit's magic resistance

### Return Value

-   **Float** - The percentage of magic abilities that are mitigated by
    the unit

------------------------------------------------------------------------

`Method`

GetMagicMitigationRating()
--------------------------

------------------------------------------------------------------------

`Method`

GetMagicMitigationRatingPercent()
---------------------------------

------------------------------------------------------------------------

`Method`

GetMana() (Deprecated)
----------------------

### Description

Returns the unit's current amount of mana

### Return Value

-   **Float** - The unit's current amount of mana

------------------------------------------------------------------------

`Method`

GetManaCostModifier() (Deprecated)
----------------------------------

### Description

Returns the current modifier to the mana cost of the unit's abilities

### Return Value

-   **Float** - The modifier to the mana cost of the unit's abilities

------------------------------------------------------------------------

`Method`

GetManaRegenInCombat() (Deprecated)
-----------------------------------

### Description

Returns the amount of Focus the unit regens during combat

### Return Value

-   **Float** - The amount of Focus the unit regens in combat

------------------------------------------------------------------------

`Method`

GetManaRegenNonCombat() (Deprecated)
------------------------------------

### Description

The amount of Focus the unit regens outside of combat

### Return Value

-   **Float** - The amount of Focus the unit regens outside of combat

------------------------------------------------------------------------

`Method`

GetMaxFocus()
-------------

------------------------------------------------------------------------

`Method`

GetMaxHealth()
--------------

### Description

Returns the unit's maximum health

### Return Value

-   **Integer** - The unit's maximum health

------------------------------------------------------------------------

`Method`

GetMaxMana() (Deprecated)
-------------------------

### Description

Returns the unit's maximum Focus

### Return Value

-   **Integer** - The unit's maximum Focus

------------------------------------------------------------------------

`Method`

GetMaxResource(iResource)
-------------------------

### Description

The maximum value for the specified resource

### Params

-   **iResource** **(Integer)** - An integer representing the various
    resources.\
    \
    0 = Endurance. Endurance is the resource used while sprinting.\
    \
    1 = Kinetic Energy (Warriors), Volatility (Engineers), Psi Points
    (Esper), Power Cores (Medic), and is not used for stalkers\
    \
    \
    2 - 3 = Unused\
    \
    4 = Suit Power (stalkers) 5-7 = Unused\

### Return Value

-   **Integer** - The maximum value for the specified resource

------------------------------------------------------------------------

`Method`

GetMiniMapMarker() (Deprecated)
-------------------------------

### Description

Returns the name for the character's marker on the minimap

### Return Value

-   **String** - A string representing the character's position on the
    minimap

------------------------------------------------------------------------

`Method`

GetMiniMapMarkers()
-------------------

------------------------------------------------------------------------

`Method`

GetMinResource(iResource)
-------------------------

### Description

Returns the minimum amount of the given resource that the unit can have

### Params

-   **iResource** **(Integer)** - An integer representing the various
    resources.\
    \
    0 = Endurance. Endurance is the resource used while sprinting.\
    \
    1 = Kinetic Energy (Warriors), Volatility (Engineers), Psi Points
    (Esper), Power Cores (Medic), and is not used for stalkers\
    \
    \
    2 - 3 = Unused\
    \
    4 = Suit Power (stalkers) 5-7 = Unused\

### Return Value

-   **Integer** - The minimum amount of a given resource that the unit
    can have

------------------------------------------------------------------------

`Method`

GetMountHealth()
----------------

### Description

Returns the current health of the mount that the unit is riding

### Return Value

-   **Integer** - The current health of the omount that the unit is
    riding

------------------------------------------------------------------------

`Method`

GetMountMaxHealth()
-------------------

### Description

The maximum health of the mount that the unit is riding

### Return Value

-   **Integer** - The maximum health of the mount that the unit is
    riding

------------------------------------------------------------------------

`Method`

GetMouseOverType()
------------------

### Description

Returns a string describing the unit's target frame type

### Return Value

-   **String** - Returns "Simple" for units that have no HP and cannot
    be attacked or "Normal" for the rest

------------------------------------------------------------------------

`Method`

GetMultiHitAmount()
-------------------

------------------------------------------------------------------------

`Method`

GetMultiHitAmountRating()
-------------------------

------------------------------------------------------------------------

`Method`

GetMultiHitAmountRatingPercent()
--------------------------------

------------------------------------------------------------------------

`Method`

GetMultiHitChance()
-------------------

------------------------------------------------------------------------

`Method`

GetMultiHitRating()
-------------------

------------------------------------------------------------------------

`Method`

GetMultiHitRatingPercent()
--------------------------

------------------------------------------------------------------------

`Method`

GetName()
---------

### Description

Returns the name of the unit

### Return Value

-   **String** - The unit's name

------------------------------------------------------------------------

`Method`

GetNameplateColor()
-------------------

### Description

Returns an ApolloColor for the unit's nameplate

### Return Value

-   **[ApolloColor](../Classes/ApolloColor.md)** - The current color of
    the unit's nameplate

------------------------------------------------------------------------

`Method`

GetOverheadAnchor()
-------------------

### Description

Returns a table with the x, y, and z positions for the unit's nameplate
(in relation to the model)

### Return Value

-   **Table** - A table containing the x, y, and z positions for the
    unit's nameplate
    -   **x** **(Integer)**
    -   **y** **(Integer)**
    -   **z** **(Integer)**

------------------------------------------------------------------------

`Method`

GetPhysicalMitigation()
-----------------------

### Description

Returns the unit's physical mitigation percent

### Return Value

-   **Float** - The percent of physical damage that is mitigated by the
    unit

------------------------------------------------------------------------

`Method`

GetPhysicalMitigationRating()
-----------------------------

------------------------------------------------------------------------

`Method`

GetPhysicalMitigationRatingPercent()
------------------------------------

------------------------------------------------------------------------

`Method`

GetPlayerMovementSpeed()
------------------------

------------------------------------------------------------------------

`Method`

GetPlayerPathType()
-------------------

### Description

Returns the unit's path. If the unit is not a player, returns nil.

### Return Value

-   **Integer** - A number representing the unit's path. This value
    corresponds with the\
    PlayerPathLib.PlayerPathType int constants.

------------------------------------------------------------------------

`Method`

GetPosition()
-------------

### Description

Returns a table with the unit's position in x, y, and z coordinates

### Return Value

-   **Table** - The unit's position in x, y, and z coordinates
    -   **x** **(Float)**
    -   **y** **(Float)**
    -   **z** **(False)**

------------------------------------------------------------------------

`Method`

GetPrereqInfo(idPrereq)
-----------------------

### Description

Validates that the player meets the prerequisites for an item and
returns a table with the results

### Params

-   **idPrereq** **(Integer)** - The ID number for the item whose
    prerequisites are being checked

### Return Value

-   **Table**
    -   **bIsMet** **(Boolean)** - Whether or not the unit meets the
        prerequisites
    -   **strText** **(String)** - A string containing the prerequisite
        for the item

------------------------------------------------------------------------

`Method`

GetPvPDamageI()
---------------

------------------------------------------------------------------------

`Method`

GetPvPDamageO()
---------------

------------------------------------------------------------------------

`Method`

GetPvPDefenseI()
----------------

------------------------------------------------------------------------

`Method`

GetPvPDefenseO()
----------------

------------------------------------------------------------------------

`Method`

GetPvPDefensePercent()
----------------------

### Description

Returns the percent of damage that is mitigated during PvP

### Return Value

-   **Float** - The percent of damage that is mitigated during PvP

------------------------------------------------------------------------

`Method`

GetPvPDefenseRating()
---------------------

### Description

Returns the unit's PvP Defense Rating

### Return Value

-   **Float** - The unit's PvP Defense Rating

------------------------------------------------------------------------

`Method`

GetPvPDefenseRatingPercent()
----------------------------

------------------------------------------------------------------------

`Method`

GetPvPHealingI()
----------------

------------------------------------------------------------------------

`Method`

GetPvPHealingO()
----------------

------------------------------------------------------------------------

`Method`

GetPvPOffensePercent()
----------------------

### Description

Returns the percent of extra damage the player does in PvP

### Return Value

-   **Float** - The percent of extra damage the unit does in PvP

------------------------------------------------------------------------

`Method`

GetPvPOffenseRating()
---------------------

### Description

Returns the unit's PvP Offense Rating

### Return Value

-   **Float** - The unit's PvP Offense Rating

------------------------------------------------------------------------

`Method`

GetPvPOffenseRatingPercent()
----------------------------

------------------------------------------------------------------------

`Method`

GetRaceId()
-----------

### Description

Returns a number representing the unit's race

### Return Value

-   **Integer** - A number representing the unit's race. This value
    corresponds with the GameLib.CodeEnumRace enum

------------------------------------------------------------------------

`Method`

GetRank()
---------

### Description

Returns an integer representing the unit's difficulty rank

### Return Value

-   **Integer** - An integer representing the unit's difficulty rank.
    This value corresponds with the\
    Unit.CodeEnumRank enum

------------------------------------------------------------------------

`Method`

GetRechargeableItems()
----------------------

------------------------------------------------------------------------

`Method`

GetRepairableItems()
--------------------

### Description

Returns a list with information on the items that the unit owns that can
be repaired

### Return Value

-   **Array of Table**
    -   **idLocation** **(Integer)** - The item's location in the
        character's inventory or equipment
    -   **idItem** **(Integer)** - The item's id number
    -   **nStackSize** **(Integer)** - The number of items in the stack
    -   **nStockCount** **(Integer)** - The number of the item the
        vendor has in stock
    -   **bMeetsPrereq** **(Boolean)** - Whether or not the unit meets
        the prerequisites to equip the item. For\
        the sake of this function, this value will always be true.
    -   **tPriceInfo** **(Table)** - The cost of repairing the item
        -   **nAmount1** **(Integer)** - The primary cost of repairing
            the item
        -   **eCurrencyType1** **(Integer)** - The primary type of
            currency used to repair the item. This value\
            corresponds with the Money.CodeEnumCurrencyType enum
        -   **eAltType1** **(Integer)** - The primary alternate form of
            currency used for repairing the item. This\
            value corresponds with the Money.CodeEnumCurrencyType enum
        -   **nAmount2** **(Integer)** - The secondary cost of repairing
            the item
        -   **eCurrencyType2** **(Integer)** - The secondary type of
            currency used to repair the item
        -   **eAltType2** **(Integer)** - The secondary alternate form
            of currency used to repair the item. This\
            value corresponds with the Money.CodeEnumCurrencyType enum
    -   **itemData** **([Item](../Classes/Item.md))** - The item
        needing repairs
    -   **strIcon** **(String)** - The name of the item's icon
    -   **strName** **(String)** - The item's name

------------------------------------------------------------------------

`Method`

GetRepTurninItems()
-------------------

### Description

Returns information on what items the player is carrying that can count
as reputation for the given unit's faction

### Return Value

-   **Array of Table** - An array containing information on each of the
    items that the player is holding that can be turned in for
    reputation
    -   **idRep** **(Integer)** - The faction the player would gain
        reputation with
    -   **nRepAmount** **(Integer)** - The amount of reputation the item
        is worth
    -   **itemRequired** **([Item](../Classes/Item.md))** - The item
        that can be turned in for reputation

------------------------------------------------------------------------

`Method`

GetResource(nResource)
----------------------

### Description

Returns the amount of the specified resource that the unit has

### Params

-   **nResource** **(Integer)** - The Resource number that the player is
    polling

### Return Value

-   **Integer** - The amount of the given resource that the unit has

### Remarks

Resource0 = Endurance. Endurance is the resource used while sprinting.\
\
\
Resource1 = Kinetic Energy (Warriors), Volatility (Engineers), Psi
Points (Esper), Power Cores (Medic), and is not used for stalkers\
\
Resource2 - 3 = Unused\
Resource4 = Suit Power (stalkers)\
Resource5-7 = Unused\

------------------------------------------------------------------------

`Method`

GetResourceConversions()
------------------------

### Description

Returns a list of resource conversions that the unit is able to perform.
If the unit is not able to perform resource conversions, this returns
nil.

### Return Value

-   **Array of Table** - An array containing each of the conversions
    available through the NPC
    -   **idConversion** **(Integer)** - The ID number for this
        conversion type
    -   **itemSource** **([Item](../Classes/Item.md))** - The item the
        player needs to trade in this conversion. This value does\
        not exist for conversions that do not require items
    -   **idSource** **(Integer)** - The ID number for the object that
        can be converted into reputation. This\
        value does not exist if the conversion requires items
    -   **nSourceCount** **(Integer)** - The number of the object
        required for the conversion
    -   **nAvailableCount** **(Integer)** - The number of the object
        required for the conversion that are in the player's inventory
    -   **eType** **(Integer)** - The type of conversion. This value
        corresponds with the\
        Unit.CodeEnumResourceConversionType enum
    -   **itemTarget** **([Item](../Classes/Item.md))** - The item that
        is given to the player by the conversion. This variable only
        exists if the conversion gives items
    -   **idTarget** **(Integer)** - The ID number of the faction who
        the player gains reputation with through this conversion. This
        value does not exist if the conversion does not grant reputation
    -   **strName** **(String)** - The name of the faction that the
        player gains reputation with through the conversion. This
        variable does not exist if the conversion does not grant
        reputation
    -   **nTargetCount** **(Integer)** - The amount of the reward that
        is granted to the player through this conversion

------------------------------------------------------------------------

`Method`

GetResourceIcon(nResource)
--------------------------

### Description

Returns the name of a resource's icon

### Params

-   **nResource** **(Integer)** - The Resource being polled.

### Return Value

-   **String** - The name of the given resource's icon.

### Remarks

Resource0 = Endurance. Endurance is the resource used while sprinting.\
\
\
Resource1 = Kinetic Energy (Warriors), Volatility (Engineers), Psi
Points (Esper), Power Cores (Medic), and is not used for stalkers\
\
Resource2 - 3 = Unused\
Resource4 = Suit Power (stalkers)\
Resource5-7 = Unused\

------------------------------------------------------------------------

`Method`

GetResourceTooltip(nResource)
-----------------------------

### Description

Returns the tooltip string for the given resource

### Params

-   **nResource** **(Integer)** - The resource being polled for its
    tooltip

### Return Value

-   **String** - The tooltip string for the given resource

### Remarks

Resource0 = Endurance. Endurance is the resource used while sprinting.\
\
\
Resource1 = Kinetic Energy (Warriors), Volatility (Engineers), Psi
Points (Esper), Power Cores (Medic), and is not used for stalkers\
\
Resource2 - 3 = Unused\
Resource4 = Suit Power (stalkers)\
Resource5-7 = Unused\

------------------------------------------------------------------------

`Method`

GetRewardInfo()
---------------

### Description

Returns a table containing information on all of the active quests,
missions, challenges, and public events that this unit is the target of

### Return Value

-   **Array of Table** - An array containing information on each thing
    that the unit is the objective of. Each type has its own variables.
    -   **Table** - If the unit is part of a mission objective, this
        table will be one of the ones returned
        -   **strType** **(String)** - The type of objective contained
            in this table
        -   **idQuest** **(Integer)** - The ID number of the quest that
            the unit is a target of
        -   **strTitle** **(String)** - The name of the quest that the
            unit is a target of
        -   **nCompleted** **(Integer)** - The number of the unit that
            has been killed for the quest or the percentage of
            completion that the player has reached
        -   **nNeeded** **(Integer)** - The number of the unit that the
            player needs to interact with for the quest. If nCompleted
            is a percent, then this value is 100.
        -   **splAbility** **([Spell](../Classes/Spell.md))** - A spell
            granted for use in the quest
        -   **splObjective** **([Spell](../Classes/Spell.md))** - A
            spell that needs to be used as one of the objectives of the
            quest
        -   **bShowCount** **(Boolean)** - Whether or not the number
            interacted with and required should be shown
    -   **Table** - If the unit is part of a challenge, then the table
        will use these values
        -   **strType** **(String)** - The type of objective. In this
            case, the value is "Challenge"
        -   **idChallenge** **(Integer)** - The ID number of the
            challenge that the unit is the target of
        -   **strTitle** **(String)** - The name of the challenge
            targeting the unit
        -   **nCompleted** **(Integer)** - The number of the unit that
            has been interacted with for the challenge
        -   **nNeeded** **(Integer)** - The number of the unit that the
            player must interact with for the challenge
    -   **Table** - If the unit is the target of a public event, the
        table will look like this
        -   **strType** **(String)** - The type of objective that the
            unit is a part of. In this case, the value is "PublicEvent"
        -   **peoObjective** **(Public Event Objective)** - The specific
            Public Event Objective that the unit is the target of
    -   **Table** - If the unit is the target of a path mission, the
        table will look like this
        -   **strType** **(String)** - The type of mission that the unit
            is the target of. This may be either "Scientist", "Soldier",
            or "Explorer" in this case
        -   **pmMission**
            **([PathMission](../Classes/PathMission.md))** - The
            PathMission that the unit is the target of
        -   **splReward** **([Spell](../Classes/Spell.md))** - Any
            spell tied to interacting with the unit, such as drops from
            scanning the unit with a Scientist or items tied to the
            mission that the player needs to use on the unit
        -   **bIsActivated** **(Boolean)** - Whether or not the player
            has interacted with the object that starts the mission. This
            value only exists for Soldier missions

------------------------------------------------------------------------

`Method`

GetSettlerImprovementInfo()
---------------------------

### Description

Returns information on Settler Improvements. Returns an empty table if
the unit is not a Settler Improvment

### Return Value

-   **Table**
    -   **arOwnerNames** **(Array of String)** - A list of the people
        who help build and maintain this improvement
    -   **bIsInfiniteDuration** **(Boolean)** - Whether or not the
        improvement lasts forever
    -   **nRemainingTime** **(Integer)** - Returns the remaining
        duration on the improvement in seconds
    -   **arTiers** **(Array of Table)** - A list of the various tiers
        of the improvement
        -   **strName** **(String)** - The name of this tier of the
            improvement
        -   **nTier** **(Integer)** - The tier number

------------------------------------------------------------------------

`Method`

GetSettlerRewardName()
----------------------

------------------------------------------------------------------------

`Method`

GetShieldCapacity()
-------------------

### Description

Returns the unit's current shield value

### Return Value

-   **Integer** - The unit's current shield value

------------------------------------------------------------------------

`Method`

GetShieldCapacityMax()
----------------------

### Description

Returns the unit's maximum shield value

### Return Value

-   **Integer** - The unit's maximum shield value

------------------------------------------------------------------------

`Method`

GetShieldMitigationPct()
------------------------

------------------------------------------------------------------------

`Method`

GetShieldRebootTime()
---------------------

### Description

Returns the amount of time the unit needs to go without taking damage
before their shields start to regenerate

### Return Value

-   **Float** - The amount of time between shield regen tics

------------------------------------------------------------------------

`Method`

GetShieldRegenPct()
-------------------

### Description

Returns the percent of the unit's maximum shields that are regenerated
each tic

### Return Value

-   **Float** - The percent of the unit's maximum shields that are
    regenerated each tic

------------------------------------------------------------------------

`Method`

GetShieldTickTime()
-------------------

### Description

Returns the intervals at which the unit's shields regenerate, in seconds

### Return Value

-   **Float** - The intervals at which the unit's shields regenerate, in
    seconds.

------------------------------------------------------------------------

`Method`

GetSpellMechanicId()
--------------------

### Description

Returns the unit's spell mechanic ID number

### Return Value

-   **Integer** - The unit's spell mechanic ID number

------------------------------------------------------------------------

`Method`

GetSpellMechanicPercentage(nResource)
-------------------------------------

### Description

Returns the percentage of the given resource the unit has.

### Params

-   **nResource** **(Integer)** - The resource that is being polled

### Return Value

-   **Float** - The percentage of the given resource the unit has

### Remarks

Resource0 = Endurance. Endurance is the resource used while sprinting.\
\
\
Resource1 = Kinetic Energy (Warriors), Volatility (Engineers), Psi
Points (Esper), Power Cores (Medic), and is not used for stalkers\
\
Resource2 - 3 = Unused\
Resource4 = Suit Power (stalkers)\
Resource5-7 = Unused\

------------------------------------------------------------------------

`Method`

GetStandState()
---------------

### Description

Returns the unit's stand state

### Return Value

-   **String** - The unit's stand state.

### Remarks

The states this function can return are "Stand", "Sit", "LyingDown",
"State0", "State1", "State2", "Looting", "Emote", "StillPose",
"DeathPose", "Burrowed", "State3", "Chair", "Mannequin"

------------------------------------------------------------------------

`Method`

GetStrikethroughChance()
------------------------

### Description

Returns the unit's strikethrough chance

### Return Value

-   **Float** - The percent chance the unit has to not have the target
    deflect the attack

------------------------------------------------------------------------

`Method`

GetStrikethroughRating()
------------------------

------------------------------------------------------------------------

`Method`

GetStrikethroughRatingPercent()
-------------------------------

------------------------------------------------------------------------

`Method`

GetSupplySatchelItems()
-----------------------

### Description

Returns a list of items and information on the contents of the player's
Supply Satchel. Note, this returns an empty table if this is called on
someone other than the player

### Return Value

-   **Array of Table**
    -   **idLocation** **(Integer)** - The item's location in the Supply
        Satchel
    -   **itemMaterial** **([Item](../Classes/Item.md))** - The item
        itself
    -   **nCount** **(Integer)** - The amount of the item that the
        player owns

------------------------------------------------------------------------

`Method`

GetSupportPower()
-----------------

### Description

Returns the unit's support power

### Return Value

-   **Float** - The unit's support power

------------------------------------------------------------------------

`Method`

GetSupportRating()
------------------

------------------------------------------------------------------------

`Method`

GetTarget()
-----------

### Description

Returns the unit's current target

### Return Value

-   **[Unit](../Classes/Unit.md)** - The unit's current target

------------------------------------------------------------------------

`Method`

GetTargetMarker()
-----------------

### Description

Returns a number representing the target marker on the unit

### Return Value

-   **Integer** - A number representing the target marker on the unit

------------------------------------------------------------------------

`Method`

GetTargetOfTarget()
-------------------

### Description

Returns the target of the unit being targeted by the calling unit

### Return Value

-   **[Unit](../Classes/Unit.md)** - The target of the unit being
    targeted by the calling unit

------------------------------------------------------------------------

`Method`

GetTechMitigation()
-------------------

### Description

Returns the percent of tech damage that is mitigated by the unit

### Return Value

-   **Float** - The percent of tech damage that is mitigated by the unit

------------------------------------------------------------------------

`Method`

GetTechMitigationRating()
-------------------------

------------------------------------------------------------------------

`Method`

GetTechMitigationRatingPercent()
--------------------------------

------------------------------------------------------------------------

`Method`

GetTitle()
----------

### Description

Returns the title that the unit is displaying

### Return Value

-   **String** - The title that the unit is displaying

------------------------------------------------------------------------

`Method`

GetTitleOrName()
----------------

### Description

If the unit has a title set, this returns it. If it doesn't, this
returns the name of the unit

### Return Value

-   **String** - The title of the unit if it has one set. The name of
    the unit if it doesn't.

------------------------------------------------------------------------

`Method`

GetTrainerTradeskills()
-----------------------

### Description

Returns a list of tradeskills available at the trainer. If the unit is
not a tradeskill trainer, this returns nil.

### Return Value

-   **Array of Table** - The name and ID of each tradeskill available
    -   **eTradeskillId** **(Integer)** - The ID number of the
        tradeskill. This number corresponds with the
        CraftingLib.CodeEnumTradeskill
    -   **strName** **(String)** - The name of the tradeskill

------------------------------------------------------------------------

`Method`

GetTransferDestination()
------------------------

### Description

Returns the destination of a taxi route that transfers the player to
another zone

### Return Value

-   **String** - The name of the destination

------------------------------------------------------------------------

`Method`

GetType()
---------

### Description

Returns the unit's type

### Return Value

-   **String** - The unit's type

### Remarks

There are several possible values that can be returned here, such as\
"NonPlayer",\
"Chest",\
"Destructible",\
"Vehicle",\
"Door",\
"Harvest",\
"Corpse",\
"Mount",\
"Collectible",\
"Taxi",\
"Simple",\
"Platform",\
"Mailbox",\
"Turret",\
"InstancePortal",\
"Plug",\
"Residence",\
"StructuredPlug",\
"PinataLoot",\
"BindPoint",\
"Player",\
"HiddenSpell",\
"Trigger",\
"Ghost",\
"Pet",\
"Esper Pet",\
"World object",\
"Scanner",\
"Camera",\
"Trap",\
"DestructibleDoor",\
"Pickup",\
"SimpleCollidable",\
"HousingMannequin",\
and "Unknown"

------------------------------------------------------------------------

`Method`

GetUnitMount()
--------------

### Description

Returns the unit's mount

### Return Value

-   **[Unit](../Classes/Unit.md)** - The unit's current mount

------------------------------------------------------------------------

`Method`

GetUnitOwner()
--------------

### Description

Returns the owner of a pet.

### Return Value

-   **[Unit](../Classes/Unit.md)** - The unit who owns the pet

------------------------------------------------------------------------

`Method`

GetUnitProperties()
-------------------

### Description

Returns a table with information on each of the unit's properties

### Return Value

-   **Array of Table**
    -   **idProperty** **(Integer)** - The id number for the property
    -   **fValue** **(Float)** - The value of the property for the unit
    -   **fBase** **(Float)** - The unit's base value for the property
    -   **strDisplayName** **(String)** - The name of the property
    -   **nTooltipDisplayOrder** **(Integer)** - Where this property
        should be displayed in item tooltips, with lower numbers being
        towards the top of the tooltip

------------------------------------------------------------------------

`Method`

GetUnitProperty(eProperty)
--------------------------

### Description

Returns information on the specified property for the unit

### Params

-   **eProperty** **(Integer)** - This value corresponds with the
    Unit.CodeEnumProperties table

### Return Value

-   **Table**
    -   **idProperty** **(Integer)** - The ID number of the property
    -   **fValue** **(Float)** - The unit's current value for the
        property
    -   **fBase** **(Float)** - The unit's base value for the property
    -   **strDisplayName** **(String)** - The name of the property
    -   **nTooltipDisplayOrder** **(Integer)** - Where this should be
        displayed on item tooltips. Lower values should be shown towards
        the top

------------------------------------------------------------------------

`Method`

GetUnitRaceId()
---------------

### Description

Returns the ID number for the unit's race

### Return Value

-   **Integer** - The race's ID number. This value corresponds with the
    GameLib.CodeEnumRace enum

------------------------------------------------------------------------

`Method`

GetVehicle()
------------

### Description

Returns the vehicle the unit is currently riding

### Return Value

-   **[Unit](../Classes/Unit.md)** - The vehicle that the unit is
    riding

------------------------------------------------------------------------

`Method`

GetVendorGroups()
-----------------

### Description

Returns a table with item categories for a vendor. If this unit is not a
vendor, this table is empty

### Return Value

-   **Array of Table**
    -   **idGroup** **(Integer)** - The group's ID number
    -   **strName** **(String)** - The group's name

------------------------------------------------------------------------

`Method`

GetVendorItems()
----------------

### Description

Returns an array containing information on each item the vendor sells

### Return Value

-   **Array of Table**
    -   **idUnique** **(Integer)** - The unique ID for the item
    -   **idItem** **(Integer)** - The static ID number for the item
    -   **eType** **(Integer)** - The type of thing being purchased.
        This value corresponds with the\
        CodeEnumLootItemType enum.
    -   **nStackSize** **(Integer)** - The number of items that are
        purchased at once
    -   **nStockCount** **(Integer)** - The number of the item that the
        vendor has in stock.
    -   **bMeetsPrereq** **(Boolean)** - Whether or not the player meets
        the prerequisites to use the item
    -   **idPrereq** **(Integer)** - An id representing the set of
        prerequisites needed to use the item
    -   **idGroup** **(Integer)** - The ID number of the group that the
        item belongs to. This value lines\
        up with one of the groups from the GetVendorGroups function
    -   **bIsSpecial** **(Boolean)** - Whether or not there is a special
        price for the item at the moment
    -   **bFutureStock** **(Boolean)** - Whether or not the unit will
        have more of the item in stock in the future.
    -   **tPriceInfo** **(Table)**
        -   **nAmount1** **(Integer)** - The amount that the item costs
        -   **eCurrencyType1** **(Integer)** - The primary currency type
            used to purchase the item
        -   **eAltType1** **(Integer)** - The alternate type of currency
            used to purchase the item
        -   **nAmount2** **(Integer)** - The amount the item costs of
            the secondary currency
        -   **eCurrencyType2** **(Integer)** - The secondary currency
            used to purchase the item
        -   **eAltType2** **(Integer)** - The secondary alternate type
            of currency used to purchase the item
    -   **itemData** **([Item](../Classes/Item.md))** - The item being
        purchased
    -   **splData** **([Spell](../Classes/Spell.md))** - A spell effect
        being purchased.
    -   **strName** **(String)** - The name of the item

------------------------------------------------------------------------

`Method`

GetVigor()
----------

------------------------------------------------------------------------

`Method`

GetVigorRating()
----------------

------------------------------------------------------------------------

`Method`

GetVigorRatingPercent()
-----------------------

------------------------------------------------------------------------

`Method`

HasTextBubble()
---------------

### Description

A function that determines whether or not the unit has a text bubble
over their head

### Return Value

-   **Boolean** - Whether or not the unit has a text bubble over their
    head

------------------------------------------------------------------------

`Method`

HasTitle()
----------

### Description

Determines whether or not the unit is displaying a title

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

Inspect()
---------

### Description

Performs the Inspect action on the given unit. This will cause the
Inspect event to be fired

------------------------------------------------------------------------

`Method`

InviteToGroup()
---------------

### Description

Sends a group invitation request to the target player

------------------------------------------------------------------------

`Method`

IsAccountFriend()
-----------------

### Description

Determines whether or not the specified unit is an Account Friend

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsACharacter()
--------------

### Description

Determines whether the unit is a player or not.

------------------------------------------------------------------------

`Method`

IsCasting()
-----------

### Description

Determines whether or not the unit is casting

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsCertainDeath()
----------------

------------------------------------------------------------------------

`Method`

IsCurrentBindPoint()
--------------------

### Description

Determines whether or not the specified bind point is the user's current
bind point.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsDead()
--------

### Description

Determines whether or not the unit is dead or not

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsElite()
---------

### Description

Not currently returning anything

------------------------------------------------------------------------

`Method`

IsFriend()
----------

### Description

Determines whether or not the unit is a friend. This does not include
account level friends

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsFriendlyWarplotStructure()
----------------------------

### Description

Determines whether or not the selected unit is both a warplot plug and
if it's friendly

### Return Value

-   **Boolean** - Returns true if both the unit is a plug and if it is
    friendly

------------------------------------------------------------------------

`Method`

IsIgnored()
-----------

### Description

Determines whether or not the selected player is ignored

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsInCCState()
-------------

### Description

Determines whether or not the unit is being affected by crowd control

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsInCombat()
------------

------------------------------------------------------------------------

`Method`

IsInstanceLockbox()
-------------------

------------------------------------------------------------------------

`Method`

IsInVehicle()
-------------

------------------------------------------------------------------------

`Method`

IsInventorySlotLocked(nLocation)
--------------------------------

### Description

Determines whether or not the specified inventory slot is locked

### Params

-   **nLocation** **(Integer)** - The inventory location of the item

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsInYourGroup()
---------------

### Description

Determines whether or not the given unit is in the player's group

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsMentoring()
-------------

### Description

Determines whether or not the selected unit is mentoring another player

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsMounted()
-----------

### Description

Determines whether or not the unit is riding a mount

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsMyGhost()
-----------

### Description

Determines whether or not the selected unit is the player's own ghost

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsOccluded()
------------

### Description

Determines whether or not the unit is currently hidden behind an object
or terrain

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsPublicEventHub()
------------------

### Description

Determines whether or not the unit is a Settler Infrastructure

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsPvpFlagged()
--------------

### Description

Determines whether or not the unit is flagged for PvP

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsRallied()
-----------

### Description

Determines whether or not the unit's level has been fixed due to
rallying

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsRare()
--------

------------------------------------------------------------------------

`Method`

IsRival()
---------

### Description

Determines whether or not the unit is a rival

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsScaled()
----------

### Description

Determines whether or not the unit is scaled to the player's level

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsSettlerImprovement()
----------------------

### Description

Determines whether or not the unit is a settler improvement

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsSettlerReward()
-----------------

### Description

Determines whether or not the unit is a settler improvement with a
reward

------------------------------------------------------------------------

`Method`

IsShieldOverloaded()
--------------------

### Description

Determines whether or not the unit's shields are overloaded

------------------------------------------------------------------------

`Method`

IsSoftKill()
------------

### Description

Determines whether or not the unit is eligible for open tagging.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsTagged()
----------

### Description

Determines whether or not the unit has been tagged

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsTaggedByMe()
--------------

### Description

Determines whether or not the current unit was tagged by the player

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsThePlayer()
-------------

### Description

Determines whether or not the targeted unit is the player

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsValid()
---------

### Description

Determines whether or not the unit is valid. Invalid units do not exist
in the world.

------------------------------------------------------------------------

`Method`

IsVisibleInstancePortal()
-------------------------

### Description

Determines whether or not the unit is an instance portal and if it is
visible

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsVisibleOnCurrentZoneMinimap()
-------------------------------

### Description

Determines whether or not the unit is currently in the same section of
the map and in the same instance

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

LockInventorySlot(nLocation)
----------------------------

### Description

Locks the specified inventory slot for the current player

### Params

-   **nLocation** **(Integer)** - The inventory slot that should be
    locked

------------------------------------------------------------------------

`Method`

PrepareInfractionReport()
-------------------------

------------------------------------------------------------------------

`Method`

PurchaseFlightPath(idDestination)
---------------------------------

### Description

Purchases the flight path to the specified destination

### Params

-   **idDestination** **(Integer)** - The ID number of the flight path's
    destination.

------------------------------------------------------------------------

`Method`

RequestRealmName()
------------------

------------------------------------------------------------------------

`Method`

Resurrect(nRezTypeChoice, nRezData)
-----------------------------------

### Description

Resurrect's the player based on the parameters passed

### Params

-   **nRezTypeChoice** **(Integer)** - Where the player should be
    resurrected
-   **nRezData** **(Integer)**

------------------------------------------------------------------------

`Method`

SetAlternateTarget(unitNewFocus)
--------------------------------

### Description

Changes the player's focus target to the specified unit. Clear the focus
target by passing in nil.

### Params

-   **unitNewFocus** **([Unit](../Classes/Unit.md))** - The unit that
    is set as the new focus target.

------------------------------------------------------------------------

`Method`

SetTargetMarker(nMarker)
------------------------

### Description

Places the specified target marker above the unit.

### Params

-   **nMarker** **(Integer)** - The integer representing which target
    marker to assign to the unit

------------------------------------------------------------------------

`Method`

ShouldDisplayMountHealth()
--------------------------

------------------------------------------------------------------------

`Method`

ShouldShowBreathBar()
---------------------

### Description

Determines whether the player's breath bar should be shown. This
function will return false if it is called for any unit other than the
current player.

### Return Value

-   **Boolean** - Whether or not the player's breath bar should be
    shown.

------------------------------------------------------------------------

`Method`

ShouldShowCastBar()
-------------------

### Description

Determines whether or not the unit's cast bar should be shown.

### Return Value

-   **Boolean** - Whether or not the unit's cast bar should be shown.

------------------------------------------------------------------------

`Method`

ShouldShowCraftingBar()
-----------------------

### Description

Determines whether or not the unit's crafting progress bar should be
shown. This function returns false if called for any unit other than the
current player.

### Return Value

-   **Boolean** - Whether or not the unit's crafting progress bar should
    be shown

------------------------------------------------------------------------

`Method`

ShouldShowNamePlate()
---------------------

### Description

Determines whether or not the unit's nameplate should be shown.

### Return Value

-   **Boolean** - Determines whether or not the unit's nameplate should
    be shown

------------------------------------------------------------------------

`Method`

ShowHintArrow()
---------------

### Description

Places a guide arrow above the player's head that points them in the
direction of the unit that called the function.

------------------------------------------------------------------------

`Method`

TakeShuttle()
-------------

### Description

When called from a taxi NPC, this will summon the taxi for the player.

------------------------------------------------------------------------

`Method`

UnlockAllInventorySlots()
-------------------------

### Description

Removes the locked state from all of the player's inventory slots.

------------------------------------------------------------------------

`Method`

UnlockInventorySlot(nInventoryLocation)
---------------------------------------

### Description

Unlocks the specified inventory slot for the player.

### Params

-   **nInventoryLocation** **(Integer)** - The inventory slot number
    that should be unlocked
