Achievement
===========

### Prefix: ach

### Description

Achievements are tasks that can be completed to gain various rewards.
These include the standard Achievements that you find in the
AchievementLog,\
as well as the elements of the Tradeskill Tech Tree.

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Determines whether the given variable is an Achievement

### Params

-   **oVariable** **(Any)** - The variable that is being checked.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

\_\_eq() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

Manually calls the Achievement's garbage collector.

------------------------------------------------------------------------

`Method`

GetCategory()
-------------

### Description

Returns the name of the category that the achievement belongs to.

### Return Value

-   **String** - The name of the achievement's parent category

### Usage/Example

```lua
    function Example:IsTradeskillAchievement(achSource)

        strCategoryName = achSource:GetCagetory() or ""

        if strCategoryName == "Tradeskill" or strCategoryName == "Hobby" then

            return true

        else

            return false

        end

    end
```

------------------------------------------------------------------------

`Method`

GetCategoryFullName()
---------------------

### Description

Returns the long version of the name of the category that the
achievement belongs to

### Return Value

-   **String**

------------------------------------------------------------------------

`Method`

GetCategoryId()
---------------

### Description

Returns the id number for the category that the achievement belongs to

### Return Value

-   **Integer** - The Id number for the Achievement's category

------------------------------------------------------------------------

`Method`

GetChecklistItems()
-------------------

### Description

Returns a list of things required to complete this achievement

### Return Value

-   **Array of Table**
    -   **strChecklistEntry** **(String)** - The name of this checklist
        item. This can be a description of a step of\
        the achievement, the name of an item that must be crafted, or
        the name\
        of a schematic that must be learned.
    -   **bIsComplete** **(Boolean)** - Whether or not this step of the
        achievement is complete
    -   **idSchematic** **(Integer)** - The id number of the schematic
        that must be learned or is the source\
        of the item required for this part of the achievement.

------------------------------------------------------------------------

`Method`

GetChildTier()
--------------

### Description

Returns the previous step of a multi-stage achievement.

### Return Value

-   **[Achievement](../Classes/Achievement.md)**

### Remarks

Multi-stage achievements are ones that have multiple tiers of
progression. A good example of this is the PvP Achievement "Cracked Your
First Skull".

------------------------------------------------------------------------

`Method`

GetCurrencySystem()
-------------------

### Description

Gets the type of currency required to progress the spefied Achievement.

### Return Value

-   **Money.CodeEnumCurrencyType** - The type of money the player

------------------------------------------------------------------------

`Method`

GetDateCompleted()
------------------

### Description

Returns a string with the date that the achievement was completed. The
formatting for the date varies based on which language is being used on
the\
client

### Return Value

-   **String** - The date that the achievement was completed. This date
    is localized for different regions.

------------------------------------------------------------------------

`Method`

GetDescription()
----------------

### Description

Returns the description text for the achievement when it is completed.
This function is not to be confused with Achievement:GetProgressText(),
which\
returns the description text for the achievement before it is complete

### Return Value

-   **String** - The text for the completed achievement

### Usage/Example

```lua
    function Example:PrintAchievementText(achSource)

        if achSource:IsComplete() then

            Print(achSource:GetDescription())

        else

            Print(achSource:GetProgressText())

        end

    end
```

------------------------------------------------------------------------

`Method`

GetGroup()
----------

### Description

Gets the name of the tradeskill that the achievement belongs to, if any.

### Return Value

-   **String**

------------------------------------------------------------------------

`Method`

GetId()
-------

### Description

Returns the achievement's ID number.

### Return Value

-   **Integer** - The ID number of the Achievement

### Usage/Example

```lua
    function Example::GetAchievement(idSource)
        local tAchievements = AchievementsLib.GetAchievements()
        for idx = 1, #tAchievements do
            achCurrent = tAchievements[idx]
            if achCurrent:GetId() == idSource then
                return achCurrent
            end
        end
```

------------------------------------------------------------------------

`Method`

GetName()
---------

### Description

Returns the name of the achievement

### Return Value

-   **String** - The name of the achievement calling this function

### Usage/Example

```lua
    function Example::DisplayNames()
    local tAchievements = AchievementsLib.GetAchievements()
    for idx = 1, #tAchievements do
        local achCurrent = tAchievements[idx]
        Print(achCurrent:GetName()
    end
```

------------------------------------------------------------------------

`Method`

GetNumCompleted()
-----------------

### Description

Returns the character's progress on this achievement.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Method`

GetNumNeeded()
--------------

### Description

Returns the amount of progress that is required to complete this
achievement

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Method`

GetParentCategoryId() (Deprecated)
----------------------------------

------------------------------------------------------------------------

`Method`

GetParentTier()
---------------

### Description

Returns the parent achievement of a multi-tier achievement.

### Return Value

-   **[Achievement](../Classes/Achievement.md)**

------------------------------------------------------------------------

`Method`

GetPoints()
-----------

### Description

Returns the number of achievement points granted when the achievement is
completed

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Method`

GetProgressText()
-----------------

### Description

Returns the description text that the achievement shows when it is not
complete. This function is not to be confused with
Achievement:GetDescription(),\
which returns the text for the achievement when it is complete

### Return Value

-   **String** - The text for the incomplete achievement

### Usage/Example

```lua
    function Example:PrintAchievementText(achSource)
        if achSource:IsComplete() then
            Print(achSource:GetDescription())
        else
            Print(achSource:GetProgressText())
        end
    end
```

------------------------------------------------------------------------

`Method`

GetRewards()
------------

### Description

Returns any title that is granted when the achievement is completed.

### Return Value

-   **[CharacterTitle](../Classes/CharacterTitle.md)**

------------------------------------------------------------------------

`Method`

GetSubGroup()
-------------

### Description

Returns the name of the subgroup that the achievement belongs to.

### Return Value

-   **String**

------------------------------------------------------------------------

`Method`

GetSubGroupId()
---------------

### Description

Returns the id number of the subgroup that the achievement belongs to.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Method`

GetTradeskillLayout()
---------------------

### Description

Returns the position information for the achievement and its parents.

### Return Value

-   **Table**
    -   **nX** **(Integer)** - The X coordinate of the Achievement node
    -   **nY** **(Integer)** - The Y coordinate of the Achievement node
    -   **arParents** **(Array of Table)** - The position of the parent
        -   **x** **(Integer)** - The X coordinate of the parent
        -   **y** **(Integer)** - The Y coordinate of the parent

------------------------------------------------------------------------

`Method`

GetTradeskillRewards()
----------------------

### Description

Returns a description of various rewards that a tradeskill achievement
grants

### Return Value

-   **Table**
    -   **idFaction** **(Integer)** - The id for the faction that the
        achievement gives rep with
    -   **nFactionAmount** **(Integer)** - The amount of reputation
        granted by the tradeskill
    -   **nTalentPoints** **(Integer)** - The number of tradeskill
        talent points granted by the Achievement
    -   **arSchematics** **(Array of Table)** - A list of tradeskill
        schematics that are unlocked by this Achievement
        -   **idSchematic** **(Integer)** - The id number for the
            schematic that the Achievement grants
        -   **itemCrafted** **([Item](../Classes/Item.md))** - The item
            created by the schematic that is granted by the Achievement
    -   **arBonuses** **(Array of Table)** - A list of Tradeskill
        bonuses granted by this Achievement
        -   **strIcon** **(String)** - The name of the icon used for the
            bonus granted by this Achievement
        -   **strName** **(String)** - The name of the bonus granted by
            this Achievement
        -   **strTooltip** **(String)** - The tooltip string for the
            bonus granted by this Achievement

------------------------------------------------------------------------

`Method`

GetTradeskillSchematicsRequired()
---------------------------------

### Description

Returns a list of schematic ids that the character must know before
unlocking this Achievement.

### Return Value

-   **Array of Integer** - An array of schematic ids the character must
    know before the achievement is unlocked.

------------------------------------------------------------------------

`Method`

GetWorldZoneId()
----------------

### Description

Returns the zone id where this achievement can be completed.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Method`

IsChecklist()
-------------

### Description

Determines if the Achievement requires multiple different steps to
complete it

### Return Value

-   **Boolean** - Whether the achievmemnt is a checklist or not.

------------------------------------------------------------------------

`Method`

IsComplete()
------------

### Description

Determines whether or not the Achievement has been completed.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Method`

IsCurrencyShown()
-----------------

### Description

Determines whether the achievent requires currency to be completed.

### Return Value

-   **Boolean** - If the achievement requires currency, this will return
    true.

------------------------------------------------------------------------

`Method`

IsGuildAchievement()
--------------------

### Description

Determines if an Achievement is a Guild Achievement

### Return Value

-   **Boolean**
