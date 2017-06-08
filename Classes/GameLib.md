GameLib
=======

------------------------------------------------------------------------

`Enum`

ChannelUpdateCraftingType
-------------------------

-   **Item**

------------------------------------------------------------------------

`Enum`

ChannelUpdateLootType
---------------------

-   **Item**
-   **Currency**
-   **ItemDestroy**

------------------------------------------------------------------------

`Enum`

ChannelUpdateProgressType
-------------------------

-   **RewardPoints**
-   **Experience**
-   **RestExperience**
-   **ElderPoints**
-   **RestElderPoints**
-   **SignatureExperience**
-   **SignatureElderPoints**

------------------------------------------------------------------------

`Enum`

CharacterRecustomizationResultCharacterRecustomizationResult
------------------------------------------------------------

-   **Success**
-   **UnknownError**
-   **NoChanges**
-   **InsufficientFunds**
-   **OutOfRange**

------------------------------------------------------------------------

`Enum`

CityDirectionType
-----------------

-   **Mailbox**
-   **Bank**
-   **AuctionHouse**
-   **CommodityMarket**
-   **AbilityVendor**
-   **Tradeskill**
-   **General**
-   **HousingNpc**
-   **Transport**
-   **Fortune**

------------------------------------------------------------------------

`Enum`

CodeEnumAccountPrivilegeRestriction
-----------------------------------

-   **Chat**
-   **Invite**
-   **PvpMatch**
-   **Trade**

------------------------------------------------------------------------

`Enum`

CodeEnumAddonSaveLevel
----------------------

-   **General**
-   **Account**
-   **Realm**
-   **Character**

------------------------------------------------------------------------

`Enum`

CodeEnumClass
-------------

-   **Warrior**
-   **Engineer**
-   **Esper**
-   **Medic**
-   **Stalker**
-   **Spellslinger**

------------------------------------------------------------------------

`Enum`

CodeEnumCombatResult
--------------------

-   **Avoid**
-   **Critical**
-   **Hit**
-   **NeedsTelegraphEvaluation**
-   **OutsideTelegraph**
-   **OutsideTelegraphInvalid**
-   **InsideTelegraph**
-   **NeedsHitResultCalc**

------------------------------------------------------------------------

`Enum`

CodeEnumConfirmButtonType
-------------------------

### Description

The different types of Action Confirm Buttons available

-   **SendMail**
-   **CommitTrade**
-   **DeleteItem**
-   **SalvageItem**
-   **EquipItem**
-   **CraftingAbandon**
-   **MarketplaceAuctionSellSubmit**
-   **MarketplaceAuctionBuySubmit**
-   **MarketplaceCommoditiesSubmit**
-   **AccountClaimItem**
-   **AccountTakeItem**
-   **AccountGiftItem**
-   **AccountGiftItemReturn**
-   **CREDDExchangeSubmit**
-   **AccountCreddRedeem**
-   **CopyToClipboard**
-   **MatchingGameRespondToPending**
-   **ReportPlayer**
-   **GenericMapNodeChoose**
-   **SubmitSupportTicket**
-   **LootItem**
-   **RuneSlotReroll** - Used when setting up an ActionConfirmButton for
    use with a rune slot reroll. Two additional parameters to
    SetActionData should be provided. The first is the item containing
    the rune slot. The second is the index of the rune slot.
-   **EldanForge**
-   **UnlockCostumeItem**
-   **ForgetCostumeItem**
-   **SaveCostumeChanges**
-   **RuneSlotClear**
-   **RuneSlotAdd**
-   **CommitCustomizationChanges**
-   **WakeHereService**
-   **CastSpellService**
-   **RapidTransport**

------------------------------------------------------------------------

`Enum`

CodeEnumDamageType
------------------

-   **Heal**
-   **Fall**
-   **Suffocate**
-   **Physical**
-   **Tech**
-   **Magic**
-   **HealShields**

------------------------------------------------------------------------

`Enum`

CodeEnumDuelState
-----------------

-   **None**
-   **Pending**
-   **WaitingToAccept**
-   **Dueling**

------------------------------------------------------------------------

`Enum`

CodeEnumEquipItemResult
-----------------------

-   **Ok**
-   **Cooldown**
-   **Invalid**
-   **LevelTooLow**
-   **WrongClass**
-   **WrongRace**

------------------------------------------------------------------------

`Enum`

CodeEnumEquippedItems
---------------------

-   **Chest**
-   **Legs**
-   **Head**
-   **Shoulder**
-   **Feet**
-   **Hands**
-   **WeaponTool**
-   **WeaponAttachment**
-   **System**
-   **Augment**
-   **Implant**
-   **Gadget**
-   **Shields**
-   **WeaponPrimary**
-   **Bag0**
-   **Bag1**
-   **Bag2**
-   **Bag3**
-   **BankBag0**
-   **BankBag1**
-   **BankBag2**
-   **BankBag3**
-   **BankBag4**
-   **DEPRECATED3**
-   **DEPRECATED2**
-   **DEPRECATED1**
-   **BankBag5**
-   **BankBag6**
-   **BankBag7**
-   **BankBag8**
-   **BankBag9**

------------------------------------------------------------------------

`Enum`

CodeEnumExitEvent
-----------------

-   **None**
-   **Camp**
-   **Quit**

------------------------------------------------------------------------

`Enum`

CodeEnumGameCommandType
-----------------------

-   **GadgetAbility**
-   **DefaultAttack**
-   **ClassInnateAbility**
-   **ActivateTarget**
-   **FollowTarget**
-   **Sprint**
-   **ToggleWalk**
-   **Dismount**
-   **Vacuum**
-   **PathAction**
-   **ToggleScannerBot**
-   **DashForward**
-   **DashBackward**
-   **DashLeft**
-   **DashRight**
-   **PathAction2**
-   **Interact**
-   **GoToBind**
-   **GoToHouse**
-   **EscapeHouse**
-   **GoToWarplot**
-   **WarplotBossTokenUI**
-   **SummonMount**
-   **UsePotion**
-   **GoToIllium**
-   **GoToThayd**
-   **HousingLandscape**
-   **HousingRemodel**
-   **HousingCrate**
-   **HousingVendor**
-   **HousingList**
-   **HousingEditMode**

------------------------------------------------------------------------

`Enum`

CodeEnumGameMode
----------------

-   **West**
-   **China**

------------------------------------------------------------------------

`Enum`

CodeEnumGenericError
--------------------

-   **Ok**
-   **Params**
-   **PlayerBusy**
-   **UnknownTargetUnit**
-   **TargetFaction**
-   **DbFailure**
-   **Item\_BadId**
-   **Vendor\_StackSize**
-   **Vendor\_SoldOut**
-   **Vendor\_UnknownItem**
-   **Vendor\_FailedPreReq**
-   **Vendor\_NotAVendor**
-   **Vendor\_TooFar**
-   **Vendor\_BadItemRec**
-   **Vendor\_NotEnoughToFillQuantity**
-   **Vendor\_NotEnoughCash**
-   **Vendor\_UniqueConstraint**
-   **Vendor\_ItemLocked**
-   **Vendor\_IWontBuyThat**
-   **Vendor\_NoQuantity**
-   **Vendor\_BagIsNotEmpty**
-   **Item\_OverFlowChestCreated**
-   **Item\_InventoryFull**
-   **Item\_UnknownItem**
-   **Item\_QuestViolation**
-   **Item\_Unique**
-   **Item\_NotValidforSlot**
-   **Item\_Locked**
-   **Item\_AlreadyEquipped**
-   **Item\_NotEquipped**
-   **Item\_BagMustBeEmpty**
-   **Item\_CannotFindBag**
-   **Item\_BagToSmall**
-   **Item\_CantPutBagInItself**
-   **Item\_WrongRace**
-   **Item\_WrongClass**
-   **Item\_FailedProficiency**
-   **Item\_LevelToLow**
-   **Embark\_PlayerAlreadyinSeat**
-   **Embark\_PlayerUnableToEmbark**
-   **Embark\_InvalidVehicleUnit**
-   **Embark\_NoSplineForTaxi**
-   **Embark\_VehicleIsBroken**
-   **Embark\_InvalidSeat**
-   **Embark\_SeatTaken**
-   **Embark\_SeatEmpty**
-   **Embark\_NotInRange**
-   **Embark\_CannotDoWhileOnTaxi**
-   **Mail\_CannotFindPlayer**
-   **Mail\_FailedToCreate**
-   **Vendor\_CuratorOnlyBuysRelics**
-   **Vendor\_CannotBuyRelics**
-   **Player\_CantDoWhileDead**
-   **Vendor\_NoBuyer**
-   **Vendor\_NoVendor**
-   **Vendor\_Buyer\_NoActionCC**
-   **Vendor\_Vendor\_NoActionCC**
-   **Vendor\_Vendor\_Disposition**
-   **Player\_CannotWhileInCombat**
-   **Mail\_Busy**
-   **Mail\_MailBoxOutOfRange**
-   **Mail\_NoAttachment**
-   **Mail\_InsufficientFunds**
-   **Mail\_InvalidInventorySlot**
-   **Mail\_UniqueExists**
-   **Mail\_CannotDelete**
-   **Mail\_DoesNotExist**
-   **Item\_CannotBeSalvaged**
-   **Conversion\_BadConversionRec**
-   **Conversion\_CannotRemoveSource**
-   **Conversion\_CannotAddTarget**
-   **Faction\_NotEnoughRep**
-   **Item\_NoItems**
-   **Craft\_TierTooLow**
-   **Craft\_MissingMaterials**
-   **Craft\_IncompleteCircuit**
-   **Craft\_SocketNotModdable**
-   **Craft\_DuplicateChip**
-   **DisEmbark\_PlayerNotInWorld**
-   **Item\_NeedsRepair**
-   **Craft\_TooManyAdditives**
-   **Item\_SlotDisabled**
-   **Matching\_NoRoleSelected**
-   **Instance\_NotFound**
-   **Mail\_CannotTransferItem**
-   **Mail\_InvalidText**
-   **Mail\_CanNotHaveCoDAndGift**
-   **Reserved02**
-   **Reserved03**
-   **Reserved04**
-   **Auction\_NotReady**
-   **Auction\_CannotFillOrder**
-   **Auction\_TooManyOrders**
-   **Auction\_OrderTooBig**
-   **Auction\_NotFound**
-   **Auction\_BidTooLow**
-   **Auction\_OwnItem**
-   **Auction\_BidTooHigh**
-   **Auction\_AlreadyHasBid**
-   **Mail\_InvalidDeliverySpeed**
-   **Housing\_InvalidDecorPlacement**
-   **Instance\_LimitExceeded**
-   **Craft\_UnknownSchematic**
-   **Craft\_MicrochipInvalidSocket**
-   **Craft\_MicrochipInvalidSlot**
-   **Craft\_FailChanceTooHigh**
-   **Instance\_EncounterInProgress**
-   **Instance\_Full**
-   **Housing\_CrateFull**
-   **TargetBusy**
-   **Mail\_CannotReturn**
-   **Mail\_CannotMailSelf**
-   **Faction\_AtMax**
-   **Housing\_MaxDecor**
-   **Auction\_ItemAuctionDisabled**
-   **Auction\_CommodityDisabled**
-   **Mail\_CannotMailTrialAccount**
-   **MissingEntitlement**
-   **Instance\_TransferPending**
-   **Instance\_InvalidDestination**
-   **Instance\_NotInGroup**
-   **Instance\_DifferentSavedInstance**
-   **Instance\_InstanceInUse**
-   **Item\_WrongFaction**
-   **Instance\_WrongLevel**
-   **Mail\_Squelched**
-   **LootForge\_QualityMismatch**
-   **LootForge\_InvalidItem**
-   **LootForge\_CountMismatch**
-   **LootForge\_Invalid**
-   **RewardTrack\_CannotClaim**
-   **RewardTrack\_InvalidRewardChoice**
-   **RewardTrack\_InvalidTrackChoice**
-   **RewardTrack\_TrackNotActive**
-   **RewardTrack\_TrackAlreadyActive**
-   **Item\_EquipPrereqFailed**
-   **Instance\_PenaltyMap**
-   **Item\_CannotBeDeleted**
-   **UNUSED81**
-   **UNUSED113**
-   **Auction\_TooManyBids**
-   **AccountItem\_MaxEntitlementCount**
-   **Item\_BadParams**
-   **Item\_BadStaticData**
-   **Craft\_TooFar**
-   **Craft\_InvalidTier**
-   **Craft\_BadId**
-   **Craft\_BadParams**
-   **Craft\_InvalidPowerCore**
-   **RewardTrack\_Locked**
-   **MTXChest\_AlreadyOpened**

------------------------------------------------------------------------

`Enum`

CodeEnumHintType
----------------

-   **None**
-   **PathMission**
-   **Quest**
-   **PublicEvent**
-   **PublicEventObjective**
-   **Unit**
-   **Challenge**
-   **NavPoint**

------------------------------------------------------------------------

`Enum`

CodeEnumHoloMark
----------------

-   **Back**
-   **Left**
-   **Right**

------------------------------------------------------------------------

`Enum`

CodeEnumInputAction
-------------------

-   **Nothing**
-   **Options**
-   **CharacterPanel**
-   **Inventory**
-   **QuestLog**
-   **Communicator**
-   **Escape**
-   **Shift**
-   **Control**
-   **Select**
-   **MouseInteract**
-   **Interact**
-   **HostileInteract**
-   **TargetSelf**
-   **TargetParty1**
-   **TargetParty2**
-   **TargetParty3**
-   **TargetParty4**
-   **TargetNextEnemy**
-   **TargetPreviousEnemy**
-   **TargetNextFriend**
-   **TargetPreviousFriend**
-   **AssistTarget**
-   **MoveForward**
-   **MoveBackward**
-   **StrafeLeft**
-   **StrafeRight**
-   **TurnLeft**
-   **TurnRight**
-   **PitchUp**
-   **PitchDown**
-   **MouseTurn**
-   **SprintModifier**
-   **VacuumLoot**
-   **PathAction**
-   **Jump**
-   **Dismount**
-   **ToggleSit**
-   **ToggleWalk**
-   **ToggleAutoRun**
-   **CameraUp**
-   **CameraDown**
-   **CameraLeft**
-   **CameraRight**
-   **CameraIn**
-   **CameraOut**
-   **MouseLook**
-   **CastObjectiveAbility**
-   **LimitedActionSet1**
-   **LimitedActionSet2**
-   **LimitedActionSet3**
-   **LimitedActionSet4**
-   **LimitedActionSet5**
-   **LimitedActionSet6**
-   **LimitedActionSet7**
-   **LimitedActionSet8**
-   **CastGadgetAbility**
-   **CastPathAbility**
-   **ActionBar0\_Unused1**
-   **ActionBar0\_Unused2**
-   **ActionBar1\_Slot1**
-   **ActionBar1\_Slot2**
-   **ActionBar1\_Slot3**
-   **ActionBar1\_Slot4**
-   **ActionBar1\_Slot5**
-   **ActionBar1\_Slot6**
-   **ActionBar1\_Slot7**
-   **ActionBar1\_Slot8**
-   **ActionBar1\_Slot9**
-   **ActionBar1\_Slot10**
-   **ActionBar1\_Slot11**
-   **ActionBar1\_Slot12**
-   **ActionBar2\_Slot1**
-   **ActionBar2\_Slot2**
-   **ActionBar2\_Slot3**
-   **ActionBar2\_Slot4**
-   **ActionBar2\_Slot5**
-   **ActionBar2\_Slot6**
-   **ActionBar2\_Slot7**
-   **ActionBar2\_Slot8**
-   **ActionBar2\_Slot9**
-   **ActionBar2\_Slot10**
-   **ActionBar2\_Slot11**
-   **ActionBar2\_Slot12**
-   **ActionBar3\_Slot1**
-   **ActionBar3\_Slot2**
-   **ActionBar3\_Slot3**
-   **ActionBar3\_Slot4**
-   **ActionBar3\_Slot5**
-   **ActionBar3\_Slot6**
-   **ActionBar3\_Slot7**
-   **ActionBar3\_Slot8**
-   **ActionBar3\_Slot9**
-   **ActionBar3\_Slot10**
-   **ActionBar3\_Slot11**
-   **ActionBar3\_Slot12**
-   **Unused1**
-   **Unused2**
-   **Unused3**
-   **Unused4**
-   **Unused5**
-   **Unused6**
-   **SetStance1**
-   **SetStance2**
-   **SetStance3**
-   **Unused7**
-   **Unused20**
-   **Unused11**
-   **ToggleInterface**
-   **ToggleFramerate**
-   **Unused21**
-   **Unused23**
-   **Unused22**
-   **WorldMap**
-   **LimitedActionSetBuilder**
-   **Unused8**
-   **Unused9**
-   **ExplicitMouseLook**
-   **ToggleWeapons**
-   **LeftMouseHold**
-   **Ri.mdouseHold**
-   **CenterMouseHold**
-   **CastInnateAbility**
-   **MarkingMenuLeftClick**
-   **MarkingMenuLeftHold**
-   **MarkingMenuRightClick**
-   **MarkingMenuRightHold**
-   **HUDShowQuests**
-   **ToggleCameraAngle**
-   **ToggleScannerBot**
-   **Codex**
-   **PathAction2**
-   **FloatingActionBar\_Slot1**
-   **FloatingActionBar\_Slot2**
-   **FloatingActionBar\_Slot3**
-   **FloatingActionBar\_Slot4**
-   **FloatingActionBar\_Slot5**
-   **FloatingActionBar\_Slot6**
-   **ScaleRampedMotion**
-   **ScaleRampedRotation**
-   **BrakeRampedMotion**
-   **BrakeRampedRotation**
-   **MoveDown**
-   **GroupFinder**
-   **CastMiscSpell**
-   **SetTargetMark1**
-   **SetTargetMark2**
-   **SetTargetMark3**
-   **SetTargetMark4**
-   **SetTargetMark5**
-   **SetTargetMark6**
-   **SetTargetMark7**
-   **SetTargetMark8**
-   **DashForward**
-   **DashBackward**
-   **DashLeft**
-   **DashRight**
-   **Unused12**
-   **Unused13**
-   **ChatReply**
-   **ChatReWhisper**
-   **Unused14**
-   **Unused15**
-   **Unused16**
-   **Unused17**
-   **Unused18**
-   **Unused19**
-   **TargetNearestEnemy**
-   **TargetNearestFriend**
-   **Achievements**
-   **AuctionListings**
-   **Challenges**
-   **Unused10**
-   **FriendsList**
-   **Lore**
-   **Mail**
-   **Path**
-   **Reputation**
-   **Social**
-   **Tradeskills**
-   **DirectionalDash**
-   **PrimaryPetActionBar\_Slot1**
-   **PrimaryPetActionBar\_Slot2**
-   **PrimaryPetActionBar\_Slot3**
-   **PrimaryPetActionBar\_Slot4**
-   **PrimaryPetActionBar\_Slot5**
-   **PrimaryPetActionBar\_Slot6**
-   **GhostModeMap**
-   **Mount**
-   **UsePotion**
-   **Guild**
-   **StunBreakoutUp**
-   **StunBreakoutDown**
-   **StunBreakoutLeft**
-   **StunBreakoutRight**
-   **ExplicitMouseLookHold**
-   **Store**
-   **AccountInventory**
-   **CreddExchange**
-   **Collectibles**
-   **Contracts**
-   **HoloWardrobe**
-   **LevelUpUnlocks**
-   **Who**
-   **NonCombatAbilities**
-   **Macros**

------------------------------------------------------------------------

`Enum`

CodeEnumInputDevice
-------------------

-   **None**
-   **Keyboard**
-   **Mouse**

------------------------------------------------------------------------

`Enum`

CodeEnumInputEventType
----------------------

-   **Raw**
-   **Click**
-   **Hold**
-   **DoubleClick**
-   **DoubleHold**
-   **Rapid**

------------------------------------------------------------------------

`Enum`

CodeEnumInputKeyLookupGroup
---------------------------

-   **Main**
-   **StunBreakoutGameplay**
-   **Count**
-   **First**
-   **Last**

------------------------------------------------------------------------

`Enum`

CodeEnumInputModifier
---------------------

-   **Shift**
-   **Control**
-   **Alt**

------------------------------------------------------------------------

`Enum`

CodeEnumInputModifierScancode
-----------------------------

-   **LeftShift**
-   **LeftCtrl**
-   **LeftAlt**
-   **RightShift**
-   **RightCtrl**
-   **RightAlt**

------------------------------------------------------------------------

`Enum`

CodeEnumInputMouse
------------------

-   **Left**
-   **Right**
-   **Middle**
-   **X1**
-   **X2**
-   **WheelUp**
-   **WheelDown**

------------------------------------------------------------------------

`Enum`

CodeEnumInputSets
-----------------

-   **Default1**
-   **Default2**
-   **Default3**
-   **Account**
-   **Character**
-   **Count**

------------------------------------------------------------------------

`Enum`

CodeEnumItemSlots
-----------------

-   **Chest**
-   **Legs**
-   **Head**
-   **Shoulder**
-   **Feet**
-   **Hands**
-   **Tool**
-   **Weapon**
-   **Shields**
-   **Gadget**
-   **Attachment**
-   **System**
-   **Augment**
-   **Implant**

------------------------------------------------------------------------

`Enum`

CodeEnumMapOverlayType
----------------------

-   **Object**
-   **PathObjective**
-   **QuestObjective**
-   **TrackedUnit**
-   **Unit**

------------------------------------------------------------------------

`Enum`

CodeEnumMissType
----------------

-   **Dodge**

------------------------------------------------------------------------

`Enum`

CodeEnumMoveSpeed
-----------------

-   **Walk**
-   **Run**
-   **Sprint**

------------------------------------------------------------------------

`Enum`

CodeEnumPetStance
-----------------

-   **Assist**
-   **Stay**
-   **Passive**
-   **Defensive**
-   **Aggressive**

------------------------------------------------------------------------

`Enum`

CodeEnumRace
------------

-   **Human**
-   **Granok**
-   **Aurin**
-   **Draken**
-   **Mechari**
-   **Mordesh**
-   **Chua**

------------------------------------------------------------------------

`Enum`

CodeEnumRecallCommand
---------------------

-   **BindPoint**
-   **House**
-   **Illium**
-   **Thayd**
-   **Warplot**

------------------------------------------------------------------------

`Enum`

CodeEnumRewardRotationContentType
---------------------------------

-   **Dungeon**
-   **DungeonNormal**
-   **Expedition**
-   **None**
-   **PeriodicQuest**
-   **PvP**
-   **WorldBoss**

------------------------------------------------------------------------

`Enum`

CodeEnumRewardRotationItemType
------------------------------

-   **AccountCurrency**
-   **Currency**
-   **Item**
-   **None**

------------------------------------------------------------------------

`Enum`

CodeEnumRewardRotationRewardType
--------------------------------

-   **Essence**
-   **Item**
-   **Modifier**
-   **None**

------------------------------------------------------------------------

`Enum`

CodeEnumSetNavPointFailed
-------------------------

-   **Unknown**
-   **InMicro**

------------------------------------------------------------------------

`Enum`

CodeEnumStoryPanel
------------------

-   **Default**
-   **Low**
-   **Center**
-   **FullScreen**
-   **Whiteout**
-   **Urgent**
-   **FullScreenBlackNoFlash**
-   **Informational**

------------------------------------------------------------------------

`Enum`

CodeEnumStoryPanelStyle
-----------------------

-   **Default**
-   **Paper**
-   **Electronic**
-   **Eldan**
-   **Arcane**
-   **Natural**
-   **Exile**
-   **Dominion**

------------------------------------------------------------------------

`Enum`

CodeEnumTutorial
----------------

-   **Codex**
-   **CharacterPanel**
-   **AbilityWindow**
-   **Crafting\_UI\_Tutorial**
-   **Special\_Ability\_Chips**
-   **Tradeskill\_Codex\_Tutorial**
-   **Crafting\_Components\_Tutorial**
-   **Crafting\_Station\_Tutorial**
-   **Basic\_Salvaging\_Tutorial**
-   **QuestCommunicatorGiven**
-   **QuestAccepted**
-   **QuestAchieved**
-   **QuestBotched**
-   **QuestCommunicatorReceived**
-   **ChallengeUnlocked**
-   **ChallengeCompleted**
-   **ChallengeRewardPanel**
-   **AchievementCompleted**
-   **Telegraphs**
-   **NewBindpoint**
-   **Path\_MissionComplete**
-   **Path\_EpisodeComplete**
-   **Soldier\_MissionUnlock**
-   **Soldier\_TowerDefense**
-   **Soldier\_Assassinate**
-   **Soldier\_SWAT**
-   **Soldier\_Demolition**
-   **Soldier\_Rescue**
-   **Explorer\_MissionUnlock**
-   **Explorer\_Vista**
-   **Explorer\_ClaimTerritory**
-   **Explorer\_Door**
-   **Explorer\_ScavengerHunt**
-   **Explorer\_PowerMap**
-   **Scientist\_FieldStudy**
-   **Settler\_MissionUnlock**
-   **Settler\_Infrastructure**
-   **Settler\_DepotActivate**
-   **Death**
-   **Hazards**
-   **PublicEventStart**
-   **GalacticArchive\_NewEntry**
-   **Soldier\_StopTheThieves**
-   **Soldier\_WhackAMole**
-   **Farmer\_Powershrooms**
-   **General\_Quest\_SpellShortcut**
-   **CoordinateCrafting**
-   **CombatBuff**
-   **General\_Social**
-   **QuestCommunicatorMissed**
-   **MailMenu**
-   **CSI\_PressAndHold**
-   **CSI\_RapidTapping**
-   **CSI\_PrecisionTapping**
-   **CSI\_Memory**
-   **CSI\_KeyPad**
-   **CSI\_Metronome**
-   **QuestCommunicatorDeclined**
-   **General\_Lore**
-   **GroupFinderMenu**
-   **Renown**
-   **AMPs**
-   **Reputation**
-   **Housing\_Landscape**
-   **Housing\_House**
-   **Housing\_Crate**
-   **Housing\_Vendor**
-   **Housing\_Room**
-   **General\_CREDD**
-   **General\_AccountServices**
-   **Contracts**
-   **Path\_AbilityUnlock**
-   **Scientist\_MissionUnlock**
-   **LootDropped**
-   **AMPTab**
-   **InventoryBag**
-   **TradeskillsInventory**
-   **Discoveries**
-   **QuestGivingItem**
-   **QuestIntroduction**
-   **QuestCanAccept**
-   **AMPSave**
-   **LASSave**
-   **LASBuilder**
-   **CharacterWindow**
-   **MultipleQuests**
-   **CraftingPowerCore**
-   **CraftingSlotColor**
-   **CraftingSlotCharge**
-   **CraftingApSp**
-   **CraftingFailChance**
-   **AbandonCraft**
-   **Daze**

------------------------------------------------------------------------

`Enum`

CodeEnumTutorialAnchor
----------------------

-   **Codex**
-   **Inventory**
-   **None**
-   **Abilities**
-   **Character**
-   **Mail**
-   **GalacticArchive**
-   **Social**
-   **GroupFinder**
-   **Challenge**
-   **Datachron**
-   **AbilityBar**
-   **MiniMap**
-   **QuestTracker**
-   **HUDAlert**
-   **PressAndHold**
-   **RapidTapping**
-   **PrecisionTapping**
-   **Memory**
-   **Keypad**
-   **Metronome**
-   **ShieldBar**
-   **InnateAbility**
-   **DashMeter**
-   **SprintMeter**
-   **HealthBar**
-   **BuffFrame**
-   **ClassResource**
-   **QuestCommunicatorReceived**
-   **DatachronBody**
-   **Recall**
-   **InterruptArmor**
-   **Contracts**
-   **CraftingApSp**
-   **InterfaceMenuListCharacter**
-   **EquippedBags**
-   **TradeskillInventory**
-   **SalvageIcon**
-   **NPCInteraction**
-   **QuestIntroduction**
-   **QuestAccept**
-   **InterfaceMenuListInventory**
-   **InventoryItem**
-   **LASBuilderButton**
-   **LASSaveActionSetButton**
-   **LASAmpTabButton**
-   **LASAbilityTypeTab**
-   **LASAbilityTier**
-   **AbandonCraft**
-   **CraftingSlotColor**
-   **CraftingSlotCharge**
-   **CraftingPowerCore**
-   **CraftingFailChance**
-   **FloatingActionBar**
-   **FloatingActionBarBase**
-   **FloatingActionBarHorz**
-   **FloatingActionBarVert**
-   **PathAbility**
-   **FloatingActionBarSecondButton**
-   **FloatingActionBarFifthButton**
-   **PathTracker**
-   **PublicEventTracker**

------------------------------------------------------------------------

`Enum`

CodeEnumTutorialAnchorOrientation
---------------------------------

-   **North**
-   **Northeast**
-   **East**
-   **Southeast**
-   **South**
-   **Southwest**
-   **West**
-   **Northwest**

------------------------------------------------------------------------

`Enum`

CodeEnumTutorialCategory
------------------------

-   **General**
-   **Beginner**
-   **Combat**
-   **PVP**
-   **Housing**
-   **Challenges**
-   **PublicEvents**
-   **Adventures**
-   **Path\_Soldier**
-   **Path\_Settler**
-   **Path\_Scientist**
-   **Path\_Explorer**
-   **Class\_Warrior**
-   **Class\_Esper**
-   **Class\_Spellslinger**
-   **Class\_Stalker**
-   **Class\_Medic**
-   **Class\_Engineer**
-   **Class\_Charmer**
-   **Tradeskill\_Outfitter**
-   **Tradeskill\_Tailor**
-   **Tradeskill\_Architect**
-   **Tradeskill\_Miner**
-   **Tradeskill\_Augmentor**
-   **Tradeskill\_Survivalist**
-   **Tradeskill\_Farmer**
-   **Tradeskill\_Weaponsmith**
-   **Tradeskill\_Armorer**
-   **UNUSED12**
-   **UNUSED13**
-   **UNUSED14**
-   **UNUSED15**
-   **UNUSED16**
-   **UNUSED17**
-   **UNUSED18**
-   **UNUSED19**
-   **UNUSED20**
-   **UNUSED21**
-   **UNUSED22**
-   **UNUSED23**
-   **UNUSED24**
-   **UNUSED25**
-   **UNUSED26**
-   **UNUSED27**
-   **Tradeskills**
-   **Zones**
-   **Classes**

------------------------------------------------------------------------

`Enum`

CodeEnumUserText
----------------

-   **CharacterName**
-   **ScientistScanbotName**
-   **GuildName**
-   **GuildRankName**
-   **GuildBankTabName**
-   **HousingResidenceName**
-   **Chat**
-   **MailSubject**
-   **MailBody**
-   **ChatCustomChannelName**
-   **FriendshipNote**
-   **ReadyCheck**
-   **ChatCustomChannelPassword**
-   **GuildMessageOfTheDay**
-   **GuildMemberNote**
-   **GuildRercuitDescription**
-   **GuildInfoMessage**
-   **FriendshipAccountName**
-   **FriendshipAccountPrivateNote**
-   **FriendshipAccountPublicNote**
-   **FriendshipAccountEmail**
-   **FriendshipInviteNote**
-   **PlayerTicketText**
-   **GuildRecruitDescription**
-   **PlayerTicketSubject**

------------------------------------------------------------------------

`Enum`

CodeEnumUserTextFilterClass
---------------------------

-   **Strict**
-   **Standard**
-   **Low**

------------------------------------------------------------------------

`Enum`

CodeEnumVital
-------------

-   **Invalid**
-   **Health**
-   **Breath**
-   **ShieldCapacity**
-   **KineticCell**
-   **Resource0**
-   **Resource1**
-   **Resource2**
-   **Resource3**
-   **Resource4**
-   **Resource5**
-   **Resource6**
-   **StalkerA**
-   **StalkerB**
-   **StalkerC**
-   **Mana**
-   **Resource7**
-   **MedicCore**
-   **SpellSurge**
-   **InterruptArmor**
-   **Absorption**
-   **PublicResource0**
-   **PublicResource1**
-   **PublicResource2**
-   **Volatility**
-   **Resource8**
-   **Resource9**
-   **Resource10**
-   **Focus**

------------------------------------------------------------------------

`Enum`

CodeEnumWhoResult
-----------------

-   **OK**
-   **Partial**
-   **UnderCooldown**

------------------------------------------------------------------------

`Enum`

CodeEnumZoneCompletionType
--------------------------

-   **Challenge**
-   **Datacube**
-   **EpisodeQuest**
-   **Journal**
-   **Tale**
-   **TaskQuest**

------------------------------------------------------------------------

`Enum`

CodeEnumZonePvpRules
--------------------

-   **None**
-   **ExileStronghold**
-   **DominionStronghold**
-   **Sanctuary**
-   **Pvp**
-   **ExilePVPStronghold**
-   **DominionPVPStronghold**

------------------------------------------------------------------------

`Enum`

DisabledGameplaySystem
----------------------

-   **Mail**
-   **Store**
-   **Omnibits**
-   **FreeLevel50Promotion**
-   **GachaProbability**
-   **PremiumLockboxKeys**

------------------------------------------------------------------------

`Enum`

DuelStateDuelState
------------------

-   **None**
-   **WaitingToAccept**
-   **Pending**
-   **Dueling**

------------------------------------------------------------------------

`Enum`

GuildHolomark
-------------

-   **Left**
-   **Right**
-   **Back**

------------------------------------------------------------------------

`Enum`

HealthyGamingStatus
-------------------

-   **Normal**
-   **Fatigue**
-   **Unhealthy**

------------------------------------------------------------------------

`Enum`

LevelUpUnlock (Deprecated)
--------------------------

-   **Builder\_NewTierPoint**
-   **Builder\_LASSlot2**
-   **Character\_GearSlot\_Shield**
-   **WorldMapNewZone\_Deradune**
-   **WorldMapAdventure\_Astrovoid**
-   **Character\_GearSlot\_Implants**
-   **GroupFinder\_Dungeons**
-   **Character\_CostumeSlot6**
-   **Builder\_AMPPoint**
-   **Customization\_Mount**
-   **WorldMapNewZone\_Ellevar**
-   **Inventory\_Salvage**
-   **Character\_GearSlot\_Gloves**
-   **GroupFinder\_Warplots**
-   **WorldMapNewZone\_Malgrave**
-   **Builder\_LASSlot8**
-   **Builder\_LASSlot7**
-   **Builder\_LASSlot4**
-   **Builder\_AbilityTier2**
-   **WorldMapDungeon\_Stormtalon**
-   **WorldMapAdventure\_Galeras**
-   **Character\_GearSlot\_Shoulders**
-   **WorldMapDungeon\_KelVoreth**
-   **GroupFinder\_Arenas**
-   **Character\_GearSlot\_Gadgets**
-   **Customization\_Scanbot**
-   **WorldMapNewZone\_Grimvault**
-   **Character\_CostumeSlot2**
-   **WorldMapNewZone\_Wilderrun**
-   **Character\_CostumeSlot4**
-   **WorldMapAdventure\_Whitevale**
-   **Character\_GearSlot\_Helm**
-   **WorldMapNewZone\_Farside**
-   **WorldMapNewZone\_Algoroc**
-   **Builder\_LASSlot6**
-   **WorldMapNewZone\_NorthernWilds**
-   **Builder\_AbilityTier8**
-   **WorldMapNewZone\_EverstarGrove**
-   **WorldMapNewZone\_Whitevale**
-   **Character\_GearSlot\_WeaponAttachment**
-   **GroupFinder\_General**
-   **WorldMapDungeon\_Skullcano**
-   **WorldMapNewZone\_CrimsonIsle**
-   **WorldMapCapital\_Illium**
-   **Builder\_LASSlot5**
-   **Builder\_AbilityTier5**
-   **Character\_GearSlot\_SupportSystem**
-   **WorldMapAdventure\_Hycrest**
-   **Character\_CostumeSlot3**
-   **WorldMapNewZone\_LevianBay**
-   **Builder\_AbilityTier6**
-   **WorldMapNewZone\_Celestion**
-   **WorldMapNewZone\_Auroria**
-   **WorldMapAdventure\_NorthernWilds**
-   **Builder\_AbilityTier4**
-   **WorldMapNewZone\_Galeras**
-   **Builder\_AbilityTier3**
-   **Character\_CostumeSystem**
-   **WorldMapCapital\_Thayd**
-   **Builder\_LASSlot3**
-   **WorldMapAdventure\_Malgrave**
-   **Builder\_AMPSystem**
-   **Character\_CostumeSlot5**
-   **Builder\_TierPointSystem**
-   **Builder\_AbilityTier7**
-   **WorldMapDungeon\_SwordMaiden**
-   **GroupFinder\_Adventures**
-   **Character\_GearSlot\_RaidKey**
-   **Tradeskills**
-   **Runecrafting**
-   **WorldMapDungeon\_UltimateProtogames**
-   **WorldMapDungeon\_ProtogamesAcademyExile**
-   **WorldMapDungeon\_ProtogamesAcademyDominion**
-   **GroupFinder\_Expeditions**
-   **Expedition\_FragmentZero**
-   **Expedition\_OutpostM13**
-   **Expedition\_Infestation**
-   **Expedition\_RageLogic**
-   **Expedition\_SpaceMadness**
-   **Expedition\_DeepSpaceExploration**
-   **Expedition\_Gauntlet**
-   **Contracts**
-   **ActionSetBuilder**
-   **HoloWardrobe**
-   **Inventory**
-   **LevelUpUnlocks**

------------------------------------------------------------------------

`Enum`

LevelUpUnlockSystem (Deprecated)
--------------------------------

-   **Path**
-   **Level**

------------------------------------------------------------------------

`Enum`

LevelUpUnlockType (Deprecated)
------------------------------

-   **Dungeon\_New**
-   **Raid\_40**
-   **Adventure\_New**
-   **Content\_Capital**
-   **Content\_Feature**
-   **Class\_LAS\_Slot**
-   **General\_Expanded\_Feature**
-   **Class\_Feature**
-   **Class\_Attribute**
-   **Path\_ScanBot**
-   **Path\_Spell**
-   **Path\_Title**
-   **Gear\_Slot**
-   **Path\_Quest**
-   **Social\_Feature**
-   **Class\_Improvement**
-   **Raid\_20**
-   **Path\_Item**
-   **Class\_Tier**
-   **Class\_Ability**
-   **PvP\_Battleground**
-   **General\_Feature**
-   **Content\_Zone**
-   **PvP\_Feature**
-   **Shiphand\_New**

------------------------------------------------------------------------

`Enum`

MapZone
-------

-   **PublicEventIslandStage2**
-   **LevianBay**
-   **Thayd**
-   **Ellevar**
-   **halonring**
-   **Grimvault**
-   **Galeras**
-   **LevianBayStarComm1**
-   **EasternGrimvault**
-   **HalonRingIsland2**
-   **Malgrave**
-   **LevianBayStarComm3**
-   **WesternGrimvault**
-   **NorthernGrimvault**
-   **EverstarGrove**
-   **EternityIslands**
-   **Celestion**
-   **CrimsonIsle**
-   **Auroria**
-   **Illium**
-   **NorthernWilds**
-   **Wilderrun**
-   **LevianBayStarComm2**
-   **HalonRingIsland3**
-   **Whitevale**
-   **Algoroc**
-   **Deradune**
-   **TheDefileScreamingSword**
-   **HalonRingBCChamberofNurielDom**
-   **HalonRingBCChamberoftheEntityDom**
-   **BlighthavenChamberEarth**
-   **NorthernWildsExoLab729**
-   **HalonRingBCChamberofMadocExile**
-   **BlighthavenQueensDen**
-   **HalonRingBCCrystalCavernsExile**
-   **TheDefileResonanceTowerControlRoomDominion**
-   **TheDefileResonanceTowerControlRoomExile**
-   **HalonRingBCCrystalCavernsDominion**
-   **BlighthavenDecrepitExoLab**
-   **HalonRingBCDoomfarer**
-   **SouthernGrimvaultCreepingCaverns**
-   **HalonRingBCTerminiteMound**
-   **BlighthavenTransfusionChamber**
-   **BlighthavenChamberAir**
-   **BlighthavenRecontaminationRoom**
-   **HalonRingBCChamberofAradelExile**
-   **BlighthavenEmpyrealCaverns**
-   **HalonRingBCCaptainKrull**
-   **HalonRingBloodCrater**
-   **HalonRingBCChamberofAradelDom**
-   **SouthernGrimvaultEtherealCavity**
-   **HalonRingBCChamberofEnochDom**
-   **HalonRingBCChamberofEnochExile**
-   **TheDefileEmperorsDaughter**
-   **HalonRingBCRoughrockUnderground**
-   **HalonRingBCChamberofEshiaDom**
-   **BlighthavenDecontaminationRoom**
-   **TheDefileStrainMaw**
-   **SouthernGrimvaultStrainTunnels**
-   **SouthernGrimvaultEtherealHollow**
-   **BlighthavenGenesisChamber**
-   **BlighthavenChamberLife**
-   **HalonRingBCChamberoftheEntityExile**
-   **HalongRingBCCraterofCarnage**
-   **BlighthavenChamberWater**
-   **BlighthavenChamberLogic**
-   **BlighthavenChamberFire**
-   **HalonRingBCChamberofMadocDom**
-   **BlighthavenNurseryObservationRoom**
-   **HalonRingBCBli.mduckAbscess**
-   **BlighthavenNurseryChecpoint**
-   **BlighthavenMindoftheGlobellum**
-   **HalonRingBCChamberofEshiaExile**
-   **BlighthavenEtherealCaverns**
-   **BlighthavenAbandonedExoLab**
-   **HalonRingBCGoldenhandsReach**
-   **HalonRingBCChamberofNurielExile**
-   **HalonRingBCGrimvoidDreadvault**
-   **TheDefileBlackFocusEvacuationHub**
-   **HalonRingBCChamberofYuriaExile**
-   **NorthernWildsColdburrowCavern**
-   **HalonRingBCChamberofYuriaDom**

------------------------------------------------------------------------

`Enum`

RewardModifierOwner
-------------------

-   **None**
-   **Spell**
-   **System**
-   **PublicEvent**
-   **HybridTier**
-   **Entitlement**

------------------------------------------------------------------------

`Enum`

RewardProperty
--------------

-   **XP**
-   **CurrencyType**
-   **RewardTrackId**
-   **RewardTrackType**
-   **OmniBits**
-   **Reputation**
-   **OmnibitDropChance**

------------------------------------------------------------------------

`Enum`

RezType
-------

-   **WakeHere**
-   **Holocrypt**
-   **ExitInstance**
-   **SpellCasterLocation**
-   **WakeHereServiceToken**

------------------------------------------------------------------------

`Enum`

SharedChallengePreference (Deprecated)
--------------------------------------

-   **AutoAccept**
-   **Prompt**
-   **AutoReject**

------------------------------------------------------------------------

`Enum`

SupportStuckAction
-------------------------------

-   **RecallBind**
-   **RecallDeath**
-   **RecallHouse**

------------------------------------------------------------------------

`Enum`

TelegraphColorSet
-----------------

-   **Default**
-   **Deuteranopia**
-   **Protanopia**
-   **Tritanopia**
-   **Custom1**
-   **Custom2**

------------------------------------------------------------------------

`Function`

AcceptDuel()
------------

------------------------------------------------------------------------

`Function`

AreAnyItemsNew()
----------------

------------------------------------------------------------------------

`Function`

AreQuestUnitCalloutsVisible()
-----------------------------

------------------------------------------------------------------------

`Function`

AreSettlerStructureCalloutsVisible()
------------------------------------

------------------------------------------------------------------------

`Function`

AssignMasterLoot()
------------------

------------------------------------------------------------------------

`Function`

BuyBankBagSlot() (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Function`

CanDisembarkVehicle()
---------------------

------------------------------------------------------------------------

`Function`

CanDye()
--------

------------------------------------------------------------------------

`Function`

CanEditKeySet(nKeySet)
----------------------

### Description

Does a lua\_pushboolean if nKeySet is NOT any of the default 3 input key
sets.

### Params

-   **nKeySet** **(Integer)**

------------------------------------------------------------------------

`Function`

CanEquipBagItem()
-----------------

------------------------------------------------------------------------

`Function`

CanRepairAll()
--------------

------------------------------------------------------------------------

`Function`

CanSetNavPoint()
----------------

------------------------------------------------------------------------

`Function`

CanShowGuildHolomark()
----------------------

------------------------------------------------------------------------

`Function`

CanVacuum()
-----------

### Description

Does a lua\_pushboolean of GetCanVacuum.

------------------------------------------------------------------------

`Function`

Cheat\_MakeMeLevel50() (Deprecated)
-----------------------------------

------------------------------------------------------------------------

`Function`

ClearAllTargetMarkers()
-----------------------

------------------------------------------------------------------------

`Function`

ClearCityDirection()
--------------------

------------------------------------------------------------------------

`Function`

ClearNavPoint()
---------------

------------------------------------------------------------------------

`Function`

CodeEnumSetNavPointFailed() (Deprecated)
----------------------------------------

------------------------------------------------------------------------

`Function`

ConfirmPartialUnlock()
----------------------

------------------------------------------------------------------------

`Function`

CurrencyCap()
-------------

------------------------------------------------------------------------

`Function`

DeclineDuel()
-------------

------------------------------------------------------------------------

`Function`

DisableTutorialType()
---------------------

------------------------------------------------------------------------

`Function`

Disembark()
-----------

------------------------------------------------------------------------

`Function`

DoAnyItemsBeginQuest()
----------------------

------------------------------------------------------------------------

`Function`

DragDropDataToItemLocation(nData)
---------------------------------

### Description

Does a lua\_newtable with eType, nBagIndex, and nBagSlot.

### Params

-   **nData** **(Integer)**

------------------------------------------------------------------------

`Function`

DyeItems() (Deprecated)
-----------------------

------------------------------------------------------------------------

`Function`

EquipBagItem()
--------------

------------------------------------------------------------------------

`Function`

ForfeitDuel()
-------------

------------------------------------------------------------------------

`Function`

GetAbilityPoints()
------------------

------------------------------------------------------------------------

`Function`

GetAccountRealmCharacter() (Deprecated)
--------------------------

### Description

Returns a table of the players character name and the realm.

### Return Value

-   **tAccountRealm** **(Table)** - Table of character and realm information.
	-	**strCharacter** **(String)** - The players character name.
	-	**strRealm** **(String)** - The name of the realm.
------------------------------------------------------------------------

`Function`

GetAllTutorials()
-----------------

------------------------------------------------------------------------

`Function`

GetAllZoneCompletionMapZones()
------------------------------

------------------------------------------------------------------------

`Function`

GetAttributePoints()
--------------------

------------------------------------------------------------------------

`Function`

GetAvailableTargetMarkers()
---------------------------

------------------------------------------------------------------------

`Function`

GetBagItem()
------------

------------------------------------------------------------------------

`Function`

GetBindPoint()
--------------

------------------------------------------------------------------------

`Function`

GetCCStateStunTimeRemaining()
-----------------------------

------------------------------------------------------------------------

`Function`

GetCharacterList() (Deprecated)
-------------------------------

### Description

Does a lua\_newtable of a counter as an integer and a character name
list entry as a string.

------------------------------------------------------------------------

`Function`

GetCharInputKeySet(nCharIndex) (Deprecated)
-------------------------------------------

### Description

Runs the GetKeyBindingsFromTable specified by nCharIndex. Also does a
lua\_pushnil if a wait is needed for the server to reply for the key
binding list.

### Params

-   **nCharIndex** **(Integer)**

------------------------------------------------------------------------

`Function`

GetClassInnateAbilitySpells()
-----------------------------

------------------------------------------------------------------------

`Function`

GetClassName()
--------------

### Description

Does a localized lua\_pushwstring corresponding to nId from
DbFileTable\_Class\_GetByID, or nil if null.

### Return Value

-   **String**

------------------------------------------------------------------------

`Function`

GetControlledUnit()
-------------------

### Description

Returns a new unit that is a copy of the controlled unit, or nil if
null.

### Return Value

-   **[Unit](../Classes/Unit.md)**

------------------------------------------------------------------------

`Function`

GetCostumeCount() (Deprecated)
------------------------------

------------------------------------------------------------------------

`Function`

GetCostumeIndex() (Deprecated)
------------------------------

------------------------------------------------------------------------

`Function`

GetCostumeItem() (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Function`

GetCostumeItemIcon() (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Function`

GetCostumeUnlockLevel() (Deprecated)
------------------------------------

------------------------------------------------------------------------

`Function`

GetCredits()
------------

------------------------------------------------------------------------

`Function`

GetCurrentClassInnateAbilityIndex()
-----------------------------------

------------------------------------------------------------------------

`Function`

GetCurrentClassInnateAbilitySpell()
-----------------------------------

------------------------------------------------------------------------

`Function`

GetCurrentWorldId()
-------------------

------------------------------------------------------------------------

`Function`

GetCurrentZoneId()
------------------

------------------------------------------------------------------------

`Function`

GetCurrentZoneMap()
-------------------

------------------------------------------------------------------------

`Function`

GetCurrentZonePvpRules()
------------------------

------------------------------------------------------------------------

`Function`

GetCurrInputKeySet()
--------------------

### Description

Does a lua\_pushinteger of CurrInputSet.

------------------------------------------------------------------------

`Function`

GetDefaultRecallCommand()
-------------------------

------------------------------------------------------------------------

`Function`

GetDisabledGameplaySystems()
----------------------------

------------------------------------------------------------------------

`Function`

GetDuelOpponent()
-----------------

------------------------------------------------------------------------

`Function`

GetDuelState()
--------------

------------------------------------------------------------------------

`Function`

GetDyeCost()
------------

------------------------------------------------------------------------

`Function`

GetDyeUnlockLevel()
-------------------

------------------------------------------------------------------------

`Function`

GetEmptyInventorySlots()
------------------------

------------------------------------------------------------------------

`Function`

GetErrorCategories()
--------------------

------------------------------------------------------------------------

`Function`

GetFrameRate()
--------------

------------------------------------------------------------------------

`Function`

GetGadgetAbility()
------------------

------------------------------------------------------------------------

`Function`

GetGameCommand()
----------------

------------------------------------------------------------------------

`Function`

GetGameExitInfo()
-----------------

------------------------------------------------------------------------

`Function`

GetGameMode()
-------------

------------------------------------------------------------------------

`Function`

GetGameTime()
-------------

### Description

Does a lua\_pushdouble of GetGameTime / 1000.0 as a double.

------------------------------------------------------------------------

`Function`

GetGearScore()
--------------

------------------------------------------------------------------------

`Function`

GetGuildHolomarkDistance()
--------------------------

------------------------------------------------------------------------

`Function`

GetGuildHolomarkVisible()
-------------------------

------------------------------------------------------------------------

`Function`

GetHealthyGamingStatus()
------------------------

------------------------------------------------------------------------

`Function`

GetInputActionCategories()
--------------------------

### Description

Does a lua\_newtable with id, strName of action categories.

------------------------------------------------------------------------

`Function`

GetInputActionNameByEnum()
--------------------------

------------------------------------------------------------------------

`Function`

GetInputKeyNameText(inputKey)
-----------------------------

### Description

Does a lua\_pushwstring of the input key's name.

### Params

-   **inputKey** **(SInputKey)**

------------------------------------------------------------------------

`Function`

GetInputKeySet(nInputSet)
-------------------------

### Description

Runs the GetKeyBindingsFromTable specified by nInputSet. Also does a
lua\_pushnil if a wait is needed for the server to reply for the key
binding list.

### Params

-   **nInputSet** **(EInputKeySet)**

------------------------------------------------------------------------

`Function`

GetInstanceSettings()
---------------------

------------------------------------------------------------------------

`Function`

GetInteractHintArrowObject()
----------------------------

------------------------------------------------------------------------

`Function`

GetInteractiveUnit()
--------------------

### Description

Does a lua\_pushinteger of g\_game's ClosestInteractiveUnit.

------------------------------------------------------------------------

`Function`

GetKeyBinding()
---------------

------------------------------------------------------------------------

`Function`

GetKeyBindingByEnum()
---------------------

------------------------------------------------------------------------

`Function`

GetKeyBindings()
----------------

### Description

Does a lua\_newtable that describes the current key bindings.

------------------------------------------------------------------------

`Function`

GetKnownDyes()
--------------

------------------------------------------------------------------------

`Function`

GetLastTargetedPlayerName()
---------------------------

------------------------------------------------------------------------

`Function`

GetLatency()
------------

------------------------------------------------------------------------

`Function`

GetLevelCap()
-------------

------------------------------------------------------------------------

`Function`

GetLevelUpFanfareDuration()
---------------------------

------------------------------------------------------------------------

`Function`

GetLevelUpUnlock()
------------------

------------------------------------------------------------------------

`Function`

GetLevelUpUnlockTypes()
-----------------------

------------------------------------------------------------------------

`Function`

GetLocalTime()
--------------

### Description

Does a lua\_newtable with year, month, day, dayOfWeek, hour, minute,
second.

------------------------------------------------------------------------

`Function`

GetLootRolls()
--------------

------------------------------------------------------------------------

`Function`

GetMasterLoot()
---------------

------------------------------------------------------------------------

`Function`

GetMoneyTradeLimit()
--------------------

------------------------------------------------------------------------

`Function`

GetMountList() (Deprecated)
---------------------------

------------------------------------------------------------------------

`Function`

GetNavPoint()
-------------

------------------------------------------------------------------------

`Function`

GetNavPointChatLinkString()
---------------------------

------------------------------------------------------------------------

`Function`

GetNearestRapidTransportNodeForWorldLocation()
----------------------------------------------

------------------------------------------------------------------------

`Function`

GetNextBankBagCost() (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Function`

GetNumBankBagSlots()
--------------------

------------------------------------------------------------------------

`Function`

GetNumClassInnateAbilitySpells()
--------------------------------

------------------------------------------------------------------------

`Function`

GetNumInventoryBagSlots()
-------------------------

------------------------------------------------------------------------

`Function`

GetOmnibitsBonusInfo()
----------------------

------------------------------------------------------------------------

`Function`

GetPendingLevelUpUnlocks()
--------------------------

------------------------------------------------------------------------

`Function`

GetPendingRemovalWarningRemaining()
-----------------------------------

------------------------------------------------------------------------

`Function`

GetPendingTutorials()
---------------------

------------------------------------------------------------------------

`Function`

GetPetDismissCommand()
----------------------

------------------------------------------------------------------------

`Function`

GetPingTime()
-------------

------------------------------------------------------------------------

`Function`

GetPlayerBaseFaction()
----------------------

------------------------------------------------------------------------

`Function`

GetPlayerBuffWindowProperties()
-------------------------------

------------------------------------------------------------------------

`Function`

GetPlayerCharacterName()
------------------------

------------------------------------------------------------------------

`Function`

GetPlayerCurrency(nType)
------------------------

### Description

Returns a new LuaGameTypes\_Money that is a copy of nType's money value.

### Params

-   **nType** **(ECurrencyType)**

------------------------------------------------------------------------

`Function`

GetPlayerDeathState()
---------------------

------------------------------------------------------------------------

`Function`

GetPlayerGenericVehicleUnit()
-----------------------------

------------------------------------------------------------------------

`Function`

GetPlayerLevel()
----------------

------------------------------------------------------------------------

`Function`

GetPlayerMountUnit()
--------------------

### Description

Returns a new unit that is a copy of the mount unit, else 1 and nil if
null.

### Return Value

-   **[Unit](../Classes/Unit.md)**

------------------------------------------------------------------------

`Function`

GetPlayerPets()
---------------

------------------------------------------------------------------------

`Function`

GetPlayerRewardProperties() (Deprecated)
----------------------------------------

------------------------------------------------------------------------

`Function`

GetPlayerRewardProperty() (Deprecated)
--------------------------------------

------------------------------------------------------------------------

`Function`

GetPlayerTaxiUnit()
-------------------

### Description

Returna the taxi that the player is currently on.

### Return Value

-   **[Unit](../Classes/Unit.md)** - The taxi that the player is riding

------------------------------------------------------------------------

`Function`

GetPlayerUnit()
---------------

### Description

Returns a new unit that is a copy of the character unit, or nil if null.

### Return Value

-   **[Unit](../Classes/Unit.md)**

------------------------------------------------------------------------

`Function`

GetPlayerUnitByName()
---------------------

------------------------------------------------------------------------

`Function`

GetPlayerVehicleUnit()
----------------------

### Description

Returns a new unit that is a copy of the vehicle unit, else 1 and nil if
null.

### Return Value

-   **[Unit](../Classes/Unit.md)**

------------------------------------------------------------------------

`Function`

GetPrimeLevelAchieved()
-----------------------

------------------------------------------------------------------------

`Function`

GetPrimeLevelsAchieved()
------------------------

------------------------------------------------------------------------

`Function`

GetPvpFlagInfo()
----------------

------------------------------------------------------------------------

`Function`

GetRapidTransportCooldown()
---------------------------

------------------------------------------------------------------------

`Function`

GetRapidTransportDestinationsForWorld()
---------------------------------------

------------------------------------------------------------------------

`Function`

GetRealmName()
--------------

### Description

Does a lua\_pushwstring of GetRealmName.

------------------------------------------------------------------------

`Function`

GetRepairAllCost()
------------------

------------------------------------------------------------------------

`Function`

GetReputationInfo()
-------------------

------------------------------------------------------------------------

`Function`

GetReputationLevels()
---------------------

------------------------------------------------------------------------

`Function`

GetRewardPropertyName() (Deprecated)
------------------------------------

------------------------------------------------------------------------

`Function`

GetRewardRotation(nContentId, bIsVeteran)
-----------------------------------------

### Description

Returns the arRewards from **GameLib.GetRewardRotations()** for a
specified **nContentId**.

### Params

-   **nContentId** **(Integer)**
-	**bIsVeteran** **(Boolean)** - This is required for those ContentId's,
	that contain a bIsVeteran variable in **GameLib.GetRewardRotations()**.
	**false** or **nil** for those, without the variable.

### Return Value

-	**arRewards** **(Table/Array)** - Array of all rewards granted
	for this **nContentId**. This array can contain more rewards
	than expected and could be outdated.
	-	**monReward** **([Money](../Classes/Money.md))** - The money
		object for this reward. This is a AccountCurrency.
	-	**nRewardType** **(CodeEnumRewardRotationRewardType)** - The type
		of this reward. Usually Modifier or Essence.
	-	**nRewardItemType** **(CodeEnumRewardRotationItemType)** - Usually
		AccountCurrency.
	-	**bGranted** **(Boolean)** - Whether or not this reward has
		been granted already.
	-	**nSecondsRemaining** **(Integer)** - The seconds till this
		reward will run out.
	-	**strIcon** **(String)** - The sprite name for the rewards icon

------------------------------------------------------------------------

`Function`

GetRewardRotations()
--------------------

### Description

Returns a array of all reward rotations categorized by
**nContentId**

### Return Value

-   **tRewardRotations** **(Table/Array)** - Array of informations about
	their specific **nContentId**.
	-	**nContentId** **(Integer)**
	-	**nContentType** **(CodeEnumRewardRotationContentType)**
	-	**arRewards** **(Table/Array)** - Array of all rewards granted
		for this **nContentId**. This array can contain more rewards
		than expected and could be outdated.
		-	**monReward** **([Money](../Classes/Money.md))** - The money
			object for this reward. This is a AccountCurrency.
		-	**nRewardType** **(CodeEnumRewardRotationRewardType)** - The type
			of this reward. Usually Modifier or Essence.
		-	**nRewardItemType** **(CodeEnumRewardRotationItemType)** - Usually
			AccountCurrency.
		-	**bGranted** **(Boolean)** - Whether or not this reward has
			been granted already.
		-	**nSecondsRemaining** **(Integer)** - The seconds till this
			reward will run out.
		-	**strIcon** **(String)** - The sprite name for the rewards icon
	-	**bIsVeteran** **(Boolean)** - Whether or not these Rewards
		apply to the veteran version of the instance. This variable does
		only exist for **nContentType** Dungeon, DungeonNormal and
		Expedition.
	-	**strWorld** **(String)** - The localized instance name. This
		variable does only exist for **nContentType** Dungeon, Expedition
		and PvP.
	-	**strZoneName** **(String)** - The localized zone name. This
		variable does only exist for **nContentType** PeriodicQuest
	-	**peWorldBoss** **([PublicEvent](../Classes/PublicEvent.md))** - The Event
		of the Worldboss. This variable does only exist for
		**nContentType** WorldBoss.
	-	**eMatchType** **([MatchMakingLib.MatchType](../Classes/MatchingGame.md))** - The Type
		of Match. Usually **MatchType.Dungeon**. This variable does only
		exist for **nContentType** DungeonNormal.

------------------------------------------------------------------------

`Function`

GetServerTime()
---------------

------------------------------------------------------------------------

`Function`

GetShortcutMount()
------------------

------------------------------------------------------------------------

`Function`

GetShortcutPotion()
-------------------

------------------------------------------------------------------------

`Function`

GetSpell()
----------

------------------------------------------------------------------------

`Function`

GetSpellThresholdTimePrcntDone()
--------------------------------

------------------------------------------------------------------------

`Function`

GetStuckCooldowns()
-------------------

### Description

Returns the cooldowns of the different unstuck methods.

### Return Value

-  **arSupportStuckAction** - The returned array has a table for each [SupportStuckAction](#supportstuckaction) entry with their cooldown.
    - **Table**
        - **fCooldownPercent** **(Float)** - How much of the cooldown time has passed from 0.0 to 1.0.
        - **fCooldownTime** **(Float)** - Remaining cooldown time in seconds.


### Usage/Example

```lua
local tCooldowns = GameLib.GetStuckCooldowns()
local fDeathCooldownTime = tCooldowns[GameLib.SupportStuckAction.RecallDeath].fCooldownTime
```

------------------------------------------------------------------------

`Function`

GetTargetMarkerIcon()
---------------------

------------------------------------------------------------------------

`Function`

GetTargetUnit()
---------------

### Description

Returns a new unit that is a copy of the target unit, else 0 if null.

### Return Value

-   **[Unit](../Classes/Unit.md)**

------------------------------------------------------------------------

`Function`

GetTaxisForWorld()
------------------

------------------------------------------------------------------------

`Function`

GetTeleportIlliumSpell()
------------------------

------------------------------------------------------------------------

`Function`

GetTeleportThaydSpell()
-----------------------

------------------------------------------------------------------------

`Function`

GetTextTypeMaxLength()
----------------------

------------------------------------------------------------------------

`Function`

GetTickCount()
--------------

### Description

Does a lua\_pushint of GetTickCount casted as an integer.

------------------------------------------------------------------------

`Function`

GetTotalAbilityPoints()
-----------------------

------------------------------------------------------------------------

`Function`

GetTotalInventorySlots()
------------------------

------------------------------------------------------------------------

`Function`

GetTutorial()
-------------

------------------------------------------------------------------------

`Function`

GetTutorialAnchorInfo()
-----------------------

------------------------------------------------------------------------

`Function`

GetTutorialLayouts()
--------------------

------------------------------------------------------------------------

`Function`

GetTutorialPopupContext()
-------------------------

------------------------------------------------------------------------

`Function`

GetTutorialsForCategory()
-------------------------

------------------------------------------------------------------------

`Function`

GetTutorialVisibilityFlags()
----------------------------

------------------------------------------------------------------------

`Function`

GetUnitById()
-------------

------------------------------------------------------------------------

`Function`

GetUnitScreenPosition()
-----------------------

------------------------------------------------------------------------

`Function`

GetUnknownDyes()
----------------

------------------------------------------------------------------------

`Function`

GetUnlockedLevelCap()
---------------------

------------------------------------------------------------------------

`Function`

GetUnlocksForLevel()
--------------------

------------------------------------------------------------------------

`Function`

GetUnlocksForType()
-------------------

------------------------------------------------------------------------

`Function`

GetVanityPetList() (Deprecated)
-------------------------------

------------------------------------------------------------------------

`Function`

GetVersionInfo()
----------------

------------------------------------------------------------------------

`Function`

GetWorldCompletionPercent()
---------------------------

------------------------------------------------------------------------

`Function`

GetWorldDifficulty()
--------------------

------------------------------------------------------------------------

`Function`

GetWorldHeroismMenaceLevel()
----------------------------

------------------------------------------------------------------------

`Function`

GetWorldMaxPrimeLevel()
-----------------------

------------------------------------------------------------------------

`Function`

GetWorldPrimeLevel()
--------------------

------------------------------------------------------------------------

`Function`

GetWorldTimeOfDay()
-------------------

### Description

Does a lua\_pushdouble of GetWorldTimeOfDay as a double. (This is not
divided by 1000.0)

------------------------------------------------------------------------

`Function`

GetWorldTooltipContainer()
--------------------------

------------------------------------------------------------------------

`Function`

GetXpBonusData(nWho)
--------------------

### Description

Does a lua\_newtable that describes an xp bonus.

### Params

-   **nWho** **(Integer)**

------------------------------------------------------------------------

`Function`

GetZoneCompletion()
-------------------

------------------------------------------------------------------------

`Function`

GetZoneCompletionTypes()
------------------------

------------------------------------------------------------------------

`Function`

GetZoneExplorationPercent()
---------------------------

------------------------------------------------------------------------

`Function`

GetZoneMap()
------------

------------------------------------------------------------------------

`Function`

HasBindPoint()
--------------

------------------------------------------------------------------------

`Function`

HasTutorialSound()
------------------

------------------------------------------------------------------------

`Function`

HasXPBonus()
------------

------------------------------------------------------------------------

`Function`

InitiateDuel()
--------------

------------------------------------------------------------------------

`Function`

InitiatePTRCharacterCopy()
--------------------------

------------------------------------------------------------------------

`Function`

InRatedPvpMatch()
-----------------

------------------------------------------------------------------------

`Function`

InvokePreOrder() (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Function`

IsCharacterLoaded()
-------------------

### Description

Does a lua\_pushboolean of g\_game's IsLoaded as a boolean.

------------------------------------------------------------------------

`Function`

IsControlledUnit()
------------------

### Description

Does a lua\_pushboolean whether pUnit is equal to GetControlledUnit.\
Parameter:\
unitToCheck: CUnit

------------------------------------------------------------------------

`Function`

IsCostumeSlotVisible() (Deprecated)
-----------------------------------

------------------------------------------------------------------------

`Function`

IsCurrentInnateAbilityActive()
------------------------------

------------------------------------------------------------------------

`Function`

IsIgnoringDuelRequests()
------------------------

------------------------------------------------------------------------

`Function`

IsInLocation()
--------------

------------------------------------------------------------------------

`Function`

IsInWorldZone()
---------------

------------------------------------------------------------------------

`Function`

IsKeyBindable()
---------------

------------------------------------------------------------------------

`Function`

IsLevelUpUnlockViewed()
-----------------------

------------------------------------------------------------------------

`Function`

IsMouseLockOn()
---------------

------------------------------------------------------------------------

`Function`

IsNavPointSet()
---------------

------------------------------------------------------------------------

`Function`

IsNeedRollAllowed()
-------------------

------------------------------------------------------------------------

`Function`

IsOverdriveActive()
-------------------

------------------------------------------------------------------------

`Function`

IsPrivilegeRestricted()
-----------------------

------------------------------------------------------------------------

`Function`

IsPvpFlagged()
--------------

------------------------------------------------------------------------

`Function`

IsPvpServer()
-------------

------------------------------------------------------------------------

`Function`

IsSpellSurgeActive()
--------------------

------------------------------------------------------------------------

`Function`

IsTextValid()
-------------

------------------------------------------------------------------------

`Function`

IsTutorialCategoryVisible()
---------------------------

------------------------------------------------------------------------

`Function`

IsTutorialNoPageAlert()
-----------------------

------------------------------------------------------------------------

`Function`

IsTutorialViewed()
------------------

------------------------------------------------------------------------

`Function`

IsTutorialZone()
----------------

------------------------------------------------------------------------

`Function`

IsZoneInZone()
--------------

------------------------------------------------------------------------

`Function`

ItemLocationToDragDropData(nLocationType, nBagIndex, nBagSlot)
--------------------------------------------------------------

### Description

Does a lua\_pushinteger of GetDragDropData specified by nLocationType,
nBagIndex, and nBagSlot.

### Params

-   **nLocationType** **(Integer for enum EInventoryLocation)**
-   **nBagIndex** **(Integer)**
-   **nBagSlot** **(EBagSlot)**

------------------------------------------------------------------------

`Function`

LeavePendingRemovalInstance()
-----------------------------

------------------------------------------------------------------------

`Function`

MarkCityDirection()
-------------------

------------------------------------------------------------------------

`Function`

MarkLevelUpUnlockViewed()
-------------------------

------------------------------------------------------------------------

`Function`

MarkTutorialViewed()
--------------------

------------------------------------------------------------------------

`Function`

OnClosedInstanceSettings()
--------------------------

------------------------------------------------------------------------

`Function`

OpenAccountInventory()
----------------------

------------------------------------------------------------------------

`Function`

OpenFortunes()
--------------

------------------------------------------------------------------------

`Function`

OpenStore()
-----------

------------------------------------------------------------------------

`Function`

PassOnLoot()
------------

------------------------------------------------------------------------

`Function`

PauseGameActionInput(bPaused)
-----------------------------

### Description

Runs the PauseGameAction with bPaused.

### Params

-   **bPaused** **(Boolean)**

------------------------------------------------------------------------

`Function`

PlayTutorialSound()
-------------------

------------------------------------------------------------------------

`Function`

PrepareInfractionReport()
-------------------------

------------------------------------------------------------------------

`Function`

RefreshCustomTelegraphColors()
------------------------------

------------------------------------------------------------------------

`Function`

ReplayLevelUp()
---------------

------------------------------------------------------------------------

`Function`

ReportBug()
-----------

------------------------------------------------------------------------

`Function`

RequestRewardUpdate()
---------------------

------------------------------------------------------------------------

`Function`

ResetAttributePoints()
----------------------

------------------------------------------------------------------------

`Function`

ResetLevelUpUnlocks()
---------------------

------------------------------------------------------------------------

`Function`

ResetSingleInstance()
---------------------

------------------------------------------------------------------------

`Function`

ResetTutorials()
----------------

------------------------------------------------------------------------

`Function`

RollOnLoot()
------------

------------------------------------------------------------------------

`Function`

SalvageKeyCount()
-----------------

------------------------------------------------------------------------

`Function`

SearchRelationshipStatusByCharacterName()
-----------------------------------------

------------------------------------------------------------------------

`Function`

SetCostumeIndex() (Deprecated)
------------------------------

------------------------------------------------------------------------

`Function`

SetCostumeItem() (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Function`

SetCostumeSlotVisible() (Deprecated)
------------------------------------

------------------------------------------------------------------------

`Function`

SetCurrentClassInnateAbilityIndex()
-----------------------------------

------------------------------------------------------------------------

`Function`

SetCurrInputKeySet(nInputSet)
-----------------------------

### Description

Does an update of InputSet specified by nInputSet. Also does a
lua\_pushboolean of false if a wait is needed for the server to reply
for the key binding list.

### Params

-   **nInputSet** **(EInputKeySet)**

------------------------------------------------------------------------

`Function`

SetDefaultRecallCommand()
-------------------------

------------------------------------------------------------------------

`Function`

SetIgnoreDuelRequests()
-----------------------

------------------------------------------------------------------------

`Function`

SetInstanceSettings()
---------------------

------------------------------------------------------------------------

`Function`

SetInteractHintArrowObject()
----------------------------

------------------------------------------------------------------------

`Function`

SetKeyBindings(tInputTable) (Deprecated)
----------------------------------------

### Description

Runs the SaveInputKeySet after updating the key bindings table.

### Params

-   **tInputTable** **(LuaTable)**

------------------------------------------------------------------------

`Function`

SetMouseLock() (Deprecated)
---------------------------

------------------------------------------------------------------------

`Function`

SetNavPoint()
-------------

------------------------------------------------------------------------

`Function`

SetSharedChallengePreference()
------------------------------

------------------------------------------------------------------------

`Function`

SetShortcutMount()
------------------

------------------------------------------------------------------------

`Function`

SetShortcutPotion()
-------------------

------------------------------------------------------------------------

`Function`

SetTargetUnit(pUnitToSelect)
----------------------------

### Description

Runs the set target id method on pUnitToSelect's unit id.

### Params

-   **pUnitToSelect** **(CUnit)**

------------------------------------------------------------------------

`Function`

SetWorldTooltipContainer()
--------------------------

------------------------------------------------------------------------

`Function`

ShowGuildHolomark()
-------------------

------------------------------------------------------------------------

`Function`

ShowNavPointHintArrow()
-----------------------

------------------------------------------------------------------------

`Function`

ShowUI()
--------

------------------------------------------------------------------------

`Function`

SpendAttributePoints()
----------------------

------------------------------------------------------------------------

`Function`

StopTutorialSound()
-------------------

------------------------------------------------------------------------

`Function`

SummonVanityPet()
-----------------

------------------------------------------------------------------------

`Function`

SupportStuck(eSupportStuckAction)
--------------
### Description

To free a player that got stuck in different ways there are 3 provided ways to make them unstuck:
* Recall transmat cast to teleport you back to your saved location.
* Recall housing cast to teleport you to your housing plot.
* Kill the player so they can revive at the closest holocrypt.

### Params

-   **eSupportStuckAction** **([SupportStuckAction](#supportstuckaction))** - What method to unstuck the player should be used, represented in the enum.

### Example

```lua
GameLib.SupportStuck(GameLib.SupportStuckAction.RecallDeath)
```

------------------------------------------------------------------------

`Function`

SwapBagItems()
--------------

------------------------------------------------------------------------

`Function`

TogglePvpFlags()
----------------

------------------------------------------------------------------------

`Function`

ToggleQuestUnitCallouts()
-------------------------

------------------------------------------------------------------------

`Function`

ToggleSettlerStructureCallouts()
--------------------------------

------------------------------------------------------------------------

`Function`

ToggleTutorialVisibilityFlags()
-------------------------------

------------------------------------------------------------------------

`Function`

UIExitCinematics()
------------------

### Description

Runs g\_game's UIExitCinematicsMode method with 100 as the parameter.

------------------------------------------------------------------------

`Function`

UIStartCinematics()
-------------------

### Description

Runs g\_game's UIEnterCinematicsMode method.

------------------------------------------------------------------------

`Function`

WhiteOutFadeIn()
----------------

### Description

Runs g\_game's WhiteOutFadeIn method.

------------------------------------------------------------------------

`Function`

WhiteOutFadeOut()
-----------------

### Description

Runs g\_game's WhiteOutFadeOut method with 3000 as the parameter.

------------------------------------------------------------------------

`Function`

WorldLocToScreenPoint(vecWorldPosition)
-----------------------

### Description

Calculates the screen pixel position from a world location.

### Params

-	**vecWorldPosition** **([Vector3](../Classes/Vector3.md))** - The world location.

### Return Value

-	**[Vector3](../Classes/Vector3.md)** - Screen pixel position of the world location.
