AbilityBook
===========

### Description

A library that contains a large number of functions that are centered
around the Limited Action Set.

------------------------------------------------------------------------

`Enum`

CodeEnumAMPRespecType
---------------------

-   **Full**
-   **Section**
-   **Single**

------------------------------------------------------------------------

`Enum`

CodeEnumEldanAvailability
-------------------------

### Description

This enum rempresents the AMP's current state.\
\
Unavailable - The player has not unlocked the AMP\
Inaccessible - The player has not unlocked that AMP's tier\
Inactivated - The player has not spent points to activate this AMP\
Activated - The player has spent points to activate this AMP

-   **Unavailable**
-   **Inaccessible**
-   **Inactivated**
-   **Activated**

------------------------------------------------------------------------

`Enum`

CodeEnumSpecConstant
--------------------

### Description

This is a single value representing the maximum number of specs the
player can have.

-   **MaxNumSpecs**

------------------------------------------------------------------------

`Enum`

CodeEnumSpecError
-----------------

### Description

Error messages that the player can receive when attempting to save their
spec. Ok is the success case.

-   **Ok**
-   **InvalidIndex**
-   **NoChange**
-   **InCombat**
-   **InvalidPlayer**
-   **IndexLocked**
-   **PvPRestricted**
-   **InVoid**

------------------------------------------------------------------------

`Function`

ActivateSpell(idSpell, bActive)
-------------------------------

### Description

Sets the spell's activated state. Spells are considered activated when
they are able to be added to the player's limited action set.

### Params

-   **idSpell** **(Integer)** - The id for the ability being activated
-   **bActive** **(Boolean)** - Whether the spell should be made active
    or inactive.

### Return Value

-   **Boolean** - Returns a boolean stating whether or not the spell was
    successfully activated.

------------------------------------------------------------------------

`Function`

ClearCachedEldanAugmentationSpec()
----------------------------------

### Description

Removes any changes that were made to players AMPs but were not saved.

------------------------------------------------------------------------

`Function`

ClearCachedLASUpdates()
-----------------------

### Description

Clears any unsaved changes to the player's limited action set.

------------------------------------------------------------------------

`Function`

CommitEldanAugmentationSpec()
-----------------------------

### Description

Submits the currently selected AMPs so they are saved to the player's
current spec.

------------------------------------------------------------------------

`Function`

GetAbilitiesList(eSpellType)
----------------------------

### Description

Returns a table with information on each of the character's abilities.

### Params

-   **eSpellType** **(Spell.CodeEnumSpellTag)** - A number representing
    the spell's type. Non-Combat abilities have either the Mount, Misc,
    or Path tags.

### Return Value

-   **Array of Table** - An array of tables that contain information on
    each spell that the player has access to.
    -   **nId** **(Integer)** - The id number of the base spell.
    -   **strName** **(String)** - The spell's name.
    -   **nMaxTiers** **(Integer)** - The maximum number of tiers that
        the spell has.
    -   **bIsActive** **(Boolean)** - Determines whether the ability is
        unlocked or not.
    -   **nCurrentTier** **(Integer)** - The current tier set for the
        spell.
    -   **strAbilityDescription** **(String)** - The description of the
        spell that is listed in the tooltip.
    -   **strAbilityPerTierPointDescription** **(String)** - A listing
        of what is added to the spell after each tier upgrade. This does
        not include the Tier 4 and Tier 8 bonuses.
    -   **tTiers** **(Array of Table)** - An array of tables that
        contain information for each tier of the spell. The contents of
        this table differ depending on whether the spell is a combat or
        non-combat spell, or if the spell summons a mount.
        -   **strName** **(String)** - The name of the spell.
        -   **nId** **(Integer)** - The id number of the base spell.
        -   **nTier** **(Integer)** - The tier that is listed in this
            table.
        -   **nTrainingCost** **(Integer)** - The number of credits
            required to unlock the base spell.
        -   **nTierPointCost** **(Integer)** - The number of Ability
            Points required to upgrade to this tier.
        -   **bCanPurchase** **(Boolean)** - Whether or not the player
            meets the requirements to unlock the spell.
        -   **bAmpUnlocked** **(Boolean)** - Whether the spell requires
            an AMP to be active before it can be unlocked. This variable
            is only used for Combat spells.
        -   **nLevelReq** **(Integer)** - The level required to unlock
            this spell's tier.
        -   **bIsActive** **(Boolean)** - Whether the player is using
            this tier of the spell.
        -   **strTierBonusDescription** **(String)** - The tier bonus
            that the player gets at this tier.
        -   **splObject** **([Spell](../Classes/Spell.md))** - The
            spell for this tier.
        -   **nTierSpellId** **(Integer)** - The id number for the spell
            at this tier. This variable is only used for non-combat
            spells.
        -   **nPreviewCreatureId** **(Integer)** - The id number of the
            creature spawned when using this ability. This is primarily
            used for preview purposes and only exists for Mount type
            spells.
        -   **nPreviewHoverboardItemDisplay** **(Integer)** - The id
            number of the hoverboard. This is primarily used for preview
            purposes and is only set if the spell is a mount.
        -   **bIsHoverboard** **(Boolean)** - Specifies whether the
            spell is for a hoverboard or another type of mount. This
            variable is only set if the spell summons a mount.

------------------------------------------------------------------------

`Function`

GetAbilityInfo(idSpell, eSpellType)
-----------------------------------

### Description

Gives the UI information on a specific spell.

### Params

-   **idSpell** **(Integer)** - The id number of the spell that is being
    queried.
-   **eSpellType** **(Spell.CodeEnumSpellTag)** - The type of spell
    being queried. This should match up with the type of spell that was
    used in the first argument.

### Return Value

-   **Table** - A table that contains information on the spell
    -   **nId** **(Integer)** - The id number of the base level of the
        spell.
    -   **strName** **(String)** - The name of the spell.
    -   **nMaxTiers** **(Integer)** - The maximum number of tiers
        allowed for the spell.
    -   **bIsActive** **(Boolean)** - Whether the spell has been
        purchased or not.
    -   **nCurrentTier** **(Integer)** - The tier that the spell is
        currently set to.
    -   **strAbilityDescription** **(String)** - The description of the
        ability, as shown in the tooltip.
    -   **strAbilityPerTierPointDescription** **(String)** - The
        description of the spell.
    -   **tTiers** **(Array of Table)** - Information on each tier of
        the spell.
        -   **strName** **(String)** - The name of the spell.
        -   **nId** **(Integer)** - The id number of the base spell.
        -   **nTier** **(Integer)** - The tier that is referenced in
            this table.
        -   **nTrainingCost** **(Integer)** - The amount of currency
            needed to train this spell. This value is usually only set
            for the base level of the spell.
        -   **nTierPointCost** **(Integer)** - The number of Ability
            Points that the player must use to unlock this tier.
        -   **bCanPurchase** **(Boolean)** - Determines whether the
            player meets the requirement to purchase this tier of the
            ability.
        -   **bAmpUnlocked** **(Boolean)** - Determines whether the
            spell is unlocked via an AMP or not.
        -   **nLevelReq** **(Integer)** - The level the player must
            reach before using this tier of the spell.
        -   **bIsActive** **(Boolean)** - Whether the player is using
            this tier or not.
        -   **strTierBonusDescription** **(String)** - The description
            of the spell at this tier.
        -   **splObject** **([Spell](../Classes/Spell.md))** - The
            spell at this tier.
        -   **nTierSpellId** **(Integer)** - The id number of the spell.
            This only exists for non - combat spells.
        -   **nPreviewCreatureId** **(Integer)** - The id number of the
            mount that can be previewed from this spell. This variable
            only exists if the spell type is Mount.
        -   **nPreviewHoverboardItemDisplay** **(Integer)** - The id of
            the hoverboard that should be displayed in the mount
            preview. This value is only valid if the spell type was set
            to Mount and the mount happens to be a Hoverboard.
        -   **bIsHoverboard** **(Boolean)** - Determines whether the
            mount is a hoverboard or not. This is only set if the Mount
            tag was passed in.

------------------------------------------------------------------------

`Function`

GetAvailableLockedInPower()
---------------------------

### Description

Gets the amount of unused AMP power the player has left in their current
saved spec. This value does not account for any changes that the player
has made that have not been saved.

### Return Value

-   **Integer** - The amount of unused AMP power in the current spec.

------------------------------------------------------------------------

`Function`

GetAvailablePower()
-------------------

### Description

Gets the amount of AMP power the player has left. This value accounts
for any changes that have not been saved.

### Return Value

-   **Integer** - The number of AMP points the player has not spent.

------------------------------------------------------------------------

`Function`

GetCurrentSpec()
----------------

### Description

Gets the number of the Action Set that the player is currently using.

### Return Value

-   **Integer** - The number of the Action Set that the player is
    currently using.

------------------------------------------------------------------------

`Function`

GetEldanAugmentationData(nSpecIndex)
------------------------------------

### Description

Gets information for each AMP for the player's class.

### Params

-   **nSpecIndex** **(Integer)** - The index of the Action Set that the
    function should return the AMP data for. If this value is not valid,
    the function will return False.

### Return Value

-   **Array of Table** - The information for each category and each AMP.
    -   **tCategories** **(Array of Table)** - The information for each
        category.
        -   **nId** **(Integer)** - The id number for the AMP category.
            The categories (in order) are:\
            \
            Damage/Support\
            Support\
            Support/Utility\
            Utility\
            Damage/Utility\
            Damage
        -   **strName** **(String)** - The localized name of the
            category.
        -   **fPowerInCategory** **(Float)** - The amount of AMP power
            the player has used on the category.
        -   **nHighestTierUnlocked** **(Integer)** - The highest tier
            that the player can access in the category. This value
            ranges from 1-3.
        -   **nCategoriesToUnlock** **(Integer)** - The number of
            categories that can help unlock this category.
        -   **tUnlockedCategories** **(Array of Table)** - Information
            on the categories that help unlock this category. The number
            of entries should match nCategoriesToUnlock.
            -   **nUnlockCategoryId** **(Integer)** - The id number of
                the category that helps unlock this one.
            -   **nTier2Amount** **(Integer)** - The amount of power
                that is needed in this category for the category in the
                parent table to increase to tier 2.
            -   **nTier3Amount** **(Integer)** - The amount of power
                that is needed in this category for the category in the
                parent table to increase to tier 3.
    -   **tAugments** **(Array of Table)** - The information for each
        AMP.
        -   **nId** **(Integer)** - The id number for the AMP.
        -   **eEldanAvailability**
            **(AbilityBook.CodeEnumEldanAvailability)** - The current
            state of the AMP.
        -   **nPowerCost** **(Integer)** - The amount of AMP power
            required to activate the AMP.
        -   **nItemIdUnlock** **(Integer)** - The item id for the for
            the item that unlocks the AMP.
        -   **bUnlocked** **(Boolean)** - Whether the item is unlocked
            or not.
        -   **nEldanAugmentationIdRequired** **(Integer)** - The id
            number of the AMP the player has to activate before this one
            unlocks.
        -   **bRequiredOkay** **(Boolean)** - Whether the required AMPs
            have been activated or not.
        -   **nDisplayRow** **(Integer)** - The row that the AMP is
            drawn on.
        -   **nDisplayColumn** **(Integer)** - The column that the AMP
            is drawn on.
        -   **nCategoryId** **(Integer)** - The id number of the
            category that the AMP belongs to.
        -   **nCategoryTier** **(Integer)** - The tier that the AMP is
            in.
        -   **nSpellIdAugment** **(Integer)** - The id number of the
            spell that unlocks when the AMP is learned.
        -   **strTitle** **(String)** - The name of the AMP.
        -   **strDescription** **(String)** - The description of what
            the AMP does.

------------------------------------------------------------------------

`Function`

GetEldanAugmentationResetData()
-------------------------------

### Return Value

-   **Table**
    -   **nCount** **(Integer)** - The number of results possible when
        the player resets their AMPs.
    -   **nSpecIndex** **(Integer)** - The spec that was affected most.
    -   **eLimitedActionSetReslut** **(Integer)** - The result that the
        SpecIndex is tied to.

------------------------------------------------------------------------

`Function`

GetEldanAugmentationRespecCost()
--------------------------------

### Description

Gets the cost to respec the character's AMPs, in copper.

### Return Value

-   **Integer** - The number of credits required to reset the
    character's AMPs, in copper.

------------------------------------------------------------------------

`Function`

GetNumUnlockedSpecs()
---------------------

### Description

Gets the number of Action Sets the current player has unlocked.

### Return Value

-   **Integer** - The number of Action Sets the player has unlocked.

------------------------------------------------------------------------

`Function`

GetSpellTierLevelRequirements()
-------------------------------

### Description

Gets the level requirememts for the player to learn each spell tier.

### Return Value

-   **Array of Integer** - The level the character has to be in order to
    unlock each tier of a spell. Index 1 is the base spell, while 2 is
    Tier 1, etc.

------------------------------------------------------------------------

`Function`

GetTagsForSpell(idSpell)
------------------------

### Description

Gets the category that the spell belongs to.

### Params

-   **idSpell** **(Integer)** - The id number for the spell that is
    being checked.

### Return Value

-   **Array of String** - An array of strings that contain the names of
    the categories that the spell belongs to.

------------------------------------------------------------------------

`Function`

GetTotalPower()
---------------

### Description

Gets the total amount of AMP points availalble to the player.

### Return Value

-   **Integer** - The total number of AMP points the player has.

------------------------------------------------------------------------

`Function`

IsLASChangeActive()
-------------------

### Description

Checks to make sure that the Change Spec ability is active.

### Return Value

-   **Boolean** - Informs the UI whether the Limited Action Set can be
    chaged.

------------------------------------------------------------------------

`Function`

NextSpec()
----------

### Description

Cycles to the next Action Set available to the player. If the player is
already at their latest action set, it cycles to the first Action Set.

------------------------------------------------------------------------

`Function`

PrevSpec()
----------

### Description

Cycles back to an earlier Action Set. If the player is already at their
first Action Set, it cycles to the last one.

------------------------------------------------------------------------

`Function`

RespecEldanAugmentations()
--------------------------

### Description

Attempts to reset the player's AMPs for their current spec.

### Return Value

-   **Boolean** - Whether the reset was successful or not.

------------------------------------------------------------------------

`Function`

SetCurrentSpec(nSpecNumber)
---------------------------

### Description

Selects a specific Action Set for the player.

### Params

-   **nSpecNumber** **(Integer)** - The Action Set that the player will
    switch to.

------------------------------------------------------------------------

`Function`

UpdateEldanAugmentationSpec(nSpecIdx, nActivatedAmps, tUnlockedAmps)
--------------------------------------------------------------------

### Description

Saves the AMPs in the Action Set that the player has been working in.

### Params

-   **nSpecIdx** **(Integer)** - The Action Set number that is being
    updated.
-   **nActivatedAmps** **(Integer)** - The number of activated AMPs in
    the Action Set.
-   **tUnlockedAmps** **(Table)** - A table with a list of activated AMP
    ids, indexed by those ids.

### Return Value

-   **Boolean** - Whether the operation was successful or not.

------------------------------------------------------------------------

`Function`

UpdateSpellTier(idBaseSpell, nTier)
-----------------------------------

### Description

Sets the spell to the specified tier in the cached copy of the Action
Set. This is not the saved copy, so any changes that are not saved are
not permenantly set.

### Params

-   **idBaseSpell** **(Integer)** - The id number for the base spell.
-   **nTier** **(Integer)** - The tier that the spell is being set to.

------------------------------------------------------------------------

`Function`

ValidateEldanAugmentationSpec(nSpecIdx, nUnlockedAmps, tUnlockedAMPIds) (Deprecated)
------------------------------------------------------------------------------------

### Description

Checks to make sure that the specified action set is valid and ready to
be updated.

### Params

-   **nSpecIdx** **(Integer)** - The Action Set that the function is
    trying to save.
-   **nUnlockedAmps** **(Integer)** - The number of AMPS that the player
    has activated.
-   **tUnlockedAMPIds** **(Table)** - A table that contains the id
    numbers of every AMP that the player has activated.

### Return Value

-   **ActionSetLib.CodeEnumLimitedActionSetResult** - The result of the
    operation
