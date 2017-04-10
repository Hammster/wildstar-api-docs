ActionSetLib
============

### Description

This library contains functions for validating and saving the player's
Limited Action Set.

------------------------------------------------------------------------

`Enum`

CodeEnumLimitedActionSetResult
------------------------------

### Description

The possible results that the UI can receive when trying to save an
Action Set or AMP loadout.

-   **Ok**
-   **SlotUnlockPrereqFalse**
-   **UnknownSpellId**
-   **UnknownClassId**
-   **UnknownSpellActionSetCategoryGroupPlacement**
-   **UnknownSlotActionSetCategoryGroupAllowed**
-   **InvalidSpellActionSetCategoryGroupPlacement**
-   **InvalidSlotActionSetCategoryGroupAllowed**
-   **SlotSpellAnyMatchFail**
-   **SlotSpellAllMatchFail**
-   **SlotSpellNoneMatchFail**
-   **UnknownSpellActionSetGroupMatchType**
-   **DuplicateSpell**
-   **SpellActionSetPrereqFalse**
-   **SpellDependencyAnyMatchFail**
-   **SpellDependencyAllMatchFail**
-   **SpellDependencyNoneMatchFail**
-   **BadSpellInActionSet**
-   **ActionSetRequirementAnyMatchFail**
-   **ActionSetRequirementAllMatchFail**
-   **ActionSetRequirementNoneMatchFail**
-   **InvalidActionSetSize**
-   **InvalidUnit**
-   **InvalidSlot**
-   **InvalidActionSetTable**
-   **SpellDependencyMaxMatchFail**
-   **RestrictedInPVP**
-   **PlayerIsDead**
-   **MissingTag**
-   **InCombat**
-   **EldanAugmentation\_NotEnoughPower**
-   **EldanAugmentation\_LockedInlaid**
-   **EldanAugmentation\_LockedCategoryTier**
-   **EldanAugmentation\_InvalidSeries**
-   **EldanAugmentation\_InvalidId**
-   **EldanAugmentation\_InvalidCategoryId**
-   **EldanAugmentation\_InvalidCategoryTier**
-   **UpdateSpellInProgress**
-   **InVoid**
-   **InvalidSpecIndex**
-   **InvalidSpellTier**
-   **InsufficientAbilityPoints**
-   **EldanAugmentation\_VersionMismatch**
-   **EldanAugmentation\_SpecNotFound**
-   **LASChangeSpellFailed**
-   **SpecUnlockPrereqFalse**

------------------------------------------------------------------------

`Enum`

CodeEnumShortcutSet
-------------------

### Description

These values represent what each Action Bar Shortcut is used for.

-   **VehicleBar**
-   **PrimaryPetBar**
-   **PetMiniBar0**
-   **PetMiniBar1**
-   **PetMiniBar2**
-   **PetMiniBar3**
-   **PetMiniBar4**
-   **FloatingSpellBar**
-   **FloatingDynamicSpellBar**
-   **Count**

------------------------------------------------------------------------

`Function`

DoesActionSetMeetRequirements() (Deprecated)
--------------------------------------------

### Return Value

-   **ActionSetLib.CodeEnumLimitedActionSetResult** - Either the reason
    that the Action Set is invalid, or OK if it is valid.

------------------------------------------------------------------------

`Function`

GetCurrentActionSet()
---------------------

### Description

Gets a list of the spell ids used in the player's current action set.

### Return Value

-   **Array of Integer** - A list of spell ids for the player's current
    action set. If a slot has no spell assigned to it, the id is 0.

------------------------------------------------------------------------

`Function`

IsSlotUnlocked(nSlotIdx)
------------------------

### Description

Determines if the specified slot is unlocked for the player.

### Params

-   **nSlotIdx** **(Integer)** - The slot number that the function
    should check.

### Return Value

-   **ActionSetLib.CodeEnumLimitedActionSetResult** - This value will be
    Ok if the slot is unlocked or SlotUnlockPrereqFalse if it is locked.

------------------------------------------------------------------------

`Function`

IsSpellCompatibleWithActionSet(idSpell, arActionSet) (Deprecated)
-----------------------------------------------------------------

### Description

Checks to make sure that a spell is compatible with an action set.

### Params

-   **idSpell** **(Integer)** - The id number of the spell that the UI
    wants to place in the action set.
-   **arActionSet** **(Array of Integer)** - An array of spell ids in
    the current action set. The array's index lines up with the slot
    with the same number.

### Return Value

-   **ActionSetLib.CodeEnumLimitedActionSetResult** - The result of the
    check. If the spell is valid in the action set, the return value
    will be Ok. Otherwise, this value will contain the error that would
    prevent the spell from being added to the action set.

### Usage/Example

```lua
    -- Attempting to add the Stalker's "Stagger" ability to the current action set

    local eCanAddToSpec = ActionSetLib.IsSpellCompatibleWithActionSet(23173, ActionSetLib.GetCurrentActionSet())

    if eCanAddToSpec == ActionSetLib.CodeEnumLimitedActionSetResult.Ok then
        Print("Stagger can be added to the current action set")
    else
        Print("Stagger can not be added to the current action set.  Error: " .. eCanAddToSpec)
    end
```

------------------------------------------------------------------------

`Function`

IsSpellCompatibleWithSlot(idSpell, nSlotIdx) (Deprecated)
---------------------------------------------------------

### Description

Checks to make sure that a spell is compatible with the specified slot
in the action bar.

### Params

-   **idSpell** **(Integer)** - The id number for the spell that the
    function is validating against the action bar slot.
-   **nSlotIdx** **(Integer)** - The action bar slot that the function
    is checking the spell against.

### Return Value

-   **ActionSetLib.CodeEnumLimitedActionSetResult** - The result of the
    validation. If the spell can be added to the slot, this value is Ok.
    Otherwise, it contains the error that explains why the spell could
    not be added to the slot.

### Remarks

This function does not account for other spells in the current action
set. Because of this, it may return a result of Ok when passing in the
id of a spell that the player already has on their action bar even
though having multiple copies of the same spell on the action bar is not
valid.

------------------------------------------------------------------------

`Function`

RequestActionSetChanges(arActionSet)
------------------------------------

### Description

Attempts to make changes to the current action set.

### Params

-   **arActionSet** **(Array of Integer)** - An array of spell ids that
    represent the proposed action set. The array's index lines up with
    the slot number in the action bar.

### Return Value

-   **Table** - A table that contains the result and other data that is
    relevant to the result.
    -   **eResult** **(ActionSetLib.CodeEnumLimitedActionSetResult)** -
        The result of the UI's attempt to change the action set. If the
        change was successful, this value will be Ok. Otherwise, it will
        list the error that prevented it from being set.
    -   **tTags** **(Array of strTag)** - An array that contains the
        name of every spell category that was required but was not found
        in the action set. This table is only relevant if eResult is
        MissingTag.

### Remarks

If the result is Ok, then the server will fire the AbilityBookChange and
CharacterEldanAugmentationUpdated events.
