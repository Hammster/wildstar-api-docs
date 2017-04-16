ApolloCursor
============

### Prefix: ac

### Description

ApolloCursors are the sprites that are used on the cursor in different
situations.

------------------------------------------------------------------------

`Function`

GetCursor(strCursorName)
------------------------

### Description

Returns the ApolloCursor with the specified name.

### Params

-   **strCursorName** **(String)** - The name of the cursor that should
    be returned.

### Return Value

-   **[ApolloCursor](../Classes/ApolloCursor.md)** - The cursor that
    was requested. If no cursor was found, this returns nil.

### Usage/Example

```lua
    ApolloCursors that are returned from this function can be passed into Apollo.SetCursor() to change the window cursor.

    function Example:ForceChangeCursor()
        local unitHover = GetMouseOverUnit()
        local unitPlayer = GameLib.GetPlayerUnit()
        local acForcedCursor = nil
        if unitPlayer and unitHover then
            local eDisposition = unitPlayer:GetDispositionTo(unitHover)
            if unitPlayer:GetClassId() == GameLib.CodeEnumClass.Warrior and eDisposition == Unit.CodeEnumDisposition.Hostile or eDisposition == Unit.CodeEnumDisposition.Neutral then
                acForcedCursor = ApolloCursor.GetCursor(AttackWarrior)
            else
                acForcedCursor = ApolloCursor.GetCursor(Attack)
            end
        end

        if acForcedCursor then
            Apollo.SetCursor(acForcedCursor)
        end
    end
```

### Remarks

The values that can be passed in for this are:\
Attack\
AttackWarrior\
AttackSpellslinger\
Attack ESPer (this is not a typo)\
AttackMedic\
Default\
DefaultGame\
DefaultResizeNS\
DefaultResizeEW\
DefaultResizeNESW\
DefaultResizeNWSE\
DragDropIgnore\
DragDropValid\
DragDropInvalid\
DragDropTrash\
DragDropTrade\
Feather\
FeatherInactive\
Gossip\
GossipInactive\
Hammer\
HammerInactive\
Instance\
InstanceInactive\
Interact\
InteractInactive\
Link\
Loot\
LootInactive\
NewQuest\
NewQuestInactive\
PathExplorer\
PathExplorerInactive\
PathScientist\
PathScientistInactive\
PathSettler\
PathSettlerInactive\
PathSoldier\
PathSoldierInactive\
PendingSpell\
PendingSpellInvalid\
QuestContinue\
QuestContinueInactive\
QuestReward\
QuestRewardInactive\
Recall\
RecallInactive\
Vendor\
VendorInactive

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Determines if the variable is an ApolloCursor.

### Params

-   **oVariable** **(Variable)** - The variable that the function will
    check.

### Return Value

-   **Boolean** - Whether the variable is an ApolloCursor or not.

------------------------------------------------------------------------

`Function`

new()
-----

### Description

Creates a new ApolloCursor with no cursor set.

### Return Value

-   **[ApolloCursor](../Classes/ApolloCursor.md)** - A fresh, empty
    ApolloCursor.

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

The ApolloCursor's garbage collection function. This will delete the
ApolloCursor and free up the memory used for it.
