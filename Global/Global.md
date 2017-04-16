Global (Deprecated)
===================

------------------------------------------------------------------------

`Event`

AbilitiesWindowClose
--------------------

### Description

Fires when the Limited Action Set Builder window closes.

### Params

-   **bAtTrainer** **(Boolean)** - Returns whether or not the player is
    at a training station when the window was closed.

------------------------------------------------------------------------

`Event`

AbilityBookChange
-----------------

### Description

Fires when a change is made to the Action Set Builder.

------------------------------------------------------------------------

`Event`

AcceptProgressInput
-------------------

### Description

Fires when CSIs turn player input on and off. This is only used for the
"Memory" CSI.

### Params

-   **bShouldAccept** **(Boolean)** - Whether or not the CSI will accept
    user input.

------------------------------------------------------------------------

`Event`

AccountCurrencyChanged
----------------------

------------------------------------------------------------------------

`Event`

AccountEntitlementUpdate
------------------------

### Description

Fires when a change is made to the current account's entitlements.

### Usage/Example

```lua
    function AccountInventory:OnAccountEntitlementUpdate()
        if not self.wndMain or not self.wndMain:IsValid() then
            return
        end
        self:RefreshEntitlements()
    end
```

------------------------------------------------------------------------

`Event`

AccountInventoryUpdate
----------------------

### Description

Fires when the Account Inventory for the current account has changed.

------------------------------------------------------------------------

`Event`

AccountInventoryWindowShow
--------------------------

------------------------------------------------------------------------

`Event`

AccountOperationResults
-----------------------

### Params

-   **eOperation** **(Integer)**
-   **eResult** **(CREDDExchangeLib.CodeEnumAccountOperationResult)** -
    The result of the operation.

------------------------------------------------------------------------

`Event`

AccountPendingItemsUpdate
-------------------------

### Description

Fires when items are added or removed from the pending list for the
player's account inventory.

------------------------------------------------------------------------

`Event`

AccountPrivilegeRestrictionUpdate
---------------------------------

------------------------------------------------------------------------

`Event`

AccountSupportTicketResult
--------------------------

### Description

Informs the player if the ticket that they submitted successfully made
it to the server or not.

### Params

-   **channelGM** **(Channel)** - The chat channel where the message
    will be displayed.
-   **bSuccess** **(Boolean)** - Whether or not the ticket was
    successfully sent.

### Usage/Example

```lua
    function ChatLog:OnAccountSupportTicketResult( channelSource, bSuccess )
        if( bSuccess ) then
            ChatSystemLib.PostOnChannel(ChatSystemLib.ChatChannel_System, Apollo.GetString("PlayerTicket_TicketSent"), "")
        else
            ChatSystemLib.PostOnChannel(ChatSystemLib.ChatChannel_System, Apollo.GetString("PlayerTicket_TicketFailed"), "")
        end
    end
```

------------------------------------------------------------------------

`Event`

AchievementGranted
------------------

### Description

Fires when an achievement is completed.

### Params

-   **achComplete** **([Achievement](../Classes/Achievement.md))** -
    The achievement that was completed.

------------------------------------------------------------------------

`Event`

AchievementUpdated
------------------

### Description

Fires when an progress is made towards an achievement's objective.

### Params

-   **achUpdated** **([Achievement](../Classes/Achievement.md))** - The
    achievement that has been updated.

### Usage/Example

```lua
    function Achievements:OnAchievementUpdated(achUpdated)
        if not self.wndMain then
            return
        end

        if self.wndMain:FindChild("RightSummaryScreen"):IsShown() then
            self:LoadSummaryScreen()
        else
            local wndRightScroll = self.wndMain:FindChild("RightScroll")
            local nVScrollPos = wndRightScroll:GetVScrollPos()
            self:BuildRightPanel()
            wndRightScroll:SetVScrollPos(nVScrollPos)
        end
        self.wndMain:FindChild("BGLeft:HeaderPointsNumber"):SetText(AchievementsLib.GetAchievementPoints())
        self.wndMain:FindChild("BGLeft:HeaderPoints"):SetText(String_GetWeaselString(Apollo.GetString("Achievement_OverallPoints")))
    end
```

------------------------------------------------------------------------

`Event`

ActionBarDescriptionSpell
-------------------------

### Description

Displays information for a spell on the actionbar.

### Params

-   **splDisplayed** **([Spell](../Classes/Spell.md))** - The spell
    currently being displayed.
-   **tEffects** **(Table)** - A table containing information about the
    spell.
    -   **sprite** **(String)** - The name of the sprite for the spell
    -   **textString** **(String)** - The spell's description
    -   **countString** **(String)** - The number of charges for the
        spell
    -   **globalCooldown** **(Boolean)** - Whether or not the spell is
        affected by the Global Cooldown
    -   **cooldownPercent** **(Float)**
    -   **cooldownTime** **(Integer)** - The number of milliseconds in
        the spell's cooldown
    -   **casting** **(Boolean)** - Whether or not the spell is being
        cast
    -   **radarSweep** **(Boolean)**
    -   **popIcon** **(Boolean)**
    -   **readyBlingSprite** **(Boolean)**
    -   **blur** **(Boolean)**
    -   **shake** **(Boolean)**
    -   **shatterSprite** **(Boolean)**
    -   **itemUnavailable** **(Boolean)**
    -   **textColor** **([CColor](../Classes/CColor.md))** - The color
        of the description text
    -   **diffuse** **([CColor](../Classes/CColor.md))** - The spell's
        diffuse color
    -   **saturation** **(Float)**
    -   **lightOverlay** **(Boolean)**
    -   **diffused** **(Boolean)**
    -   **indicatorSprite** **(Boolean)**
-   **tReasons** **(Table)** - A list of flags that may be referenced by
    Lua.

------------------------------------------------------------------------

`Event`

ActionBarNonSpellShortcutAddFailed
----------------------------------

### Description

Fires when a non-spell fails to be placed on the action bar.

### Usage/Example

```lua
    function FloatText:OnActionBarNonSpellShortcutAddFailed()
        local strMessage = Apollo.GetString("FloatText_ActionBarAddFail")
        self:OnSpellCastFailed( LuaEnumMessageType.GenericPlayerInvokedError, nil, GameLib.GetControlledUnit(), GameLib.GetControlledUnit(), strMessage )
    end
```

------------------------------------------------------------------------

`Event`

ActionSetError
--------------

### Description

Fires when the player attempts to save an invalid action set.

### Params

-   **eResult** **(ActionSetLib.CodeEnumLimitedActionSetResult)** - The
    message describing why there is an error in the current action set.

### Usage/Example

```lua
    function Abilities:OnActionSetError(eResult)
        local strMessage = nil  
        if eResult == ActionSetLib.CodeEnumLimitedActionSetResult.InVoid then
            strMessage = Apollo.GetString("ActionSet_Error_InTheVoid")
        end

        if strMessage then      
            self:BuildWindow() -- This can happen after the set has "successfully" closed, so bring it back up if closed
            self:HelperShowError(strMessage)
        end
    end
```

------------------------------------------------------------------------

`Event`

ActivateCCStateStun
-------------------

### Description

Fires when the player is stunned.

### Params

-   **eChosenDirection** **(Unit.CodeEnumCCStateStunVictimGameplay)** -
    The direction the player needs to press to get out of the CC State.

### Usage/Example

```lua
    function CrowdControlGameplay:OnActivateCCStateStun(eChosenDirection)
        self.wndProgress = Apollo.LoadForm(self.xmlDoc, "ButtonHit_Progress", nil, self)
        self.wndProgress:Show(true) -- to get the animation
        self.wndProgress:FindChild("TimeRemainingContainer"):Show(false)

        local bLeft     = eChosenDirection == Unit.CodeEnumCCStateStunVictimGameplay.Left
        local bUp       = eChosenDirection == Unit.CodeEnumCCStateStunVictimGameplay.Forward
        local bRight    = eChosenDirection == Unit.CodeEnumCCStateStunVictimGameplay.Right
        local bDown     = eChosenDirection == Unit.CodeEnumCCStateStunVictimGameplay.Backward

        -- TODO: Swap to Stun Breakout Keys when they exist
        self.wndProgress:FindChild("ProgressButtonArtLeft"):SetText(GameLib.GetKeyBinding("StunBreakoutLeft"))
        self.wndProgress:FindChild("ProgressButtonArtUp"):SetText(GameLib.GetKeyBinding("StunBreakoutUp"))
        self.wndProgress:FindChild("ProgressButtonArtRight"):SetText(GameLib.GetKeyBinding("StunBreakoutRight"))
        self.wndProgress:FindChild("ProgressButtonArtDown"):SetText(GameLib.GetKeyBinding("StunBreakoutDown"))

        -- Disabled is invisible text, which will hide the button text
        self.wndProgress:FindChild("ProgressButtonArtLeft"):Enable(bLeft)
        self.wndProgress:FindChild("ProgressButtonArtUp"):Enable(bUp)
        self.wndProgress:FindChild("ProgressButtonArtRight"):Enable(bRight)
        self.wndProgress:FindChild("ProgressButtonArtDown"):Enable(bDown)

        if not bLeft and not bUp and not bRight and not bDown then -- Error Case
            self:OnRemoveCCStateStun()
            return
        end

        self:OnCalculateTimeRemaining()
    end
```

------------------------------------------------------------------------

`Event`

AddSpellShortcut
----------------

### Description

Fires whenever a spell is granted to the player as part of a quest,
challenge, public event, or path mission.

### Params

-   **splDisplayed** **([Spell](../Classes/Spell.md))** - The spell
    that is granted to the player.
-   **eReason** **(Integer)** - The reason the spell was granted to the
    player.
-   **idSource** **(Integer)** - The id of the quest, quest objective,
    challenge, public event, public event objective, or path mission
    that granted the spell to the player.

------------------------------------------------------------------------

`Event`

AlertMailInfo
-------------

### Description

Fires when the player gets new mail.

### Params

-   **tMessageInfo** **(Table)** - A table containing information about
    the new piece of mail.
    -   **strId** **(String)** - A string with the mail's unique id, in
        string format.
    -   **strSenderName** **(String)** - The name of the player who sent
        the mail.
    -   **strSubject** **(String)** - The subject of the mail.
    -   **strBody** **(String)** - The body of the email.
    -   **strBodyAML** **(String)** - The body of the email, along with
        any formatting strings. This element is not present on every
        mail message.
    -   **fDeliveryTime** **(Float)** - The number of seconds until the
        mail is received.
    -   **fExpirationTime** **(Float)** - The number of seconds until
        the mail expires.
    -   **monCOD** **([Money](../Classes/Money.md))** - The amount of
        money that must be paid before any items can be retreived.
    -   **monGift** **([Money](../Classes/Money.md))** - The amount of
        money sent to the recipient.
    -   **bIsRead** **(Boolean)** - Determines whether or not the piece
        of mail has been read.
    -   **bIsSaved** **(Boolean)** - Determines if the player has
        archived this piece of mail or not.
    -   **bIsReturnable** **(Boolean)** - Determines whether or not the
        player can return the piece of mail to the sender. This will
        typically be false for NPCs or CSRs.
    -   **eSenderType** **(Integer)** - A number representing the source
        of the mail. These values line up with the MailSystem.EmailType
        set of constants.
    -   **arAttachments** **(Array of Table)** - A table containing
        information on the items that are attached to the mail.
        -   **itemAttached** **([Item](../Classes/Item.md))** - The
            item object that is attached to the piece of mail
        -   **nStackCount** **(Integer)** - The number of items in the
            stack
        -   **nServerIndex** **(Integer)** - The index of the attachment

------------------------------------------------------------------------

`Event`

AlternateTargetUnitChanged
--------------------------

### Description

Fires when the player's focus target changes.

### Params

-   **unitFocus** **([Unit](../Classes/Unit.md))** - The player's new
    focus target.

### Usage/Example

```lua
    function UnitFrames:OnAlternateTargetUnitChanged(unitTarget)
        self.luaFocusFrame:SetTarget(unitTarget)
    end
```

------------------------------------------------------------------------

`Event`

AppearanceChanged
-----------------

### Description

Fires whenever the player updates a costume, purchases a dye job on
their equipment, or purchases a character customization change.

------------------------------------------------------------------------

`Event`

ApplicationWindowSizeChanged
----------------------------

------------------------------------------------------------------------

`Event`

ApplyCCState
------------

### Description

Fires when a CC state is applied to a unit.

### Params

-   **eState** **(Unit.CodeEnumCCState)** - A number representing the CC
    applied to the player.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that is
    affected by the CC state.

------------------------------------------------------------------------

`Event`

AuctionWindowClose
------------------

### Description

Fires whent he player moves out of range of an Auctioneer NPC.

### Usage/Example

```lua
    function MarketplaceAuction:OnDocumentReady()
                    Apollo.RegisterEventHandler("AuctionWindowClose",           "OnDestroy", self)
    end

    function MarketplaceAuction:OnDestroy()
        if self.wndMain and self.wndMain:IsValid() then
            self:OnSearchClearBtn()
            self.wndMain:Destroy()
        end

        Event_CancelAuctionhouse()
    end
```

------------------------------------------------------------------------

`Event`

AvailableMail
-------------

### Description

Fires mail is added to the player's inbox.

### Params

-   **arMail** **(Integer)** - An array of mail IDs for the mail added
    to the player's inbox.
-   **bIsNewMail** **(Boolean)** - Whether or not the messages added to
    the player's inbox are "new".

### Usage/Example

```lua
    function Mail:OnAvailableMail(arItems, bNewMail)
        if not self.wndMain:IsVisible() then
            self:CalculateMailAlert()
            return
        end

        self:PopulateList()
    end
```

------------------------------------------------------------------------

`Event`

BankSlotPurchased (Deprecated)
------------------------------

### Description

Fires when the player successfully purchases a bank slot.

### Usage/Example

```lua
    function BankViewer:OnBankSlotPurchased()
        self.wndMain:FindChild("BankTitleText"):SetText(Apollo.GetString("Bank_BuySuccess"))
        Apollo.CreateTimer("BankViewer_NewBagPurchasedAlert", 12, false)
        self:Build()
    end
```

------------------------------------------------------------------------

`Event`

BarberClose
-----------

------------------------------------------------------------------------

`Event`

BarberOpen
----------

------------------------------------------------------------------------

`Event`

BonusEventsChanged
------------------

------------------------------------------------------------------------

`Event`

Breath\_FlashEvent
------------------

### Description

Fires when the player has run out of breath and starts taking damage.

### Params

-   **fHealthPercentRemaining** **(Float)** - The percentage of
    remaining health the player has.

### Usage/Example

```lua
    function Hazards:OnDocumentReady()
                    Apollo.RegisterEventHandler("Breath_FlashEvent", "OnFlash", self)
    end

    function Hazards:OnFlash( nHealthPercentage )
        self.wndSuffocatingProgress:SetSprite("sprNp_WhiteBarFlash")
    end
```

------------------------------------------------------------------------

`Event`

BreathChanged
-------------

### Description

Fires whenever the player's breath meter should change value.

### Params

-   **nCurrentBreath** **(Integer)** - The player's current breath.
-   **nMaxBreath** **(Integer)** - The maximum amount of breath the
    character can have.

------------------------------------------------------------------------

`Event`

BuffAdded
---------

### Description

Fires whenever a buff or debuff is added to a unit.

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that received the buff/debuff.
-   **tBuff** **(Table)** - Information about the added buff.
    -   **fTimeRemaining** **(Float)** - The amount of time (in seconds) left before the buff ends.
    -   **idBuff** **(Integer)** - The id number for the buff itself. This is not to be confused with the id number of the spell containing the buff's effect.
    -   **nCount** **(Integer)** - The number of stacks of a buff that are on the unit.
    -   **splEffect** **([Spell](../Classes/Spell.md))** - The spell containing the buff's effect.
    -   **strTooltip** **(String)** - Description of the buff or debuff.
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - Source of the buff. Can be nil if the caster unit got destroyed.
    -   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that received the buff/debuff.

### Remarks

This event is only fired for units that have been activated by targetting them or setting them to focus target. The player and group members are always activated.

------------------------------------------------------------------------

`Event`

BuffUpdated
-----------

### Description

Fires whenever a buff or debuff is updated on a unit e.g. stacks added or removed. Before a buff is removed the stacks will count down one by one in this event.

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that received the buff/debuff.
-   **tBuff** **(Table)** - Information about the added buff.
    -   **fTimeRemaining** **(Float)** - The amount of time (in seconds) left before the buff ends.
    -   **idBuff** **(Integer)** - The id number for the buff itself. This is not to be confused with the id number of the spell containing the buff's effect.
    -   **nCount** **(Integer)** - The number of stacks of a buff that are on the unit.
    -   **splEffect** **([Spell](../Classes/Spell.md))** - The spell containing the buff's effect.
    -   **strTooltip** **(String)** - Description of the buff or debuff.
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - Source of the buff. Can be nil if the caster unit got destroyed.
    -   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that received the buff/debuff.

### Remarks

This event is only fired for units that have been activated by targetting them or setting them to focus target. The player and group members are always activated.

------------------------------------------------------------------------
`Event`

BuffRemoved
---------

### Description

Fires whenever a buff or debuff is removed on a unit.

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that received the buff/debuff.
-   **tBuff** **(Table)** - Information about the added buff.
    -   **fTimeRemaining** **(Float)** - The amount of time (in seconds) left before the buff ends.
    -   **idBuff** **(Integer)** - The id number for the buff itself. This is not to be confused with the id number of the spell containing the buff's effect.
    -   **nCount** **(Integer)** - The number of stacks of a buff that are on the unit.
    -   **splEffect** **([Spell](../Classes/Spell.md))** - The spell containing the buff's effect.
    -   **strTooltip** **(String)** - Description of the buff or debuff.
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - Source of the buff. Can be nil if the caster unit got destroyed.
    -   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that received the buff/debuff.

### Remarks

This event is only fired for units that have been activated by targetting them or setting them to focus target. The player and group members are always activated.

------------------------------------------------------------------------

`Event`

BuybackItemsUpdated
-------------------

### Description

Fires when there is a change in the list of Buyback items at a vendor.

------------------------------------------------------------------------

`Event`

CanVacuumChange
---------------

### Description

Fires when the player's ability to vacuum nearby loot has changed due to
loot dropping, being vacuumed, or being removed from the world.

### Params

-   **bCanVacuum** **(Boolean)** - Whether or not the ability to vacuum
    is active.

### Usage/Example

```lua
    function HUDAlerts:OnCanVacuumChanged(bCanVacuum)

    local strKeybind = GameLib.GetKeyBinding("VacuumLoot")

    self.wndLootAlert:FindChild("AlertItemKeybindText"):SetText(strKeybind)

    self.wndLootAlert:FindChild("AlertItemKeybind"):Show(strKeybind ~= Apollo.GetString("HUDAlert_Unbound"))


    if not self.wndLootAlert:IsShown() and bCanVacuum then

    self.wndLootAlert:Show(bCanVacuum, true)

    self.wndLootAlert:FindChild("AlertItemTransition"):SetSprite("sprAlert_SectionGlowRingFlash")

    else

    self.wndLootAlert:Show(bCanVacuum)


    end


    self:OnUpdateInventory() -- Check Full Bag Indicator


    self.wndAlertContainer:ArrangeChildrenHorz(0)

    end
```

------------------------------------------------------------------------

`Event`

CardFlipped
-----------

------------------------------------------------------------------------

`Event`

CasterResurrectedPlayer
-----------------------

### Description

Fires when the current player is revived by another player.

### Params

-   **strCasterName** **(String)** - The name of the player that
    resurrected the player.

------------------------------------------------------------------------

`Event`

ChallengeAreaRestriction
------------------------

### Description

Fires when the player attempts to start/retry a challenge while they are
outside of the challenge's starting area.

### Params

-   **idChallenge** **(Integer)** - The ID number for the challenge.
-   **strHeader** **(String)** - The challenge's title.
-   **strDescription** **(String)** - The message that should be
    displayed so the player knows they are outside of the challenge
    area.
-   **fDuration** **(Float)** - The length of time (in seconds) that the
    message is displayed.

------------------------------------------------------------------------

`Event`

ChallengeCompletedSound
-----------------------

### Description

Fires whenever we should play the sound for a completed challenge.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge that
    was completed.

------------------------------------------------------------------------

`Event`

ChallengeCooldownActive
-----------------------

### Description

Fires when the player attempts to start a challenge that is on cooldown.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge.
-   **strHeader** **(String)** - The challenge's title.
-   **strErrorMsg** **(String)** - The error message that should be
    shown for this event.
-   **nDuration** **(Integer)** - The duration that the error message
    should be shown for (in milliseconds).

------------------------------------------------------------------------

`Event`

ChallengeFailArea
-----------------

### Description

Fires when a challenge fails because the player left the area.

### Params

-   **chalFailed** **(Challenge)** - The challenge that was failed.
-   **strHeader** **(String)** - The header for the "Fail" notification.
-   **strDescription** **(String)** - The body of the "Fail"
    notification.
-   **nDuration** **(Integer)** - How long the "Fail" notification
    should be shown (in milliseconds).

------------------------------------------------------------------------

`Event`

ChallengeFailGeneric
--------------------

### Description

Fires if a player fails a challenge for reasons other than time or
leaving the area.

### Params

-   **chalFailed** **(Challenge)** - The challenge that the player
    failed.
-   **strHeader** **(String)** - The header for the "Fail" notification.
-   **strDescription** **(String)** - The body of the "Fail"
    notification.
-   **nDuration** **(Integer)** - How long the "Fail" notification
    should be shown (in milliseconds).

------------------------------------------------------------------------

`Event`

ChallengeFailSound
------------------

### Description

Fires when the "Fail" sound should be played for a challenge.

### Params

-   **idChallenge** **(Integer)** - The id number for the challenge that
    the sound is played for.

------------------------------------------------------------------------

`Event`

ChallengeFailTime
-----------------

### Description

Fires when the player fails a challenge due to time running out before
any tiers were reached.

### Params

-   **chalFailed** **(Challenge)** - The challenge that was failed.
-   **strHeader** **(String)** - The header for the "Fail" notification.
-   **strDescription** **(String)** - The body of the "Fail"
    notification.
-   **nDuration** **(Integer)** - How long the "Fail" notification
    should be displayed (in milliseconds).

------------------------------------------------------------------------

`Event`

ChallengeRewardListReady
------------------------

### Description

Fires when we have the information we need to populate the challenge's
rewards.

### Params

-   **idChallenge** **(Integer)** - The challenge that was completed.
-   **nRewardTier** **(Integer)** - The challenge tier that the player
    completed. 1 is Bronze, 2 is Silver, 3 is Gold.

------------------------------------------------------------------------

`Event`

ChallengeRewardReady
--------------------

### Description

Fires when the challenge's reward has been determined.

### Params

-   **idChallenge** **(Challenge)** - The id number of the challenge
    that was completed.
-   **nReward** **(Integer)** - The reward number that the player
    received from the challenge.

### Remarks

This is used in the stock UI to show where the roulette wheel lands
after completing a challenge.

------------------------------------------------------------------------

`Event`

ChallengeShared
---------------

### Description

Fired when a challenge is shared with the player.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge being
    shared.
-   **idSharingPlayer** **(Integer)** - The id number of the player who
    shared the challenge.
-   **nTimeToAccept** **(Integer)** - The amount of time the player has
    to accept the challenge (in seconds).

------------------------------------------------------------------------

`Event`

ChallengeShareTimedOut
----------------------

### Description

Fires when the player runs out of time to accept a shared challenge.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge that
    was shared.

------------------------------------------------------------------------

`Event`

ChallengeTierAchieved
---------------------

### Description

Fires whenever the player completes a challenge tier.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge.
-   **nTierCompleted** **(Integer)** - The challenge tier that was
    completed. 1 = Bronze, 2 = Silver, 3 = Gold.

------------------------------------------------------------------------

`Event`

ChallengeTimeUpdated
--------------------

------------------------------------------------------------------------

`Event`

ChallengeUpdated
----------------

### Description

Fires whenever progress is made on a challenge, when the player leaves
and re-enters a challenge area, and whenever the player selects a
challenge reward to receive their tier roll bonus.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge that
    was updated.

------------------------------------------------------------------------

`Event`

ChangeWorld
-----------

### Description

Fires when the player is moved to a different zone or instance.

------------------------------------------------------------------------

`Event`

ChannelUpdate\_Crafting
-----------------------

------------------------------------------------------------------------

`Event`

ChannelUpdate\_Loot
-------------------

------------------------------------------------------------------------

`Event`

ChannelUpdate\_Progress
-----------------------

------------------------------------------------------------------------

`Event`

CharacterCreated
----------------

### Description

Fires when the player's character is first placed in the world.

### Remarks

Note: This is not fired if the UI is reloaded.\
\
Also Note: All of the character's information may not be populated in
other systems when the character is created. This is an important event,
but extra checks, such as GameLib.IsCharacterLoaded() could prove useful
here.

------------------------------------------------------------------------

`Event`

CharacterEldanAugmentationsReset (Deprecated)
---------------------------------------------

------------------------------------------------------------------------

`Event`

CharacterEldanAugmentationsUpdated
----------------------------------

### Description

Fires whenever the player selects an AMP or purchases an AMP reset.

------------------------------------------------------------------------

`Event`

CharacterEntitlementUpdate
--------------------------

------------------------------------------------------------------------

`Event`

CharacterFlagsUpdated
---------------------

### Description

Fires whenever the player's state flags are updated. Changing any of the
following states will trigger this event:\
PvP Flag\
Block Friendships\
Limit Hazard Rez\
Ignore Duel Requests\
Hide Top Guild Holomark\
Hide Left Guild Holomark\
Hide Right Guild Holomark\
Hide Back Guild Holomark\
Disable Character\
Display Guild Holomark Near\
Require Name Change

------------------------------------------------------------------------

`Event`

CharacterRecustomizationResult
------------------------------

------------------------------------------------------------------------

`Event`

CharacterUnlockedInlaidEldanAugmentation
----------------------------------------

### Description

Fires whenever the player unlocks a new AMP.

------------------------------------------------------------------------

`Event`

ChatAccountTellFailed
---------------------

### Description

Fires whenever the player tries to send an account whisper to an invalid
player.

### Params

-   **channelWhisper**
    **([ChatChannelLib](../Classes/ChatChannelLib.md))** - The chat
    channel that the player tried to whisper from. This should always be
    the "Account Whisper" channel.
-   **strName** **(String)** - The name of the player who was intended
    to receive the account whisper.

------------------------------------------------------------------------

`Event`

ChatAction
----------

### Description

Fires whenever an action is taken on a custom chat channel. These
actions include passing the owner of the channel to another player,
adding or removing the Moderator status from a player, muting and
unmuting a player, kicking a player from the channel, and
adding/removing a password to the channel.

### Params

-   **channelSource**
    **([ChatChannelLib](../Classes/ChatChannelLib.md))** - The channel
    that the action was applied to.
-   **eAction** **(Integer)** - The action that fired the event. This
    value lines up with the ChatSystemLib.ChatChannelAction set of
    constants.
-   **strActor** **(String)** - The player who performed the action.
-   **strActedOn** **(String)** - The target of the action.

------------------------------------------------------------------------

`Event`

ChatFlag
--------

------------------------------------------------------------------------

`Event`

ChatJoin
--------

### Description

Fires when the player joins a chat channel.

### Params

-   **chanJoined**
    **([ChatChannelLib](../Classes/ChatChannelLib.md))** - The chat
    channel that the character just joined.

------------------------------------------------------------------------

`Event`

ChatJoinResult
--------------

### Description

Fires whenever the player fails to join a channel.

### Params

-   **chanJoin** **([ChatChannelLib](../Classes/ChatChannelLib.md))** -
    The channel that the player attempted to join.
-   **eResult** **(Integer)** - The reason why the player failed to join
    the channel. This value lines up with the
    ChatSystemLib.ChatChannelResult system of int constants.

------------------------------------------------------------------------

`Event`

ChatLeave
---------

### Description

Fires when the player leaves or is kicked from a chat channel.

### Params

-   **chanLeft** **([ChatChannelLib](../Classes/ChatChannelLib.md))** -
    The channel that the player left.
-   **bKicked** **(Boolean)** - Whether or not the player was kicked
    from the channel
-   **bBanned** **(Boolean)** - Whether or not the player was banned
    from the channel.

------------------------------------------------------------------------

`Event`

ChatList
--------

### Description

Fired in response to the ChatChannel:RequestMembers() function. Passes
the channel that was polled for its members.

### Params

-   **channelSource** **([ChatChannel](../Classes/ChatChannel.md))** -
    The channel that is being polled for its members.

------------------------------------------------------------------------

`Event`

ChatMessage
-----------

### Description

Fires when a message is sent on a chat channel

### Params

-   **channelSource** **([ChatChannel](../Classes/ChatChannel.md))** -
    The channel where the message should be displayed.
-   **tMessageInfo** **(Table)** -
    -   **bAutoResponse** **(Boolean)** - Whether or not the message is
        an auto response (from messaging an afk player for example)
    -   **bGM** **(Boolean)** - Whether the message was sent by a GM or
        not.
    -   **bSelf** **(Boolean)** - Whether the message was sent by the
        player or not.
    -   **strSender** **(String)** - The name of the source of the
        message.
    -   **strRealmName** **(String)** - The name of the sender's home
        realm.
    -   **nPresenceState** **(Integer)** - The sender's status. This
        value lines up with the FriendshipLib.AccountPresenceState set
        of constants. Returns
        FriendshipLib.AccountPresenceStateAvailable if it is not a
        player.
    -   **arMessageSegments** **(Table)** - This is currently using the
        incorrect prefix. It is a table with different types in it.
        -   **bAlien** **(Boolean)** - Whether or not the text is
            flagged to show alien font.
        -   **bProfanity** **(Boolean)** - Whether or not the text
            contains profanity.
        -   **bRoleplay** **(Boolean)** - Whether or not the text is
            flagged as Role Play text.
        -   **strText** **(String)** - The text that is displayed.
    -   **unitSource** **([Unit](../Classes/Unit.md))** - The unit that
        sent the message. This variable does not exist for messages not
        sent by a unit, such as system messages.
    -   **bShowChatBubble** **(Boolean)** - Whether or not a chat bubble
        should be shown above the character.
    -   **bCrossFaction** **(Boolean)** - Whether or not the message
        came from a character of the other faction.
    -   **nReportId** **(Integer)** - The id that corresponds with the
        message. This value is used for chat reporting purposes.

------------------------------------------------------------------------

`Event`

ChatReply
---------

### Description

Fires when the player uses the ChatReply keybinding.

------------------------------------------------------------------------

`Event`

ChatResult
----------

### Description

Fires when there is an error with a chat message that the player tried
to send.

### Params

-   **channelSource** **([ChatChannel](../Classes/ChatChannel.md))** -
    The channel where the original message was sent.
-   **eResult** **(Integer)** - The error with the message that was
    sent. This value lines up with the ChatSystemLib.ChatChannelResult
    constants.

------------------------------------------------------------------------

`Event`

ChatReWhisper
-------------

### Description

Fires when the Chat Re-Whisper keybinding is pressed.

------------------------------------------------------------------------

`Event`

ChatTellFailed
--------------

### Description

Fires whenever the player makes an unsuccessful tell

### Params

-   **channelSource** **([ChatChannel](../Classes/ChatChannel.md))** -
    The channel that the player attempted to use for the failed tell.
    This is likely the Whisper channel.
-   **strName** **(String)** - The name of the player you attempted to
    send a whisper to.

------------------------------------------------------------------------

`Event`

ChatZoneChange
--------------

### Description

Fires when the Zone channel changes, such as when a player moves from
one zone to another.

### Params

-   **strNewZone** **(String)** - The name of the new zone that the
    player has moved into.

------------------------------------------------------------------------

`Event`

CinematicsCancel (Deprecated)
-----------------------------

### Params

-   **nParam** **(Integer)**

------------------------------------------------------------------------

`Event`

CinematicsNotify (Deprecated)
-----------------------------

### Description

Notifies the player that a cinematic is starting

### Params

-   **strMessage** **(String)** - The notification message that should
    be displayed.
-   **idParam** **(Integer)** - The message's id.

------------------------------------------------------------------------

`Event`

CityDirectionClear
------------------

### Description

Removes the specified direction marker from the map.

### Params

-   **idDirection** **(Integer)** - The ID number for the direction that
    should be cleared.

------------------------------------------------------------------------

`Event`

CityDirectionMarked
-------------------

### Description

Fires when a city direction marker is displayed on the map / minimap

### Params

-   **tLocationInfo** **(Table)**
    -   **idDestination** **(Integer)** - The direction marker's ID.
    -   **eType** **(GameLib.CityDirectionType)** - The type of NPC that
        the player is being guided towards.
    -   **strName** **(String)** - The name of the direction marker's
        destination.
    -   **tLoc** **(Table)**
        -   **x** **(Float)** - The x coordinate of the city direction's
            destination.
        -   **y** **(Float)** - The y coordinate of the city direction's
            destination.
        -   **z** **(Float)** - The z coordinate of the city direction's
            destination

------------------------------------------------------------------------

`Event`

CityDirectionsClose
-------------------

### Description

Fires when the City Directions UI closes.

------------------------------------------------------------------------

`Event`

CityDirectionsList
------------------

### Description

Fires when the player interacts with a guard in a capital city.

------------------------------------------------------------------------

`Event`

ClearSpellThreshold
-------------------

### Description

Fires when the "Window of Opportunity" for spells with multiple uses
(ex. Stalker's Nano Field, Esper's Psychic Frenzy) should close. This
can happen either because the timer ran out, the player used another
ability, or the player activated the max number of times.

### Params

-   **idSpell** **(Integer)** - The id number of the spell whose
    threshold needs to close.

------------------------------------------------------------------------

`Event`

CloseCraftingWindow
-------------------

### Description

Fired when the UI explicity calls the Event\_CloseCraftingWindow()
function.

------------------------------------------------------------------------

`Event`

CloseTradeskillTrainerWindow
----------------------------

### Description

Fired if the player interacts with another unit while interacting with a
tradeskill trainer. It's also fired when the
Event\_CloseTradeskillTrainerWindow() function is called in Lua.

------------------------------------------------------------------------

`Event`

CloseVendorWindow
-----------------

### Description

Fired when the player interacts with another unit while the Vendor UI is
up, moves out of range of a vendor while the Vendor UI is open, or the
Event\_CloseVendorWindow() function is explicitly called in Lua.

------------------------------------------------------------------------

`Event`

ColorChanged
------------

### Description

Fired whent he player selects a color from the ColorPicker window

### Params

-   **crNewColor** **([CColor](../Classes/CColor.md))** - The color
    that was selected when this event was fired.

------------------------------------------------------------------------

`Event`

CombatFloaters\_Configure (Deprecated)
--------------------------------------

### Description

Fires when the player uses the /cfconfig command in chat

------------------------------------------------------------------------

`Event`

CombatLogAbsorption
-------------------

### Description

Fires whenever a unit is granted an absorb shield.

### Params

-   **tCombatLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who
        used the ability.
    -   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The unit
        who controls the caster. This variable only exists if the caster
        is a pet.
    -   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit
        affected by the ability.
    -   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
        who controls the target. This only exists if the target is a
        pet.
    -   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - The
        effect of the abiility on the target. This will most likely be
        Hit in this case.
    -   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The
        spell that was used.
    -   **nAmount** **(Integer)** - The amount of damage that the absorb
        shield will mitigate.

------------------------------------------------------------------------

`Event`

CombatLogBuildSwitch
--------------------

### Description

Fires when the player switches to a different action set.

### Params

-   **tLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who
        changed their build. Since this event shold only be fired for
        the current player, this should always be them.
    -   **nNewSpecIndex** **(Integer)** - The index of player's new
        spec.

------------------------------------------------------------------------

`Event`

CombatLogCCState
----------------

### Description

Fires whenever a player enters a crowd control state.

### Params

-   **tLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
        cast the ability that applied the CC state.
    -   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The unit
        that owns the unitCaster. This variable will only exist if the
        unit that applied the state is a pet.
    -   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that
        the CC state was applied to.
    -   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
        that owns the target of the ability. This variable only exists
        if the target was a pet.
    -   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - A number
        that represents the effect of the ability on the player. This
        will most likely be either Hit or Avoid.
    -   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The
        spell that was used to apply the CC state on the player.
    -   **eState** **(Unit.CodeEnumCCState)** - The type of CC that the
        spell should cause.
    -   **bRemoved** **(Boolean)** - If this is true, then the crowd
        control state is removed from the player. If not, then it is
        added to the player.
    -   **strState** **(String)** - The name of the CC state.
    -   **strTriggerCapCategory** **(String)** - The name of the CC
        category this effect falls under.\
        \
        Results can be:\
        Stun\
        Root\
        Pacify\
        Blind\
        Taunt\
        Knockdown\
        Tether\
        Disorient\
        Subdue\
        Pull\
        Knockback\
        Snare\
        Position Switch\
        Pushback\
        \
        Not every CC State has a dimminishing returns category.
    -   **bHideFloater** **(Boolean)** - Determines whether the floater
        for the state should be hidden. This variable will only be set
        to true or nil.
    -   **nInterruptArmorHit** **(Integer)** - The amount of interrupt
        armor removed by the spell.
    -   **eResult**
        **(CombatFloaterLib.CodeEnumCCStateApplyRulesResult)** - The
        result of trying to apply the CC state to the unit.

------------------------------------------------------------------------

`Event`

CombatLogCCStateBreak
---------------------

### Description

Fires when the player breaks out of a CC state.

### Params

-   **tLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
        broke out of their CC state. This should always be the current
        player.
    -   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The unit
        that controls the unit that broke their CC state. This should
        only be returned if a pet broke out of its crowd control state.
    -   **eState** **(Unit.CodeEnumCCState)** - The type of CC that the
        unitCaster broke out of.
    -   **strState** **(String)** - The name of the CC state that the
        unit broke out of.

------------------------------------------------------------------------

`Event`

CombatLogCrafting (Deprecated)
------------------------------

### Description

Fires when the player finishes crafting an item using a non-simple craft
schematic.

### Params

-   **tLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who
        crafted the item. This should always be the current player.
    -   **itemCrafted** **([Item](../Classes/Item.md))** - The item
        that the player crafted.

------------------------------------------------------------------------

`Event`

CombatLogDamage
---------------

### Description

Fires when a unit takes damage.

### Params

-   **tLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who
        used the spell that caused the damage.
    -   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The
        player that owns the unit who dealt the damage. This only
        applies if the unitCaster is a pet.
    -   **unitTarget** **([Unit](../Classes/Unit.md))** - The target of
        the ability.
    -   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
        that owns the unitTarget. This only exists if unitTarget is a
        pet.
    -   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - The
        effect of the ability on its target.
    -   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The
        spell that caused the damage.
    -   **nDamageAmount** **(Integer)** - The amount of damage done by
        the spell.
    -   **nRawDamage** **(Integer)** - Damage amount that is directly
        related to ???
    -   **eDamageType** **(GameLib.CodeEnumDamageType)** - The type of
        damage that was done.
    -   **nShield** **(Integer)** - The amount of damage done to the
        unit's shield.
    -   **nAbsorbtion** **(Integer)** - The amount of damage done to the
        player's absorption shield.
    -   **nOverkill** **(Integer)** - The amount of damage done to the
        unit over their remaining HP.
    -   **bTargetVulnerable** **(Boolean)** - Whether or not the target
        is in the vulnerable state.
    -   **bTargetKilled** **(Boolean)** - Whether or not the unitTarget
        was killed by the attack.
    -   **bPeriodic** **(Boolean)** - Whether the damage was caused by
        an ability that does periodic damage.
    -   **eEffectType** **(Integer)** - The spell's effect type. The
        values for this enum are not currently exposed in the Apollo
        API.

------------------------------------------------------------------------

`Event`

CombatLogDamageShields
----------------------

------------------------------------------------------------------------

`Event`

CombatLogDatacube
-----------------

### Description

Fires when the player interacts with a datacube, journal, or TFBTF entry
in the world.

### Params

-   **tLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
        activated the datacube. This will always be the current player.
    -   **eDatacubeType** **(Integer)** - The type of datacube. This can
        be either DatacubeLib.DatacubeType\_Datacube,
        DatacubeLib.DatacubeType\_Chronicle (Tales from Beyond the
        Fringe), or DatacubeLib.DatacubeType\_Journal.
    -   **bHasPieces** **(Boolean)** - Whether or not the datacube has
        multiple parts. This should only be true for Tales from Beyond
        the Fringe.

------------------------------------------------------------------------

`Event`

CombatLogDeath
--------------

### Description

Fires when the player dies.

### Params

-   **tLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
        died. This will always be the current player.

------------------------------------------------------------------------

`Event`

CombatLogDeflect
----------------

### Description

Fires when a unit deflects an attack.

### Params

-   **tLogInfo** **(Table)**
    -   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
        used the spell.
    -   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The unit
        that owns unitCaster. This variable only exists if unitCaster is
        a pet.
    -   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that
        deflected the spell.
    -   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
        that owns unitTarget. This only exists if unitTarget is a pet.
    -   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - The
        result of the attack. This should always be
        GameLib.CodeEnumCombatResult.Avoid
    -   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The
        ability that was used in the attack.

------------------------------------------------------------------------

`Event`

CombatLogDelayDeath
-------------------

### Description

Fires when death missed his bus?

------------------------------------------------------------------------

`Event`

CombatLogDispel (Deprecated)
----------------------------

### Description

Fires when a buff or debuff is dispelled.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    used the spell that triggered the event.
-   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The unit who
    owns unitCaster. This only applies if unitCaster is a pet.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that the
    buff/debuff was dispelled from.
-   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
    that owns unitTarget. This only applies if unitTarget is a pet.
-   **bRemoveSingleInstance** **(Boolean)** - Whether or not a single
    stack of the buff is removed.
-   **nInstancesRemoved** **(Integer)** - The number of stacks of the
    buff that are removed from the unit.
-   **splRemovedSpell** **([Spell](../Classes/Spell.md))** - The spell
    that was removed from the unit.

------------------------------------------------------------------------

`Event`

CombatLogDurabilityLoss (Deprecated)
------------------------------------

### Description

Fires when a player's equipment loses a point of durability.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit wearing
    the equipment that lost durability. This will always be the current
    player.
-   **nAmount** **(Integer)** - The amount of durability that was lost.

------------------------------------------------------------------------

`Event`

CombatLogElderPointsLimitReached
--------------------------------

### Description

Fires when the player reaches the daily cap of elder points.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    reached their Elder Point Cap. This should always be the current
    player.

------------------------------------------------------------------------

`Event`

CombatLogEndGameCurrencies (Deprecated)
---------------------------------------

### Description

Fires whenever the player gains non-credit currencies.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    gained the currency. This is always the current player.
-   **monLoot** **([Money](../Classes/Money.md))** - The currency that
    was gained.

------------------------------------------------------------------------

`Event`

CombatLogExperience
-------------------

### Description

Fires whenever the player gaines experience or elder points.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    gained the experience or elder points. This will always be the
    current player.
-   **nXP** **(Integer)** - The base amount of experience gained.
-   **nRestXP** **(Integer)** - The amount of experience gained from the
    player's rested bonus.
-   **nEP** **(Integer)** - The amount of elder points the player
    gained.
-   **nRestEP** **(Integer)** - The amount of elder points gained from
    the player's rested bonus.

------------------------------------------------------------------------

`Event`

CombatLogExtracting (Deprecated)
--------------------------------

------------------------------------------------------------------------

`Event`

CombatLogFallingDamage
----------------------

### Description

Fires whenever the player takes fall damage

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    took the falling damage. This should always be the current player.
-   **nAmount** **(Integer)** - The amount of damage the player took.

------------------------------------------------------------------------

`Event`

CombatLogHeal
-------------

### Description

Fires whenever a unit gets healed.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who used
    the spell that caused the heal.
-   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The owner of
    unitCaster. This only applies if unitCaster is a pet.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that
    received the heal.
-   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
    that owns unitTarget. This only applies if unitTarget is a pet.
-   **nHealAmount** **(Integer)** - The amount missing health that was
    healed for the target. This value does not include overheals.
-   **nOverheal** **(Integer)** - The amount of overhealing done by the
    spell.
-   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - A number
    representing any special things that went on with the spell, such as
    a critical hit.
-   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The spell
    that was used for the heal.
-   **eEffectType** **(Spell.CodeEnumSpellEffectType)** - The effect the
    spell has on the target.

------------------------------------------------------------------------

`Event`

CombatLogImmunity
-----------------

------------------------------------------------------------------------

`Event`

CombatLogInterrupted
--------------------

### Description

Fires when a unit is interrupted by a spell. This includes if the player
interrupted their own spell cast.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    cast the spell that caused the interrupt.
-   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The owner of
    unitCaster. This only applies if unitCaster is a pet.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that was
    interrupted.
-   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The owner of
    unitTarget. This only applies if unitTarget is a pet.
-   **eCombatResult** **(Integer)** - The result the spell that was
    used.
-   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The spell
    that was interrupted.
-   **splInterruptingSpell** **([Spell](../Classes/Spell.md))** - The
    spell that caused the interrupt.
-   **eCastResult** **(Spell.CodeEnumCastResult)** - Explains why the
    spell was interrupted.
-   **strCastResult** **(String)** - A string explaining why the spell
    was interrupted.

------------------------------------------------------------------------

`Event`

CombatLogItemDestroy (Deprecated)
---------------------------------

### Description

Fires when the player destroys an item.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    destroyed the item.
-   **itemDestroyed** **([Item](../Classes/Item.md))** - The item that
    was destroyed.

### Remarks

Note: This is not triggered by salvaging, selling, or turning an item in
for a quest.

------------------------------------------------------------------------

`Event`

CombatLogKillPVP
----------------

### Description

Fires when a player assists in a PvP kill.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    assisted in the kill.
-   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The unit
    that owns unitCaster. This only applies if unitCaster is a pet.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that was
    killed in PvP.
-   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
    that owns unitTarget. This only applies if unitTarget was a pet.
-   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - The result of
    using the ability.
-   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The spell
    that killed the player.

### Remarks

Currently bugged. This is being fired for a player when they die in PvP,
not for when they get a kill assist.

------------------------------------------------------------------------

`Event`

CombatLogKillStreak
-------------------

### Description

Fires when the player gets multiple kills in quick succession.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that got
    the kill streak. This should either be the current player or one of
    their pets.
-   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The unit
    that owns unitCaster. This only applies if unitCaster is a pet.
-   **eStatType** **(CombatFloater.CodeEnumCombatMomentum)** - The type
    of streak the player is on.
-   **nStreakAmount** **(Integer)** - The player's current streak count.

------------------------------------------------------------------------

`Event`

CombatLogLAS
------------

### Description

Fires when a player changes their Limited Action Set.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    changed their Limited Action Set. This should always be the current
    player.

------------------------------------------------------------------------

`Event`

CombatLogLifeSteal
------------------

------------------------------------------------------------------------

`Event`

CombatLogLoot (Deprecated)
--------------------------

### Description

Fires whenever a player loots money or an item. This will fire for each
visible "item" looted in the world and each item distributed to the
player via the group's looting system.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    received the money or item.
-   **monLoot** **([Money](../Classes/Money.md))** - The money object
    for the money that was looted. If there was no money looted, this
    will be nil.
-   **itemLoot** **([Item](../Classes/Item.md))** - The item that was
    looted. If no item was looted in this event, this will be nil.
-   **nItemAmount** **(Integer)** - The stack size of itemLooted for
    this event. If money was looted in this event and not an item, this
    value will be 0.

------------------------------------------------------------------------

`Event`

CombatLogModifying
------------------

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    fired this event.
-   **itemHost** **([Item](../Classes/Item.md))**
-   **itemRemoved** **([Item](../Classes/Item.md))**
-   **itemAdded** **([Item](../Classes/Item.md))**

------------------------------------------------------------------------

`Event`

CombatLogModifyInterruptArmor
-----------------------------

### Description

Fires whenever a player gains or loses interrupt armor.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who
    caused a player's interrupt armor to change
-   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The owner of
    unitCaster. This is nil if unitCaster is not a pet.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit whose
    interrupt armor was changed.
-   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The player
    who owns unitTarget. This is nil if unitTarget is not a pet.
-   **nAmount** **(Integer)** - The change in the unit's interrupt
    armor.

------------------------------------------------------------------------

`Event`

CombatLogMount
--------------

### Description

Fires if the player mounts or dismounts.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The player that
    mounted.
-   **bDismounted** **(Boolean)** - Whether or not the player
    dismounted.

------------------------------------------------------------------------

`Event`

CombatLogMultiHeal
------------------

------------------------------------------------------------------------

`Event`

CombatLogMultiHit
-----------------

------------------------------------------------------------------------

`Event`

CombatLogMultiHitShields
------------------------

------------------------------------------------------------------------

`Event`

CombatLogPet
------------

### Description

Fires whenever a player summons or despawns a pet, or a pet dies.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who used
    the ability to summon, kill, or despawn the pet.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The pet that was
    spawned.
-   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
    that owns the pet. This is the current player.
-   **bDismissed** **(Boolean)** - Whether or not the pet was despawned.
-   **bKilled** **(Boolean)** - Whether or not the pet was killed.
-   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - The end
    result of the spell that was used.

------------------------------------------------------------------------

`Event`

CombatLogReflect
----------------

------------------------------------------------------------------------

`Event`

CombatLogResurrect
------------------

### Description

Fires whenever the player is rezzed. This includes all methods of
resurrection.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that was
    resurrected.

------------------------------------------------------------------------

`Event`

CombatLogStealth
----------------

### Description

Fires whenever the player enters or leaves stealth.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit whose
    stealth state has changed.
-   **bExiting** **(Boolean)** - Whether or not the player left stealth.

------------------------------------------------------------------------

`Event`

CombatLogString
---------------

### Description

Fires whenever a string is directly written in the combat log. This
event will always accompany another combat log event

### Params

-   **strLogMessage** **(String)** - The message printed to the combat
    log.

------------------------------------------------------------------------

`Event`

CombatLogTransference
---------------------

### Description

Fires whenever a spell does damage and heals the user at the same time.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit who used
    the spell that triggered the event.
-   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The player
    that owns unitCaster. This only applies if unitCaster was a pet.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that was
    affected by the spell that triggered this event.
-   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit who
    owns unitTarget. This only applies if unitTarget is a pet.
-   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - The effect of
    the spell that triggered the event.
-   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The spell
    that triggered the event.
-   **nDamageAmount** **(Integer)** - The amount of damage done to
    unitTarget.
-   **eDamageType** **(GameLib.CodeEnumDamageType)** - The type of
    damage done by the spell.
-   **nShield** **(Integer)** - The amount of damage done to the
    target's shields.
-   **nAbsorption** **(Integer)** - The amount of damage done to the
    target's absorption shield.
-   **nOverkill** **(Integer)** - The amount of damage done over the
    target's max health.
-   **bTargetVulnerable** **(Boolean)** - Whether or not the target is
    in a "Moment of Opportunity" state.
-   **tHealData** **(Array of Table)**
    -   **nHealAmount** **(Integer)** - The amount that the caster is
        healed for.
    -   **eVitalType** **(GameLib.CodeEnumVital)** - The stat that is
        increased after the spell is cast.
    -   **nOverheal** **(Integer)** - The amount of healing the caster
        received while they were at their maximum health.

### Remarks

A good example of a spell that fires this event is the Stalker ability
"Nano Field". It is different from Lifesteal in that it is build into
the spell, whereas lifesteal is a stat that is granted to all of the
player's spells.

------------------------------------------------------------------------

`Event`

CombatLogVitalModifier (Deprecated)
-----------------------------------

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    used the spell that caused the event to fire.
-   **unitCasterOwner** **([Unit](../Classes/Unit.md))** - The unit
    that owns unitCaster. This only applies if unitCaster is a pet.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that was
    the target of the spell.
-   **unitTargetOwner** **([Unit](../Classes/Unit.md))** - The unit
    that owns unitTarget. This only applies if unitTarget is a pet.
-   **eCombatResult** **(GameLib.CodeEnumCombatResult)** - The spell's
    effect on the target.
-   **splCallingSpell** **([Spell](../Classes/Spell.md))** - The spell
    that caused the event to fire.
-   **nAmount** **(Integer)** - How much the specified vital is modified
    by.
-   **eVitalType** **(GameLib.CodeEnumVital)** - The vital that is
    modified.
-   **bShowCombatLog** **(Boolean)** - Whether or not this event should
    appear in the combat log.

------------------------------------------------------------------------

`Event`

CombatMomentum
--------------

### Description

Fires whenever one of the player's "momentum" bonuses increases.

### Params

-   **eType** **(CombatFloater.CodeEnumCombatMomentum)** - The type of
    momentum bonus that was increased.
-   **nCount** **(Integer)** - The current count for the momentum bonus.
-   **strMessage** **(String)** - A string for displaying the event.

------------------------------------------------------------------------

`Event`

CommodityAuctionFilledPartial
-----------------------------

### Description

Fires whenever a buy or sell order on the Commodities Exchange is
partially filled by another player.

### Params

-   **nFilledCount** **(Integer)** - How many items in the order were
    actually bought or sold.
-   **orderFilled**
    **([CommodityOrder](../Classes/CommodityOrder.md))** - The order
    that was partially filled.

------------------------------------------------------------------------

`Event`

CommodityAuctionRemoved
-----------------------

### Description

Fires whenever a buy or sell order is removed from the Commodities
Exchange.

### Params

-   **eReason** **(MarketplaceLib.AuctionEventType)** - The reason the
    auction was removed from the Commodities Exchange. This will either
    be Fill, Expire, or Cancel.
-   **orderRemoved**
    **([CommodityOrder](../Classes/CommodityOrder.md))** - The order
    that was removed from the Commodities Exchange.

------------------------------------------------------------------------

`Event`

CommodityAuctionsDisabled
-------------------------

### Description

Fired when the Commodity Exchange gets disabled or enabled.

### Params

-   **bDisabled** **(Boolean)** - Whether or not this event was fired
    because the Commodity Exchange is disabled.

### Remarks

This is only for actions taken by GMs that enable and disable the
Commodity Exchange for everyone on the server

------------------------------------------------------------------------

`Event`

CommodityInfoResults
--------------------

### Description

Fires for each item returned by MarketplaceLib.RequestCommodityInfo().
It contains information on all of the buy and sell orders out for the
item.

### Params

-   **idItem** **(Integer)** - The id number for the item that the
    results are referencing.
-   **tStats** **(Table)**
    -   **nBuyOrderCount** **(Integer)** - The number of buy orders out
        for the item.
    -   **nSellOrderCount** **(Integer)** - The number of sell orders
        out for the item.
    -   **arBuyOrderPrices** **(Array of Table)**
        -   **monPrice** **([Money](../Classes/Money.md))** - The
            amount that the buy order is paying per item.
        -   **nCount** **(Integer)** - The number of items that the buy
            order will purchase before it is fulfilled.
    -   **arSellOrderPrices** **(Array of Table)**
        -   **monPrice** **([Money](../Classes/Money.md))** - The sell
            order's price per item.
        -   **nCount** **(Integer)** - The number of items in the sell
            order.
-   **arOrders** **(Array of
    [CommodityOrder](../Classes/CommodityOrder.md))** - A listing of
    all of the buy and sell orders open for the item.

------------------------------------------------------------------------

`Event`

Communicator\_ShowQueuedMsg
---------------------------

------------------------------------------------------------------------

`Event`

CommunityRegistrarClose
-----------------------

------------------------------------------------------------------------

`Event`

CommunityRegistrarOpen
----------------------

------------------------------------------------------------------------

`Event`

ContractBoardClose
------------------

------------------------------------------------------------------------

`Event`

ContractBoardOpen
-----------------

------------------------------------------------------------------------

`Event`

ContractFloater
---------------

------------------------------------------------------------------------

`Event`

ContractGoodQualityChanged
--------------------------

------------------------------------------------------------------------

`Event`

ContractObjectiveUpdated
------------------------

------------------------------------------------------------------------

`Event`

ContractStateChanged
--------------------

------------------------------------------------------------------------

`Event`

CostumeCooldownComplete
-----------------------

------------------------------------------------------------------------

`Event`

CostumeForgetResult
-------------------

------------------------------------------------------------------------

`Event`

CostumeSaveResult
-----------------

------------------------------------------------------------------------

`Event`

CostumeUnlockResult
-------------------

------------------------------------------------------------------------

`Event`

CraftingDiscoveryHotCold
------------------------

### Description

Fires whenever the player completes a coordinate crafting session inside
a discovery area.

### Params

-   **eHotColdResult**
    **(CraftingLib.CodeEnumCraftingDiscoveryHotCold)** - Returns how
    close the previous crafting attempt was to a discoverable recipe.
-   **eDirection** **(CraftingLib.CodeEnumCraftingDirection)** - The
    direction of the discoverable schematic from the previous result.

------------------------------------------------------------------------

`Event`

CraftingExtractItem (Deprecated)
--------------------------------

------------------------------------------------------------------------

`Event`

CraftingInterrupted
-------------------

### Description

Fires whenever a crafting attempt is interrupted by the player moving or
other external source.

------------------------------------------------------------------------

`Event`

CraftingModItem (Deprecated)
----------------------------

### Description

Fires when the player is holding ALT and clicks on an item. This fires
when the mouse button is raised.

### Params

-   **itemMod** **([Item](../Classes/Item.md))** - The item that the
    player is attempting to moddify.

------------------------------------------------------------------------

`Event`

CraftingSchematicComplete
-------------------------

### Description

Fires when the player finishes crafting an item.

### Params

-   **idSchematic** **(Integer)** - The id number for the schematic that
    was completed.
-   **bSuccess** **(Boolean)** - Whether or not the crafting attempt was
    successful.
-   **nXPGained** **(Integer)** - The amount of XP gained from the
    crafting attempt.
-   **arMaterials** **(Array of Integer)** - The id number of each
    material that is returned to the player.
-   **idResultSchematic** **(Integer)** - The schematic id for the final
    item that is created. This can be different from idSchematic when
    crafting a variant.
-   **idCraftedItem** **(Integer)** - The item that was crafted from the
    schematic.

------------------------------------------------------------------------

`Event`

CraftingSchematicInfoReceived (Deprecated)
------------------------------------------

------------------------------------------------------------------------

`Event`

CraftingSchematicLearned
------------------------

### Description

Fires when the player learns a new crafting schematic.

### Params

-   **eTradeskill** **(CraftingLib.CodeEnumTradeskill)** - The
    tradeskill associated with the schematic.
-   **idSchematic** **(Integer)** - The id number for the schematic that
    the player learned.

------------------------------------------------------------------------

`Event`

CraftingSchematicList (Deprecated)
----------------------------------

------------------------------------------------------------------------

`Event`

CraftingStationClose
--------------------

### Description

Fired when the player stops interacting with or moves too far away from
a crafting station.

------------------------------------------------------------------------

`Event`

CraftingUpdateCurrent
---------------------

### Description

Fires whenever the current crafting schematic is updated. This includes
starting/resuming a schematic, adding additives and catalysts,
adding/removing/modifying microchips, and completing the craft.

------------------------------------------------------------------------

`Event`

CREDDExchangeInfoResults
------------------------

### Description

Returns results for the CREDDExchangeLib.RequestExchangeInfo() call from
the server.

### Params

-   **tStats** **(Table)**
    -   **nBuyOrderCount** **(Integer)** - The number of CREDD buy
        orders that are open.
    -   **nSellOrderCount** **(Integer)** - The number of CREDD sell
        orders that are open.
    -   **arBuyOrderPrices** **(Array of Table)**
        -   **monPrice** **([Money](../Classes/Money.md))** - The
            amount that the buy order is paying for CREDD.
        -   **nCount** **(Integer)** - The number of CREDD that the buy
            order tries to buy before it is fulfilled.
    -   **arSellOrderPrices** **(Array of Table)**
        -   **monPrice** **([Money](../Classes/Money.md))** - The
            amount of money the sell order is asking for each CREDD.
        -   **nCount** **(Integer)** - The number of CREDD available in
            the sell order.
-   **arOrders** **(Array of
    [CREDDExchangeOrder](../Classes/CREDDExchangeOrder.md))** - A table
    with all the CREDD buy and sell orders.

------------------------------------------------------------------------

`Event`

CREDDExchangeOperationResults (Deprecated)
------------------------------------------

------------------------------------------------------------------------

`Event`

CREDDExchangeWindowClose
------------------------

### Description

Fires when the player changes their interaction target from a CREDD
Exchange to another NPC, when a player moves far enough away from a
CREDD Exchange, or after Event\_CancelCREDDExchange() is called.

------------------------------------------------------------------------

`Event`

CREDDOperationHistoryResults
----------------------------

### Description

Returns the results of the CREDDExchangeLib.GetCREDDHistory() call.

### Params

-   **tHistory** **(Array of Table)**
    -   **eOperation** **(CREDDExchangeLib.CodeEnumAccountOperation)** -
        The type of operation performed in entry.
    -   **bInitiator** **(Boolean)** - Whether or not the player set up
        the buy or sell order for this entry.
    -   **monAmount** **([Money](../Classes/Money.md))** - The amount
        of money exchanged in this entry.
    -   **nLogAge** **(Float)** - How long ago the listed operation took
        place, in days.
    -   **nFriendId** **(Integer)** - The account friend id number of
        the other player involved in the transaction. This only returns
        a value if an account friend was involved in the transaction.

------------------------------------------------------------------------

`Event`

CREDDRedeemResult
-----------------

------------------------------------------------------------------------

`Event`

CrystalTooltip
--------------

------------------------------------------------------------------------

`Event`

CSIKeyPressed
-------------

### Description

When the client side interaction input key is pressed or released

### Params

-   **bKeyDown** **(Boolean)** - True when the key is down; false when
    the key is up.

------------------------------------------------------------------------

`Event`

DailyLoginUpdate
----------------

------------------------------------------------------------------------

`Event`

DashCastFail
------------

### Description

Fires when the player attempts to dash while they have no dash charges.

------------------------------------------------------------------------

`Event`

DashCastSuccess
---------------

### Description

Fires when the player successfully dashes.

------------------------------------------------------------------------

`Event`

DashEnergyUpdated
-----------------

------------------------------------------------------------------------

`Event`

DatacubePlaybackEnded
---------------------

### Description

Fires when a datacube's VO ends or is forced to end.

------------------------------------------------------------------------

`Event`

DatacubeUpdated
---------------

### Description

Fires when the player unlocks with a new datacube, journal entry, or
Tales From Beyond the Fringe.

### Params

-   **idEntry** **(Integer)** - The id number for the entry.
-   **bIsVolume** **(Boolean)** - Whether or not the entry was unlocked
    by entering a trigger volume.

------------------------------------------------------------------------

`Event`

DebugPrerequisite (Deprecated)
------------------------------

### Description

Fires when certain dev commands are used. Displays the debug string for
prereqs.

### Params

-   **outputStr** **(String)**

------------------------------------------------------------------------

`Event`

DecorPreviewClose
-----------------

### Description

Fires whenever a decor or plug preview window closes.

------------------------------------------------------------------------

`Event`

DecorPreviewOpen
----------------

### Description

Fires whenever the player opens the decor or plug preview window.

### Params

-   **idItemDisplayed** **(Integer)** - The id number for the plug or
    decor being previewed.

------------------------------------------------------------------------

`Event`

Dialog\_Close
-------------

### Description

Fires whenever the player picks a dialog option that should close the
dialog window.

------------------------------------------------------------------------

`Event`

Dialog\_QuestShare
------------------

### Description

Fires whenever a group member attempts to share a quest that the player
does not have yet.

### Params

-   **queShared** **([Quest](../Classes/Quest.md))** - The quest that
    the player is attempting to share.
-   **unitSharingPlayer** **([Unit](../Classes/Unit.md))** - The unit
    that shared the quest.

------------------------------------------------------------------------

`Event`

Dialog\_ResponseText
--------------------

### Description

Fires whenever the player selects an option in the dialog text.

### Params

-   **strText** **(String)** - The option that the player selected in
    the dialog tree.

------------------------------------------------------------------------

`Event`

Dialog\_ShowState
-----------------

### Description

Updates and displays the Dialog's contents and responses based on the
provided Ids.

### Params

-   **nStateId** **(Integer)** - The id of the state, such as
    DialogState\_TopicChoice or DialogState\_QuestAccept or
    DialogState\_QuestComplete or more.
-   **queDialog** **([Quest](../Classes/Quest.md))** - The quest
    associated with the dialog tree.

------------------------------------------------------------------------

`Event`

Dialog\_ViewIntro (Deprecated)
------------------------------

------------------------------------------------------------------------

`Event`

DialogClosing (Deprecated)
--------------------------

------------------------------------------------------------------------

`Event`

DisabledGameplaySystemNotification
----------------------------------

------------------------------------------------------------------------

`Event`

DuelAccepted
------------

### Description

Fires whenever a player accepts a duel request.

### Params

-   **fCountdownTimer** **(Float)** - The countdown timer before the
    duel starts (in seconds).

------------------------------------------------------------------------

`Event`

DuelCancelWarning
-----------------

### Description

Fires whenever a player re-enters the dueling area while the "Left Area"
warning is displayed.

------------------------------------------------------------------------

`Event`

DuelLeftArea
------------

### Description

Fires whenever the player leaves the dueling area.

### Params

-   **fWarningTime** **(Float)** - The amount of time (in seconds) that
    the player has to re-enter the dueling area before they forfiet.

------------------------------------------------------------------------

`Event`

DuelStateChanged
----------------

### Description

Fires whenever the player's duel state changes.

### Params

-   **unitDueling** **([Unit](../Classes/Unit.md))** - The player's
    duel opponent.
-   **eDuelState** **(GameLib.CodeEnumDuelState)** - The duel state that
    the player has entered.

------------------------------------------------------------------------

`Event`

DyeLearned
----------

### Description

Fires whenever the player learns a new dye color.

### Params

-   **idDye** **(Integer)** - The id number of the dye.
-   **arDyeInfo** **(Array of Integer)** - A list of ids for each dye
    the player has learned.

------------------------------------------------------------------------

`Event`

EldanForgeClose
---------------

------------------------------------------------------------------------

`Event`

EldanForgeOpen
--------------

------------------------------------------------------------------------

`Event`

EldanForgeResult
----------------

------------------------------------------------------------------------

`Event`

ElderPointsGained
-----------------

### Description

Fires whenever the player gains elder points.

### Params

-   **nAmount** **(Integer)** - The base number of elder points the
    player gained.
-   **nRested** **(Integer)** - The number of elder points granted by
    the player's rested bonus.

------------------------------------------------------------------------

`Event`

ElderPointsLimitReached
-----------------------

### Description

Fires whenever the player reaches their daily elder point cap.

------------------------------------------------------------------------

`Event`

EpisodeStateChanged
-------------------

### Description

Fires whenever the episode becomes active or is completed.

### Params

-   **idEpisode** **(Integer)** - The id number for the episode whose
    state changed.
-   **eOldState** **(Integer)** - The episode's previous state. This
    lines up with the Episode.EpisodeState set of int constants.
-   **eNewState** **(Integer)** - The episode's new state. This lines up
    with the Episode.EpisodeState set of int constants.

------------------------------------------------------------------------

`Event`

ErrorDialogSetSelection (Deprecated)
------------------------------------

### Params

-   **index** **(Integer)**

------------------------------------------------------------------------

`Event`

EscapeKeyPressed\_Gacha
-----------------------

------------------------------------------------------------------------

`Event`

FactionFloater
--------------

### Description

Fires whenever the player gains reputation with a faction and float text
should be shown.

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit who
    gained the reputation. This should always be the current player.
-   **strMessage** **(String)** - The string that should be displayed in
    the floating text.
-   **nAmount** **(Integer)** - The amount of reputation gained.
-   **strFactionName** **(String)** - The name of the faction that the
    player gained reputation with.
-   **idFaction** **(Integer)** - The id number of the faction that the
    player gained reputation with.

------------------------------------------------------------------------

`Event`

FlightPathUpdate
----------------

### Description

Fires whenever the player learns a new flight path, a settler builds a
flight path improvement, or a settler built flight path expires.

------------------------------------------------------------------------

`Event`

FlippedCardMouseEnter
---------------------

------------------------------------------------------------------------

`Event`

FlippedCardMouseLeave
---------------------

------------------------------------------------------------------------

`Event`

FloaterMultiHeal
----------------

------------------------------------------------------------------------

`Event`

FloaterMultiHit
---------------

------------------------------------------------------------------------

`Event`

FloaterTransference
-------------------

------------------------------------------------------------------------

`Event`

ForceResurrect
--------------

### Description

Fires when the player's automatic release timer runs out while they are
dead.

------------------------------------------------------------------------

`Event`

FortuneCoinSpent
----------------

------------------------------------------------------------------------

`Event`

FriendshipAccountCharacterLevelUpdate
-------------------------------------

### Description

Fires whenever an account friend's character gains a level.

### Params

-   **idFriend** **(Integer)** - The friend id of the player that gained
    a level.

------------------------------------------------------------------------

`Event`

FriendshipAccountDataUpdate
---------------------------

### Description

Fires whenever an account friend's nickname, presence, public note, or
online/offline status changes.

### Params

-   **idFriend** **(Integer)** - The account friend ID of the player.

------------------------------------------------------------------------

`Event`

FriendshipAccountFriendRemoved
------------------------------

### Description

Fires whenever one person on either side of an account friendship
removes the other as an account friend.

### Params

-   **idFriend** **(Integer)** - The friend id of the account friend
    that was removed.

------------------------------------------------------------------------

`Event`

FriendshipAccountFriendsRecieved
--------------------------------

### Description

Fires whenever a player accepts an account friend invite that was sent
to them, when another player accepts an account friend invite that they
sent, or when the player logs in.

### Params

-   **arFriendInfo** **(Array of Table)**
    -   **nId** **(Integer)** - The new friend id.
    -   **strPublicNote** **(String)** - The new friend's public note.
    -   **strPrivateNote** **(String)** - The new friend's private note.
    -   **strCharacterName** **(String)** - The name of the character
        that the account friend is currently on.
    -   **nPresenceState** **(Integer)** - The player's current presence
        state. This lines up with the FriendshipLib.AccountPresenceState
        set of contants.
    -   **fLastOnline** **(Float)** - The amount of time since the
        player was last online (in days). If this value is 0, then the
        player is online.

------------------------------------------------------------------------

`Event`

FriendshipAccountInviteRemoved
------------------------------

### Description

Fires whenever the player declines an account friend invite from another
player.

### Params

-   **idFriend** **(Integer)** - The id number for the invite that was
    sent.

------------------------------------------------------------------------

`Event`

FriendshipAccountInvitesRecieved
--------------------------------

### Description

Fired whenever the player receives an account friend invite from another
player or when the player logs in.

### Params

-   **arInviteInfo** **(Array of Table)**
    -   **nId** **(Integer)** - The friendship id for the invite.
    -   **strInviteType** **(Integer)** - The type of invite that was
        received. This value lines up with the
        FriendshipLib.CharacterFriendshipType set of int constants.
    -   **strNote** **(String)** - The note that was sent along with the
        invite.
    -   **strDisplayName** **(string)** - The display name of the player
        who sent the invite. This should be the name of the character
        that they're currently on @ the realm that that player is on.
    -   **bIsNew** **(Boolean)** - Whether the invite has been seen by
        the player before or not.

------------------------------------------------------------------------

`Event`

FriendshipAccountPersonalStatusUpdate
-------------------------------------

### Description

Fires if an account friend logs on or off, updates their presence, or
updates their public note.

------------------------------------------------------------------------

`Event`

FriendshipAdd
-------------

### Description

Fires whenever a new friend is added to the friends list.

### Params

-   **idFriend** **(Integer)** - The friend id for the new friend.

------------------------------------------------------------------------

`Event`

FriendshipInviteRemoved
-----------------------

### Description

Fires whenever a player declines a friend invite from another player.

### Params

-   **idFriend** **(Integer)** - The friend id of the invite that was
    removed.

------------------------------------------------------------------------

`Event`

FriendshipInvitesRecieved
-------------------------

### Description

Fires whenever the player receives a new friend invite.

### Params

-   **arInviteInfo** **(Array of Table)**
    -   **nId** **(Integer)** - The friend id associated with the
        invite.
    -   **strCharacterName** **(String)** - The name of the character
        that sent the invite.
    -   **nClassId** **(GameLib.CodeEnumClass)** - The inviting
        character's class.
    -   **nPathId** **(Integer)** - This lines up with the
        PlayerPathLib.PlayerPathType set of constants.
    -   **nLevel** **(Integer)** - The invitor's current level.
    -   **bIsNew** **(Boolean)** - Whether or the player has seen the
        invite before or not.
    -   **strNote** **(String)** - The note that was sent along with the
        invite.
    -   **fDaysUntilExpired** **(Float)** - The number of days before
        the invite automatically expires.

------------------------------------------------------------------------

`Event`

FriendshipLoaded
----------------

### Description

Fires when the FriendshipLib has loaded. This only occurrs when a
character is logged in, not when reloading the UI.

------------------------------------------------------------------------

`Event`

FriendshipLocation
------------------

### Description

Fired in response to FriendshipLib.GetLocations(). Returns all the
necessary data to see the name of the zone that the player is in.

### Params

-   **arLocationInfo** **(Array of Table)**
    -   **nId** **(Integer)** - The friend id associated with this
        location.
    -   **strWorldZone** **(String)** - The name of the zone where the
        player is.

------------------------------------------------------------------------

`Event`

FriendshipPostRemove
--------------------

------------------------------------------------------------------------

`Event`

FriendshipRemove
----------------

### Description

Fired whenever a friend is removed from the player's friends list.

### Params

-   **idFriend** **(Integer)** - The friend id of the player that was
    removed from the friends list.

------------------------------------------------------------------------

`Event`

FriendshipRequest (Deprecated)
------------------------------

------------------------------------------------------------------------

`Event`

FriendshipResult
----------------

### Description

Fires whenever an error is encountered when working with FriendsLib
functionality.

### Params

-   **strName** **(String)** - This value is always 0.
-   **eResult** **(Integer)** - The type of error that was fired. This
    lines up with the values in FriendshipLib.FriendshipResult.

------------------------------------------------------------------------

`Event`

FriendshipSuggestedAdd
----------------------

### Description

Fired whenever a suggested player is added to the friends list.

### Params

-   **idFriend** **(Integer)** - The friend id that was added to the
    friends list from the suggested list.

------------------------------------------------------------------------

`Event`

FriendshipSuggestedRemove
-------------------------

### Description

Fires whenever a player is removed from the Suggested Friends list. This
includes when players on the Suggested list are removed due to going
over the maximum number of friends on that list.

### Params

-   **idFriend** **(Integer)** - The friend id of the player that was
    removed from the friends list.

------------------------------------------------------------------------

`Event`

FriendshipSuggestedUpdate
-------------------------

### Description

Fires whenever a suggested friend's information updates. This is usually
due to level changes.

### Params

-   **idFriend** **(Integer)** - The id number of the suggested friend
    that was updated.

------------------------------------------------------------------------

`Event`

FriendshipUpdate
----------------

### Description

Fired whenever a friend's character gets updated, such as when their
level changes.

### Params

-   **idFriend** **(Integer)** - The friend id of the player who was
    updated.

------------------------------------------------------------------------

`Event`

FriendshipUpdateOnline
----------------------

### Description

Fired whenever the player comes online or goes offline.

### Params

-   **idFriend** **(Integer)** - The friend id of the player whose
    online/offline state changed.

------------------------------------------------------------------------

`Event`

GalacticArchiveArticleAdded
---------------------------

### Description

Fires whenever the player unlocks the first entry of a particular
Galactic Archive Article.

### Params

-   **artNewArticle**
    **([GalacticArchiveArticle](../Classes/GalacticArchiveArticle.md))** -
    The article that was just unlocked.

------------------------------------------------------------------------

`Event`

GalacticArchiveEntryAdded
-------------------------

### Description

Fires whenever a new entry is unlocked for an already known Galactic
Archive Article.

### Params

-   **artParent**
    **([GalacticArchiveArticle](../Classes/GalacticArchiveArticle.md))** -
    The article that this entry belongs to.
-   **entUnlocked**
    **([GalacticArchiveEntry](../Classes/GalacticArchiveEntry.md))** -
    The newly unlocked entry.

------------------------------------------------------------------------

`Event`

GalacticArchiveLinkClick (Deprecated)
-------------------------------------

### Description

Fired whenever a player clicks a link in a Galactic Archive article.

### Params

-   **artLinkTarget**
    **([GalacticArchiveArticle](../Classes/GalacticArchiveArticle.md))** -
    The target of the link that was clicked.

------------------------------------------------------------------------

`Event`

GalacticArchiveRefresh
----------------------

### Description

Fires whenever the Galactic Archive refreshes. This is generally when
the player changes zones.

------------------------------------------------------------------------

`Event`

GameClickProp
-------------

### Description

Fires whenever the player left clicks on a non-interactive object in the
world.

### Params

-   **idProp** **(Integer)** - The id number of the prop that the player
    selected.

------------------------------------------------------------------------

`Event`

GameClickSky
------------

### Description

Fires when the player left clicks on the sky.

------------------------------------------------------------------------

`Event`

GameClickUnit
-------------

### Description

Fires whenever the player left clicks on a unit in game.

### Params

-   **unitSelected** **([Unit](../Classes/Unit.md))** - The unit that
    was clicked on.

------------------------------------------------------------------------

`Event`

GameClickWorld
--------------

### Description

Fires whenever the player left clicks a location in the world.

### Params

-   **vec3Location** **([Vector3](../Classes/Vector3.md))** - The
    location where the player clicked in the world.

------------------------------------------------------------------------

`Event`

GameEnd
-------

------------------------------------------------------------------------

`Event`

GenericError
------------

### Description

Fires whenever the player causes a generic error that is flashed on the
screen.

### Params

-   **eError** **(GameLib.CodeEnumGenericError)** - The error that was
    fired.
-   **strMessage** **(String)** - The string that should be shown when
    the error is thrown.

------------------------------------------------------------------------

`Event`

GenericEvent\_PlayerCampStart (Deprecated)
------------------------------------------

### Description

Fired whenever the player starts to log off.

------------------------------------------------------------------------

`Event`

GenericEvent\_PlayerExitCancel (Deprecated)
-------------------------------------------

### Description

Fires when the player cancels the log off timer.

------------------------------------------------------------------------

`Event`

GenericMapNodeDisabled
----------------------

### Description

Fires whenever a GenericMapNode is disabled and hidden on the
GenericMap.

### Params

-   **mapDisabled**
    **([GenericMapNode](../Classes/GenericMapNode.md))** - The
    GenericMapNode that was disabled.

------------------------------------------------------------------------

`Event`

GenericMapNodeEnabled
---------------------

### Description

Fires whenever a GenericMapNode becomes active and is shown on the
GenericMap.

### Params

-   **mapEnabled**
    **([GenericMapNode](../Classes/GenericMapNode.md))** - The
    GenericMapNode that was enabled.

------------------------------------------------------------------------

`Event`

GenericMapShow
--------------

### Description

Fires when the generic map should be shown to the player.

### Params

-   **idZoneMap** **(Integer)** - The zone map id that should be shown.
-   **arGenericMapNodeInfo** **(Array of Table)**
    -   **bEnabled** **(Boolean)** - Whether or not the map node is
        enabled when the map is shown.
    -   **oNode**
        **([GenericMapNode](../Classes/GenericMapNode.md))** - A
        GenericMapNode that should be placed on the map.

------------------------------------------------------------------------

`Event`

GMChatTellFailed
----------------

------------------------------------------------------------------------

`Event`

Group\_Add
----------

### Description

Fires whenever another player is added to a group that the current
player is already part of.

### Params

-   **strName** **(String)** - The name of the player that was added to
    the group.

------------------------------------------------------------------------

`Event`

Group\_FlagsChanged
-------------------

------------------------------------------------------------------------

`Event`

Group\_Join
-----------

### Description

Fires whenever the current player first joins a group.

------------------------------------------------------------------------

`Event`

Group\_JoinRequest
------------------

### Description

Fires whenever a player sends a request to join an existing party.

### Params

-   **strRequesterName** **(String)** - The name of the player
    requesting to join the group.

------------------------------------------------------------------------

`Event`

Group\_Left
-----------

### Description

Fires whenever the player is no longer in the group. This only fires for
the current player.

### Params

-   **eReason** **(GroupLib.RemoveReason)** - The method used to remove
    the player from the group.

------------------------------------------------------------------------

`Event`

Group\_LootRulesChanged
-----------------------

------------------------------------------------------------------------

`Event`

Group\_MemberFlagsChanged
-------------------------

### Params

-   **nMemberIdx** **(Integer)** - The member index of the character
    whose permissions changed.
-   **bIsFromPromotion** **(boolean)** - Whether or not the change in
    permissions is due to the character being promoted.
-   **tFlags** **(Table)**
    -   **bCanInvite** **(Boolean)** - Whether or not the player can
        send invites to other players.
    -   **bCanKick** **(Boolean)** - Whether or not the player can kick
        members from the group.
    -   **bDisconnected** **(Boolean)** - Whether or not the character
        has disconnected from the game.
    -   **bPending** **(Boolean)**
    -   **bTank** **(Boolean)** - Whether or not the player has been
        marked as a tank.
    -   **bHealer** **(Boolean)** - Whether or not the player has been
        marked as a Healer.
    -   **bDPS** **(Boolean)** - Whether or not the player has been
        marked as DPS.
    -   **bMainTank** **(Boolean)** - Whether or not the player is
        marked as a raid's Main Tank.
    -   **bMainAssist** **(Boolean)** - Whether or not the player is
        flagged as one of the raid's Main Assists.
    -   **bRaidAssistant** **(Boolean)** - Whether or not the group
        member is flagged as a Raid Assistant.
    -   **bReady** **(Boolean)** - Whether or not the player has
        responded positively to a ready check.
    -   **bRoleLock** **(Boolean)** - Whether or not the Role Lock has
        been turned on.
    -   **bCanMark** **(Boolean)** - Whether or not the player can place
        target markers on units.
    -   **bHasSetReady** **(Boolean)**

------------------------------------------------------------------------

`Event`

Group\_MemberOrderChanged (Deprecated)
--------------------------------------

### Description

Fires whenever the group's order has changed.

### Usage/Example

```lua
    Note, this functionality is not currently implemented, so this event will never fire.
```

------------------------------------------------------------------------

`Event`

Group\_MemberPromoted
---------------------

### Description

Fires whenever a group member is promoted to group leader

### Params

-   **strName** **(String)** - The name of the player who was promoted
    to leader.
-   **bSelf** **(Boolean)** - Whether the current player was promoted.

------------------------------------------------------------------------

`Event`

Group\_Mentor
-------------

### Description

Fired whenever the player should be given the option to mentor another
character and whenever they stop mentoring someone.

### Params

-   **arMentorTargets** **(Table)**
    -   **unitMentee** **([Unit](../Classes/Unit.md))** - The unit that
        can be mentored.
    -   **tMemberInfo** **(Table)**
        -   **nMemberIdx** **(Integer)** - The member's index in the
            group.
        -   **nOrder** **(Integer)**
        -   **eRaceId** **(GameLib.CodeEnumRace)** - The player's race.
        -   **eClassId** **(GameLib.CodeEnumClass)** - The player's
            class.
        -   **strCharacterName** **(String)** - The player's name.
        -   **strRaceName** **(String)** - The name of the player's
            race.
        -   **strClassName** **(String)** - The name of the player's
            class.
        -   **ePathType** **(Integer)** - The player's path. This lines
            up with the PlayerPathLib.PlayerPathType set of constants.
        -   **bIsLeader** **(Boolean)** - Whether or not the player is
            the group leader.
        -   **bIsOnline** **(Boolean)** - Whether or not the player is
            online.
        -   **nLevel** **(Integer)** - The player's level.
        -   **nEffectiveLevel** **(Integer)** - The player's effective
            level, after mentoring or rallying modifications.
        -   **nHealth** **(Integer)** - The player's current health.
        -   **nHealthMax** **(Integer)** - The player's maximum health.
        -   **nShield** **(Integer)** - The amount of shield strength
            the player currently has.
        -   **nShieldMax** **(Integer)** - The maximum amount of shield
            the player can have.
        -   **nInterruptArmor** **(Integer)** - The player's current
            Interrupt Armor.
        -   **nInterruptArmorMax** **(Integer)** - The maximum amount of
            interrupt armor a player can have.
        -   **nAbsorption** **(Integer)** - The amount of absorption
            shield the player currently has.
        -   **nAbsorptionMax** **(Integer)** - The maximum amount of
            absorption shield the player can have.
        -   **nMana** **(Integer)** - The amount of focus the player
            currently has.
        -   **nManaMax** **(Integer)** - The maximum amount of focus the
            player can have.
        -   **nMarkerId** **(Integer)** - The target marker assigned to
            the player.
        -   **nMenteeIdx** **(Integer)** - The index of the player in
            the list of potential units to mentor.
        -   **bIsMentoring** **(Boolean)** - Whether or not the player
            is currently mentoring another player.
        -   **bIsMentored** **(Boolean)** - Whether or not another
            player is already being mentored by another player.
        -   **tMentoredBy** **(Array of Integer)** - The indices of
            players within the group that are mentoring the player.
        -   **tFlags** **(Table)**
            -   **bCanInvite** **(Boolean)** - Whether or not the player
                can invite other players to the group.
            -   **bCanKick** **(Boolean)** - Whether or not the player
                can kick other members from the group.
            -   **bDisconnected** **(Boolean)** - Whether or not the
                player is currently disconnected from the game.
            -   **bPending** **(Boolean)**
            -   **bTank** **(Boolean)** - Whether or not this player has
                been marked as a tank.
            -   **bHealer** **(Boolean)** - Whether or not this player
                has been marked as a healer.
            -   **bDPS** **(Boolean)** - Whether or not this player has
                been flagged as DPS.
            -   **bMainTank** **(Boolean)** - Whether or not the player
                has been marked as a raid's Main Tank.
            -   **bMainAssist** **(Boolean)** - Whether or not the
                player has been marked as a raid's Main Assist.
            -   **bRaidAssistant** **(Boolean)** - Whether or not the
                player has been marked as a raid's Raid Assistant.
            -   **bReady** **(Boolean)** - Whether or not the player has
                responded positively to a ready check.
            -   **bRoleLocked** **(Boolean)** - Whether or not the
                raid's roles are locked.
            -   **bCanMark** **(Boolean)** - Whether or not the player
                can place target markers on units.
            -   **bHasSetReady** **(Boolean)**

------------------------------------------------------------------------

`Event`

Group\_MentorLeftAOI
--------------------

### Description

Fired whenever a pair of players using mentoring get too far apart, when
the players move within range again, and when the timer to move within
range runs out.

### Params

-   **nTimeUntilCanceled** **(Integer)** - How long the players have (in
    seconds) to return to eachother's Area of Interest before the
    Mentoring status is canceled.
-   **bTimerStop** **(Boolean)** - Whether or not the countdown timer
    has stopped. This can be because the players have moved within range
    of eachother or the timer has expired.

------------------------------------------------------------------------

`Event`

Group\_MentorRelationship
-------------------------

### Description

Fires whenever a player begins mentoring another player. This event is
passed to every member in the group.

### Params

-   **unitMentor** **([Unit](../Classes/Unit.md))** - The unit that is
    mentoring the other member.
-   **unitMentee** **([Unit](../Classes/Unit.md))** - The unit being
    mentored.

------------------------------------------------------------------------

`Event`

Group\_Operation\_Result
------------------------

### Description

Fires whenever an error occurs when attempting a group related action.

### Params

-   **strName** **(String)** - The name of the player that the operation
    was attempted on.
-   **eResult** **(GroupLib.ActionResult)** - The reason why the
    operation failed.

------------------------------------------------------------------------

`Event`

Group\_ReadyCheck
-----------------

### Description

Fires whenever a ready check is started.

### Params

-   **nMemberIdx** **(Integer)** - The group index of the player who
    started the ready check.
-   **strMessage** **(String)** - The message sent out with the ready
    check.

------------------------------------------------------------------------

`Event`

Group\_ReadyCheckCooldownExpired
--------------------------------

------------------------------------------------------------------------

`Event`

Group\_Referral
---------------

### Description

Fires whenever a group member referrs another player for an invitation
to the group.

### Params

-   **nMemberIdx** **(Integer)** - The group index of the member who
    sent the referral.
-   **strTargetName** **(String)** - The name of the player that was
    referred to the group.

------------------------------------------------------------------------

`Event`

Group\_Remove
-------------

### Description

Fired whenever a player is removed from the group

### Params

-   **strMemberName** **(String)** - The name of the player that was
    removed from the group.
-   **eReason** **(GroupLib.RemoveReason)** - The method used to remove
    the player from the group.

------------------------------------------------------------------------

`Event`

Group\_Request\_Result
----------------------

### Description

Fires whenever actions related to joining an existing group processed by
the server.

### Params

-   **strPlayerName** **(String)** - The name of the player whose group
    the player is attempting to join.
-   **eResult** **(GroupLib.Result)** - The type of action that was
    processed.
-   **bIsJoin** **(Boolean)** - Whether the message is an attempt to
    join the group or not.

------------------------------------------------------------------------

`Event`

Group\_SetMark
--------------

### Description

Fires whenever a group member sets a target marker on a unit.

### Params

-   **idMarker** **(Integer)** - The id number of the target marker that
    was placed on the unit.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit the
    marker was placed on.

------------------------------------------------------------------------

`Event`

Group\_Updated
--------------

### Description

Fires whenever the the number of players in a group change, the instance
difficulty is changed,

------------------------------------------------------------------------

`Event`

Group\_UpdatePosition
---------------------

### Description

Fires at regular, 1 second intervals with updates to the player's
positions in the world.

### Params

-   **arMemberPosInfo** **(Array of Table)**
    -   **nIndex** **(Integer)** - The member index of the player that
        this position information belongs to.
    -   **idWorld** **(Integer)** - The id of the world that the player
        is on.
    -   **bInCombatPvp** **(Boolean)** - Whether or not the player is in
        combat with another player.
    -   **bInCombatPve** **(Boolean)** - Whether or not the player is in
        combat with an NPC.
    -   **bInCombat** **(Boolean)** - Whether or not the player is in
        combat.
    -   **tZoneMap** **(Table)**
        -   **strFolder** **(string)** - The folder that the zone is
            found in. This is usually the zone name, without any spaces
            or punctuation.
        -   **strName** **(String)** - The name of the zone that the
            player is in.
        -   **id** **(Integer)** - The id number of the zone that the
            player is in.
        -   **fNorth** **(Float)** - The northern coordinate boundry of
            the zone.
        -   **fSouth** **(Float)** - The southern coordinate boundry of
            the zone.
        -   **fEast** **(Float)** - The eastern coordinate boundry of
            the zone.
        -   **fWest** **(Float)** - The western coordinate boundry of
            the zone.
        -   **continentId** **(Integer)** - The id number for the
            continent that the zone is on.
        -   **parentZoneId** **(Integer)** - The id number for the
            parent zone of the current zone. If the zone has no parent,
            this will be 0.
    -   **tWorldLoc** **(Table)** - The player's coordinates in the
        world.
        -   **x** **(Float)**
        -   **y** **(Float)**
        -   **z** **(Float)**

------------------------------------------------------------------------

`Event`

GroupBag\_Changed (Deprecated)
------------------------------

------------------------------------------------------------------------

`Event`

GroupBag\_ItemDistributed (Deprecated)
--------------------------------------

### Params

-   **idItem** **(Integer)**
-   **idWinner** **(Integer)**

------------------------------------------------------------------------

`Event`

GroupLeaderPhaseChanged
-----------------------

### Description

Fires whenever the group leader moves in another phase.

### Params

-   **bJoinAllowed** **(Boolean)** - Whether or not the player is
    allowed to join the group leader's phase.
-   **nReferenceType** **(Integer)**
-   **nReferenceId** **(Integer)**

------------------------------------------------------------------------

`Event`

GuildBankerClose
----------------

### Description

Fires whenever the player interacts with another target or moves away
from a guild bank while interacting with it.

------------------------------------------------------------------------

`Event`

GuildBankerOpen
---------------

### Description

Fires whenever the player interacts with a guild bank.

### Params

-   **unitBank** **([Unit](../Classes/Unit.md))** - The unit that the
    player interacted with to open the guild bank.

------------------------------------------------------------------------

`Event`

GuildBankItem
-------------

### Description

Fires whenever an item is added or removed from the guild bank, or moved
to a different slot within the bank.

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild that
    owns the bank.
-   **eGuildType** **(Integer)** - The type of guild that owns the bank.
    This should always be GuildLib.GuildType\_Guild.
-   **nSlotIndex** **(Integer)** - The bank slot where the item is
    placed.
-   **bRemoved** **(Boolean)** - Whether the item was removed from the
    bank or not.

------------------------------------------------------------------------

`Event`

GuildBankLog
------------

### Description

Returns the results from Guild:RequestBankLogs(),
Guild:RequestMoneyLogs(), and Guild:RequestRepairLogs().

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild that
    owns the bank that the logs belong to.
-   **arLogs** **(Array of Table)** - Each log entry contains the name
    of the player who performed the action and the time since the action
    occurred. All other variables depend on the type of log entry. The
    different combinations are:\
    \
    uMoneyDeposit\
    \
    uMoneyWithdraw\
    \
    uRepairWithdraw\
    \
    nTab\
    uItemDeposit\
    nStack\
    \
    nTab\
    uItemWithdraw\
    nStack
    -   **strName** **(String)** - The name of the player that performed
        the action in the log.
    -   **fOccuredAgoDays** **(Float)** - The amount of time since the
        action was created (in days).
    -   **uMoneyDeposit** **([Money](../Classes/Money.md))** - The
        money that was deposited in the bank.
    -   **uMoneyWithdraw** **([Money](../Classes/Money.md))** - The
        money that was withdrawn from the bank.
    -   **uRepairWithdraw** **([Money](../Classes/Money.md))** - The
        money that was spent on a guild repair.
    -   **nTab** **(Integer)** - The tab that an item was added or
        removed from.
    -   **nStack** **(Integer)** - The number of items in the stack that
        was added or removed from the guild bank.
    -   **uItemDeposit** **([Item](../Classes/Item.md))** - The item
        that was deposited in the guild bank.
    -   **uItemWithdraw** **([Item](../Classes/Item.md))** - The item
        that was withdrawn from the guild bank.

------------------------------------------------------------------------

`Event`

GuildBankTab
------------

### Description

Fires in response to Guild:OpenBankTab(), verifying that the tab was
successfully opened.

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild who
    owns the bank that the player is interacting with.
-   **nTab** **(Integer)** - The index of the tab that was opened.

------------------------------------------------------------------------

`Event`

GuildBankTabCount
-----------------

### Description

Fires whenever a Bank Tab perk is purchased for the guild.

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild who
    owns the bank that the tab was added to.

------------------------------------------------------------------------

`Event`

GuildBankTabRename
------------------

### Description

Fires whenever the player successfully renames a guild bank tab. To
actually get the new tab names, Guild:GetBankTabName() will have to be
called for each tab.

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild who
    owns the bank that contains the renamed tab.

------------------------------------------------------------------------

`Event`

GuildBankWithdraw
-----------------

### Description

Fires whenever a player successfully withdraws money or items from the
guild bank. This only fires for the player who performed the withdraw
action.

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild who
    owns the bank that the player withdrew from.

------------------------------------------------------------------------

`Event`

GuildChange
-----------

### Description

Fired whenever the player is added to or removed from a guild, circle,
arena team, or warparty.

------------------------------------------------------------------------

`Event`

GuildClassification
-------------------

------------------------------------------------------------------------

`Event`

GuildEmblem (Deprecated)
------------------------

------------------------------------------------------------------------

`Event`

GuildEventLogChange
-------------------

### Description

Fires whenever a player joins the guild, a player leaves the guild, the
guild unlocks a perk, activates a perk, or calls
Guild:RequestEventLogList()

### Params

-   **guildSource** **([Guild](../Classes/Guild.md))** - The guild
    whose logs have changed.

------------------------------------------------------------------------

`Event`

GuildFlags
----------

### Description

Fires whenever the guild turns taxes or recruitment on or off.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))** - The guild
    whose flags have been updated.

------------------------------------------------------------------------

`Event`

GuildInfluenceAndMoney
----------------------

### Description

Fires whenever a guild's credits or influence are gained, withdrawn, or
spent.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))** - The guild
    whose influence or credits were updated.
-   **nInfluence** **(Integer)** - The amount of influence the guild has
    after the update.
-   **monUpdated** **([Money](../Classes/Money.md))** - The amount of
    money the guild has after the update.
-   **nBonusInfluenceRemaining** **(Integer)** - The amount of bonus
    influence remaining after the update.

------------------------------------------------------------------------

`Event`

GuildInfoMessage
----------------

### Description

Fires whenever a guild's Info Message is updated.

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild whose
    Info Message has changed.

------------------------------------------------------------------------

`Event`

GuildInvite
-----------

### Description

Fired whenever the player receives an invitation to a guild.

### Params

-   **strGuildName** **(String)** - The name of the guild that the
    player is invited to join.
-   **strInvitorName** **(String)** - The player who sent the invite.
-   **eGuildType** **(Integer)** - An integer representing the type of
    guild that the player is invited to join. This lines up with the
    GuildLib.GuildType set of constants.
-   **tFlags** **(Table)**
    -   **bTax** **(Boolean)** - Whether or not guild taxes are enabled
        for the guild that sent the invite.
    -   **bRecruiting** **(Boolean)** - Whether or not the guild has
        flagged itself as "Recruiting"

------------------------------------------------------------------------

`Event`

GuildMemberChange
-----------------

### Description

Fires whenever information about a guild member has changed. This
includes coming online, going offline, leveling up, having their guild
rank changed, joining or leaving the guild, or changing their guild
note.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))** - The guild
    whose member's info changed.

------------------------------------------------------------------------

`Event`

GuildMessageOfTheDay
--------------------

### Description

Fires whenever the guild's Message of the Day has been updated and when
the player logs in on a character.

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild that
    the Message of the Day belongs to.

### Remarks

There is currently a bug where the GuildMessageOfTheDay event fires long
before the chat log is loaded, so players are not seeing the message of
the day.

------------------------------------------------------------------------

`Event`

GuildName
---------

### Description

Fires whenever the guild's name is changed. This is only done when a
player or GM sets up a new guild name after a forced name change.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))** - The guild
    whose name was updated.

------------------------------------------------------------------------

`Event`

GuildNameplateChange
--------------------

### Description

Fires whenever a player changes the guild name on their nameplate. This
event only fires for the character that changed the nameplate.

### Params

-   **guildShown** **([Guild](../Classes/Guild.md))** - The guild that
    the player selected to show on their nameplate.

------------------------------------------------------------------------

`Event`

GuildPerkActivated
------------------

### Description

Fires whenever a limited duration guild perk has been activated.

### Params

-   **guildActivated** **([Guild](../Classes/Guild.md))** - The guild
    that the perk was activated for.
-   **idGuildPerk** **(Integer)** - The id number of the guild perk that
    was activated.

------------------------------------------------------------------------

`Event`

GuildPerkDeactivated
--------------------

### Description

Fires whenever a guild perk is turned off or runs out of time.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))** - The guild
    whose perk was turned off.

------------------------------------------------------------------------

`Event`

GuildPerkUnlocked
-----------------

------------------------------------------------------------------------

`Event`

GuildPvp
--------

### Description

Fires whenever an Arena Team's or Warparty's win/loss record or rating
has updated.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))**

------------------------------------------------------------------------

`Event`

GuildQueueStateChanged
----------------------

### Description

Fires whenever the arena team's or warparty's enters a queue, leaves a
queue, enters a match, or leaves a match.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))** - The guild
    who's queue state has updated.
-   **eOldState** **(Integer)** - The guild's previous queue state. This
    lines up with the GuildLib.GuildQueueState set of constants.
-   **eNewState** **(Integer)** - The guild's new queue state. This
    lines up with the GuildLib.GuildQueueState set of constants.

### Remarks

Possible values for the different states are:\
GuildLib.GuildQueueState\_Normal\
GuildLib.GuildQueueState\_Queuing\
GuildLib.GuildQueueState\_Queued\
GuildLib.GuildQueueState\_InBattle

------------------------------------------------------------------------

`Event`

GuildRankChange
---------------

### Description

Fires whenever a guild, circle, or warparty adds a rank, removes a rank,
renames a rank, or changes a rank's permissions.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))** - The guild
    whose rank was updated.

------------------------------------------------------------------------

`Event`

GuildRegistrarClose
-------------------

### Description

Fires whenever the player was interacting with a Guild Registrar and
either interacts with another NPC or moves too far from the Registrar

------------------------------------------------------------------------

`Event`

GuildRegistrarOpen
------------------

### Description

Fires whenever the player interacts with a Guild Registrar NPC.

------------------------------------------------------------------------

`Event`

GuildResult
-----------

### Description

Fires the result of various guild operations. These can be error
messages, operation types, or success messages

### Params

-   **guildSource** **([Guild](../Classes/Guild.md))** - The guild that
    the operation was performed on.
-   **strTarget** **(String)** - The name of the target of the
    operation. This can be a character name or rank name.
-   **nRank** **(Integer)** - If the operation was a rank update, then
    this value is the index of the rank that was updated. Otherwise,
    this can be 1 or 0.
-   **eResult** **(Integer)** - The result of the operation. This value
    is pulled from the GuildLib.GuildResult set of constants.

------------------------------------------------------------------------

`Event`

GuildRoster
-----------

### Description

Fires in response to Guild:RequestMembers(). This returns a list of the
guild's members.

### Params

-   **arMembers** **(Array of Table)**
    -   **strName** **(String)** - The name of the guild member.
    -   **nRank** **(Integer)** - The member's guild rank.
    -   **strClass** **(String)** - The member's class, in string form.
    -   **eClass** **(GameLib.CodeEnumClass)** - The member's class, as
        an enum.
    -   **ePathType** **(Integer)** - The member's path type. This lines
        up with the PlayerPathLib.PlayerPathType set of constants.
    -   **nLevel** **(Integer)** - The member's level.
    -   **fLastOnline** **(Float)** - The amount of time since the
        player was last online, in days.
    -   **nPvPWins** **(Integer)** - The number of PvP wins that the
        player has participated in with the guild. This value is only
        relevant for Arena Teams and Warparties.
    -   **nPvPLosses** **(Integer)** - The number of PvP losses that the
        player participated in with the guild. This only applies for
        Arena Teams and Warparties.
    -   **nPvPDraws** **(Integer)** - The number of PvP draws the player
        was involved in with the guild. This only applies for Arena
        Teams and Warparties.
    -   **strNote** **(String)** - The note set by the player.
-   **guildSource** **([Guild](../Classes/Guild.md))** - The guild that
    is returning its member roster.

------------------------------------------------------------------------

`Event`

GuildStandard
-------------

### Description

Fires whenever the guild's holomark is updated.

### Params

-   **guildOwner** **([Guild](../Classes/Guild.md))** - The guild that
    owns the holomark.

------------------------------------------------------------------------

`Event`

GuildWarCoinsChanged
--------------------

### Description

Fires whenever the Warparty gains or spends warcoins.

### Params

-   **guildUpdated** **([Guild](../Classes/Guild.md))** - The Warparty
    whose warcoins were updated.
-   **nWarcoinsDelta** **(Integer)** - The change in the number of
    warcoins that the guild has.

------------------------------------------------------------------------

`Event`

HarvestItemsSentToOwner
-----------------------

### Description

Fires whenever the player harvests resources on a neighbor's housing
plot while the plot's Resource Sharing returns more than 0% to the
owner.

### Params

-   **arItemsSent** **(Table)**
    -   **item** **([Item](../Classes/Item.md))** - The item that is
        sent to the plug's owner.
    -   **nCount** **(Integer)** - The stack count of the item that is
        sent to the plug's owner.

------------------------------------------------------------------------

`Event`

HazardEnabled
-------------

### Description

Fires whenever a hazard is activated for the player. This can be
triggered by entering a hazard area or by a quest/event starting a
hazard for the player.

### Params

-   **idHazard** **(Integer)** - The hazard's id number.
-   **strDisplayText** **(String)** - The string associated with the
    hazard. This is displayed next to the hazard bar in the base UI.

------------------------------------------------------------------------

`Event`

HazardRemoved
-------------

### Description

Fires whenever a the conditions for a hazard are removed from the
player.

### Params

-   **idHazard** **(Integer)** - The hazard's id number.

------------------------------------------------------------------------

`Event`

HazardRemoveMinimapUnit
-----------------------

### Description

Fires whenever a hazard that is currently shown on the Minimap should be
removed.

### Params

-   **idHazard** **(Integer)** - The id number for the hazard that
    should be removed.
-   **unitRemoved** **([Unit](../Classes/Unit.md))** - The unit used to
    represent the hazard on the minimap.

------------------------------------------------------------------------

`Event`

HazardShowMinimapUnit
---------------------

### Description

Fires whenever a hazard should be displayed on the minimap.

### Params

-   **idHazard** **(Integer)** - The hazard's id number.
-   **unitMarker** **([Unit](../Classes/Unit.md))** - The unit used to
    mark the hazard on the minimap.
-   **bBeneficial** **(Boolean)** - Whether or not the hazard is helpful
    to the player.

------------------------------------------------------------------------

`Event`

HazardUpdated
-------------

### Description

Fires whenever information about the hazard has been updated.

------------------------------------------------------------------------

`Event`

HealthyGamingUpdate
-------------------

------------------------------------------------------------------------

`Event`

HideBank
--------

### Description

Fires whenever the player is interacting with a Bank NPC and either
interacts with another unit or moves too far from the NPC.

------------------------------------------------------------------------

`Event`

HideDye
-------

### Description

Fires whenever the player is interacting with a Stylist NPC and either
interacts with another unit or moves too far from the NPC.

------------------------------------------------------------------------

`Event`

HideGachaUI
-----------

------------------------------------------------------------------------

`Event`

HideInstanceGameModeDialog
--------------------------

### Description

Fires whenever the the player moves away from an instance portal or
teleporter after receiving a ShowInstanceGameModeDialog event.

### Params

-   **bNeedToNotifyServer** **(Boolean)** - Whether or not the server
    needs to be notified of the window closing. This should be passed
    into GameLib.OnClosedInstanceSettings().

------------------------------------------------------------------------

`Event`

HideQuestLog
------------

### Description

Fires in response to the Event\_HideQuestLog() function that can be
called from Lua.

------------------------------------------------------------------------

`Event`

HighlightProgressOption
-----------------------

### Description

Fires whenever a button flashes during Memory CSIs.

### Params

-   **nButton** **(Integer)** - The button that should be highlighted.

------------------------------------------------------------------------

`Event`

HintArrowDistanceUpdate
-----------------------

------------------------------------------------------------------------

`Event`

HousingBasicsUpdated
--------------------

### Description

Fires whenever the player changes the visitor rules for their housing
plot.

------------------------------------------------------------------------

`Event`

HousingBuildComplete
--------------------

### Description

Fires whenever a housing plug starts building.

### Params

-   **nSocketUpdated** **(Integer)** - The socket that was updated.

------------------------------------------------------------------------

`Event`

HousingBuildStarted
-------------------

### Description

Fires whenever the player starts to build a plug on a housing plot.

### Params

-   **nSocket** **(Integer)** - The socket number where the plug is
    being built.

------------------------------------------------------------------------

`Event`

HousingButtonCrate
------------------

------------------------------------------------------------------------

`Event`

HousingButtonLandscape
----------------------

------------------------------------------------------------------------

`Event`

HousingButtonList
-----------------

------------------------------------------------------------------------

`Event`

HousingButtonRemodel
--------------------

------------------------------------------------------------------------

`Event`

HousingButtonVendor
-------------------

------------------------------------------------------------------------

`Event`

HousingEditModeChanged
----------------------

------------------------------------------------------------------------

`Event`

HousingExitEditMode
-------------------

------------------------------------------------------------------------

`Event`

HousingMannequinClose
---------------------

### Description

Fires when the player is interacting with a mannequin and either
interacts with another NPC or moves too far away from the mannequin.

------------------------------------------------------------------------

`Event`

HousingMannequinOpen
--------------------

### Description

Fires whenever the player interacts with a Mannequin.

------------------------------------------------------------------------

`Event`

HousingNamePropertyOpen
-----------------------

### Description

Fires when a player enters their housing plot when it does not have a
name. It is meant to inform the UI that the player needs to name their
home.

------------------------------------------------------------------------

`Event`

HousingNeighborInviteAccepted
-----------------------------

### Description

Fires whenever a player is added to the Neighbors list.

### Params

-   **strName** **(String)** - The new neighbor's name.

------------------------------------------------------------------------

`Event`

HousingNeighborInviteDeclined
-----------------------------

### Description

Fired whenever a player declines a neighbor invite that they received.
This event is sent to both the person who sent the invite and the person
who declined the invite.

### Params

-   **strName** **(String)** - The name of the player who declined the
    invite.

------------------------------------------------------------------------

`Event`

HousingNeighborInviteRecieved
-----------------------------

### Description

Fires whenever a player is sent an invite from another player.

### Params

-   **strInvitorName** **(String)** - The name of the player that sent
    the neighbor invite.

------------------------------------------------------------------------

`Event`

HousingNeighborsLoaded
----------------------

### Description

Fires whenever a player is removed from the Neighbors list.

------------------------------------------------------------------------

`Event`

HousingNeighborUpdate
---------------------

### Description

Fires whenever a player is added as a neighbor, a neighbor goes offline
or comes online, or a player is set as a roommate.

### Params

-   **idNeighbor** **(Integer)** - The neighbor id of the player that
    was updated.

------------------------------------------------------------------------

`Event`

HousingPrivacyUpdated
---------------------

### Description

Fires whenever a player changes their housing plot's visiter rules to or
from Private.

### Params

-   **bIsPrivate** **(Boolean)** - Determines whether or not the
    building is private.

------------------------------------------------------------------------

`Event`

HousingRandomResidenceListRecieved
----------------------------------

### Description

Fires in response to HousingLib.RequestRandomResidenceList().

### Usage/Example

```lua
    Note, this event does not contain the resdence list.  It only informs the player that the list is ready to be obtained via the HousingLib.GetRandomResidenceList.
```

------------------------------------------------------------------------

`Event`

HousingRealtorOpen (Deprecated)
-------------------------------

------------------------------------------------------------------------

`Event`

HousingResult
-------------

### Description

Fires whenever an error is thrown due to a housing operation.

### Params

-   **strName** **(String)** - The name of the player who caused the
    error.
-   **eResult** **(Integer)** - The error message sent. These are found
    in the HousingLib.HousingResult set of constants.

------------------------------------------------------------------------

`Event`

Inspect
-------

### Description

Fires whenever the server returns information from the Unit:Inspect()
function.

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that the
    inspect function was called on.
-   **arItems** **(Array of [Item](../Classes/Item.md))** - The items
    that unitTarget currently has equipped.

------------------------------------------------------------------------

`Event`

InstanceSetBusy (Deprecated)
----------------------------

------------------------------------------------------------------------

`Event`

Interaction (Deprecated)
------------------------

### Params

-   **title** **(String)**
-   **type** **(Integer)**
-   **speed** **(Integer)**
-   **sweetspot** **(Integer)**
-   **width1** **(Integer)**
-   **width2** **(Integer)**

------------------------------------------------------------------------

`Event`

InterfaceMenu\_ToggleLoreWindow
-------------------------------

### Description

Fires whenever the player presses the key bound to the Lore window.

------------------------------------------------------------------------

`Event`

InvokeCraftingWindow
--------------------

### Description

Fires whenever the player interacts with a crafting station.

------------------------------------------------------------------------

`Event`

InvokeEscapeMenu (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Event`

InvokeFriendsList (Deprecated)
------------------------------

------------------------------------------------------------------------

`Event`

InvokeOptionsDialog (Deprecated)
--------------------------------

------------------------------------------------------------------------

`Event`

InvokeScientistExperimentation
------------------------------

### Description

Fires whenever the player interacts with an object or NPC that starts a
Scientist Experimentation minigame.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    mission that the experimentation minigame belongs to.

------------------------------------------------------------------------

`Event`

InvokeSettlerBuild
------------------

### Description

Fires whenever a settler interacts with a settler depot.

### Params

-   **unitHub** **([Unit](../Classes/Unit.md))** - The settler hub that
    the player is interacting with.
-   **arImprovements** **(Array of
    [SettlerImprovement](../Classes/SettlerImprovement.md))** - An
    array of settler improvements that can be built at this hub.

------------------------------------------------------------------------

`Event`

InvokeShuttlePrompt (Deprecated)
--------------------------------

------------------------------------------------------------------------

`Event`

InvokeSoldierBuild (Deprecated)
-------------------------------

------------------------------------------------------------------------

`Event`

InvokeTaxiWindow
----------------

### Description

Fires whenever the player interacts with a taxi vendor.

### Params

-   **unitTaxi** **([Unit](../Classes/Unit.md))** - The taxi station
    that the player interacted with.
-   **bIsSettlerTaxi** **(Boolean)** - Whether or not this taxi station
    was created as a settler improvement.

------------------------------------------------------------------------

`Event`

InvokeTradeskillTrainerWindow
-----------------------------

### Description

Fires whenever the player interacts with a tradeskill trainer.

### Params

-   **unitTrainer** **([Unit](../Classes/Unit.md))** - The tradeskill
    trainer NPC that the player interacted with.

------------------------------------------------------------------------

`Event`

InvokeVendorWindow
------------------

### Description

Fires whenever the player interacts with a vendor NPC.

### Params

-   **unitVendor** **([Unit](../Classes/Unit.md))** - The vendor that
    the player interacted with.

------------------------------------------------------------------------

`Event`

ItemAdded
---------

### Description

Fires whenever an item is placed in a player's inventory by a method
other than looting.

### Params

-   **itemBase** **([Item](../Classes/Item.md))** - The base version of
    the item that was added, before random stats, glyphs, or microchips
    are factored in.
-   **nCount** **(Integer)** - How many stacks of the item were added to
    the player's inventory.
-   **eUpdateReason** **(Item.CodeEnumItemUpdateReason)** - A value that
    represents the method that was used to obtain the item.
-   **itemInstance** **([Item](../Classes/Item.md))** - The specific
    instance of the item. This is the version of the item that the
    player sees in their inventory.

### Remarks

Examples of actions that would trigger this event include salvaging
items, taking an item from the account inventory, crafting an item, and
purchasing an item from a vendor.

------------------------------------------------------------------------

`Event`

ItemAuctionBidPosted
--------------------

### Description

Fires whenever someone places a bid on an item that the player has
posted on the Auction House. This does not apply for items where the
person who bought the item selected the "Buy Now" option

### Params

-   **auctBidOn** **([ItemAuction](../Classes/ItemAuction.md))** - The
    auction that was bid on.

------------------------------------------------------------------------

`Event`

ItemAuctionBidResult
--------------------

### Description

Fires whenever the player places a bid or selects the "Buy Now" option
for an item on the auction house.

### Params

-   **eResult** **(GameLib.CodeEnumGenericError)** - The result of the
    player's attempt to place a bid on the auction. A result of Ok means
    the bid was successful.
-   **auctBidOn** **([ItemAuction](../Classes/ItemAuction.md))** - The
    auction that the player bid on or bought.

------------------------------------------------------------------------

`Event`

ItemAuctionExpired
------------------

### Description

Fires whenever an auction's listing expires.

### Params

-   **auctExpired** **([ItemAuction](../Classes/ItemAuction.md))** -
    The auction that expired.

------------------------------------------------------------------------

`Event`

ItemAuctionOutbid
-----------------

### Description

Fires whenever someone else places a higher bid or buys an auction that
the player had bid on.

### Params

-   **auctBidOn** **([ItemAuction](../Classes/ItemAuction.md))** - The
    item that the player was outbid on.

------------------------------------------------------------------------

`Event`

ItemAuctionsDisabled
--------------------

### Description

Fires if the Auction House is disabled or re-enabled by the server.

### Params

-   **bDisabled** **(Boolean)** - Whether or not the Auction House is
    disabled.

------------------------------------------------------------------------

`Event`

ItemAuctionSearchResults
------------------------

### Description

Returns results from the the MarketplaceLib.SearchAuctionableItems()
function.

### Params

-   **nPage** **(Integer)** - The page that the player is currently
    viewing.
-   **nTotalResults** **(Integer)** - The total number of search results
    that the player has received.
-   **arAuctions** **(Array of
    [ItemAuction](../Classes/ItemAuction.md))** - An array containing
    all of the auctions returned in the search results.

------------------------------------------------------------------------

`Event`

ItemAuctionWon
--------------

### Description

Fires whenever the player wins an auction.

### Params

-   **auctWon** **([ItemAuction](../Classes/ItemAuction.md))** - The
    auction that the player won.

------------------------------------------------------------------------

`Event`

ItemCancelResult
----------------

### Description

Fires whenever the player tries to cancel one of their auctions.

### Params

-   **eResult** **(GameLib.CodeEnumGenericError)** - The result of the
    player's attempt to cancel the auction. If it was successful, this
    value will be Ok.
-   **auctCanceled** **([ItemAuction](../Classes/ItemAuction.md))** -
    The auction that the player attempted to cancel.

------------------------------------------------------------------------

`Event`

ItemConfirmClearRestockOnEquip
------------------------------

------------------------------------------------------------------------

`Event`

ItemDeprecationAlert
--------------------

------------------------------------------------------------------------

`Event`

ItemDurabilityUpdate
--------------------

### Description

Fires whenever one of the player's items loses some durability or gets
repaired.

### Params

-   **itemUpdated** **([Item](../Classes/Item.md))** - The item whose
    durability changed.
-   **nPreviousDurability** **(Integer)** - The item's durability before
    the update.

------------------------------------------------------------------------

`Event`

ItemLink
--------

### Description

Fires whenever the player attempts to add an item link to the chat
window.

### Params

-   **itemLinked** **([Item](../Classes/Item.md))** - The item that was
    linked in chat.

------------------------------------------------------------------------

`Event`

ItemModified
------------

### Description

Fires whenever the player makes a change to an item. These changes
include adding runes, removing runes, and unlocking additional rune
slots.

### Params

-   **itemModified** **([Item](../Classes/Item.md))** - The item that
    the player modified.

------------------------------------------------------------------------

`Event`

ItemRemoved
-----------

### Description

Fires whenever an item is removed from the player's inventory. This can
be caused by destroying the item, turning in a quest that auto-removes
the item, salvaging the item, or selling the item at a vendor.

### Params

-   **itemRemoved** **([Item](../Classes/Item.md))** - The item that
    was removed from the player's inventory.
-   **nCount** **(Integer)** - The stack size of the item that was
    deleted.
-   **eReason** **(Item.CodeEnumItemUpdateReason)** - The reason the
    item was updated.

------------------------------------------------------------------------

`Event`

ItemSentToCrate
---------------

### Description

Fires whenever the player sends a decor item from their inventory to the
crate.

### Params

-   **itemMoved** **([Item](../Classes/Item.md))** - The decor item
    that the player placed in their crate.
-   **nCount** **(Integer)** - The stack size of the item that was sent
    to the crate.
-   **eReason** **(Item.CodeEnumItemUpdateReason)** - The method the
    player used to send the item to the crate.

------------------------------------------------------------------------

`Event`

KeyBindingKeyChanged
--------------------

### Description

Fires whenever a player saves changes to their keybindings. The event is
fired once for each keybinding that was changed.

### Params

-   **strKeybinding** **(String)** - The name of the keybinding that was
    changed.

------------------------------------------------------------------------

`Event`

LoginError
----------

### Description

Fires whenever an error is thrown while the player attempts to log in.

### Params

-   **strErrorMessage** **(String)** - The error message that should be
    shown to the player.
-   **bHandled** **(Boolean)** - Whether or not the error was handled
    before it affected the player.

------------------------------------------------------------------------

`Event`

LogOut
------

### Description

Fires whenever the player finishes logging out with their character.

------------------------------------------------------------------------

`Event`

LootAssigned
------------

### Description

Fires whenever a master looter assigns loot to a party or raid member.
This event is seen by everyone in the party or raid.

### Params

-   **itemAssigned** **([Item](../Classes/Item.md))** - The item that
    was assigned to the player.
-   **strWinnerName** **(String)** - The name of the player that the
    item was assigned to.

------------------------------------------------------------------------

`Event`

LootBindcheck
-------------

### Description

Fires whenever the player attempts to loot an item that is Bind on
Pickup while in a group.

### Params

-   **tLootInfo** **(Table)** - A table that contains information about
    the Bind on Pickup items that the player is trying to loot.
    -   **nLootId** **(Integer)** - A unique identifier for the item
        that was dropped.
    -   **itemDrop** **([Item](../Classes/Item.md))** - The item that
        was dropped.

------------------------------------------------------------------------

`Event`

LootRoll
--------

### Description

Fires whenever a playerrolls on an item in the Need vs. Greed looting
system. This only fires after every member has selected need, greed, or
pass on the item and is sent to every member in the group.

### Params

-   **itemLoot** **([Item](../Classes/Item.md))** - The item that the
    players are rolling for.
-   **strPlayerName** **(String)** - The player that rolled for the
    item.
-   **bNeed** **(Boolean)** - Whether or not the player chose "Need" for
    the item.

------------------------------------------------------------------------

`Event`

LootRollAllPassed
-----------------

### Description

Fires when everyone in the group passes on an item under the Need vs.
Greed system.

### Params

-   **itemPassed** **([Item](../Classes/Item.md))** - The item that all
    of the players passed on.

------------------------------------------------------------------------

`Event`

LootRollPassed
--------------

### Description

Fires whenever a player passes on an item or does not select an option
within the time limit under the Need vs. Greed system.

### Params

-   **itemPassed** **([Item](../Classes/Item.md))** - The item that the
    player passed on.
-   **strPlayerName** **(String)** - The name of the player that passed
    on the item.

------------------------------------------------------------------------

`Event`

LootRollSelected
----------------

### Description

Fires whenever a player selects Need or Greed under the Need vs. Greed
loot system.\
\

### Params

-   **itemRolling** **([Item](../Classes/Item.md))** - The item that
    the player chose to roll for.
-   **strPlayerName** **(String)** - The name of the player that chose
    to roll.
-   **bNeed** **(Boolean)** - Whether or not the player chose to roll
    Need on the item.

------------------------------------------------------------------------

`Event`

LootRollUpdate
--------------

### Description

Fires whenever a new item is added or removed from the list of items
that the player can roll for.

------------------------------------------------------------------------

`Event`

LootRollWon
-----------

### Description

Fires whenever a player wins a piece of loot under the Need vs. Greed
system.

### Params

-   **itemWon** **([Item](../Classes/Item.md))** - The item that the
    player won.
-   **strWinnerName** **(String)** - The name of the player who won the
    roll.
-   **bNeed** **(Boolean)** - Whether or not the player chose "Need" on
    the item.

------------------------------------------------------------------------

`Event`

LootTakenBy
-----------

------------------------------------------------------------------------

`Event`

MailAddAttachment
-----------------

### Description

Fires whenever the player right clicks an item in their inventory to
attach it to a mail message.

### Params

-   **nLocationId** **(Integer)** - An id number that represents the
    item's location in the player's inventory.

### Usage/Example

```lua
    The value from this function can be passed into functions such as Unit:LockInventorySlot().
```

------------------------------------------------------------------------

`Event`

MailBoxActivate
---------------

### Description

Fires whenever the player interacts with a mailbox.

------------------------------------------------------------------------

`Event`

MailBoxDeactivate
-----------------

### Description

Fires whenever the player is interacting with a mailbox and interacts
with another targets or moves far enough away from the mailbox.

------------------------------------------------------------------------

`Event`

MailRead
--------

### Description

Fires whenever the player opens a piece of mail that was previously
unread.

### Params

-   **strMailId** **(String)** - The identifier for the mail that was
    read.

------------------------------------------------------------------------

`Event`

MailResult
----------

### Description

Fires whenever an error is thrown when the player attempts to perform a
mail action

### Params

-   **eResult** **(GameLib.CodeEnumGenericError)** - The reason the
    operation failed.

------------------------------------------------------------------------

`Event`

MannequinWindowClose (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Event`

MannequinWindowOpen (Deprecated)
--------------------------------

------------------------------------------------------------------------

`Event`

MapHexesRevealed (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Event`

MapTrackedUnitDisable (Deprecated)
----------------------------------

------------------------------------------------------------------------

`Event`

MapTrackedUnitUpdate (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Event`

MarketplaceWindowClose
----------------------

### Description

Fires whenever the player is interacting with the Commodities Exchange
NPC, then interacts with another NPC or moves too far from the
Commodities Exchange NPC.

------------------------------------------------------------------------

`Event`

MasterCraftsmanClose
--------------------

------------------------------------------------------------------------

`Event`

MasterCraftsmanOpen
-------------------

------------------------------------------------------------------------

`Event`

MasterLootUpdate
----------------

### Description

Fires whenever the items available to be assigned by the master looter
change. This is fired for everyone in the party or raid.

------------------------------------------------------------------------

`Event`

MatchEntered
------------

### Description

Fired whenever the player enters a PvP Match.

------------------------------------------------------------------------

`Event`

MatchExited
-----------

### Description

Fires whenever the player leaves a PvP Match.

------------------------------------------------------------------------

`Event`

MatchFinished
-------------

### Description

Fires when the PvP Match ends.

------------------------------------------------------------------------

`Event`

MatchingAverageWaitTimeUpdated
------------------------------

### Description

Fires whenever the server recognizes a change in the average wait time
for the Match the player is queued for.

------------------------------------------------------------------------

`Event`

MatchingCancelPendingGame
-------------------------

### Description

Fires whenever a player fails to respond to a pending Match notification
before it times out or a member of the group declines to join the
pending game.

------------------------------------------------------------------------

`Event`

MatchingEligibilityChanged
--------------------------

### Description

Fires whenever a group member's eligibility for the dungeon that the
group is queued for changes.

------------------------------------------------------------------------

`Event`

MatchingGamePendingUpdate
-------------------------

### Description

Fires whenever players that were sent the pending game notification
accept or decline to join the match.

------------------------------------------------------------------------

`Event`

MatchingGameReady
-----------------

### Description

Fires whenever the player is able to join a matching game.

### Params

-   **bInProgress** **(Boolean)** - Whether the match that the player
    has already started or not.

------------------------------------------------------------------------

`Event`

MatchingJoinQueue
-----------------

### Description

Fires whenever the player successfully joins a matching queue.

------------------------------------------------------------------------

`Event`

MatchingLeaveQueue
------------------

### Description

Fires whenever the player successfully leaves a matching queue, declines
to join a pending match, or allows a pending match notification to time
out.

------------------------------------------------------------------------

`Event`

MatchingPvpInactivityAlert
--------------------------

### Description

Fires at regular intervals if the player is AFK in a PvP match. This is
triggered when the player has 2 minutes, 1 minute, 30 seconds, and 5
second intervals before they are removed from a match.

### Params

-   **nRemainingTimeMs** **(Integer)** - The amount of time before the
    player is removed from the match, in Milliseconds.

------------------------------------------------------------------------

`Event`

MatchingRoleCheckCanceled
-------------------------

------------------------------------------------------------------------

`Event`

MatchingRoleCheckHidden
-----------------------

### Description

Fires if the player is the one who joined the queue for a dungeon or
adventure. If the player is part of a group that joined the queue
together but is not the leader of that group, they will not receive this
event.

------------------------------------------------------------------------

`Event`

MatchingRoleCheckStarted
------------------------

### Description

Fires when a group queues for a dungeon or adventure or when they look
for new members from the queue.

------------------------------------------------------------------------

`Event`

MatchJoined
-----------

### Description

Fires when the player initially joins a match.

------------------------------------------------------------------------

`Event`

MatchLeft
---------

### Description

Fires whenever the player leaves the matching game.

------------------------------------------------------------------------

`Event`

MatchLookingForReplacements
---------------------------

### Description

Fires when an existing group starts looking for replacements. This event
is the result of the MatchingGame:LookForReplacements() function
successfully processing.

------------------------------------------------------------------------

`Event`

MatchStoppedLookingForReplacements
----------------------------------

### Description

Fires whenever a group that is looking for replacements fills or in
response to MatchingGame:StopLookingForReplacements()

------------------------------------------------------------------------

`Event`

MatchVoteKickBegin
------------------

### Description

Fires in response to someone in the group starting a vote to kick
another player from the group using the
MatchingGame:InitiateVoteToKick() function.

### Params

-   **unitMember** **([Unit](../Classes/Unit.md))** - The member that
    will be kicked if the vote is successful.

------------------------------------------------------------------------

`Event`

MatchVoteKickEnd
----------------

### Description

Fires when the server determines that a vote to kick a player has
finished or was canceled.

------------------------------------------------------------------------

`Event`

MatchVoteSurrenderBegin
-----------------------

### Description

Fires whenever a call to MatchingGame:InitiateVoteToSurrender() is
successfully called by someone on the player's team during a PvP match.

------------------------------------------------------------------------

`Event`

MatchVoteSurrenderEnd
---------------------

### Description

Fires when the server determines that a vote to surrender a PvP match
has finished or was canceled.

------------------------------------------------------------------------

`Event`

MessageFinished
---------------

### Description

Fires whenever a floating text message is destroyed.

### Params

-   **uMessage** **(Userdata)** - The floating text object that was
    destroyed.

------------------------------------------------------------------------

`Event`

MountUnlocked
-------------

### Description

Fires whenever the player unlocks a new mount.

### Params

-   **nMountId** **(Integer)** - The id number of the mount that was
    unlocked.

------------------------------------------------------------------------

`Event`

MouseOverUnitChanged
--------------------

### Description

Fires whenever the mouse is moved over a unit or off of a unit.

### Params

-   **unitMouseOver** **(unit)** - The unit that the mouse is currently
    over. This value is nil if the mouse moves off of a unit.

------------------------------------------------------------------------

`Event`

NavPointCleared
---------------

------------------------------------------------------------------------

`Event`

NavPointSet
-----------

------------------------------------------------------------------------

`Event`

NewCustomerSurveyRequest
------------------------

### Description

Fires whenever the player is asked to fill out a customer survey.

### Params

-   **nSurveyCount** **(Integer)** - The number of customer surveys the
    player has queued.

------------------------------------------------------------------------

`Event`

NextFrame
---------

### Description

Fires once every frame.

------------------------------------------------------------------------

`Event`

OnInstanceResetResult
---------------------

### Description

Fires whenever the player attempts to reset an instance of a dungeon or
adventure.

### Params

-   **bSuccessful** **(Boolean)** - Whether or not the instance was able
    to reset.

------------------------------------------------------------------------

`Event`

OpenSignature
-------------

------------------------------------------------------------------------

`Event`

OpenStore
---------

------------------------------------------------------------------------

`Event`

OpenStoreLinkCategory
---------------------

------------------------------------------------------------------------

`Event`

OpenStoreLinkSingle
-------------------

------------------------------------------------------------------------

`Event`

OwnedCommodityOrders
--------------------

### Description

Fires in response to MarketplaceLib.RequestOwnedCommodityOrders().

### Params

-   **arOrders** **(Array of
    [CommodityOrder](../Classes/CommodityOrder.md))** - An array that
    contains the player's open buy and sell orders on the commodity
    exchange.

------------------------------------------------------------------------

`Event`

OwnedItemAuctions
-----------------

### Description

Fires in response to the MarketplaceLib.RequestOwnedItemAuctions()
function.

### Params

-   **arAuctions** **([ItemAuction](../Classes/ItemAuction.md))** - An
    array of the player's open bids and listed items on the auction
    house.

------------------------------------------------------------------------

`Event`

P2PTradeCommit
--------------

### Description

Fired whenever the player commits to a trade using a TradeCommitButton
or an ActionConfirmButton whose data is set to
GameLib.CodeEnumConfirmButtonType.CommitTrade.

------------------------------------------------------------------------

`Event`

PartyBagItemAdded (Deprecated)
------------------------------

### Params

-   **guid** **(Integer)**

------------------------------------------------------------------------

`Event`

PartyBagItemAwarded (Deprecated)
--------------------------------

### Params

-   **guid** **(Integer)**

------------------------------------------------------------------------

`Event`

PartyBagItemRemoved (Deprecated)
--------------------------------

### Params

-   **guid** **(Integer)**

------------------------------------------------------------------------

`Event`

PartyBagItemTimerStarted (Deprecated)
-------------------------------------

### Params

-   **guid** **(Integer)**

------------------------------------------------------------------------

`Event`

PartyBagItemTimerStopped (Deprecated)
-------------------------------------

### Params

-   **guid** **(Integer)**

------------------------------------------------------------------------

`Event`

PartyBagItemTimerTick (Deprecated)
----------------------------------

### Params

-   **msTimeRemaining** **(Integer)**

------------------------------------------------------------------------

`Event`

PartyBagItemUpdated (Deprecated)
--------------------------------

### Params

-   **guid** **(Integer)**

------------------------------------------------------------------------

`Event`

PartyBagSharedItemsChanged (Deprecated)
---------------------------------------

------------------------------------------------------------------------

`Event`

PathLevelUp
-----------

### Description

Fires whenever the player gains a path level.

### Params

-   **nLevel** **(Integer)** - The player's new path level.
-   **strMessage** **(String)** - The message that is shown in chat when
    the event is fired.

------------------------------------------------------------------------

`Event`

PendingLootInteract
-------------------

------------------------------------------------------------------------

`Event`

PendingWorldRemovalCancel
-------------------------

------------------------------------------------------------------------

`Event`

PendingWorldRemovalWarning
--------------------------

------------------------------------------------------------------------

`Event`

PersonaUpdateCharacterStats
---------------------------

### Description

Fires whenever the player moves an item from one inventory slot to
another, the player gains a new item, or the player's stats change (via
a buff, debuff, or new equipment).

------------------------------------------------------------------------

`Event`

PetCustomizationFailed
----------------------

### Description

Fires whenever the player attempts to customize their pet or scanbot and
the attempt is not successful.

### Params

-   **tInfo** **(Table)**
    -   **ePetType** **(PetCustomizationLib.PetType)** - The type of pet
        that the player tried to customize.
    -   **idPet** **(Integer)** - The id number of the pet.
    -   **nFlairSlotIndex** **(Integer)** - The flair slot that the
        player tried to modify.
    -   **pcFlair** **([PetFlair](../Classes/PetFlair.md))** - The
        piece of flair that the player tried to set to nFlairSlotIndex.
-   **eResult** **(PetCustomizationLib.PetCustomizeResult)** - The
    reason why the customization attempt failed.

------------------------------------------------------------------------

`Event`

PetCustomizationUpdated
-----------------------

### Description

Fires whenever the player successfully update's a pet or scanbot's
customization options.

### Params

-   **pcCustomization**
    **([PetCustomization](../Classes/PetCustomization.md))** - The
    pet's new customization info.

------------------------------------------------------------------------

`Event`

PetFlairCleared
---------------

------------------------------------------------------------------------

`Event`

PetFlairUnlocked
----------------

### Description

Fires whenever the player unlocks a new piece of flair for their pet or
scanbot.

### Params

-   **idFlair** **(Integer)** - The id number of the pet flair that was
    unlocked.

------------------------------------------------------------------------

`Event`

PlayedTime
----------

### Description

Fires whenever the player types /played in chat.

### Params

-   **strCreationMessage** **(String)** - A string describing when the
    character was created.
-   **strPlayedTotal** **(String)** - A string describing the amount of
    time the player has played the game.
-   **strPlayedThisLevel** **(String)** - A string describing how much
    time the player has spent in game since gaining a level.
-   **strPlayedThisSession** **(String)** - A string describing how long
    the player has played since logging in this session.
-   **strCreationDate** **(String)** - A string that contains the
    character's creation date and time.
-   **nTimePlayedTotal** **(Integer)** - The amount of time that the
    player has played this character, in seconds.
-   **nTimePlayedLevel** **(Integer)** - The amount of time that the
    player has played since the character last leveled up, in seconds.
-   **nTimePlayedSession** **(Integer)** - The amount of time the player
    has played since logging in, in seconds.

------------------------------------------------------------------------

`Event`

PlayerChanged
-------------

### Description

Fires when the player first logs in, indicating that it has loaded.

------------------------------------------------------------------------

`Event`

PlayerCurrencyChanged
---------------------

### Description

Fires whenever the player earns or spends any form of currency.

------------------------------------------------------------------------

`Event`

PlayerEnteredWorld
------------------

------------------------------------------------------------------------

`Event`

PlayerEquippedItemChanged
-------------------------

### Description

Fires whenever the player equips or removes a piece of equipment.

### Params

-   **eSlot** **(GameLib.CodeEnumEquippedItems)** - The equipment slot
    that was updated.
-   **itemNew** **([Item](../Classes/Item.md))** - The item that was
    placed in the slot after the update. If no item was added, then this
    value will be nil.
-   **itemOld** **([Item](../Classes/Item.md))** - The item that was in
    the slot before the update. If the slot was empty, this value will
    be nil.

------------------------------------------------------------------------

`Event`

PlayerLevelChange
-----------------

### Description

Fires whenever the player gains a level. This is not effected by changes
in effective level caused by mentoring or rallying.

### Params

-   **nLevel** **(Integer)** - The player's new level.
-   **nAttributePoints** **(Integer)** - The number of attribute points
    that the player has available at the new level. This should always
    be 0.
-   **nAbilityPoints** **(Integer)** - The number of ability points
    granted to the character at the new level.

------------------------------------------------------------------------

`Event`

PlayerMovementSpeedUpdate
-------------------------

------------------------------------------------------------------------

`Event`

PlayerPathAdd
-------------

------------------------------------------------------------------------

`Event`

PlayerPathExplorerPowerMapEntered
---------------------------------

### Description

Fires whenever the player enters an area where a Tracking mission can be
started

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    Tracking mission that can be started at this location.

------------------------------------------------------------------------

`Event`

PlayerPathExplorerPowerMapExited
--------------------------------

### Description

Fires whenever the player leaves a location where a power map mission
can be started.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    mission that could have been started from the location that the
    player left.

------------------------------------------------------------------------

`Event`

PlayerPathExplorerPowerMapFailed
--------------------------------

### Description

Fires whenever the player fails a Tracking mission.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    mission that the player failed.

------------------------------------------------------------------------

`Event`

PlayerPathExplorerPowerMapStarted
---------------------------------

### Description

Fires whenever the player successfully starts a Tracking mission.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    Tracking mission that the player started.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that the
    player is supposed to follow for the mission.

------------------------------------------------------------------------

`Event`

PlayerPathExplorerPowerMapWaiting
---------------------------------

### Description

Fires when the unit that is being tracked in a Tracking mission reaches
its destination before the player.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    Tracking mission that the player is on.
-   **nVictoryDelay** **(Integer)** - The amount of time the player has
    to reach the destination before the mission fails.

------------------------------------------------------------------------

`Event`

PlayerPathExplorerScavengerHuntStarted
--------------------------------------

### Description

Fires whenever the player interacts with the NPC that starts a Scavenger
Hunt mission.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    Scavenger Hunt mission that was started.

------------------------------------------------------------------------

`Event`

PlayerPathMissionAdvanced
-------------------------

### Description

Fires whenever progress is made on a multi-step path mission.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    mission that was advanced.

------------------------------------------------------------------------

`Event`

PlayerPathMissionComplete
-------------------------

### Description

Fires whenever the player completes a path mission.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    mission that the player just completed.

------------------------------------------------------------------------

`Event`

PlayerPathMissionCompleteSound (Deprecated)
-------------------------------------------

------------------------------------------------------------------------

`Event`

PlayerPathMissionUnlocked
-------------------------

### Description

Fires whenever the player unlocks a new path mission. If multiple
missions are unlocked at once, an event will be fired for each of them.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    mission that was unlocked.

------------------------------------------------------------------------

`Event`

PlayerPathMissionUnlockedSound
------------------------------

### Description

Fires whenever a path mission is unlocked.

------------------------------------------------------------------------

`Event`

PlayerPathMissionUpdate
-----------------------

### Description

Fires whenever a path mission is unlocked, advanced, completed, or
failed.

### Params

-   **pmMission** **([PathMission](../Classes/PathMission.md))** - The
    path mission that was updated.

------------------------------------------------------------------------

`Event`

PlayerPathRefresh
-----------------

### Description

Fires whenever the player needs to redraw their path information, such
as on reloadui or changing zones.

------------------------------------------------------------------------

`Event`

PlayerPathRewardAvailable
-------------------------

### Description

Fires whenever the player completes all of the path missions in an
episode.

### Params

-   **peCompleted** **([PathEpisode](../Classes/PathEpisode.md))** -
    The path episode that the player completed.

------------------------------------------------------------------------

`Event`

PlayerPathScientistScanBotCooldown
----------------------------------

### Description

Fires when the player's ability to summon their scanbot is on cooldown,
such as after the player despawns their scanbot or their scanbot is
destroyed.

### Params

-   **fCooldown** **(Float)** - The number of seconds before the player
    can summon their scanbot.

------------------------------------------------------------------------

`Event`

PlayerPathScientistScanBotDeployed
----------------------------------

### Description

Fires whenever the player summons their scanbot.

------------------------------------------------------------------------

`Event`

PlayerPathScientistScanBotDespawned
-----------------------------------

### Description

Fires whenever the player manually despawns their scanbot or their
scanbot runs out of HP.

------------------------------------------------------------------------

`Event`

PlayerPathSoldierNewWhackAMoleBurrows (Deprecated)
--------------------------------------------------

------------------------------------------------------------------------

`Event`

PlayerPortraitMessage (Deprecated)
----------------------------------

### Params

-   **text** **(String)**
-   **crText** **(Color)**

------------------------------------------------------------------------

`Event`

PlayerRealmName
---------------

------------------------------------------------------------------------

`Event`

PlayerTitleChange
-----------------

### Description

Fires whenever the player changes their title. This only fires to the
current player. Other players should handle the UnitTitleChange event.

------------------------------------------------------------------------

`Event`

PlayerTitleUpdate
-----------------

### Description

Fires whenever the player gains a new title.

------------------------------------------------------------------------

`Event`

PostCommodityOrderResult
------------------------

### Description

Fires whenever the player attempts to post a buy or sell order on the
commodities exchange. Informs the player if the order was successfully
placed or an error was thrown.

### Params

-   **eResult** **(GameLib.CodeEnumGenericError)** - The result of the
    operation. This will return the error that is received, or OK if the
    operation was successful.
-   **orderPosted**
    **([CommodityOrder](../Classes/CommodityOrder.md))** - The
    commodity order that the player attempted to post on the Commodities
    Exchange.
-   **monCost** **([Money](../Classes/Money.md))** - The cost to post
    the order.

------------------------------------------------------------------------

`Event`

PostItemAuctionResult
---------------------

### Description

Fires when the player attempts to post an auction on the Auction House.

### Params

-   **eResult** **(GameLib.CodeEnumGenericError)** - If there was a
    problem posting the auction, this will contain the error explaining
    why it failed. Otherwise, this value will be Ok.
-   **auctPosted** **([ItemAuction](../Classes/ItemAuction.md))** - The
    auction that the player tried to post.

------------------------------------------------------------------------

`Event`

PrereqFailureMessage (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Event`

PreviousActionBar (Deprecated)
------------------------------

------------------------------------------------------------------------

`Event`

ProfessionAchievementUpdated
----------------------------

### Description

Fires whenever the player crafts an item that advances a node in the
Tradeskill tech tree.

### Params

-   **achUpdated** **([Achievement](../Classes/Achievement.md))** - The
    achievement that go updated.

------------------------------------------------------------------------

`Event`

ProfessionsLoaded
-----------------

### Description

Fires when the player's tradeskills are done loading.

------------------------------------------------------------------------

`Event`

ProfessionUpdated
-----------------

### Description

Fires whenever a profession gains XP, gains a talent point, chooses a
talent, unlocks a schematic, or gets traded for another tradeskill.

### Remarks

Note, this does not get fired for updates to Runecrafting.

------------------------------------------------------------------------

`Event`

ProgressClickHighlightTime
--------------------------

### Description

Fires twice per frame while the Precision and Metronome CSIs are active.
This informs the UI of whether or not the target areas have been
successfully hit by the player.

### Params

-   **nTargetIdx** **(Integer)** - The target area being referenced. 0
    is the first target, and 1 is the second. If there is only one
    target, then events will still be fired for both, but only events
    with nTargetIdx of 0 will matter for that CSI.
-   **nPercentageHighlight** **(Integer)** - Informs the UI of how much
    the color for the target area should be changed. 0 is the default
    color.

------------------------------------------------------------------------

`Event`

ProgressClickWindowCompletionLevel
----------------------------------

### Description

Fires once per frame while the Click and Hold, Rapid Tap, Precision Tap,
and Metronome CSIs are active. For Click and Hold and Rapid Tap CSIs,
this tells the UI the CSI's progress.

### Params

-   **nProgress** **(Integer)** - The CSI's progress on the meter, with
    0 being the beginning and 100 being the end.
-   **bIsReversed** **(Boolean)** - Whether or not the CSI's progress is
    reversed. This is primarily used in Metronome CSIs.

------------------------------------------------------------------------

`Event`

ProgressClickWindowDisplay
--------------------------

### Description

Fires whenever a CSI should be drawn or hidden.

### Params

-   **bIsActive** **(Boolean)** - Whether or not the CSI should be
    shown.

------------------------------------------------------------------------

`Event`

PublicEventBombDropped
----------------------

------------------------------------------------------------------------

`Event`

PublicEventBombStatus
---------------------

------------------------------------------------------------------------

`Event`

PublicEventCleared (Deprecated)
-------------------------------

### Description

Fires whenever a PublicEvent is removed from the player's list of active
events.

### Params

-   **peEnding** **([PublicEvent](../Classes/PublicEvent.md))** - The
    PublicEvent that was cleared from the active list.

------------------------------------------------------------------------

`Event`

PublicEventEnd
--------------

### Description

Fires when a public event ends.

### Params

-   **peEvent** **([PublicEvent](../Classes/PublicEvent.md))** - The
    public event that ended.
-   **eReason** **(Integer)** - The reason the event ended. This lines
    up with the PublicEvent.PublicEventParticipantRemoveReason set of
    int constants.
-   **tEventInfo** **(Table)**
    -   **nElapsedTime** **(Integer)** - The amount of time that elapsed
        since the event started, in milliseconds.
    -   **eRewardTier** **(Integer)** - The reward tier that the player
        earned. This value lines up with the
        PublicEvent.PublicEventRewardTier set of int constants.
    -   **eRewardType** **(Integer)** - The reason the player received
        the reward. This lines up with the
        PublicEvent.PublicEventRewardTier set of int constants.
    -   **arRewardThresholds** **(Array of Integer)** - The thresholds
        that the player needs to cross to achieve bronze, silver, and
        gold rewards.
    -   **arTeamStats** **(Array of Table)** - The total stats for each
        team involved in the event.
        -   **nDamage** **(Integer)** - The amount of damage the team
            dealt.
        -   **nDamageReceived** **(Integer)** - The amount of damage
            that the team took.
        -   **nHits** **(Integer)** - The number of attacks the team
            made that connected with the enemy.
        -   **nHaters** **(Integer)** - The number of people who are
            gonna hate.
        -   **nKills** **(Integer)** - The number of enemy units the
            team managed to land the killing blow against.
        -   **nMaxMultiKills** **(Integer)** - The highest number of
            enemies that were killed with a single attack.
        -   **nDeaths** **(Integer)** - The number of times players on
            the team died.
        -   **nHealed** **(Integer)** - The amount of healing the team
            did.
        -   **nHealingReceived** **(Integer)** - The amount of healing
            that was done to players on the team.
        -   **nContributions** **(Integer)** - The number of objectives
            the team completed.
        -   **nLongestLife** **(Integer)** - The longest amount of time
            the team spent between deaths, in milliseconds.
        -   **nAssists** **(Integer)** - The number of enemies players
            on the team helped kill, but did not land the killing blow
            against.
        -   **nSaves** **(Integer)** - The number of times the team
            stopped the enemy from capturing an objective.
        -   **nOverhealed** **(Integer)** - The amount of healing the
            team did when their target was already at their max health.
        -   **nOverhealingReceived** **(Integer)** - The amount of
            healing that was done to players on the team while they were
            at max health.
        -   **nLongestImpulse** **(Integer)** - The highest number of
            attacks that the team avoided in a row.
        -   **nKillStreak** **(Integer)** - The team's highest kill
            streak.
        -   **arCustomStats** **(Array of Table)** - An array of stats
            that are specific to the event.
            -   **strName** **(String)** - The name of the stat.
            -   **nValue** **(Integer)** - The value of the stat.
    -   **arParticipantStats** **(Array of Table)** - The stats for each
        player involved in the event.
        -   **nDamage** **(Integer)** - The amount of damage the player
            did.
        -   **nDamageReceived** **(Integer)** - The amount of damage the
            player took.
        -   **nHits** **(Integer)** - The number of attacks the player
            made that hit an enemy.
        -   **nHaters** **(Integer)** - The number of people who are
            hating on the player.
        -   **nKills** **(Integer)** - The number of killing blows the
            player landed.
        -   **nMaxMultiKills** **(Integer)** - The most enemies that
            were killed in a single attack made by the player.
        -   **nDeaths** **(Integer)** - The number of times the player
            died.
        -   **nHealed** **(Integer)** - The amount of healing the player
            did.
        -   **nHealingReceived** **(Integer)** - The amount of healing
            that other players did to the player.
        -   **nContributions** **(Integer)** - The number of objectives
            the player completed.
        -   **nLongestLife** **(Integer)** - The longest amount of time
            the player spent between deaths.
        -   **nAssists** **(Integer)** - The number of enemies the
            player helped kill, but did not land the killing blow
            against.
        -   **nSaves** **(Integer)** - The number of times the player
            prevented the enemy from completing an objective.
        -   **nOverhealed** **(Integer)** - The amount of healing the
            player did on targets that were already at their max health.
        -   **nOverhealingReceived** **(Integer)** - The amount of
            healing done to the player while they are at max health.
        -   **nLongestImpulse** **(Integer)** - The highest number of
            attacks that the player avoided in a row.
        -   **nKillStreak** **(Integer)** - The highest kill streak the
            player achieved.
        -   **arCustomStats** **(Array of Table)** - An array of custom
            stats that are specific to the event.
            -   **strName** **(String)** - The name of the stat.
            -   **nValue** **(Integer)** - The value of the stat.
    -   **arObjectives** **(Array of Table)** - An array of the public
        event's objectives.
        -   **eStatus** **(Integer)** - The status of the public event.
            This lines up with the
            PublicEventObjective.PublicEventStatus set of int constants.
        -   **peoObjective**
            **([PublicEventObjective](../Classes/PublicEventObjective.md))** -
            One of the objectives for this event.

------------------------------------------------------------------------

`Event`

PublicEventInitiateVote
-----------------------

### Description

Fires whenever the public event requires the group to vote on a decision
before progressing.

------------------------------------------------------------------------

`Event`

PublicEventLeave
----------------

### Description

Fires whenever the player leaves a public event area or zone.

### Params

-   **peEvent** **([PublicEvent](../Classes/PublicEvent.md))** - The
    public event that the player left.
-   **eReason** **(Integer)** - The reason the event was fired. This
    lines up with the PublicEvent.PublicEventParticipantRemoveReason set
    of int constants.

------------------------------------------------------------------------

`Event`

PublicEventLiveStatsUpdate
--------------------------

### Description

Fires once per second during events with live stats, such as PvP
matches.

### Params

-   **peUpdated** **([PublicEvent](../Classes/PublicEvent.md))** - The
    public event whose stats were updated.

------------------------------------------------------------------------

`Event`

PublicEventLocationAdded (Deprecated)
-------------------------------------

### Description

Fires whenever a new location is added to a public event.

### Params

-   **peUpdated** **([PublicEvent](../Classes/PublicEvent.md))** - The
    public event that the location was added to.

------------------------------------------------------------------------

`Event`

PublicEventLocationRemoved (Deprecated)
---------------------------------------

### Description

Fires whenever a location is removed from the public event.

### Params

-   **peUpdated** **([PublicEvent](../Classes/PublicEvent.md))** - The
    public event that the location was removed from.

------------------------------------------------------------------------

`Event`

PublicEventObjectiveLocationAdded
---------------------------------

### Description

Fires whenever a location is added to a public event objective.

### Params

-   **peoUpdated**
    **([PublicEventObjective](../Classes/PublicEventObjective.md))** -
    The objective that the location was added to.

------------------------------------------------------------------------

`Event`

PublicEventObjectiveLocationRemoved
-----------------------------------

### Description

Fires whenever a location is removed from an objective.

### Params

-   **peoUpdated**
    **([PublicEventObjective](../Classes/PublicEventObjective.md))** -
    The public event objective that the location was removed from.

### Usage/Example

```lua
    This event is fired after speaking to villagers during the Exodus portion of the Malgrave Adventure.
```

------------------------------------------------------------------------

`Event`

PublicEventObjectiveUpdate
--------------------------

### Description

Fires whenever a player progresses a public event objective.

### Params

-   **peoUpdated**
    **([PublicEventObjective](../Classes/PublicEventObjective.md))** -
    The public event objective that was updated.

------------------------------------------------------------------------

`Event`

PublicEventStart
----------------

### Description

Fires whenever a public event begins.

### Params

-   **peStarting** **([PublicEvent](../Classes/PublicEvent.md))** - The
    public event that just started.

------------------------------------------------------------------------

`Event`

PublicEventStatsUpdate
----------------------

### Description

Fires whenever players' public event stats update.

### Params

-   **peUpdated** **([PublicEvent](../Classes/PublicEvent.md))** - The
    public event whose stats were updated.

### Remarks

The types of actions that will fire this update are more directly
related to progressing the event, such as picking up a mask in Walatiki
Temple or speaking to a villager during the Malgrave Adventure.

------------------------------------------------------------------------

`Event`

PublicEventUnitUpdate
---------------------

------------------------------------------------------------------------

`Event`

PublicEventUpdate
-----------------

### Description

Fires whenever a public event updates.

### Params

-   **peUpdated** **([PublicEvent](../Classes/PublicEvent.md))** - The
    public event that was updated.

------------------------------------------------------------------------

`Event`

PublicEventVoteEnded
--------------------

### Description

Fires when every member of a group has voted when the public event
requires it, or when the voting timer runs out.

### Params

-   **nWinner** **(Integer)** - The voting option with the most votes.

------------------------------------------------------------------------

`Event`

PublicEventVoteTallied
----------------------

### Description

Fires whenever a group member selections an option during a public event
vote.

### Params

-   **nSelection** **(Integer)** - The option that was selected by a
    player.

------------------------------------------------------------------------

`Event`

PVPDeathmatchPoolUpdated
------------------------

### Description

Fires whenever the respawn pool is updated during a PvP match with the
Deathmatch ruleset, such as Arenas.

### Params

-   **nLivesRemainingTeam1** **(Integer)** - The number of respawns team
    1 has left.
-   **nLivesRemainingTeam2** **(Integer)** - The number of respawns team
    2 has left.

------------------------------------------------------------------------

`Event`

PvpKillNotification
-------------------

### Description

Fires when a player is killed in PvP.

### Params

-   **strVictimName** **(String)** - The name of the player that was
    killed.
-   **eReason** **(MatchingGame.PvpDeathReason)** - The reason the
    victim died.
-   **strKillerName** **(String)** - The name of the unit that killed
    the victim.
-   **eKillerClass** **(GameLib.CodeEnumClass)** - The killer's class.
-   **eVictimTeam** **(MatchingGame.Team)** - The team that the victim
    is on.

------------------------------------------------------------------------

`Event`

PVPMatchFinished
----------------

### Description

Fires when a PvP match ends.

### Params

-   **eWinner** **(MatchingGame.Winner)** - The team that won the match.
-   **eReason** **(MatchingGame.MatchEndReason)** - The reason that the
    match ended.
-   **nRatingChangeTeam1** **(Integer)** - The amount that Team 1's
    rating was changed by.
-   **nRatingChangeTeam2** **(Integer)** - The amount that Team 2's
    rating was changed by.

------------------------------------------------------------------------

`Event`

PVPMatchStateUpdated
--------------------

### Description

Fires whenever the PvP match's state is changed.

### Params

-   **eState** **(MatchingGame.PVPGameState)** - The match's new state.
-   **fTimeRemaining** **(Float)** - The amount of time remaining before
    the match automatically changes states, in seconds.

------------------------------------------------------------------------

`Event`

PVPMatchTeamInfoUpdated
-----------------------

### Description

Fires whenever the information for a team in a PvP match is updated
during a match. This includes when a team first joins a match.

### Usage/Example

```lua
    Examples of changes that could fire this are updating the team's name or rating.
```

------------------------------------------------------------------------

`Event`

PvpRatingUpdated
----------------

### Description

Fires whenever a player's or PvP team's rating changes.

### Params

-   **eRatingType** **(MatchingGame.RatingType)** - The type of rating
    that was changed.

------------------------------------------------------------------------

`Event`

QuestCalloutToggle
------------------

### Description

Fires in response to the GameLib.ToggleQuestUnitCallouts() function.
This event tells the UI that the gear / path interact icons on objects
in the world were toggled on or off.

------------------------------------------------------------------------

`Event`

QuestFloater
------------

### Description

Fires whenever the quest is advanced, abandoned, failed, or completed.
This event is meant to give the UI the information it needs to show
floating text related to the quest's state change.

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit who the
    quest belonged to.
-   **strMessage** **(String)** - The message that should be shown in
    the floating text.
-   **queUpdated** **([Quest](../Classes/Quest.md))** - The quest that
    was updated.

------------------------------------------------------------------------

`Event`

QuestGetCurrentQuestId (Deprecated)
-----------------------------------

------------------------------------------------------------------------

`Event`

QuestInit
---------

### Description

Fires when the quest system is initialized.

------------------------------------------------------------------------

`Event`

QuestObjectiveUpdated
---------------------

### Description

Fires whenever the player makes progress on a quest objective.

### Params

-   **queUpdated** **([Quest](../Classes/Quest.md))** - The quest that
    the objective belongs to.
-   **idObjective** **(Integer)** - The id of the quest objective that
    was updated.
-   **bIsPathQuest** **(Boolean)** - Whether or not the quest objective
    belongs to a path quest.

------------------------------------------------------------------------

`Event`

QuestPeriodicReset
------------------

------------------------------------------------------------------------

`Event`

QuestStateChanged
-----------------

### Description

Fires whenever the quest's state is updated.

### Params

-   **queUpdated** **([Quest](../Classes/Quest.md))** - The quest whose
    state was changed.
-   **eState** **(Integer)** - The quest's new state. This value lines
    up with the Quest.QuestState set of int constants.

------------------------------------------------------------------------

`Event`

QuestTrackedChanged
-------------------

### Description

Fires whenever a quest becomes tracked or untracked.

### Params

-   **queUpdated** **([Quest](../Classes/Quest.md))** - The quest that
    was updated.
-   **bTracked** **(Boolean)** - Whether the quest is now tracked or
    not.
-   **bIsPathQuest** **(Boolean)** - Whether or not the quest is a path
    quest.

------------------------------------------------------------------------

`Event`

RaidInfoResponse (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Event`

RealmBroadcastTierHigh
----------------------

### Description

Fires whenever a high priority message is broadcast to the entire realm.

### Params

-   **strMessage** **(String)** - The message that was broadcast.

------------------------------------------------------------------------

`Event`

RealmBroadcastTierMedium
------------------------

### Description

Fires whenever a medium priority message is broadcast to the entire
realm.

### Params

-   **strMessage** **(String)** - The message that was broadcast.

------------------------------------------------------------------------

`Event`

RealmFirstAchievementAnnounce
-----------------------------

### Description

Fires whenever a player or guild is the first on the realm to earn an
achievement. This only applies to select achievements, such as hitting a
certain level, reaching the highest tier of a tradeskill, and clearing
certain dungeons and raids, etc.

### Params

-   **idAchievement** **(Integer)** - The achievement that the player or
    guild earned.
-   **bGuildAchievement** **(Boolean)** - Whether the achievement was a
    guild achievement or not.
-   **strName** **(String)** - The name of the player or guild who
    earned the achievement.
-   **strMessage** **(String)** - The message that is broadcast to the
    realm when the achievement is earned.

------------------------------------------------------------------------

`Event`

RecallShardChanged (Deprecated)
-------------------------------

------------------------------------------------------------------------

`Event`

RecruitmentDemands
------------------

------------------------------------------------------------------------

`Event`

RecruitmentDescription
----------------------

------------------------------------------------------------------------

`Event`

RecruitmentDetailedGuildInfo
----------------------------

------------------------------------------------------------------------

`Event`

RecruitmentDetailedInfoRequestsUnblocked
----------------------------------------

------------------------------------------------------------------------

`Event`

RecruitmentGuildsList
---------------------

------------------------------------------------------------------------

`Event`

RecruitmentGuildsUpdated
------------------------

------------------------------------------------------------------------

`Event`

RecruitmentMinLevel
-------------------

------------------------------------------------------------------------

`Event`

RecruitmentUnsubscribed
-----------------------

------------------------------------------------------------------------

`Event`

RefreshHealthShieldBar
----------------------

### Description

Fires whenever the a unit's health or shields is updated.

### Remarks

Note, this is not fired if the player's absorption shield is updated.
Also, if the damage is applied to both health and shields, this event
will fire twice.

------------------------------------------------------------------------

`Event`

RefreshInventoryBags
--------------------

### Description

Fires whenever the player right clicks to use an item or equip an item,
or attempts to send a piece of decor to the crate. This only fires if
the item is in the player's inventory.

------------------------------------------------------------------------

`Event`

RefreshMail
-----------

### Description

Fires whenever the player removes money or items attached to a piece of
mail.

### Params

-   **strMailId** **(String)** - The mail's unique id number....as a
    string. Yeah, it's weird.

------------------------------------------------------------------------

`Event`

RemoveCCState
-------------

### Description

Fires whenever a CC state is removed from a unit.

### Params

-   **eState** **(Unit.CodeEnumCCState)** - The CC state that was
    removed from the unit.
-   **unitSource** **([Unit](../Classes/Unit.md))** - The unit that the
    CC state was removed from.

------------------------------------------------------------------------

`Event`

RemoveCCStateStun
-----------------

### Description

Fires whenever the player leaves the Stun CC state.

### Remarks

This is a more focused event than RemoveCCState, in that it only fires
for the player that the state was removed from and it only applies if
the CC State that was removed was Stun.

------------------------------------------------------------------------

`Event`

RemoveSpellShortcut
-------------------

### Description

Fires whenever a spell that is part of a quest, challenge, public event,
or path mission is removed from the character.

### Params

-   **spellData** **([Spell](../Classes/Spell.md))** - The spell that
    was removed from the character.
-   **eReason** **(Integer)** - The reason the player had the spell.
-   **idSource** **(Integer)** - The id number of the quest, quest
    objective, challenge, public event, public event objective, or path
    mission that the spell is tied to.

------------------------------------------------------------------------

`Event`

RepairItemCompleted (Deprecated)
--------------------------------

------------------------------------------------------------------------

`Event`

ReputationBoundryWarning
------------------------

### Description

Fires whenever a player has 75% of the reputation required to reach the
next reputation level with a faction

### Params

-   **strReputationLevel** **(String)** - The name of the reputation
    level that the player is approaching.
-   **strFactionName** **(String)** - The name of the faction that the
    player gained reputation with.

------------------------------------------------------------------------

`Event`

ReputationChanged
-----------------

### Description

Fires whenever the player gains or loses reputation with a faction.

### Params

-   **strFactionname** **(String)** - The name of the faction that the
    player gained or lost reputation with.
-   **nReputation** **(Integer)** - The amount of reputation the player
    has with the faction.
-   **fReputationDelta** **(Float)** - The amount that the player's
    reputation was changed by.

------------------------------------------------------------------------

`Event`

ReputationLevel
---------------

### Description

Fires whenever the player reaches a new reputation level with a faction.

### Params

-   **strReputationLevel** **(String)** - The name of the reputation
    level that the player reached.
-   **strFactionName** **(String)** - The name of the faction that the
    player gained reputation with.

------------------------------------------------------------------------

`Event`

ResolutionChanged
-----------------

### Description

Fires whenever the player logs into the game, reloads the UI, or changes
their resolution.

### Params

-   **nWidth** **(Integer)** - The resolution's width value.
-   **nHeight** **(Integer)** - The resolution's height value.

------------------------------------------------------------------------

`Event`

ResourceConversionClose
-----------------------

### Description

Fires whenever the UI calls Event\_CancelConverting(), the player
interacts with another NPC while interacting with a Resource Conversion
NPC, or when the player moves far enough away from the resource
conversion NPC.

------------------------------------------------------------------------

`Event`

ResourceConversionOpen
----------------------

### Description

Fires whenever the player interacts with a Resource Conversion NPC.

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The resource
    conversion NPC that the player interacted with.

------------------------------------------------------------------------

`Event`

RewardTrackActive
-----------------

------------------------------------------------------------------------

`Event`

RewardTracksLoaded
------------------

------------------------------------------------------------------------

`Event`

RewardTrackUpdated
------------------

------------------------------------------------------------------------

`Event`

RuneTooltip
-----------

------------------------------------------------------------------------

`Event`

ScientistExperimentationResult
------------------------------

### Description

Fires in response to a valid call to
PathMission:AttemptScientistExperimentation(). This event returns the
results of the player's attempt.

### Params

-   **arResults** **(Array of Integer)** - An array of all the results
    from the player's experimentation attempt. These values line up with
    the PathMission.ScientistExperimentationResult set of int constants.

------------------------------------------------------------------------

`Event`

ScriptResurrect
---------------

### Description

Fires when the player is forced to resurrect by a scripted event in
game.

------------------------------------------------------------------------

`Event`

SetNavPointFailed
-----------------

------------------------------------------------------------------------

`Event`

SetPlayerPath
-------------

### Description

Fires whenever the player's path changes. This should only be fired when
the character is initially created.

------------------------------------------------------------------------

`Event`

SetProgressClickTimes
---------------------

### Description

Fires whenever the player starts a Press and Hold, Rapid Tap, Precision,
or Metronome CSI. Informs the UI of the areas the player is supposed to
hit during the CSI.

### Params

-   **nWidth** **(Integer)** - The width of the target area. If this is
    0, the target area is hidden.
-   **nLocation1Start** **(Integer)** - The starting location of the
    first target area.
-   **nLocation2Start** **(Integer)** - The starting area of the second
    target area.
-   **nPasses** **(Integer)** - The number of times the progress meter
    is supposed to move back and forth over the CSI. This value is nil
    for Press and Hold and Rapid Tap CSIs, 1 for Precision CSIs, and a
    number larger than 1 for Metronome CSIs.

------------------------------------------------------------------------

`Event`

SettlerBuildResult
------------------

### Description

Fires whenever the player build's a settler improvement.

### Params

-   **eResult** **(Integer)** - The result of the player's build action.
-   **strName** **(String)** - The name of the improvement that was
    built.

------------------------------------------------------------------------

`Event`

SettlerBuildStatusUpdate
------------------------

### Description

Fires whenever the player builds or adds time to a settler improvement.

### Params

-   **idHub** **(Integer)** - The id number of the hub that the player
    built the improvement at.
-   **unitHub** **([Unit](../Classes/Unit.md))** - The settler hub that
    the improvement was buit at.

------------------------------------------------------------------------

`Event`

SettlerHubClose
---------------

### Description

Fires whenever the UI calls Event\_CancelSettlerHub() or the player
moves too far from a settler hub that they are interacting with.

------------------------------------------------------------------------

`Event`

SettlerHubReward
----------------

### Description

Fires whenever settlers unlock a reward for the players in the zone.

### Params

-   **strNotification** **(String)** - The message that was broadcast,
    telling players about the reward that was unlocked.

------------------------------------------------------------------------

`Event`

SettlerHubUpdated
-----------------

### Description

Fires whenever a settler builds an improvement, the time on an
improvement is updated, or a player adds time to an improvement. This
event is only sent to settlers.

------------------------------------------------------------------------

`Event`

SettlerInfrastructureAdvanced (Deprecated)
------------------------------------------

### Description

Fires whenever a the completion percentage of an infrastructure project
is updated. This event is only sent to settlers.

------------------------------------------------------------------------

`Event`

SettlerInfrastructureComplete
-----------------------------

### Description

Fires when a settler brings the last resource needed to finish an
infrastructure project.

------------------------------------------------------------------------

`Event`

SettlerInfrastructureStarted
----------------------------

### Description

Fires whenever a settler interacts with an infrastructure NPC while the
project is not in progress.

------------------------------------------------------------------------

`Event`

SettlerInfrastructureUpdated
----------------------------

### Description

Fires whenever a the completion percentage of an infrastructure project
is updated. This event is only sent to settlers.

------------------------------------------------------------------------

`Event`

SettlerNotifyUse (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Event`

ShieldsOverloaded
-----------------

### Description

Fires whenever a unit's shields are overloaded or the overload effect
ends.

### Params

-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit whose
    shields are overloaded or lost the overloaded state.
-   **bOverloaded** **(Boolean)** - Whether the shields entered or left
    the overloaded state.

------------------------------------------------------------------------

`Event`

ShinyTooltip
------------

------------------------------------------------------------------------

`Event`

ShowActionBarShortcut
---------------------

### Description

Fires whenever an action bar shortcut is supposed to be shown or hidden.

### Params

-   **nBarIdx** **(Integer)** - The bar whose visiblity state has
    updated.
-   **bShow** **(Boolean)** - Whether the bar is supposed to be shown or
    not.
-   **nShortcuts** **(Integer)** - The number of buttons to show from
    the bar.

### Usage/Example

```lua
    Examples of action bar shortcuts:
    Stances for engineer bots
    Housing buttons
    Warplots commands
    Some path missions
```

------------------------------------------------------------------------

`Event`

ShowBank
--------

### Description

Fires whenever the player interacts with a bank NPC.

------------------------------------------------------------------------

`Event`

ShowDye
-------

### Description

Fires whenever the player interacts with a stylist NPC.

------------------------------------------------------------------------

`Event`

ShowGachaUI
-----------

------------------------------------------------------------------------

`Event`

ShowInstanceGameModeDialog
--------------------------

### Description

Fires whenever a player should be shown the instance difficulty window.
This is primarily used when a player attempts to enter an adventure or
dungeon via the entrance instead of via the group finder UI.

### Params

-   **tInfo** **(Table)**
    -   **bDifficultyNormal** **(Boolean)** - Whether or not the Normal
        difficulty is available for the group.
    -   **bDifficultyVeteran** **(Boolean)** - Whether the group meets
        the criteria for the veteran version of the dungeon or not.
    -   **bFlagsScaling** **(Boolean)** - Whether the group is allowed
        to choose whether they scale their level to the dungeon's
        difficulty or not.
    -   **eExistingDifficulty** **(GroupLib.Difficulty)** - If the
        difficulty has already been chosen, this variable will be set to
        the appropriate value.
    -   **bExistingScaling** **(Boolean)** - Whether the scaling flag is
        turned on or off for the dungeon or adventure.

------------------------------------------------------------------------

`Event`

ShowInstanceRestrictedDialog (Deprecated)
-----------------------------------------

------------------------------------------------------------------------

`Event`

ShowInstanceWaitingDialog (Deprecated)
--------------------------------------

------------------------------------------------------------------------

`Event`

ShowInventory
-------------

### Description

Fires in response to the ShowInventory() function.

### Params

-   **bShow** **(Boolean)** - Whether the inventory should be shown or
    not.

------------------------------------------------------------------------

`Event`

ShowItemInDressingRoom
----------------------

### Description

Fires when the player presses Control + right click on a piece of
equipment in a bag window.

### Params

-   **itemPreview** **([Item](../Classes/Item.md))** - The item that
    the player wants to preview.

------------------------------------------------------------------------

`Event`

ShowLocOnWorldMap
-----------------

### Description

Fires whenever a player clicks a location that was linked in an galactic
archive article or quest.

### Params

-   **tLocationInfo** **(Table)**
    -   **zoneMap** **(Table)**
        -   **strFolder** **(String)** - The folder name where the map
            is found.
        -   **strName** **(String)** - The zone's name.
        -   **id** **(Integer)** - The zone's ID.
        -   **fNorth** **(Float)** - The northern most coordinate on the
            map.
        -   **fSouth** **(Float)** - The southern most coordinate on the
            map.
        -   **fEast** **(Float)** - The eastern most coordinate on the
            map.
        -   **fWest** **(Float)** - The western most coordinate on the
            map.
        -   **continentId** **(Integer)** - The continent's ID.
        -   **parentZoneId** **(Integer)** - The ID of the zone's
            parent.
    -   **worldLoc** **(Table)**
        -   **x** **(Float)** - The coordinate's X position.
        -   **y** **(Float)** - The coordinate's Y position.
        -   **z** **(Float)** - The coordinate's Z position.

------------------------------------------------------------------------

`Event`

ShowPurchaseReminder
--------------------

------------------------------------------------------------------------

`Event`

ShowQuestLog
------------

### Description

Fires when the UI calls the Event\_ShowQuestLoc() function.

### Params

-   **idQuest** **(Integer)** - The id number of the quest that the
    quest log should open to.

------------------------------------------------------------------------

`Event`

ShowResurrectDialog
-------------------

### Description

Fires when the player shows up as a ghost after death and when the
player's resurrect options update.

### Params

-   **bPlayerIsDead** **(Boolean)** - Whether the player is dead or not.
-   **bWakeHere** **(Boolean)** - Whether the player has the option to
    resurrect at their current location or not.
-   **bRezHolocrypt** **(Boolean)** - Whether the player has the option
    to resurrect at the nearest holocrypt or not.
-   **bExitInstance** **(Boolean)** - Whether the player has the option
    to exit the instance to resurrect or not. This option is only
    available during dungeons, adventures, and shiphand missions.
-   **bRezAtCaster** **(Boolean)** - Whether the player has the option
    to resurrect at the same location as a player who revived them or
    not.
-   **bHasRezFromPlayer** **(Boolean)** - Whether another player has
    attempted to revive the player or not.
-   **nTimeBeforeRez** **(Integer)** - How long the player must wait
    before they are able to select any resurrect options, in
    milliseconds.
-   **nTimeBeforeWakeHere** **(Integer)** - The amount of time before
    the player is able to use the "Wake Here" option, in milliseconds.
-   **nForceRezTimer** **(Integer)** - The amount of time before the
    player is forced to resurrect at the nearest holocrypt.

------------------------------------------------------------------------

`Event`

ShowTutorial
------------

### Description

Fires whenever a tutorial should be shown or when the UI calls
Event\_ShowTutorial(). It informs the UI which tutorial to display and
where to display it.

### Params

-   **idTutorial** **(Integer)** - The tutorial's id number.
-   **bInstant** **(Boolean)** - Whether the tutorial is shown
    immediately or is placed in a queue.
-   **strText** **(String)** - The text for the tutorial.
-   **eAnchor** **(GameLib.CodeEnumTutorialAnchor)** - The anchor that
    the tutorial should be attached to.
-   **wndContainer** **([Window](../WindowControls/Window.md))** - The
    window where the tutorial is displayed.
-   **nOffsetX** **(Integer)** - The amount the window is offset from
    the anchor along the X axis.
-   **nOffsetY** **(Integer)** - The amount the window is offset from
    the anchor point along the Y axis.

------------------------------------------------------------------------

`Event`

ShuttlePromptClose
------------------

### Description

Fires whenever the player interacts with another unit or moves too far
from a shuttle NPC while interacting with it.

------------------------------------------------------------------------

`Event`

SoldierHoldoutDeath
-------------------

### Description

Fires if a player that has either triggered the Holdout or damaged
Holdout NPCs dies.

### Params

-   **solHoldout** **([SoldierEvent](../Classes/SoldierEvent.md))** -
    The holdout that the player was participating in.

------------------------------------------------------------------------

`Event`

SoldierHoldoutEnd
-----------------

### Description

Fires whenever a soldier holdout ends, no matter if it was successful or
unsuccessful. This event fires for everyone who participated in the
holdout.

### Params

-   **solHoldout** **([SoldierEvent](../Classes/SoldierEvent.md))** -
    The holdout that ended.
-   **eReason** **(Integer)** - The reason the holdout ended. This value
    lines up with the PathMission.PlayerPathSoldierResult set of int
    constants.

------------------------------------------------------------------------

`Event`

SoldierHoldoutNextWave
----------------------

### Description

Fires whenever the next wave of a soldier holdout begins. This event
fires for everyone participating in the holdout.

### Params

-   **solHoldout** **([SoldierEvent](../Classes/SoldierEvent.md))** -
    The holdout that triggered the event.

------------------------------------------------------------------------

`Event`

SoldierHoldoutStatus
--------------------

### Description

Fires whenever a holdout's state updates. This is sent to every player
involved in the holdout.

### Params

-   **solUpdated** **([SoldierEvent](../Classes/SoldierEvent.md))** -
    The soldier event whose state was updated.

------------------------------------------------------------------------

`Event`

SpecChanged
-----------

### Description

Fires whenever the player attempts to change their spec. This event is
only seen by the player that triggers the event.

### Params

-   **nSpecIndex** **(Integer)** - The index of the spec that the player
    changed to.
-   **eResult** **(AbilityBook.CodeEnumSpecError)** - The result of the
    player's attempt to change their spec. This will show any errors
    caused by the attempt, or OK if successful.

------------------------------------------------------------------------

`Event`

SpellCastWithServiceToken
-------------------------

------------------------------------------------------------------------

`Event`

SplineHintObjectEnd (Deprecated)
--------------------------------

------------------------------------------------------------------------

`Event`

SplitItemStack
--------------

### Description

Fires whenever the player attempts to split a stack of items in their
inventory. The default keybind for this is Shift + Left Click on the
item. This event is only fired for the player who tried to split the
stack.

### Params

-   **itemSplitting** **([Item](../Classes/Item.md))** - The item stack
    that the player is trying to split.

------------------------------------------------------------------------

`Event`

SprintEnergyUpdated
-------------------

------------------------------------------------------------------------

`Event`

SprintStateUpdated
------------------

------------------------------------------------------------------------

`Event`

StalkerWoundsUpdate (Deprecated)
--------------------------------

### Params

-   **percent** **(Integer)**
-   **numWounds** **(Integer)**

------------------------------------------------------------------------

`Event`

StanceChanged
-------------

### Description

Fires whenever the player changes their character's innate ability. This
event is only sent to the player who triggered it.

------------------------------------------------------------------------

`Event`

StartSpellThreshold
-------------------

### Description

Fires whenever the player uses a spell that can be used multiple times
within the same cooldown, such as the Warrior's Rampage or Esper's
Telekinetic Strike.

### Params

-   **idSpell** **(Integer)** - The id number of the spell that
    triggered this event.
-   **nMaxThresholds** **(Integer)** - The maximum number of thresholds
    the spell has
-   **eCastMethod** **(Spell.CodeEnumCastMethod)** - The method the
    player used to activate the spell.

------------------------------------------------------------------------

`Event`

StoreCatalogReady
-----------------

------------------------------------------------------------------------

`Event`

StoreCatalogUpdated
-------------------

------------------------------------------------------------------------

`Event`

StoreClosed
-----------

------------------------------------------------------------------------

`Event`

StoreError
----------

------------------------------------------------------------------------

`Event`

StoreLinksRefresh
-----------------

------------------------------------------------------------------------

`Event`

StorePurchaseHistoryReady
-------------------------

------------------------------------------------------------------------

`Event`

StorePurchaseOfferResult
------------------------

------------------------------------------------------------------------

`Event`

StorePurchaseVirtualCurrencyPackageResult
-----------------------------------------

------------------------------------------------------------------------

`Event`

StoreRealCurrencyPurchaseHistoryReady
-------------------------------------

------------------------------------------------------------------------

`Event`

StoryPanelDialog\_Hide
----------------------

### Description

Fires whenever the UI is supposed to stop showing the currently
displayed Story Panel. This event is fired to individual players.

### Usage/Example

```lua
    This is usually shown immediately before StoryPanelDialog_Show to ensure that only one Story Panel is shown at a time.
```

### Remarks

Story Panels are windows used for messaging information to the player.
They are not an actual window type, but they are grouped together so
they can be controlled easily via addons. Only one Story Panel

------------------------------------------------------------------------

`Event`

StoryPanelDialog\_Show
----------------------

### Description

Fires whenever the UI is supposed to show a Story Panel window.

### Params

-   **ePanel** **(GameLib.CodeEnumStoryPanel)** - The type of story
    panel that should be shown.
-   **arMessageLines** **(Array of String)** - An array of text to show
    in the story panel.
-   **fDisplayTime** **(Float)** - The amount of time before the Story
    Panel stould stop being shown.
-   **eStyle** **(GameLib.CodeEnumStoryPanelStyle)** - The style flag
    for the story panel window.

### Remarks

Story Panels are windows used for messaging information to the player.
They are not an actual window type, but they are grouped together so
they can be controlled easily via addons. Only one Story Panel

------------------------------------------------------------------------

`Event`

StunVGPressed
-------------

### Description

Fired once every half second that the player is stunned. This informs
the UI of whether the player pressed the correct button to break out of
the stun. This event is only fired for the person who is stunned.

### Params

-   **bButtonPressed** **(Boolean)** - Whether the player pressed the
    correct button or not.

------------------------------------------------------------------------

`Event`

SubZoneChanged
--------------

### Description

Fires whenever the player moves into a new subzone.

### Params

-   **idZone** **(Integer)** - The id number for subzone.
-   **strSubZoneName** **(String)** - The name of the subzone.

------------------------------------------------------------------------

`Event`

TalentRespecPointsChanged (Deprecated)
--------------------------------------

------------------------------------------------------------------------

`Event`

TalentsChanged (Deprecated)
---------------------------

------------------------------------------------------------------------

`Event`

TargetedByUnit
--------------

### Description

Fires whenever the player's threat is increased with a hostile NPC to
the point that it targets the player. This only fires for the person
being targeted.

### Params

-   **unitTargeting** **(unit)** - The unit that is targeting the
    player.

### Remarks

This isn't fired if the player's threat level is 0, if the unit doing
the targeting is friendly, or if the unit doing the targeting is a
player.

------------------------------------------------------------------------

`Event`

TargetThreatListUpdated
-----------------------

### Description

Fires whenever the threat list for the targeted unit updates. This is
fired to any character that is targeting the unit whose threat table was
updated.

### Params

-   **unitTarget1** **([Unit](../Classes/Unit.md))** - The player at
    the top of the threat list.
-   **nTarget1Threat** **(Integer)** - unitTarget1's threat vs. the
    target unit.
-   **unitTarget2** **([Unit](../Classes/Unit.md))** - The unit with
    the second highest threat against the target unit.
-   **nTarget2Threat** **(Integer)** - unitTarget2's threat vs. the
    target unit.
-   **unitTarget3** **([Unit](../Classes/Unit.md))** - The unit with
    the third highest threat against the target unit.
-   **nTarget3Threat** **(Integer)** - unitTarget3's threat vs. the
    target unit.
-   **unitTarget4** **([Unit](../Classes/Unit.md))** - The player with
    the fourth highest threat against the target unit.
-   **nTarget4Threat** **(Integer)** - unitTarget4's threat vs. the
    target unit.
-   **unitTarget5** **([Unit](../Classes/Unit.md))** - The unit with
    the fifth highest threat against the target unit.
-   **nTarget5Threat** **(Integer)** - unitTarget5's threat vs. the
    target unit.

### Remarks

Note, this is not fired if the targeted unit is a player.

------------------------------------------------------------------------

`Event`

TaxiWindowClose
---------------

### Description

Fires whenever the player interacts with another NPC, calls the
Event\_CancelTaxiVendor() function, or moves too far from a taxi NPC
while interacting with it. This is only sent to the person that
triggered the event.

------------------------------------------------------------------------

`Event`

TickClaimCount
--------------

------------------------------------------------------------------------

`Event`

ToggleAbilitiesWindow
---------------------

### Description

Fires whenever the player presses the key bound to toggle the Limited
Action Set Builder. This is only fired for the player who pressed the
keybind.

### Params

-   **bShow** **(Boolean)** - Whether the Limited Action Set Builder
    should be shown or not.

------------------------------------------------------------------------

`Event`

ToggleAccountInventoryWindow
----------------------------

------------------------------------------------------------------------

`Event`

ToggleAchievementWindow
-----------------------

### Description

Fires whenever the player presses the keybinding tied to the
achievements window or the Event\_ToggleAchievementWindow() function is
called from the UI.. This is only fired for the player who clicked the
keybinding.

------------------------------------------------------------------------

`Event`

ToggleAuctionList
-----------------

### Description

Fires whenever the player presses the keybinding tied to the Marketplace
Listings. This event is only fired for the player who presses the
keybind.

------------------------------------------------------------------------

`Event`

ToggleAuctionWindow
-------------------

### Description

Fires when the player interacts with an auctioneer NPC. This is only
fired for the player who pressed the keybinding.

------------------------------------------------------------------------

`Event`

ToggleChallengesWindow (Deprecated)
-----------------------------------

------------------------------------------------------------------------

`Event`

ToggleCharacterWindow
---------------------

### Description

Fires whenever the player presses the keybinding tied to the character
window. This is only received by the player who pressed the button

------------------------------------------------------------------------

`Event`

ToggleCodex
-----------

### Description

Fires whenever the player presses the keybind tied to the Codex menu or
called Event\_ToggleCodex() from the UI. This event is only fired for
the player who pressed the keybinding.

------------------------------------------------------------------------

`Event`

ToggleCollectiblesWindow
------------------------

------------------------------------------------------------------------

`Event`

ToggleContractsWindow
---------------------

------------------------------------------------------------------------

`Event`

ToggleCREDDExchangeWindow
-------------------------

### Description

Fires when the player interacts with a CREDD Exchange NPC.

------------------------------------------------------------------------

`Event`

ToggleErrorDialog
-----------------

### Description

Fires whenever a Lua error occurs. This is only received by the client
that the error occurred on.

------------------------------------------------------------------------

`Event`

ToggleFramerate
---------------

### Description

Fires whenever the player toggles the framerate display (Ctrl + F by
default). This is only fired for the client where the key combination
was pressed.

------------------------------------------------------------------------

`Event`

ToggleGhostModeMap (Deprecated)
-------------------------------

### Description

Fired whenever the player presses the button to toggle the ghost mode.
This is only fired for the player.

------------------------------------------------------------------------

`Event`

ToggleGroupFinder
-----------------

### Description

Fires whenever the player presses the key bound to the GroupFinder UI.
This event is only received by the player who pressed the keybinding.

------------------------------------------------------------------------

`Event`

ToggleGroupSharedBag (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Event`

ToggleGroupsWindow (Deprecated)
-------------------------------

------------------------------------------------------------------------

`Event`

ToggleGuild
-----------

### Description

Fired whenever the player presses the keybinding tied to the Guild UI.
This event is only handled by the player who pressed the keybinding.

------------------------------------------------------------------------

`Event`

ToggleHoloWardrobeWindow
------------------------

------------------------------------------------------------------------

`Event`

ToggleInventory
---------------

### Description

Fires whenever the player presses the key bound to the Inventory. This
is only received by the player who pressed the key.

------------------------------------------------------------------------

`Event`

ToggleItemContextMenu
---------------------

------------------------------------------------------------------------

`Event`

ToggleLevelUpUnlockWindow
-------------------------

------------------------------------------------------------------------

`Event`

ToggleMacrosWindow
------------------

------------------------------------------------------------------------

`Event`

ToggleMailWindow
----------------

### Description

Fires whenever the player presses the key bound to Mail. This event is
only handled by the player who pressed the key.

------------------------------------------------------------------------

`Event`

ToggleMarketplaceWindow
-----------------------

### Description

Fires whenever the player interacts with a Commodities Marketplace NPC.
This is only handled by the player who triggered the event.

------------------------------------------------------------------------

`Event`

ToggleNonCombatAbilitiesWindow
------------------------------

------------------------------------------------------------------------

`Event`

TogglePlayerTicketWindow
------------------------

### Description

Fires whenever the player types the slash command to open the Player
Ticket Window. It is only handled by the player who used the command.

------------------------------------------------------------------------

`Event`

ToggleQuestLog
--------------

### Description

Fires whenever the UI calls the Event\_ToggleQuestLog() function or the
player presses the key bound to the quest log. This is only sent to the
player that fired it.

------------------------------------------------------------------------

`Event`

ToggleReputationInterface
-------------------------

### Description

Fires whenever the UI calls Event\_ToggleReputationWindow(). This is
only fired to the player with the addon that called the function.

------------------------------------------------------------------------

`Event`

ToggleSocialWindow
------------------

### Description

Fires whenever the player presses the key bound to the Social window. It
is only sent to the player that pressed the button.

------------------------------------------------------------------------

`Event`

ToggleStuckWindow
-----------------

### Description

Fires whenever the player types /stuck while in game or the UI calls
ShowStuckUI(). This event will only fire for the player who used the
command or whose UI called the function.

------------------------------------------------------------------------

`Event`

ToggleTradeskills
-----------------

### Description

Fires whenever the player presses the key bound to Tradeskills. This
only fires for the player that pressed the key.

------------------------------------------------------------------------

`Event`

ToggleTradeSkillsInventory
--------------------------

### Description

Fires whenever the ToggleTradeSkillsInventory() function is called from
the UI. This is only sent to the player whose UI called the function.

------------------------------------------------------------------------

`Event`

ToggleWhoWindow
---------------

------------------------------------------------------------------------

`Event`

ToggleZoneMap
-------------

### Description

Fires whenever the player presses the key bound to the Map. This event
only fires for the player that pressed the key.

------------------------------------------------------------------------

`Event`

TradeskillAchievementComplete
-----------------------------

### Description

Fires whenever the player finishes an entry on a tradeskill's tech tree.

### Params

-   **idAchievement** **(Integer)** - The id number for the achievement
    that the player earned.

### Remarks

Elements on the tech tree are Achievement type objects, hence the name
of the event.

------------------------------------------------------------------------

`Event`

TradeskillAchievementUpdate
---------------------------

### Description

Fires whenever progress is made on an entry in the player's tech tree.

### Params

-   **achUpdated** **([Achievement](../Classes/Achievement.md))** - The
    tech tree entry that was updated.
-   **nCurrentProgress** **(Integer)** - The progress the player has
    made towards completing the achievement.
-   **nProgressNeeded** **(Integer)** - The total amount of progress
    needed to complete the achievement.

------------------------------------------------------------------------

`Event`

TradeskillEngravingStationClose
-------------------------------

### Description

Fires whenever the player interacts with another NPC or moves away from
the Engraving Station while they are interacting with it.

------------------------------------------------------------------------

`Event`

TradeskillEngravingStationOpen
------------------------------

### Description

Fires whenever the player interacts with an Engraving Station NPC.

------------------------------------------------------------------------

`Event`

TradeSkills\_Crafting (Deprecated)
----------------------------------

### Params

-   **text** **(String)**
-   **percentComplete** **(Integer)**

------------------------------------------------------------------------

`Event`

TradeSkills\_Learned
--------------------

### Description

Fires whenever the player learns a new crafting tradeskill. This does
not get fired for learning Runecrafting or harvesting (Mining,
Survivalist, Relic Hunter) tradeskills.

### Params

-   **eTradeskill** **(CraftingLib.CodeEnumTradeskill)** - The
    tradeskill that was learned.

------------------------------------------------------------------------

`Event`

TradeSkills\_Show (Deprecated)
------------------------------

### Params

-   **schematicId** **(Integer)**

------------------------------------------------------------------------

`Event`

TradeSkills\_UpdateQuantities (Deprecated)
------------------------------------------

------------------------------------------------------------------------

`Event`

TradeSkillsBreakdown\_Show
--------------------------

### Params

-   **bShow** **(Boolean)**

------------------------------------------------------------------------

`Event`

TradeSkillSigilResult
---------------------

### Description

Fires whenever the player attempts to add a rune to a rune slot on a
piece of equipment.

### Params

-   **eResult** **(CraftingLib.CodeEnumTradeskillResult)** - The result
    of the player's attempt to add a rune to a piece of equipment.

------------------------------------------------------------------------

`Event`

TradeSkillsItemBreakdown\_BreakCompleted (Deprecated)
-----------------------------------------------------

### Params

-   **success** **(Boolean)**

------------------------------------------------------------------------

`Event`

TutorialPlaybackEnded
---------------------

### Description

Fires whenever the VO for a tutorial ends.

------------------------------------------------------------------------

`Event`

UI\_EffectiveLevelChanged
-------------------------

### Description

Fires whenever the player's effective level changes due to rallying or
mentoring.

### Params

-   **nNewEffectiveLevel** **(Integer)** - The player's current
    effective level.

------------------------------------------------------------------------

`Event`

UI\_EnergyChanged (Deprecated)
------------------------------

### Description

Fires whenever the amount of energy that the player has for sprinting
changes.

### Params

-   **nCurrentEnergy** **(Integer)** - The amount of energy the player
    currently has.
-   **nMaxEnergy** **(Integer)** - The maximum amount of energy the
    player can have.

------------------------------------------------------------------------

`Event`

UI\_HealthChanged
-----------------

### Description

Fires whenever the player's HP changes

### Params

-   **nHP** **(Integer)** - The player's current HP.
-   **nMaxHP** **(Integer)** - The character's maximum HP.

------------------------------------------------------------------------

`Event`

UI\_LevelChanged
----------------

### Description

Fires whenever the player's level changes.

### Params

-   **nLevel** **(Integer)** - The player's current level.

------------------------------------------------------------------------

`Event`

UI\_XPBonusAwarded (Deprecated)
-------------------------------

### Description

Queues an XP award bonus to various RewardQueues and updates the
RewardBar's progress.

### Params

-   **awardType** **(CharacterStat)** - The corresponding queue to award
    towards. Calculated as: awardType -
    CharacterStat\_KillingSpreeBonus + 1
-   **newValue** **(Float)** - The amount to reward.

------------------------------------------------------------------------

`Event`

UI\_XPBonusUpdated (Deprecated)
-------------------------------

### Params

-   **who** **(Integer)**
-   **preview** **(Boolean)**
-   **earnsXP** **(Boolean)**

------------------------------------------------------------------------

`Event`

UI\_XPChanged
-------------

### Description

Fires whenever the player's XP, Elder Points, or rested bonus changes.

### Params

-   **nXP** **(Integer)** - The player's current XP. Note, this will not
    list the player's current EP once they have hit level 50.
-   **nMinXPForLevel** **(Integer)** - The amount of XP the player had
    to earn before becoming their current level.
-   **nXPToLevel** **(Integer)** - The amount of XP the player needs to
    reach the next level. This is -1 if the player is at the maximum
    level.
-   **nRestedBonus** **(Integer)** - The amount of XP or EP the player
    can get from their rested bonus.

------------------------------------------------------------------------

`Event`

UnavailableMail
---------------

### Description

Fires whenever a piece of mail is deleted or the player reports a piece
of mail as spam.

### Params

-   **strMailId** **(Array of String)** - An array of strings that
    contain the mail's Id

------------------------------------------------------------------------

`Event`

UnitEvaded
----------

### Description

Fires if an NPC evades or resets due to the player being in stealth for
too long.

### Params

-   **unitEvading** **([Unit](../Classes/Unit.md))** - The unit that
    evaded.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that the
    NPC was targeting before it evaded.
-   **eReason** **(Integer)** - The reason that the NPC evaded. This
    should be either 2 (Timeout), 5 (FailedToPath) or 6
    (StealthWanderTimeout)
-   **strText** **(String)** - The floating text that should be shown
    when the unit evades.

### Remarks

Note: This does not fire for creatures tethering naturally.

------------------------------------------------------------------------

`Event`

UnitGibbed
----------

------------------------------------------------------------------------

`Event`

UnitGroupChanged
----------------

### Description

Fires whenever a player is added or removed from the group. This is sent
to every member of the group.

### Params

-   **unitUpdated** **([Unit](../Classes/Unit.md))** - The unit that
    was added or removed from the group.

------------------------------------------------------------------------

`Event`

UnitGuildNameplateChanged
-------------------------

### Description

Fires whenever a nearby player updates their guild tag on their
nameplate.

### Params

-   **unitUpdated** **([Unit](../Classes/Unit.md))** - The unit whose
    guild tag was updated.

------------------------------------------------------------------------

`Event`

UnitLevelChanged
----------------

### Description

Fires whenever a nearby player's level or effective level changes.

### Params

-   **unitUpdated** **([Unit](../Classes/Unit.md))** - The unit whose
    level or effective level changed.

------------------------------------------------------------------------

`Event`

UnitMemberOfGuildChange
-----------------------

### Description

Fires whenever a nearby player is added or removed from a guild.

### Params

-   **unitUpdated** **([Unit](../Classes/Unit.md))** - The player that
    was added to or removed from a guild.

------------------------------------------------------------------------

`Event`

UnitPvpFlagsChanged
-------------------

### Description

Fires whenever a nearby player changes their PvP flag state.

### Params

-   **unitUpdated** **([Unit](../Classes/Unit.md))** - The unit who
    toggled their PvP flag state.

------------------------------------------------------------------------

`Event`

UnitTextBubbleCreate
--------------------

### Description

Fires whenever an unit should display a text bubble over their head.

### Params

-   **unitSpeaker** **([Unit](../Classes/Unit.md))** - The unit that
    the text bubble is attached to.
-   **strText** **(String)** - The text in the text bubble.
-   **bImmediate** **(Boolean)** - Whether the text bubble should be
    shown immediately or fade in.
-   **fRange** **(Boolean)** - The maximum range that people can see the
    text bubble from.

------------------------------------------------------------------------

`Event`

UnitTextBubblesDestroyed
------------------------

### Description

Fires whenever a text bubble's internal timer has expired.

------------------------------------------------------------------------

`Event`

UnitTitleChanged
----------------

### Description

Fires whenever a nearby unit changes their title.

### Params

-   **unitUpdated** **([Unit](../Classes/Unit.md))** - The unit who
    changed their title.

------------------------------------------------------------------------

`Event`

UnlockCostumeItem
-----------------

------------------------------------------------------------------------

`Event`

UnTargetedByUnit
----------------

### Description

Fires whenever a unit stops targeting the current player.

### Params

-   **unitAttacking** **([Unit](../Classes/Unit.md))** - The unit who
    changed their target.

------------------------------------------------------------------------

`Event`

UpdateCCStateStun
-----------------

### Description

Fires every 0.2 seconds while the player is stunned. This event informs
the UI how much progress the player has made towards breaking out of the
stun.

### Params

-   **fProgress** **(Float)** - The progress the player has made towards
    breaking out of the stun. This value is percentage based, with the
    player breaking out on 100 or higher.

------------------------------------------------------------------------

`Event`

UpdateGearScore
---------------

### Description

Fires whenever an item is added or removed from the player that changes
their Gear Score.

------------------------------------------------------------------------

`Event`

UpdateInventory
---------------

### Description

Fires whenever an item is added to, removed from, or moved within the
player's inventory.

------------------------------------------------------------------------

`Event`

UpdatePathXp
------------

### Description

Fires whenever the player gains Path XP.

### Params

-   **nXPDelta** **(Integer)** - The amount of Path XP the player
    gained.
-   **strFloaterMessage** **(String)** - The message that should be
    displayed on a combat floater when this event is fired.

------------------------------------------------------------------------

`Event`

UpdateResurrectDialog
---------------------

------------------------------------------------------------------------

`Event`

UpdateRewardProperties
----------------------

------------------------------------------------------------------------

`Event`

UpdateSoldierBuild (Deprecated)
-------------------------------

------------------------------------------------------------------------

`Event`

UpdateSpellThreshold
--------------------

### Description

Fires whenever the player uses a spell with a threshold timer, while the
timer is running.

### Params

-   **idSpell** **(Integer)** - The spell's id number.
-   **nCurrentThreshold** **(Integer)** - The number of times the player
    has used the ability since the threshold timer was started.

------------------------------------------------------------------------

`Event`

Vacuum
------

### Description

Fires whenever the player press the key bound to vacuum looting.

------------------------------------------------------------------------

`Event`

VendorItemsUpdated
------------------

### Description

Fires whenever the player opens the Vendor UI, any player purchases a
limited supply item while the player is interacting with the vendor, or
the vendor restocks a limited supply item while the player is
interacting with it.

------------------------------------------------------------------------

`Event`

WalletUpdate
------------

### Description

Fires whenever the wallet tied to a player's account updates. The wallet
is used to purchase microtransaction items.

### Params

-   **nAmount** **(Integer)** - The amount of currency that was added to
    the player's wallet.

------------------------------------------------------------------------

`Event`

WarPartyBankerClose
-------------------

### Description

Fires whenever the player interacts with another NPC or moves too far
away while interacting with the warparty bank, or whenever the UI calls
Event\_CancelWarpartyBank()..

------------------------------------------------------------------------

`Event`

WarPartyBankerOpen
------------------

### Description

Fires whenever the player interacts with the Warparty Bank.

------------------------------------------------------------------------

`Event`

WarPartyBattleClose
-------------------

### Description

Fires whenever the player's UI reloads and they are not on a warplot or
in a warplot match.

------------------------------------------------------------------------

`Event`

WarPartyBattleOpen
------------------

### Description

Fires whenever the player presses the Warparty Crate button in the
Warplot UI.

### Params

-   **guildWarparty** **([Guild](../Classes/Guild.md))** - The warparty
    that the plot belongs to.

------------------------------------------------------------------------

`Event`

WarPartyBossTokensUpdated
-------------------------

### Description

Fires whenever a player uses a boss token during a Warplot match or the
player adds a boss token to the Warparty Bank.

### Params

-   **guildWarparty** **([Guild](../Classes/Guild.md))** - The warparty
    whose boss tokens were updated.

------------------------------------------------------------------------

`Event`

WarPartyMatchResults
--------------------

### Description

Fires when a Warplot match ends. This event is sent to every player
involved in the match.

### Params

-   **arTeamResults** **(Array of Table)**
    -   **nRating** **(Integer)** - The amount that the team's rating
        changed by.
    -   **nRepairCost** **(Integer)** - The amount it will cost the team
        to repair their warplot.
    -   **nDestroyedPlugs** **(Integer)** - The number of the team's
        plugs that were destroyed during the match.
    -   **nWarCoinsEarned** **(Integer)** - The number of Warcoins that
        the team earned during the match.

------------------------------------------------------------------------

`Event`

WarPartyRegistrarClose (Deprecated)
-----------------------------------

------------------------------------------------------------------------

`Event`

WarPartyRegistrarOpen (Deprecated)
----------------------------------

------------------------------------------------------------------------

`Event`

WarplotBattleStateChanged
-------------------------

### Description

Fires when the player enters the warplot or when one of the warparty's
plugs is destroyed.

------------------------------------------------------------------------

`Event`

WhoResponse
-----------

### Description

The response the player gets when they use the /who slash command.

### Params

-   **tResults** **(Array of Table)**
    -   **strName** **(String)** - The player's name.
    -   **nLevel** **(Integer)** - The player's level.
    -   **eRaceId** **(GameLib.CodeEnumRace)** - The player's race.
    -   **eClassId** **(GameLib.CodeEnumClass)** - The player's class.
    -   **ePlayerPathType** **(Integer)** - The player's path. This
        lines up with the PlayerPathLib.PlayerPathType set of constants.
    -   **idWorldZone** **(Integer)** - The id of the zone the player is
        in.
    -   **strRace** **(String)** - The name of the player's race.
    -   **strClass** **(String)** - The name of the player's class.
    -   **strZone** **(String)** - The name of the zone the player is
        in.
    -   **strPath** **(String)** - The name of the player's path.

------------------------------------------------------------------------

`Event`

WindowGainedFocus
-----------------

------------------------------------------------------------------------

`Event`

WindowLostFocus
---------------

------------------------------------------------------------------------

`Event`

WorkOrderLocate
---------------

### Description

Fires whenever the player clicks a work order quest in the Quest
Tracker.

### Params

-   **idSchematic** **(Integer)** - The id number of the schematic
    required for the work order.

### Remarks

This event is intended to open the tradeskill window to the appropriate
schematic

------------------------------------------------------------------------

`Event`

WrangleCreature (Deprecated)
----------------------------

### Params

-   **uTarget** **([Unit](../Classes/Unit.md))** - A UnitId of the
    targetted creature
-   **fMeter** **(Float)** - The current progress of the action, the
    player wants this to remain within the success and failure
    thresholds
-   **fSuccessThreshold** **(Float)** - The maximum cieling for the
    capture meter
-   **fFailureThreshold** **(Float)** - The minimum floor for the
    capture meter
-   **nRangeBand** **(Integer)** - Converted to text for the distance
    indicator
-   **fRate** **(Float)** - Currently unused

------------------------------------------------------------------------

`Event`

ZoneCompletionUpdated
---------------------

### Description

Fires whenever the player enters a zone, explores a new part of the
zone, or completes a challenge, task, datacube, or path mission

### Params

-   **idZone** **(Integer)** - The id number for the zone whose
    completion percentage was updated.

------------------------------------------------------------------------

`Event`

ZoneMapPing
-----------

### Description

Fires whenever the player or a group member clicks the minimap.

### Params

-   **idUnit** **(Integer)** - The id number of the unit that pinged the
    map.
-   **tPos** **([Vector3](../Classes/Vector3.md))** - The coordinates
    that were pinged.

------------------------------------------------------------------------

`Event`

ZoneMapPlayerIndicatorUpdated
-----------------------------

### Description

Fires whenever a player is added or removed from the Zone Map.

### Params

-   **bVisible** **(Boolean)** - Whether the player is visible on the
    map or not.

### Remarks

An example of this is when a player joins or leaves a group.

------------------------------------------------------------------------

`Event`

ZoneMapUpdateHexGroup
---------------------

### Description

Fires when a hex group is added or removed from the zone map.

### Params

-   **hexUpdated** **([HexGroups](../Classes/HexGroups.md))** - The hex
    group that was shown or hidden.

------------------------------------------------------------------------

`Function`

BuybackItemFromVendor(idItem)
-----------------------------

### Description

Performs a buyback on an item that was recently sold to a vendor. This
function will only work if the player is within range of a vendor.

### Params

-   **idItem** **(Integer)** - The unique ID of the item that is being
    bought back from the vendor.

------------------------------------------------------------------------

`Function`

BuyItemFromVendor(idUnique, nQuantity)
--------------------------------------

### Description

Purchases the specified item from the vendor if the player can afford
it.

### Params

-   **idUnique** **(Integer)** - The item's unique id number.
-   **nQuantity** **(Integer)** - How many of the specified item the
    player wishes to buy.

------------------------------------------------------------------------

`Function`

Camp()
------

### Description

Causes the player to return to character select.

------------------------------------------------------------------------

`Function`

CancelExit()
------------

### Description

Stops the player's logout timer and cancels the request to leave the
game.

------------------------------------------------------------------------

`Function`

Chat\_PostDatachronMsg(idCreature, strText)
-------------------------------------------

### Description

Posts a chat message on the Datachron chat channel from the specified
unit.

### Params

-   **idCreature** **(Integer)** - the id number of the NPC that spoke
    the message.
-   **strText** **(String)** - The text that was said by the NPC

------------------------------------------------------------------------

`Function`

Cinematics\_Cancel()
--------------------

### Description

Cancels a cutscene while it is displayed.

------------------------------------------------------------------------

`Function`

Cinematics\_Play()
------------------

### Description

Starts a cinematic.

------------------------------------------------------------------------

`Function`

Creature\_GetName(idCreature)
-----------------------------

### Description

Returns the name of the creature with the specified ID.

### Params

-   **idCreature** **(Integer)** - The creature's Id number.

### Return Value

-   **String** - The name of the creature with the given ID.

------------------------------------------------------------------------

`Function`

Event\_CancelAuctionhouse()
---------------------------

### Description

If the player's current interact target is an Auctioneer, this function
deselects it and fires the AuctionWindowClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelBanking()
----------------------

### Description

If the player's current interact target is a player bank, this function
deselects it and fires the BankWindowClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelBarber()
---------------------

------------------------------------------------------------------------

`Function`

Event\_CancelCityDirections()
-----------------------------

### Description

If the player's current interact target is a capital city guard, this
function deselects it and fires the CityDirectionsClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelCommodities()
--------------------------

### Description

If the player's current interact target is a Commodities Exchange NPC,
this function deselects it and fires the MarketplaceWindowClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelContractBoard()
----------------------------

------------------------------------------------------------------------

`Function`

Event\_CancelConverting()
-------------------------

### Description

If the player's current interact target is a resource conversion NPC,
this function deselects it and fires the ResourceConversionClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelCrafting()
-----------------------

### Description

If the player's current interact target is a crafting station, this
function deselects it and fires the CraftingStationClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelCREDDExchange()
----------------------------

### Description

Forces the CREDD Exchange window to close.

### Usage/Example

```lua
    This function will cause the Event_CREDDExchangeWindowClose event to fire.
```

------------------------------------------------------------------------

`Function`

Event\_CancelDyeWindow()
------------------------

### Description

If the player's current interact target is a Stylist NPC, this function
deselects it and fires the DyeWindowClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelEldanForge()
-------------------------

------------------------------------------------------------------------

`Function`

Event\_CancelEngravingStation()
-------------------------------

### Description

If the player's current interact target is an engraving station, this
function deselects it and fires the TradeskillEngravingStationClose
event.

------------------------------------------------------------------------

`Function`

Event\_CancelExperimentation()
------------------------------

### Description

If the player's current interact target is a Scientist Experimentation
mission, this clears it.

### Remarks

Currently, this only changes things on the back end. This function will
not cancel the Experimentation mission and has no event tied to it.

------------------------------------------------------------------------

`Function`

Event\_CancelGuildBank()
------------------------

### Description

If the player's current interact target is a Guild Bank NPC, this
function deselects it and fires the GuildBankerClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelGuildRegistration()
--------------------------------

### Description

If the player's current interact target is a Guild Registrar NPC, this
function deselects it and fires the GuildRegistrarClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelHousingMannequin()
-------------------------------

### Description

If the player's current interact target is a Mannequin NPC, this
function deselects it and fires the MannequinWindowClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelMail()
-------------------

### Description

If the player's current interact target is a Mailbox NPC, this function
deselects it and fires the MailBoxDeactivate event.

------------------------------------------------------------------------

`Function`

Event\_CancelMasterCraftsman()
------------------------------

------------------------------------------------------------------------

`Function`

Event\_CancelSettlerHub()
-------------------------

### Description

If the player's current interact target is a Settler Hub, this function
deselects it and fires the SettlerHubClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelTaxiVendor()
-------------------------

### Description

If the player's current interact target is a Taxi NPC, this function
deselects it and fires the TaxiWindowClose event.

------------------------------------------------------------------------

`Function`

Event\_CancelTradeskillTraining()
---------------------------------

### Description

If the player's current interact target is a Tradeskill Trainer NPC,
this function deselects it and fires the CloseTradeskillTrainer event.

------------------------------------------------------------------------

`Function`

Event\_CancelTraining() (Deprecated)
------------------------------------

### Description

If the player's current interact target is a Ability Trainer NPC, this
function deselects it and fires the AbilitiesWindowClose event.

### Remarks

Since Ability Trainers are no longer in game, this function does
nothing.

------------------------------------------------------------------------

`Function`

Event\_CancelVending()
----------------------

### Description

If the player's current interact target is a Vendor NPC, this function
deselects it and fires the CloseVendorWindow event.

------------------------------------------------------------------------

`Function`

Event\_CancelWarpartyBank()
---------------------------

### Description

If the player's current interact target is a Warparty Bank, this
function deselects it and fires the WarPartyBankerClose event.

------------------------------------------------------------------------

`Function`

Event\_CloseBankWindow()
------------------------

### Description

Fires the BankWindowClose event.

------------------------------------------------------------------------

`Function`

Event\_CloseCraftingWindow()
----------------------------

### Description

Calls the CloseCraftingWindow event.

------------------------------------------------------------------------

`Function`

Event\_CloseTradeskillTrainerWindow()
-------------------------------------

### Description

Calls the CloseTradeskillTrainerWindow event and clears the player's
interact target if it is a tradeskill trainer (which will call
CloseTradeskillTrainerWindow a second time).

### Remarks

This differs from the Event\_CancelTradeskillTraining function in that
it is guarenteed to call CloseTradeskillTrainerWindow, even if the
player isn't targeting a tradeskill trainer. Because of this,
Event\_CancelTradeskillTraining is a safer function to use.

------------------------------------------------------------------------

`Function`

Event\_CloseVendorWindow()
--------------------------

### Description

Fires the CloseVendorWindow event.

------------------------------------------------------------------------

`Function`

Event\_FireGenericEvent(strEventName)
-------------------------------------

### Description

Fires an event for other addons to handle.

### Params

-   **strEventName** **(String)** - The event that you want to fire.

### Remarks

This will fire any custom event, making it easy to pass information
between addons on the same machine. Any additional parameters passed in
to the function will be passed along in the function handler.

------------------------------------------------------------------------

`Function`

Event\_HideQuestLog()
---------------------

### Description

Fires the HideQuestLog event.

------------------------------------------------------------------------

`Function`

Event\_ShowQuestLog(idQuest)
----------------------------

### Description

Fires the ShowQuestLog event.

### Params

-   **idQuest** **(Integer)** - The id number of the quest that the
    Quest Log should open to.

------------------------------------------------------------------------

`Function`

Event\_ShowTutorial(idTutorial, bInstant, wndAnchor, nRelativePostion1, nRelativePosition2, nSpacing)
-----------------------------------------------------------------------------------------------------

### Description

Fires the ShowTutorial event.

### Params

-   **idTutorial** **(Integer)** - The id number of the tutorial that
    should be shown.
-   **bInstant** **(Boolean)** - Determines whether the tutorial should
    appear instantly or fade in.
-   **wndAnchor** **([Window](../WindowControls/Window.md))** - The
    window that the tutorial is anchored to. This variable is optional.
-   **nRelativePostion1** **(Integer)** - The tutorial's position in
    relation to the window it is attached to. This only needs to be
    included if wndAnchor is set.
-   **nRelativePosition2** **(Integer)** - tutorial's position in
    relation to the window it is anchored to. This only needs to be
    included if wndAnchor is set.
-   **nSpacing** **(Integer)** - The amount of spacing between the
    tutorial and the window it is anchored to. This only needs to be
    included if wndAnchor is set.

------------------------------------------------------------------------

`Function`

Event\_ToggleAchievementWindow()
--------------------------------

### Description

Fires the ToggleAchievementWindow event.

------------------------------------------------------------------------

`Function`

Event\_ToggleCodex()
--------------------

### Description

Fires the ToggleCodex event.

------------------------------------------------------------------------

`Function`

Event\_ToggleMailWindow()
-------------------------

### Description

Fires the ToggleMailWindow event.

------------------------------------------------------------------------

`Function`

Event\_ToggleQuestLog()
-----------------------

### Description

Fires the ToggleQuestLog event.

------------------------------------------------------------------------

`Function`

ExitGame()
----------

### Description

Attempts to start the process of leaving the game and shutting down the
client.

------------------------------------------------------------------------

`Function`

ExitNow()
---------

### Description

If the Exit Game process has already started, this function will force
the client to shut down.

------------------------------------------------------------------------

`Function`

GetAbilitiesWindow() (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Function`

GetCharacterWindow() (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Function`

GetConColor(nCompareLevel)
--------------------------

### Description

Determines the color used for the level difference between a given level
and the player's level.

### Params

-   **nCompareLevel** **(Integer)** - The level that the player's level
    is compared to.

### Return Value

-   **String** - The color code representing the difference between the
    given level and the player's level.

------------------------------------------------------------------------

`Function`

GetCurrentSubZoneName()
-----------------------

### Description

Returns the name for the sub-zone that the player is currently in.

### Return Value

-   **String** - The name of the sub-zone that the player is in.

------------------------------------------------------------------------

`Function`

GetCurrentZoneName() (Deprecated)
---------------------------------

### Description

Returns the name for the sub-zone that the player is currently in.

### Return Value

-   **String**

------------------------------------------------------------------------

`Function`

GetDeathPenalty() (Deprecated)
------------------------------

### Description

Returns the amount of time before the player can select a resurrection
option.

### Return Value

-   **Integer** - The amount of time before the player can resurrect, in
    milliseconds.

------------------------------------------------------------------------

`Function`

GetDemoTimeRemaining() (Deprecated)
-----------------------------------

### Description

Returns the amount of time before a demo is over.

### Return Value

-   **Float** - The amount of time remaining in the demo, in seconds.

------------------------------------------------------------------------

`Function`

GetDemoType() (Deprecated)
--------------------------

### Description

Returns the type of demo is running.

### Return Value

-   **Integer** - The type of demo that is currently running.

------------------------------------------------------------------------

`Function`

GetElderPoints()
----------------

### Description

Returns the number of elder points the player has.

### Return Value

-   **Integer** - The number of elder points the player currently has.

------------------------------------------------------------------------

`Function`

GetForceRezTime() (Deprecated)
------------------------------

### Description

Returns the amount of time before the player is forced to resurrect.

### Return Value

-   **Integer** - The amount of time before they are forced to
    resurrect, in millisenonds.

------------------------------------------------------------------------

`Function`

GetGameFloat(strVarName, fDefault)
----------------------------------

### Description

Searches for floats set up by the game client and returns the value for
the specified float.

### Params

-   **strVarName** **(String)** - The name of the float that was passed
    to the client.
-   **fDefault** **(Float)** - The default value that will be returned
    if no variable is found. This value defaults to 0.0f if no value is
    passed in.

### Return Value

-   **Float** - The value of the specified variable, or the default if
    no variable is found.

### Remarks

There are currently no values that are accessible via this function.

------------------------------------------------------------------------

`Function`

GetGameInt(strVarName, nDefault)
--------------------------------

### Description

Searches for integers set up by the game client and returns the value
for the specified integer.

### Params

-   **strVarName** **(String)** - The name of the variable that the
    function is attempting to get the value of.
-   **nDefault** **(Integer)** - The default value that should be
    returned if the variable is not found. This defaults to 0.

### Return Value

-   **Integer** - The value of the specified variable, or the default
    value if the variable was not found.

### Remarks

Currently, the only variable that works with this function is
FrameCount, which displays the number of frames since the player logged
in.

------------------------------------------------------------------------

`Function`

GetGameString(strVarName, strDefault)
-------------------------------------

### Description

Searches for strings set up by the game client and returns the value for
the specified string.

### Params

-   **strVarName** **(String)** - The name of the variable that the
    function is attempting to get the value of.
-   **strDefault** **(String)** - The default string that the function
    should return if the variable could not be found. This defaults to
    an empty string.

### Return Value

-   **String** - The value of the specified variable, or the default
    value if the variable could not be found.

### Remarks

Currently, the only string that can be found here is ZoneName. This
returns the name of the subzone that the player is in.

------------------------------------------------------------------------

`Function`

GetItemInfo(nInventoryIdx)
--------------------------

### Description

Returns information about the item at a specified inventory index.

### Params

-   **nInventoryIdx** **(Integer)** - The inventory slot where the item
    is found.

### Return Value

-   **Table** - A table containing information about the item found at
    the specified inventory index.
    -   **itemId** **(Integer)** - The item's unique id.
    -   **name** **(String)** - The name of the item.
    -   **icon** **(String)** - The file name of the item's icon.
    -   **StackCount** **(Integer)** - The number of items that are in
        the stack at the specified location.
    -   **InventoryIndex** **(Integer)** - The location in the player's
        inventory where the item can be found. Yes, this is the same
        number that was passed in to the function.

------------------------------------------------------------------------

`Function`

GetMapTrackedUnitData() (Deprecated)
------------------------------------

------------------------------------------------------------------------

`Function`

GetMouseOverUnit()
------------------

### Description

Returns the unit that the player's mouse is hovering over.

### Return Value

-   **[Unit](../Classes/Unit.md)** - The unit that the player's mouse
    is hovering over. If there is no unit there, this returns nil.

------------------------------------------------------------------------

`Function`

GetNthResolution(nIndex) (Deprecated)
-------------------------------------

### Description

Returns one of three resolutions that were used in early development.

### Params

-   **nIndex** **(Integer)** - The index of the resolution that is being
    polled.

### Return Value

-   **String** - The resolution value at the specified index.

### Usage/Example

```lua
    The table that is polled has three resolutions that fill indexes 0-2.  These are:

    0 = "1024x768"
    1 = "1280x1024"
    2 = "1600x1200"
```

### Remarks

This should not be used, as we have other ways of getting a more
accurate look at the client's resolution.

------------------------------------------------------------------------

`Function`

GetPeriodicElderPoints()
------------------------

### Description

Returns the number of elder points that the player has earned towards
their daily maximum amount.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Function`

GetQuestItem(idQuest, nObjective)
---------------------------------

### Description

Returns the id of the quest item associated with the specified quest
objective.

### Params

-   **idQuest** **(Integer)** - The id number for the quest that is
    being polled.
-   **nObjective** **(Integer)** - The quest objective number that is
    being polled.

### Return Value

-   **Integer** - The id number of the quest item that the specified
    objective requires.

------------------------------------------------------------------------

`Function`

GetQuestItemCount()
-------------------

### Description

Returns the number of quest items that the player has in their
posession.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Function`

GetResolutionCount() (Deprecated)
---------------------------------

### Description

The number of resultions available using the GetNthResolution function.

### Return Value

-   **Integer** - 3!

------------------------------------------------------------------------

`Function`

GetResourceCooldownPercent() (Deprecated)
-----------------------------------------

------------------------------------------------------------------------

`Function`

GetRestXp()
-----------

### Description

Returns the amount of rest XP/EP the player has accumulated.

------------------------------------------------------------------------

`Function`

GetRestXpKillCreaturePool()
---------------------------

### Description

Returns the point where the player will run out of their rested XP/EP
bonus given their current pool.

### Return Value

-   **Integer** - The amount of bonus EP the player will get before
    their rest bonus runs out.

------------------------------------------------------------------------

`Function`

GetRezCost() (Deprecated)
-------------------------

### Description

The amount of copper required for the "Rez Here" resurrection option.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Function`

GetRezIsDead() (Deprecated)
---------------------------

### Description

Returns whether or not the player is dead.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Function`

GetRezOptionAcceptCasterRez() (Deprecated)
------------------------------------------

### Description

Returns whether the player was resurrected by another player or not.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Function`

GetRezOptionExitInstance() (Deprecated)
---------------------------------------

### Description

Returns whether the player has the option to resurrect outside the
instance or not.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Function`

GetRezOptionHolocrypt() (Deprecated)
------------------------------------

### Description

Returns whether the player has the option to resurrect at the nearest
holocrypt or not.

------------------------------------------------------------------------

`Function`

GetRezOptionWakeHere() (Deprecated)
-----------------------------------

### Description

Returns whether the player has the option to resurrect at their current
location or not.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Function`

GetUnit(idUnit)
---------------

### Description

Returns the unit with the specified unit id.

### Params

-   **idUnit** **(Integer)** - The unit's id number.

### Return Value

-   **[Unit](../Classes/Unit.md)** - The unit that the id belongs to.

------------------------------------------------------------------------

`Function`

GetWakeHereTime() (Deprecated)
------------------------------

### Description

The amount of time remaining until the player can resurrect at their
current location.

### Return Value

-   **Integer** - The amount of time before the player can use the "Wake
    Here" resurrect option, in milliseconds.

------------------------------------------------------------------------

`Function`

GetXp()
-------

### Description

Returns the amount of XP the player has earned.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Function`

GetXpPercentToNextLevel()
-------------------------

### Description

Calculates the amount of XP the player needs to reach their next level,
then returns the percentage of that XP that they have not yet earned.

### Return Value

-   **Float**

### Remarks

This does a basic calculation of\
\
(XPToNextLevel - XPToCurrentLevel) / (CurrentXP - XPToCurrentLevel)

------------------------------------------------------------------------

`Function`

GetXpToCurrentLevel()
---------------------

### Description

The amount of XP required to reach the player's current level.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Function`

GetXpToNextLevel()
------------------

### Description

The amount of XP required for the player to reach the next level.

------------------------------------------------------------------------

`Function`

Interaction\_Result() (Deprecated)
----------------------------------

### Description

Depricated. Used to poll whether we passed or failed the interaction
result

------------------------------------------------------------------------

`Function`

InvokeOptionsScreen()
---------------------

### Description

Opens the Options UI.

------------------------------------------------------------------------

`Function`

IsActionBarSetVisible(nBar)
---------------------------

### Description

Checks whether or not the specified ActionBarShortcut bar is active.\

### Params

-   **nBar** **(Integer)** - The ActionBarShortuct bar that the function
    is checking.

### Return Value

-   **Boolean** - Whether the bar is shown or not.

------------------------------------------------------------------------

`Function`

IsDemo()
--------

### Description

Returns whether the player is playing a demo version of the game.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Function`

IsGameValid()
-------------

### Description

Returns whether or not the game is running.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Function`

IsInGame()
----------

### Description

Checks if the current player is in the game or not.

### Return Value

-   **Boolean** - Whether the current player is in the game or not.

------------------------------------------------------------------------

`Function`

IsInVehicle() (Deprecated)
--------------------------

### Description

Checks if the player is in a vehicle or not.

### Return Value

-   **Boolean** - Whether the player is in a vehicle or not.

------------------------------------------------------------------------

`Function`

IsRechargeVendor() (Deprecated)
-------------------------------

### Description

This function returns false. The concept of recharge vendors was cut
before the game launched.

### Return Value

-   **Boolean** - False.

------------------------------------------------------------------------

`Function`

IsRepairVendor(unitVendor)
--------------------------

### Description

Checks if the vendor allows the player to repair.

### Params

-   **unitVendor** **([Unit](../Classes/Unit.md))** - The vendor that
    the player is checking.

### Return Value

-   **Boolean** - Whether or not the vendor allows players to repair.

------------------------------------------------------------------------

`Function`

NextQuestItem()
---------------

### Description

Cycles forward to the next quest item in the list.

------------------------------------------------------------------------

`Function`

Pet\_GetStance(idUnit)
----------------------

### Description

Returns the specified pet's stance.

### Params

-   **idUnit** **(Integer)** - The id number of the pet that is being
    checked.

### Return Value

-   **GameLib.CodeEnumPetStance** - The pet's current stance.

------------------------------------------------------------------------

`Function`

Pet\_GetValidStances(idUnit)
----------------------------

### Description

Checks the list of stances available for the specified pet.

### Params

-   **idUnit** **(Integer)** - The id number of the pet that is being
    checked.

### Return Value

-   **Integer** - The bit flag for the stances that are available to the
    pet.

------------------------------------------------------------------------

`Function`

Pet\_SetStance(idUnit, eStance)
-------------------------------

### Description

Sets the stance for a specified unit.

### Params

-   **idUnit** **(Integer)** - The id number for the pet whose stance is
    being set. Setting this to 0 will set the stance for all of the
    player's pets.
-   **eStance** **(GameLib.CodeEnumPetStance)** - The stance that the
    pet will be set to.

------------------------------------------------------------------------

`Function`

PlayerTicket\_GetErrorTypeList()
--------------------------------

### Description

Gets a list of categories for CS tickets, along with a localized name
for the category.

### Return Value

-   **Array of Table** - An array of tables containing the category IDs
    and localized names.
    -   **index** **(Integer)** - The category's id number.
    -   **localizedText** **(String)** - The localized name of the
        category.

------------------------------------------------------------------------

`Function`

PlayerTicket\_GetSubtype(idParentCategory)
------------------------------------------

### Description

Gets a list of all the subcategories under a specific player ticket
category.

### Params

-   **idParentCategory** **(Integer)** - The function will return all of
    the subcategories for the parent category with this id.

### Return Value

-   **Array of Table** - An array of subcategory ids and names for the
    specified category.
    -   **index** **(Integer)** - The ticket subcategory's id number.
    -   **localizedText** **(String)** - The name of the subcategory.

------------------------------------------------------------------------

`Function`

PlayerTicketDialog\_Report() (Deprecated)
-----------------------------------------

------------------------------------------------------------------------

`Function`

PreviousQuestItem()
-------------------

### Description

Cycles to the previous item in the quest item list.

------------------------------------------------------------------------

`Function`

Print(strOutput)
----------------

### Description

Sends text to the System chat channel. This text will only be shown on
the client that calls this function

### Params

-   **strOutput** **(String)** - The string that is output to the System
    channel.

### Usage/Example

```lua
    Integers and floats can also be passed in as parameters, but other variable types are not output correctly.
```

------------------------------------------------------------------------

`Function`

RechargeItemVendor() (Deprecated)
---------------------------------

### Description

Calls a function that does nothing.

------------------------------------------------------------------------

`Function`

RepairAllItemsVendor()
----------------------

### Description

Repairs all of the player's damaged items using thier own currency. If
the player is not at a vendor that can repair items, this function will
do nothing.

### Usage/Example

```lua
    Results from this attempt
```

------------------------------------------------------------------------

`Function`

RepairItemVendor(nInventoryLocation)
------------------------------------

### Description

Repairs the item in the specified inventory slot.

### Params

-   **nInventoryLocation** **(Integer)** - The index where the item can
    be found in the player's inventory.

------------------------------------------------------------------------

`Function`

ReportError()
-------------

### Description

Fires the InvokeErrorDialog event.

------------------------------------------------------------------------

`Function`

RequestReloadUI()
-----------------

### Description

Reloads the UI.

------------------------------------------------------------------------

`Function`

SellItemToVendor(nInventoryLocation, nQuantity)
-----------------------------------------------

### Description

Sells the item at the specified inventory location to the vendor. If the
player is not interacting with a vendor, this function will do nothing.

### Params

-   **nInventoryLocation** **(Integer)** - The index where the item can
    be found within the player's inventory.
-   **nQuantity** **(Integer)** - The number of items to sell to the
    vendor.

------------------------------------------------------------------------

`Function`

SellItemToVendorById(idItem, nQuantity)
---------------------------------------

### Description

Sells the specified item to the vendor. If the player is not interacting
with a vendor, this function will do nothing.

### Params

-   **idItem** **(Integer)** - The unique ID of the item being sold.
-   **nQuantity** **(Integer)** - The number of items being sold.

------------------------------------------------------------------------

`Function`

SellJunkToVendor()
------------------

------------------------------------------------------------------------

`Function`

SetQuestItem(idItem) (Deprecated)
---------------------------------

### Description

Picks a specific quest item from a the list.

### Params

-   **idItem** **(Integer)** - The id of the quest item that was
    selected.

------------------------------------------------------------------------

`Function`

ShowInventory(bShow)
--------------------

### Description

Fires the ShowInventory event with the specified value.

### Params

-   **bShow** **(Boolean)** - Whether the player's inventory should be
    shown or hidden.

------------------------------------------------------------------------

`Function`

String\_GetString(idString)
---------------------------

### Description

Returns a localized string using the specified string id.

### Params

-   **idString** **(Integer)** - The id number for the string that this
    should return.

------------------------------------------------------------------------

`Function`

String\_GetWeaselString(idString, oParameter)
---------------------------------------------

### Description

Concatinates localized strings that contain tokens with other
parameters.

### Params

-   **idString** **(Integer)** - The id number of the base string.
-   **oParameter** **(Any)** - The function can take in any number or
    type of parameter depending on what the string needs. Every variable
    after the idString needs to match the type and order that the string
    is expected.

### Return Value

-   **String** - The final string after the variables are added.

### Usage/Example

```lua
    Localized strings can have a number of different tokens that are used to create specialized strings.  Input tokens always begin with $ and include the parameter number that goes in that location.
    For example:
    $1n will add the first parameter at this location and expects a string.
    $5f will add the fifth parameter at this location and expects a floating point value.

    Input token key:
    n = string
    c = integer
    f[0-9] = floating point number that is limited to 0-9 decimal places.  If the number of decimal places is not set, it will not use a limit.

    ^ = capitalize the next string
    ~ = uncapitalize the next string

    m = force pluralization of the string (note, this requires the string to have pluralization text, which is explained below)
    + = show the count and the pluralized name.  This requires a table with "count" (the number of the thing) and "name" (the string to pluralize) as variables within the table.
    # = pluralize the string based on the "count", but do not show the count.  This requires a table with "count" (the number of the thing) and "name" (the string to pluralize) as variables within the table.
    Example:

     EnumName: CRB_Knife
     string: knife{p:knives}

    EnumName: CRB_Stab_Em_With_Your
    string: Stab ‘em with your $#(1)

    EnumName: CRB_Stab_Em_With_Your_Count
    string: Stab ‘em with your $+(1)

    Lua:
    local nNumberOfKnives = 1

    local tActor1 =
    {
       ["count"] = nNumberOfKnives,
        ["name"] = Apollo.GetString("CRB_Knife")
    }

    Print(String_GetWeaselString(Apollo.GetString("CRB_Stab_Em_With_Your"), tActor1))
    tActor1[“count”] = 2

    Print(String_GetWeaselString(Apollo.GetString("CRB_Stab_Em_With_Your"), tActor1))
    Print(String_GetWeaselString(Apollo.GetString(“CRB_Stab_Em_With_Your_Count”), tActor1))

    Output:
    Stab ‘em with your knife
    Stab ‘em with your knives
    Stab ‘em with your 2 knives
```

------------------------------------------------------------------------

`Function`

ToggleAbilitiesWindow()
-----------------------

### Description

Fires the ToggleAbilitiesWindow event.

------------------------------------------------------------------------

`Function`

ToggleCharacterWindow()
-----------------------

### Description

Fires the ToggleCharacterWindow event.

------------------------------------------------------------------------

`Function`

ToggleInventory()
-----------------

### Description

Fires the ToggleInventory event.

------------------------------------------------------------------------

`Function`

ToggleTradeSkillsInventory()
----------------------------

### Description

Fires the ToggleTradeSkillsInventory event.
