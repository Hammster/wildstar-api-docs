AttributeMilestonesLib
======================

### Description

This library contains functions for viewing a character's Attribute
Milestones. These milestones are reached when the player's attribute
reaches a specific threshold.

------------------------------------------------------------------------

`Enum`

CodeEnumAttributeMilestoneResult
--------------------------------

### Description

The possible results when attempting to get an Attribute Milestone's
info.

-   **Ok**
-   **InvalidUnit**
-   **UnknownClassId**

------------------------------------------------------------------------

`Function`

GetAttributeMilestoneInfo(eClass)
---------------------------------

### Description

Gets information on all of the Attribute Milestones for the given class.

### Params

-   **eClass** **(GameLib.CodeEnumClass)** - The function will return
    the Attribute Milestones for this class.

### Return Value

-   **Table** - The Attribute Milestones and stat gains for the class.
    -   **eResult**
        **(AttributeMilestonesLib.CodeEnumAttributeMilestoneResult)** -
        This value will contain any errors found when trying to get a
        class' Milestone info. If this value is not "Ok", then no other
        values will be found in the table.
    -   **tMilestones** **(Table)** - A table that contains all of the
        milestones for the class.
        -   **strength** **(Table)** - The class's Brutality milestones.
            -   **tAttributeMilestones** **(Array of Table)** - The
                milestones for the attribute.
                -   **bIsMini** **(Boolean)** - Whether the milestone
                    provides a secondary stat bonus or not.
                -   **nRequiredAmount** **(Integer)** - The amount of
                    the attribute that a unit needs to reach the
                    milestone.
                -   **eUnitProperty** **(Unit.CodeEnumProperties)** -
                    The property that is modified when the player
                    reaches the milestone. This value only exists if
                    bIsMini is true.
                -   **fModifier** **(Float)** - The amount of the
                    specified property that the unit gains when they
                    reach the milestone. This only exists if bIsMini is
                    true.
                -   **nSpellId** **(Integer)** - The id number for the
                    spell that is granted when the player reaches the
                    milestone. This value only exists if bIsMini is
                    false.
                -   **nTier** **(Integer)** - The tier of the spell that
                    is granted by the milestone. This only exists if
                    bIsMini is false.
            -   **tSecondaryStats** **(Array of Table)** - The secondary
                stats that the class gains per attribute point.
                -   **eUnitProperty** **(Unit.CodeEnumProperties)** -
                    The stat that a player gains whenever they gain a
                    point in this attribute.
                -   **fBonus** **(Float)** - The amount of the stat that
                    is gained per attribute point.
        -   **dexterity** **(Table)** - The class's Finesse milestones.
        -   **technology** **(Table)** - The class's Tech milestones.
        -   **magic** **(Table)** - The class's Insight milestones.
        -   **wisdom** **(Table)** - The class's Moxie milestones.
        -   **stamina** **(Table)** - The class's Grit milestones.

### Remarks

Major milestones are an outdated concept. Any milestones where bIsMini
is false should be ignored for the time being.
