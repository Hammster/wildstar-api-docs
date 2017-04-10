Spell
=====

### Prefix: spl

------------------------------------------------------------------------

`Enum`

CodeEnumAOESelectionType
------------------------

-   **None**
-   **Closest**
-   **Furthest**
-   **Random**
-   **LowestAbsoluteHealth**
-   **MissingMostHealth**

------------------------------------------------------------------------

`Enum`

CodeEnumCastMethod
------------------

-   **Normal**
-   **Channeled**
-   **ChanneledField**
-   **ClientSideInteraction**
-   **PressHold**
-   **RapidTap**
-   **ChargeRelease**
-   **Multiphase**
-   **Transactional**
-   **UNUSED04**
-   **Aura**

------------------------------------------------------------------------

`Enum`

CodeEnumCastResult
------------------

-   **Ok**
-   **UnableToCreateSpell**
-   **MovingToCast**
-   **PendingSpellCast**
-   **SpellBad**
-   **SpellCancelled**
-   **SpellMaxChannel**
-   **SpellRemoved**
-   **SpellCountered**
-   **SpellCastingInterrupts**
-   **SpellInterrupted**
-   **SpellCombatModeActiveCount**
-   **SpellAlreadyCasting**
-   **SpellGlobalCooldown**
-   **SpellCooldown**
-   **SpellGroupCooldown**
-   **SpellPreRequisites**
-   **ActionBarSetDisallows**
-   **DamageInterrupts**
-   **InvalidInventoryIndex**
-   **ItemUnknown**
-   **ItemBad**
-   **ItemNoSpellId**
-   **ItemUnEquipped**
-   **ItemCharges**
-   **ItemTooHighLevel**
-   **ItemQuestRequirementsNotMet**
-   **ItemObjectiveComplete**
-   **CasterUnknown**
-   **CasterMustHaveTarget**
-   **CasterCannotBePrimaryTarget**
-   **CasterNotIncontrolOfSelf**
-   **CasterMovement**
-   **CasterMaxCast**
-   **CCStun**
-   **CCSleep**
-   **CCRoot**
-   **CCDisarm**
-   **CCSilence**
-   **CCPolymorph**
-   **CCFear**
-   **CCHold**
-   **CasterVitalCostHealth**
-   **CasterVitalCostXp**
-   **CasterVitalCostMoney**
-   **CasterVitalCostCurrency1**
-   **CasterVitalCostCurrency2**
-   **CasterVitalCostCurrency3**
-   **CasterVitalCostResource0**
-   **CasterVitalCostResource1**
-   **CasterVitalCostResource2**
-   **CasterVitalCostResource3**
-   **CasterVitalCostResource4**
-   **CasterVitalCostResource5**
-   **CasterVitalCostResource6**
-   **Caster\_CannotBeDead**
-   **Caster\_MustBeDead**
-   **Caster\_CannotBe\_Moving**
-   **Caster\_MustBe\_Moving**
-   **Caster\_CannotBe\_Stealth**
-   **Caster\_MustBe\_Stealth**
-   **Caster\_CannotBe\_Piloting**
-   **Caster\_MustBe\_Piloting**
-   **Caster\_CannotBe\_Embarked**
-   **Caster\_MustBe\_Embarked**
-   **Caster\_CannotBe\_Taxi**
-   **Caster\_MustBe\_Taxi**
-   **Caster\_CannotBe\_Stun**
-   **Caster\_MustBe\_Stun**
-   **Caster\_CannotBe\_Sleep**
-   **Caster\_MustBe\_Sleep**
-   **Caster\_CannotBe\_Root**
-   **Caster\_MustBe\_Root**
-   **Caster\_CannotBe\_Disarm**
-   **Caster\_MustBe\_Disarm**
-   **Caster\_CannotBe\_Silence**
-   **Caster\_MustBe\_Silence**
-   **Caster\_CannotBe\_Pacify**
-   **Caster\_MustBe\_Pacify**
-   **Caster\_CannotBe\_Fear**
-   **Caster\_MustBe\_Fear**
-   **Caster\_CannotBe\_Confuse**
-   **Caster\_MustBe\_Confuse**
-   **TargetGroup**
-   **TargetUnknown**
-   **NoTarget**
-   **Target\_ImmuneToSpellType**
-   **Target\_ImmuneToSpell**
-   **Target\_ImmuneToSpellGroupList**
-   **Target\_ImmuneToSpellGroup**
-   **Target\_Invulnerable**
-   **TargetMaxTarget**
-   **TargetVital**
-   **TargetFaction**
-   **TargetIsNotUseable**
-   **TargetOrientation**
-   **TargetCannotBePlayer**
-   **TargetCannotBeNpc**
-   **TargetRangeMin**
-   **TargetRangeMax**
-   **Target\_CannotBeDead**
-   **Target\_MustBeDead**
-   **Target\_CannotBe\_Moving**
-   **Target\_MustBe\_Moving**
-   **Target\_CannotBe\_Stealth**
-   **Target\_MustBe\_Stealth**
-   **Target\_CannotBe\_Piloting**
-   **Target\_MustBe\_Piloting**
-   **Target\_CannotBe\_Embarked**
-   **Target\_MustBe\_Embarked**
-   **Target\_CannotBe\_Taxi**
-   **Target\_MustBe\_Taxi**
-   **Target\_CannotBe\_Stun**
-   **Target\_MustBe\_Stun**
-   **Target\_CannotBe\_Sleep**
-   **Target\_MustBe\_Sleep**
-   **Target\_CannotBe\_Root**
-   **Target\_MustBe\_Root**
-   **Target\_CannotBe\_Disarm**
-   **Target\_MustBe\_Disarm**
-   **Target\_CannotBe\_Silence**
-   **Target\_MustBe\_Silence**
-   **Target\_CannotBe\_Pacify**
-   **Target\_MustBe\_Pacify**
-   **Target\_CannotBe\_Fear**
-   **Target\_MustBe\_Fear**
-   **Target\_CannotBe\_Confuse**
-   **Target\_MustBe\_Confuse**
-   **Target\_CannotBe\_Swimming**
-   **Target\_MustBe\_Swimming**
-   **InWrongWorldZone**
-   **DuelOver**
-   **UNUSED142**
-   **UNUSED143**
-   **MissingResult**
-   **IsP2PTrading**
-   **ClientSideInteractionFail**
-   **StackingRefreshExistingSpell**
-   **StackingTargetHasMorePowerfulSpells**
-   **StackingCasterHasMorePowerfulSpells**
-   **StackingError**
-   **Prereq\_CasterCast**
-   **CCKnockdown**
-   **CCVulnerability**
-   **Target\_MustBe\_Knockdown**
-   **Target\_MustBe\_Vulnerability**
-   **Caster\_MustBe\_Vulnerability**
-   **Caster\_MustBe\_Knockdown**
-   **Caster\_CannotBe\_Knockdown**
-   **Caster\_CannotBe\_Vulnerability**
-   **Target\_CannotBe\_Vulnerability**
-   **Target\_CannotBe\_Knockdown**
-   **MissingReagent\_Item**
-   **MissingReagent\_ItemFamily**
-   **MissingReagent\_ItemCategory**
-   **MissingReagent\_ItemType**
-   **Caster\_Needs\_LoS**
-   **CasterVitalCostMana**
-   **TargetImmuneToSpellEffect**
-   **WeaponSlot**
-   **Caster\_MustBe\_Jumping**
-   **Caster\_CannotBe\_Jumping**
-   **Target\_CannotBe\_Jumping**
-   **Target\_MustBe\_Jumping**
-   **InvalidPosition**
-   **CasterVitalCost**
-   **CasterVitalCostShieldCapacity**
-   **CasterVitalCostResource7**
-   **FailSpecialRestrictions**
-   **NoValidActivateSpell**
-   **SchematicAlreadyKnown**
-   **TradeskillTier**
-   **SpellNoCharges**
-   **TargetRangeVertical**
-   **StackingDuplicateDurationalSpell**
-   **SpellMaxPhaseReached**
-   **CCVulnerabilityWithAct**
-   **CCDisorient**
-   **CCDisable**
-   **CCTaunt**
-   **CCDeTaunt**
-   **CCBlind**
-   **CCKnockback**
-   **CCPushback**
-   **CCPull**
-   **CCPositionSwitch**
-   **CCTether**
-   **CCSnare**
-   **Caster\_MustBe\_Polymorph**
-   **Target\_MustBe\_Polymorph**
-   **Caster\_CannotBe\_Polymorph**
-   **Target\_CannotBe\_Polymorph**
-   **Caster\_MustBe\_Hold**
-   **Target\_MustBe\_Hold**
-   **Caster\_CannotBe\_Hold**
-   **Target\_CannotBe\_Hold**
-   **Caster\_MustBe\_Disorient**
-   **Target\_MustBe\_Disorient**
-   **Caster\_CannotBe\_Disorient**
-   **Target\_CannotBe\_Disorient**
-   **Caster\_MustBe\_Disable**
-   **Target\_MustBe\_Disable**
-   **Caster\_CannotBe\_Disable**
-   **Target\_CannotBe\_Disable**
-   **Caster\_MustBe\_Taunt**
-   **Target\_MustBe\_Taunt**
-   **Caster\_CannotBe\_Taunt**
-   **Target\_CannotBe\_Taunt**
-   **Caster\_MustBe\_DeTaunt**
-   **Target\_MustBe\_DeTaunt**
-   **Caster\_CannotBe\_DeTaunt**
-   **Target\_CannotBe\_DeTaunt**
-   **Caster\_MustBe\_Blind**
-   **Target\_MustBe\_Blind**
-   **Caster\_CannotBe\_Blind**
-   **Target\_CannotBe\_Blind**
-   **Caster\_MustBe\_Knockback**
-   **Target\_MustBe\_Knockback**
-   **Caster\_CannotBe\_Knockback**
-   **Target\_CannotBe\_Knockback**
-   **Caster\_MustBe\_Pushback**
-   **Target\_MustBe\_Pushback**
-   **Caster\_CannotBe\_Pushback**
-   **Target\_CannotBe\_Pushback**
-   **Caster\_MustBe\_Pull**
-   **Target\_MustBe\_Pull**
-   **Caster\_CannotBe\_Pull**
-   **Target\_CannotBe\_Pull**
-   **Caster\_MustBe\_PositionSwitch**
-   **Target\_MustBe\_PositionSwitch**
-   **Caster\_CannotBe\_PositionSwitch**
-   **Target\_CannotBe\_PositionSwitch**
-   **Caster\_MustBe\_Tether**
-   **Target\_MustBe\_Tether**
-   **Caster\_CannotBe\_Tether**
-   **Target\_CannotBe\_Tether**
-   **Caster\_MustBe\_Snare**
-   **Target\_MustBe\_Snare**
-   **Caster\_CannotBe\_Snare**
-   **Target\_CannotBe\_Snare**
-   **CasterVitalCostInterruptArmor**
-   **CCNoAbilities**
-   **Blacklisted**
-   **TargetCannotBePickup**
-   **CasterVitalCostAbsorption**
-   **Target\_MustBe\_CastersPet**
-   **Target\_MustBe\_CastersMaster**
-   **CCInterrupt**
-   **Caster\_MustBe\_Interrupt**
-   **Target\_MustBe\_Interrupt**
-   **Caster\_CannotBe\_Interrupt**
-   **Target\_CannotBe\_Interrupt**
-   **CSICooldown**
-   **CCDaze**
-   **Caster\_MustBe\_Daze**
-   **Target\_MustBe\_Daze**
-   **Caster\_CannotBe\_Daze**
-   **Target\_CannotBe\_Daze**
-   **CCSubdue**
-   **Caster\_MustBe\_Subdue**
-   **Target\_MustBe\_Subdue**
-   **Caster\_CannotBe\_Subdue**
-   **Target\_CannotBe\_Subdue**
-   **Target\_CannotBe\_Evading**
-   **Target\_StructuredPlugBenefitRestricted**
-   **CasterVitalCostPublicResource0**
-   **CasterVitalCostPublicResource1**
-   **CasterVitalCostPublicResource2**
-   **InactiveInnateAbilitySpell**
-   **Caster\_CannotBe\_Swimming**
-   **Caster\_MustBe\_Swimming**
-   **Prereq\_TargetCast**
-   **Prereq\_CasterPersistence**
-   **Prereq\_TargetPersistence**
-   **Prereq\_Trap**
-   **IllegalSpellCast**
-   **TargetNotInSameGroup**
-   **BossToken\_Permission**
-   **BossToken\_NotReady**
-   **CCGrounded**
-   **Caster\_MustBe\_Grounded**
-   **Target\_MustBe\_Grounded**
-   **Caster\_CannotBe\_Grounded**
-   **Target\_CannotBe\_Grounded**
-   **SpellUnknown**
-   **ItemAchievementComplete**
-   **Caster\_CannotBeInCombat**
-   **Caster\_MustBeInCombat**
-   **Target\_CannotBeInCombat**
-   **Target\_MustBeInCombat**
-   **CCDisableCinematic**
-   **Caster\_MustBe\_DisableCinematic**
-   **Target\_MustBe\_DisableCinematic**
-   **Caster\_CannotBe\_DisableCinematic**
-   **Target\_CannotBe\_DisableCinematic**
-   **CCAbilityRestriction**
-   **Caster\_MustBe\_AbilityRestriction**
-   **Target\_MustBe\_AbilityRestriction**
-   **Caster\_CannotBe\_AbilityRestriction**
-   **Target\_CannotBe\_AbilityRestriction**
-   **Target\_VehicleBenefitRestricted**
-   **TargetCannotBePet**
-   **Target\_HostileInvulnerability**
-   **Target\_InvulnerableToOther**
-   **Target\_BeneficialInvulnerability**
-   **Caster\_MustBe\_Falling**
-   **Caster\_CannotBe\_Falling**
-   **Target\_CannotBe\_Falling**
-   **Target\_MustBe\_Falling**
-   **Caster\_MustBe\_Sprinting**
-   **Caster\_CannotBe\_Sprinting**
-   **Target\_CannotBe\_Sprinting**
-   **Target\_MustBe\_Sprinting**
-   **Queued**
-   **ItemWrongRace**
-   **ItemWrongClass**
-   **ItemAlreadyUnlocked**
-   **PlayerSpellPending**
-   **Target\_MustBe\_PvpFlagged**
-   **Caster\_MustBe\_PvpFlagged**
-   **Target\_OutsideTelegraph**
-   **ShieldsOverloaded**
-   **CasterVitalCostResource8**
-   **CasterVitalCostResource9**
-   **CasterVitalCostResource10**
-   **RapidTransport\_Invalid**
-   **CasterVitalCostFocus**
-   **ServiceTokens\_InsufficentFunds**

------------------------------------------------------------------------

`Enum`

CodeEnumComparison
------------------

-   **Equals**
-   **Greater**
-   **GreaterThanEqualTo**
-   **Less**
-   **LessThanEqualTo**
-   **Percent\_Equals**
-   **Percent\_Greater**
-   **Percent\_GreaterThanEqualTo**
-   **Percent\_Less**
-   **Percent\_LessThanEqualTo**

------------------------------------------------------------------------

`Enum`

CodeEnumReagentType
-------------------

-   **Item**
-   **ItemFamily**
-   **ItemCategory**

------------------------------------------------------------------------

`Enum`

CodeEnumSchool
--------------

-   **Spell**
-   **Melee**
-   **Ranged**
-   **Unarmed**

------------------------------------------------------------------------

`Enum`

CodeEnumSpellClass
------------------

-   **BuffDispellable**
-   **BuffNonDispellable**
-   **DebuffDispellable**
-   **DebuffNonDispellable**
-   **BuffNonDispelRightClickOk**

------------------------------------------------------------------------

`Enum`

CodeEnumSpellEffectType
-----------------------

-   **UnitPropertyModifier**
-   **VitalModifier**
-   **SpellCounter**
-   **ForcedMove**
-   **CCStateSet**
-   **Transference**
-   **SummonVehicle**
-   **Activate**
-   **Damage**
-   **FactionSet**
-   **Heal**
-   **Harvest**
-   **DistanceDependentDamage**
-   **Script**
-   **Proc**
-   **UnitStateSet**
-   **Resurrect**
-   **Fluff**
-   **Scale**
-   **ProxyLinearAE**
-   **SummonCreature**
-   **HousingTeleport**
-   **ActionBarSet**
-   **ForcedAction**
-   **ProxyChannel**
-   **Proxy**
-   **CCStateBreak**
-   **ForceFacing**
-   **Absorption**
-   **SapVital**
-   **Disguise**
-   **SpellImmunity**
-   **DistributedDamage**
-   **ChangePhase**
-   **NpcExecutionDelay**
-   **SummonMount**
-   **ReputationModify**
-   **GiveSchematic**
-   **ModifySchematic**
-   **TradeSkillProfession**
-   **QuestAdvanceObjective**
-   **GiveItemToPlayer**
-   **GiveLootTableToPlayer**
-   **NpcLootTableModify**
-   **ThreatModification**
-   **ThreatTransfer**
-   **WarplotTeleport**
-   **CraftItem**
-   **ItemBreakdown**
-   **SpellForceRemoveChanneled**
-   **ModifyInterruptArmor**
-   **SpellDispel**
-   **TradeSkillProfessionXp**
-   **ModifySpell**
-   **ModifySpellEffect**
-   **AddSpell**
-   **AddSpellEffect**
-   **SuppressSpellEffect**
-   **VacuumLoot**
-   **ShieldOverload**
-   **Teleport**
-   **TitleGrant**
-   **TitleRevoke**
-   **VendorPriceModifier**
-   **RechargeItemBatteries**
-   **FacilityModification**
-   **PetAIStanceSet**
-   **ModifySpellCooldown**
-   **FinishingMove**
-   **ChangeIcon**
-   **ItemVisualSwap**
-   **AggroImmune**
-   **SpellEffectImmunity**
-   **SpellForceRemove**
-   **RavelSignal**
-   **ChangeDisplayName**
-   **Stealth**
-   **RemoveStealth**
-   **PathActionExplorerDig**
-   **HazardEnable**
-   **HazardModify**
-   **HazardSuspend**
-   **NpcForceFacing**
-   **AchievementAdvance**
-   **PathXpModify**
-   **ProxyChannelVariableTime**
-   **FullScreenEffect**
-   **ProxyRandomExclusive**
-   **DespawnUnit**
-   **SummonPet**
-   **MimicDisplayName**
-   **MimicDisguise**
-   **GrantXP**
-   **DatacubeUpdate**
-   **DatacubeVolumeUpdate**
-   **SettlerCampfire**
-   **SummonTrap**
-   **SetBusy**
-   **CooldownReset**
-   **RestedXpDecorBonus**
-   **LearnDyeColor**
-   **PetCastSpell**
-   **DisguiseOutfit**
-   **RewardBuffModifier**
-   **HousingEscape**
-   **NPCForceAIMovement**
-   **HealShields**
-   **PathMissionIncrement**
-   **GrantLevelScaledXP**
-   **DelayDeath**
-   **GrantLevelScaledPrestige**
-   **UnlockPetFlair**
-   **WarplotPlugUpgrade**
-   **SetMatchingEligibility**
-   **UnlockActionBar**
-   **UNUSED040**
-   **ModifyCreatureFlags**
-   **UNUSED061**
-   **UNUSED063**
-   **ApplyLASChanges**
-   **GiveAbilityPointsToPlayer**
-   **ModifyAbilityCharges**
-   **UNUSED091**
-   **UNUSED104**
-   **UnlockMount**
-   **UnlockInlaidAugment**
-   **GiveAugmentPowerToPlayer**
-   **TemporarilyUnflagPvp**
-   **SupportStuck**
-   **MiniMapIcon**
-   **Disembark**
-   **ChangePlane**
-   **ModifyRestedXP**
-   **UNUSED011**
-   **UNUSED039**
-   **UNUSED050**
-   **UNUSED054**
-   **UNUSED070**
-   **UNUSED072**
-   **UNUSED074**
-   **UNUSED102**
-   **UNUSED103**
-   **UNUSED114**
-   **UNUSED115**
-   **HousingPlantSeed**
-   **UnlockVanityPet**
-   **SummonVanityPet**
-   **DamageShields**
-   **RewardPropertyModifier**
-   **RapidTransport**

------------------------------------------------------------------------

`Enum`

CodeEnumSpellTag
----------------

-   **Assault**
-   **Support**
-   **Path**
-   **Misc**
-   **Mount**
-   **DoesNotUseSpecIndex**
-   **Utility**
-   **NotAutoActivated**
-   **Conditional**
-   **VanityPet**
-   **MTX**

------------------------------------------------------------------------

`Enum`

CombatMessageType
-----------------

-   **General**
-   **Experience**
-   **QuestUpdate**
-   **LocationChange**
-   **Combat\_Damage\_Done**
-   **Combat\_Damage\_Done\_Critical**
-   **Combat\_Damage\_Taken**
-   **Combat\_Damage\_Taken\_Critical**
-   **Combat\_Healing\_Done**
-   **Combat\_Healing\_Done\_Critical**
-   **Combat\_Healing\_Taken**
-   **Combat\_Healing\_Taken\_Critical**
-   **Combat\_Block\_Taken**
-   **Combat\_Block\_Done**
-   **Combat\_Parry\_Taken**
-   **Combat\_Parry\_Done**
-   **Combat\_Dodge\_Taken**
-   **Combat\_Dodge\_Done**
-   **Combat\_NoEffect\_Taken**
-   **Combat\_NoEffect\_Done**
-   **Combat\_Shallow\_Taken**
-   **Combat\_Shallow\_Done**
-   **Combat\_Falling\_Damage\_Done**
-   **Combat\_Death**
-   **Error**
-   **SpellFailure**
-   **UNUSED00**
-   **UNUSED01**
-   **Faction**
-   **LootBase**
-   **LootAverage**
-   **LootGood**
-   **LootExcellent**
-   **LootSuperb**
-   **LootLegendary**
-   **LootQuestActivation**
-   **Achievement**
-   **Experience\_KillCreature**
-   **Experience\_ClusterBonus**
-   **Experience\_Quest**
-   **Absorption\_Taken**
-   **Absorption\_Done**
-   **Transference\_Taken**
-   **Transference\_Done**
-   **SpellFailure\_Long**
-   **SpellFailure\_Medium**
-   **SpellFailure\_Short**
-   **SpellFailure\_Target\_Head**
-   **SpellFailure\_Target\_Feet**
-   **Special\_Done**
-   **Special\_Taken**
-   **UNUSED02**
-   **PlayerPath**
-   **KillPerformanceReward**
-   **MultiKillReward**
-   **KillingSpreeReward**
-   **LootInferior**
-   **TelegraphEvadeReward**
-   **TelegraphInterruptReward**
-   **RestedReward**
-   **UNUSED04**
-   **UNUSED03**
-   **LootArtifact**

------------------------------------------------------------------------

`Function`

is()
----

------------------------------------------------------------------------

`Function`

ShowFloater()
-------------

------------------------------------------------------------------------

`Method`

\_\_eq() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

GetAbilityCharges()
-------------------

------------------------------------------------------------------------

`Method`

GetAOETargetInfo()
------------------

### Description

Does a lua\_newtable of eSelectionType if not aoe, otherwise many (10+)
fields relating to the aoe data.

### Return Value

-   **Table**
    -   **eSelectionType** **(Integer)**
    -   **idTarget** **(Integer)**
    -   **fMinimumRange** **(Float)**
    -   **fMaximumRange** **(Float)**
    -   **fAngle** **(Float)**
    -   **nTargetCount** **(Integer)**
    -   **bCanAffectDead** **(Boolean)**
    -   **bClusterOnly** **(Boolean)**
    -   **bGroupOnly** **(Boolean)**
    -   **bMustBeInCombat** **(Boolean)**

------------------------------------------------------------------------

`Method`

GetBaseSpellId()
----------------

------------------------------------------------------------------------

`Method`

GetCasterInnateCosts()
----------------------

### Description

Does a lua\_newtable with an index, eType, and nValue.

------------------------------------------------------------------------

`Method`

GetCasterInnateRequirements()
-----------------------------

### Description

Does a lua\_newtable with an index, eVital, nValue, and eEval.

------------------------------------------------------------------------

`Method`

GetCastInfoString()
-------------------

------------------------------------------------------------------------

`Method`

GetCastMethod()
---------------

### Description

Does a lua\_pushinteger of pSpell's castMethod.

------------------------------------------------------------------------

`Method`

GetCastTime()
-------------

### Description

Does a lua\_pushnumber of pSpell's castTime \* 0.001f, else 0.0f if
null.

------------------------------------------------------------------------

`Method`

GetCastTimeOverride()
---------------------

------------------------------------------------------------------------

`Method`

GetChannelData()
----------------

### Description

Does a lua\_newtable with fMaxTime, fInitialDelay, and fPulseTime.

------------------------------------------------------------------------

`Method`

GetClass()
----------

### Description

Does a lua\_pushinteger of pSpell's SpellClass.

------------------------------------------------------------------------

`Method`

GetClassPower() (Deprecated)
----------------------------

### Description

Does a lua\_pushinteger of pSpell's power, 0 if pSpell's spellClass
&lt;= 0.

------------------------------------------------------------------------

`Method`

GetCombatMode() (Deprecated)
----------------------------

### Description

Does a lua\_pushinteger of pSpell's combatModeId.

------------------------------------------------------------------------

`Method`

GetCooldownRemaining()
----------------------

------------------------------------------------------------------------

`Method`

GetCooldownTime()
-----------------

### Description

Does a lua\_pushnumber of pSpell's spellCoolDown \* 0.001f.

------------------------------------------------------------------------

`Method`

GetCostInfoString()
-------------------

------------------------------------------------------------------------

`Method`

GetFlavor()
-----------

### Description

Does a lua\_pushstring of pSpell's localized ActionBarTooltip, or nil if
null.

------------------------------------------------------------------------

`Method`

GetGCDTime()
------------

------------------------------------------------------------------------

`Method`

GetIcon()
---------

### Description

Does a lua\_pushstring of pSpell's iconPath, or nil if null.

------------------------------------------------------------------------

`Method`

GetId()
-------

------------------------------------------------------------------------

`Method`

GetLasBonusEachTierDesc()
-------------------------

------------------------------------------------------------------------

`Method`

GetLasTierDesc()
----------------

------------------------------------------------------------------------

`Method`

GetMaximumRange()
-----------------

### Description

Does a lua\_pushinteger of pSpell's targetMaximumRange, or 0.0f if null.

------------------------------------------------------------------------

`Method`

GetMinimumRange()
-----------------

### Description

Does a lua\_pushinteger of pSpell's targetMinimumRange, or 0.0f if null.

------------------------------------------------------------------------

`Method`

GetName()
---------

### Description

Does a lua\_pushwstring of pSpell's localized IdName, or nil if null.

------------------------------------------------------------------------

`Method`

GetPrerequisites()
------------------

### Description

Does a lua\_newtable of many (10+) fields relating to pSpell's
preqrequisites.

### Return Value

-   **Table**
    -   **bTargetAvoided** **(Boolean)**
    -   **bTargetBlocked** **(Boolean)**
    -   **bTargetGlancing** **(Boolean)**
    -   **bTargetFierce** **(Boolean)**
    -   **bNOTUSED** **(Boolean)**
    -   **bCasterAvoided** **(Boolean)**
    -   **bCasterBlocked** **(Boolean)**
    -   **bCasterGlancing** **(Boolean)**
    -   **bCasterFierce** **(Boolean)**
    -   **bNOTUSED1** **(Boolean)**
    -   **bCasterSpellSuccess** **(Boolean)**
    -   **bLastCasterSpellSuccess** **(Boolean)**

------------------------------------------------------------------------

`Method`

GetPrice()
----------

### Description

Does a LuaGameTypes\_Money::New of pSpell's price.

------------------------------------------------------------------------

`Method`

GetProxyChannelData()
---------------------

------------------------------------------------------------------------

`Method`

GetReagents()
-------------

### Description

Does a lua\_newtable with an index, nRequired, eType, and item relating
to pSpell's reagents.

------------------------------------------------------------------------

`Method`

GetRequiredLevel()
------------------

------------------------------------------------------------------------

`Method`

GetRequiredWorldZone()
----------------------

### Description

Does a lua\_pushwstring of a localized pWorldZone's nameId if pSpell
requires a specific world zone.

------------------------------------------------------------------------

`Method`

GetSchool()
-----------

### Description

Does a lua\_pushinteger of pSpell's school.

------------------------------------------------------------------------

`Method`

GetSpellServiceTokenCost()
--------------------------

------------------------------------------------------------------------

`Method`

GetTargetAngle()
----------------

### Description

Does a lua\_pushnumber of pSpell's targetAngle.

------------------------------------------------------------------------

`Method`

GetTargetInnateRequirements()
-----------------------------

### Description

Does a lua\_newtable with an index, eVital, nValue, and eEval of target
inate requirements.

------------------------------------------------------------------------

`Method`

GetThresholdTime()
------------------

------------------------------------------------------------------------

`Method`

GetTier()
---------

### Description

Does a lua\_pushinteger of pSpell's tierIndex.

------------------------------------------------------------------------

`Method`

GetTradeskillRequirements()
---------------------------

------------------------------------------------------------------------

`Method`

IsBeneficial()
--------------

------------------------------------------------------------------------

`Method`

IsFreeformTarget()
------------------

------------------------------------------------------------------------

`Method`

IsMovingInterrupted()
---------------------

------------------------------------------------------------------------

`Method`

IsNew()
-------

### Description

Does a lua\_pushboolean of pSpell's IsNewItem.

------------------------------------------------------------------------

`Method`

IsSelfSpell()
-------------

------------------------------------------------------------------------

`Method`

SetNewFlag(bNew)
----------------

### Params

-   **bNew** **(Boolean)** - (Default value: false)

------------------------------------------------------------------------

`Method`

ShouldHideCooldownInTooltip()
-----------------------------
