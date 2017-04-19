CraftingLib
===========

### Description

This library is the primary way that the UI interacts with various
tradeskills and schematics. This includes tradeskills that the player
has chosen, as well as ones that they are automatically granted such as
cooking and runecrafting.

------------------------------------------------------------------------

`Enum`

CodeEnumCraftingDirection
-------------------------

### Description

A list of directions used when performing non-equipment based
tradeskills.

-   **None**
-   **N**
-   **NE**
-   **E**
-   **SE**
-   **S**
-   **SW**
-   **W**
-   **NW**

------------------------------------------------------------------------

`Enum`

CodeEnumCraftingDiscoveryHotCold
--------------------------------

### Description

A set of enums representing how close a player was to discovering a
schematic while performing non-equipment based tradeskills.

-   **Cold**
-   **Warm**
-   **Hot**
-   **Success**

------------------------------------------------------------------------

`Enum`

CodeEnumItemCraftingGroupFlag
-----------------------------

-   **Air**
-   **Water**
-   **Earth**
-   **Fire**
-   **Logic**
-   **Life**
-   **Fusion**

------------------------------------------------------------------------

`Enum`

CodeEnumItemStatType
--------------------

-   **None**
-   **UnitProperty**
-   **Random**
-   **Set**
-   **UnlockedGroup**
-   **UNUSED03**

------------------------------------------------------------------------

`Enum`

CodeEnumTradeskill
------------------

### Description

A list of the different tradeskills available to the player. Augmentor,
Farmer, and Fishing are not currently used.

-   **Weaponsmith**
-   **Cooking**
-   **Armorer**
-   **Mining**
-   **Outfitter**
-   **Survivalist**
-   **Augmentor**
-   **Architect**
-   **Relic\_Hunter**
-   **Fishing**
-   **Farmer**
-   **Tailor**
-   **Runecrafting**

------------------------------------------------------------------------

`Enum`

CodeEnumTradeskillResult
------------------------

### Description

A list of possible outcomes for several tradeskill actions.

-   **Success**
-   **InsufficentFund**
-   **InvalidItem**
-   **InvalidSlot**
-   **MissingEngravingStation**
-   **Unlocked**
-   **UnknownError**
-   **GlyphExists**
-   **MissingGlyph**
-   **DuplicateGlyph**
-   **AttemptFailed**
-   **GlyphSlotLimit**
-   **RuneExists**
-   **MissingRune**
-   **DuplicateRune**
-   **RuneSlotLimit**

------------------------------------------------------------------------

`Enum`

CodeEnumTradeskillTier
----------------------

### Description

These values represent the various tradeskill tiers.

-   **Novice**
-   **Apprentice**
-   **Journeyman**
-   **Expert**
-   **Artisan**
-   **Zero**
-   **Master**
-   **GrandMaster**

------------------------------------------------------------------------

`Function`

AddAdditive(itemAdditive)
-------------------------

### Description

Attempts to add an additive to the current crafting attempt.

### Params

-   **itemAdditive** **([Item](../Classes/Item.md))** - The additive
    that should be used for the current crafting session.

### Usage/Example

```lua
    If the function is successful, the CraftingUpdateCurrent event will fire.  Otherwise, the client will show the appropriate error message.
```

------------------------------------------------------------------------

`Function`

AddRuneSlot(nNewSlotCount) (Deprecated)
---------------------------------------

### Description

Attempts to add a rune slot to an item.

### Params

-   **nNewSlotCount** **(Integer)** - The number of rune slots on the
    item after adding a new one.

------------------------------------------------------------------------

`Function`

ClearRuneSlot(nSlotIdx) (Deprecated)
------------------------------------

### Description

Attempts to remove the rune in the specified rune slot.

### Params

-   **nSlotIdx** **(Integer)** - The index of the rune slot that the
    function will attempt to clear.

------------------------------------------------------------------------

`Function`

CompleteCraft(tCrafting)
------------------------

### Description

Tells the client to complete the current schematic. If this is called on
a non-equipment based crafting schematic, no parameters are needed.

### Params

-   **tCrafting** **(Table)** - The parameters representing the player's
    chooses while crafting.
    -   **nApSpSplitDelta** **(Integer)** - The number of Ap/Sp
        increments to use when calculating the split. A positive number
        will make the item more support based.
    -   **itemPowerCore** **([Item](../Classes/Item.md))** - The item
        to use as the power core. This must be a valid power core for
        the item.
    -   **arStats** **(Array of Table)** - An array representing the
        player's crafting chooses per stat.
        -   **nChargeDelta** **(Integer)** - A number representing the
            number of charge increments to adjust the budget of the stat
            by.
        -   **eProperty** **(Unit.CodeEnumProperties)** - The property
            selected for this stat during crafting.

### Return Value

-   **Bool** - Returns true if the request was sent to the server.

### Usage/Example

```lua
    This function will fire the CraftingSchematicComplete event if it is successful.
```

------------------------------------------------------------------------

`Function`

CompleteRerollRuneType() (Deprecated)
-------------------------------------

------------------------------------------------------------------------

`Function`

CraftItem(idSchematic)
----------------------

### Description

Begins a crafting attempt for the specified schematic.

### Params

-   **idSchematic** **(Integer)** - The schematic that the player is
    trying to craft.

### Usage/Example

```lua
    If the crafting attempt is successfully started, then the CraftingUpdateCurrent event will fire and the materials for the schematic will be consumed.
```

------------------------------------------------------------------------

`Function`

ForgetTradeskill() (Deprecated)
-------------------------------

### Description

This function has no code and does nothing.

------------------------------------------------------------------------

`Function`

GetAchievementCategoryForTier(eTradeskill, eTier)
-------------------------------------------------

### Description

Gets the achievement category id for the tradeskill tier's associated
achievement.

### Params

-   **eTradeskill** **(CraftingLib.CodeEnumTradeskill)** - The
    tradeskill that the function will use to find the achievement
    category.
-   **eTier** **(CraftingLib.CodeEnumTradeskillTier)** - The tier that
    the function will return the achievement category id for.

### Return Value

-   **Integer** - The id number for the achievement category that the
    tradeskill tier belongs to.

------------------------------------------------------------------------

`Function`

GetAvailableAdditives(eTradeskill, idSchematic)
-----------------------------------------------

### Description

Gets a list of the additives that are available for the specified
schematic.

### Params

-   **eTradeskill** **(CraftingLib.CodeEnumTradeskill)** - The
    tradeskill that the schematic belongs to.
-   **idSchematic** **(Integer)** - The function will get the additives
    that can be used with the schematic with this id.

### Return Value

-   **Array of [Item](../Classes/Item.md)** - An array of the different
    additives that can be used with the schematic.

------------------------------------------------------------------------

`Function`

GetAvailableCatalysts(eTradeskill, idSchematic)
-----------------------------------------------

### Description

Gets a list of the catalysts that are in the player's inventory and can
be used with the specified schematic.

### Params

-   **eTradeskill** **(CraftingLib.CodeEnumTradeskill)** - The
    tradeskill that the schematic belongs to.
-   **idSchematic** **(Integer)** - The function will get a list of the
    catalysts that can be used with the schematic with this id.

### Return Value

-   **Array of Table** - An array that contains both the catalyst items
    that can be used with the schematic and the number that the player
    has in their inventory.
    -   **nCount** **(Integer)** - The number of this catalyst that is
        in the player's inventory.
    -   **itemCatalyst** **([Item](../Classes/Item.md))** - The
        catalyst that is in the player's inventory.

------------------------------------------------------------------------

`Function`

GetAvailableMicrochips(idSchematic, eUnitProperty, nOffset, nCount, nPowerCoreId) (Deprecated)
----------------------------------------------------------------------------------------------

### Description

Gets a list of the microchips that can be used with the specified
schematic.

### Params

-   **idSchematic** **(Integer)** - The schematic that the function will
    poll for the microchips that can be used.
-   **eUnitProperty** **(Unit.CodeEnumProperties)** - The microchips
    that are returned all share this property.
-   **nOffset** **(Integer)** - The starting index of the returned
    table.
-   **nCount** **(Integer)** - The number of entries in the table that
    is returned by the function. This value defaults to 1 if none is
    passed in.
-   **nPowerCoreId** **(Integer)** - The item id of the power core that
    is slotted for the recipe. This will affect the microchips that are
    returned. If no value is passed in, it defaults to 0.

### Return Value

-   **Array of [Item](../Classes/Item.md)** - A table that contains a
    list of microchips that are available for the schematic.

------------------------------------------------------------------------

`Function`

GetAvailablePowerCores(idSchematic)
-----------------------------------

### Description

Gets a list of power cores that can be used with the specified
schematic.

### Params

-   **idSchematic** **(Integer)** - The function will return a list of
    power cores that are compatable with the schematic with this id.

### Return Value

-   **Array of [Item](../Classes/Item.md)** - A table that contains the
    item information for power cores that can be used for the specified
    schematic.

------------------------------------------------------------------------

`Function`

GetAvailableProperties()
------------------------

### Description

Gets details of of all craftable properties. During a crafting session
then this will include the properties that the player has learned.

### Return Value

-   **Array of Table** - An array of tables representing each group of
    properties.
    -   **eCraftingGroup**
        **(CraftingLib.CodeEnumItemCraftingGroupFlag)** - The group
        identifing this set of properties. The Fusion group will contain
        all properties.
    -   **arProperties** **(Array of Unit.CodeEnumProperties)** - The
        set of properties within this crafting group.

------------------------------------------------------------------------

`Function`

GetCurrentCraft()
-----------------

### Description

If the player has an unfinished crafting attempt, this function will
return information on that craft.

### Return Value

-   **Table** - A table that contains information on the player's last
    crafting attempt. The variables in the table will differ based on
    what type of schematic the player was attempting to craft.
    -   **nSchematicId** **(Itneger)** - The id number for the schematic
        that the player was trying to craft.
    -   **nSchematicCount** **(Integer)** - The number of items created
        ty the schematic.
    -   **fVectorX** **(Float)** - The X coordinate of the target marker
        for Coordinate Crafting. This variable is only used if the
        schematic that is referenced uses Coordinate Crafting.
    -   **fVectorY** **(Float)** - The Y coordinate of the target marker
        in Coordinate Crafting. This variable is only used if the
        schematic that is referenced uses Coordinate Crafting.
    -   **nSubSchematicId** **(Integer)** - The id number of a sub
        schematic that the player has landed the target marker on. This
        variable is only used if the schematic that is referenced uses
        Coordinate Crafting.
    -   **nAdditiveCount** **(Integer)** - The number of additives that
        the player has used on the schematic so far. This variable is
        only used if the schematic that is referenced uses Coordinate
        Crafting.
    -   **itemGlobalCatalyst** **([Item](../Classes/Item.md))** - The
        global catalyst that the player used on the schematic. This
        variable is only used if the schematic that is referenced uses
        Coordinate Crafting.
    -   **arStats** **(Array of Table)** - An array of tables
        representing the results of the player's crafting chooses and
        server forced chooses.
        -   **nBudget** **(Float)** - Amount of budget normally applied
            to this stat.
        -   **eProperty** **(Unit.CodeEnumProperties)** - The current
            selected property.
        -   **nUsedBudget** **(Float)** - Amount of budget allocated to
            this stat.
        -   **nCraftingBudget** **(Float)** - Amount of budget used when
            determine overcharge. This will be greater than nUsedBudget
            if there's slot mismatch.
        -   **eCraftingGroup**
            **(CraftingLib.CodeEnumItemCraftingGroupFlag)** - The server
            selected crafting group for this stat.
    -   **tSettings** **(Table)** - A table representing the settings
        for circuitboard crafting.
        -   **nApSpSplitIncrement** **(Float)** - The amount of ApSp
            split per ApSp split delta point.
        -   **nApSpSplitCap** **(Float)** - The absolute range of the
            ApSp split.
        -   **nApSpSplitMaxDelta** **(Integer)** - The number of ApSp
            split deltas possible. A delta can be a negative number of
            these.
        -   **nChargeIncrement** **(Integer)** - The amount of charge
            per charge delta.
        -   **nChargeCap** **(Integer)** - The absolute range of charge.
        -   **nChargeMaxDelta** **(Integer)** - The number of charge
            deltas possible. A delta can be a negative number of these.
        -   **nMismatchPenalty** **(Float)** - Percentage of penalty
            budget incurred when mismatching crafting group properties.
    -   **tResult** **(Table)** - A table representing the current
        calculate results.
        -   **nCraftedBudget** **(Float)** - The current crafted budget
            including penalties due to mismatch.
        -   **nFailCap** **(Float)** - The maximum failure percentage
            allowed.
        -   **nFailChance** **(Float)** - The current failure
            percentage.
        -   **bIsValidCraft** **(Integer)** - A basic validation against
            the parameters.
        -   **nBudget** **(Float)** - The normally expected budget for
            this item.
        -   **monCraftingCost** **([Money](../Classes/Money.md))** - If
            there is a cost to craft then this will be the currenct cost
            to complete the crafting process.

------------------------------------------------------------------------

`Function`

GetCurrentOverchargeInfo(arMicrochipIds, arThresholds) (Deprecated)
-------------------------------------------------------------------

### Description

Gets information on the current overcharge and various overcharge limits
of the current Circuit Board schematic.

### Params

-   **arMicrochipIds** **(Array of Integer)** - An array that contains
    the item ids of each microchip set in the schematic.
-   **arThresholds** **(Array of Integer)** - An array that contains the
    thresholds used for each microchip slot.

### Return Value

-   **Table** - A table that contains information on all things
    overcharge related to the current schematic.
    -   **arMultipliers** **(Array of Float)** - The property
        multipliers used for each microchip where the player matched the
        color of the chip with the slot.
    -   **fOverchargeCompleteSuccess** **(Float)** - The maximum amount
        of overcharge where the chance of success is 100%.
    -   **fOverchargeCompleteFailure** **(Float)** - The amount of
        overcharge where the chance to fail will reach 100%.
    -   **fCraftingOvercharge** **(Float)** - The current amount of
        overcharge for the schematic.
    -   **fOverchargeAllowable** **(Float)** - The maximum amount of
        overcharge that is allowed for the schematic.
    -   **fCraftingFailChance** **(Float)** - The chance that the
        crafting attempt will fail with the current amount of
        overcharge.
    -   **fFailureAtAllowable** **(Float)** - The failure chance when
        the maximum amount of overcharge is set for the schematic.

------------------------------------------------------------------------

`Function`

GetEngravingInfo(itemSource)
----------------------------

### Description

Gets information about adding, clearing, rerolling, and unlocking Rune
Slots in an item.

### Params

-   **itemSource** **([Item](../Classes/Item.md))** - The item that the
    function will query for information on its Rune Slots.

### Return Value

-   **Table** - A table that contains information on the requirements to
    modify an item's Rune Slots.
    -   **tAddInfo** **(Table)** - Information on adding Rune Slots to
        the item.
        -   **tReagent** **(Table)** - Information on the reagent used
            for adding a rune slot. Includes owned count, cost, and
            allowed usage.
            -   **nOwnedCount** **(Integer)** - Quantity owned by the
                character.
            -   **itemReagent** **([Item](../Classes/Item.md))** - The
                object representing the reagent used for adding a rune
                slot.
            -   **nSuccessChance** **(Float)** - Provided if the success
                chance of adding the rune is not 100%.
            -   **nMaximumRuneSlots** **(Integer)** - Maximum number of
                rune slots that this item can have.
            -   **nCost** **(Integer)** - The number of reagents
                necessary to add a slot.
    -   **tClearInfo** **(Table)** - Information on clearing a Rune from
        a Rune Slot.
        -   **arSlot** **(Array of Table)** - Details for clearing each
            rune slot.
            -   **bAllowed** **(Boolean)** - If true then this rune slot
                can be cleared.
            -   **monCost** **([Money](../Classes/Money.md))** - The
                cost to clear this rune slot.
    -   **tRerollInfo** **(Table)** - Information on rerolling a Rune
        Slot on the item.
        -   **tReagent** **(Table)** - Description about the reagent use
            and costs.
            -   **nOwnedCount** **(Integer)** - The quantity of reagents
                owned by the character.
            -   **itemReagent** **([Item](../Classes/Item.md))** - The
                item represents the reagent used for reroll.
            -   **nCost** **(Integer)** - The number of reagents needed
                to do a reroll.
            -   **nSuccessChance** **(Float)** - The chance of sucess if
                success is not 100%.
        -   **arAllowed** **(Array of Boolean)** - Used to determine if
            the corresponding rune slot can be rerolled.

------------------------------------------------------------------------

`Function`

GetItemsWithRuneSlots(bIncludeEquipped, bIncludeBags)
-----------------------------------------------------

### Description

Gets a list of each item with rune slots that the player owns.

### Params

-   **bIncludeEquipped** **(Boolean)** - Whether items that the player
    has equipped should be included in the list or not.
-   **bIncludeBags** **(Boolean)** - Whether items that are in the
    player's bags should be included in the list or not.

### Return Value

-   **Array of [Item](../Classes/Item.md)** - An array of items that
    have rune slots and are in the specified locations.

### Remarks

If neither variable that is passed in is set to true, the list of items
will be empty.

------------------------------------------------------------------------

`Function`

GetItemsWithRuneSlots() (Deprecated)
------------------------------------

------------------------------------------------------------------------

`Function`

GetKnownTradeskills()
---------------------

### Description

Gets the id numbers and names of the tradeskills known by the character.

### Return Value

-   **Array of Table** - The names and id numbers of tradeskills that
    are active for the character.
    -   **eId** **(CraftingLib.CodeEnumTradeskill)** - The tradeskill's
        id.
    -   **strName** **(String)** - The name of the tradeskill.

------------------------------------------------------------------------

`Function`

GetModSchematicInfo(itemCrafting) (Deprecated)
----------------------------------------------

### Description

Gets information on the item's schematic and microchip sockets.

### Params

-   **itemCrafting** **([Item](../Classes/Item.md))** - The item that
    the player is trying to craft.

### Return Value

-   **Table**
    -   **nSchematicId** **(Integer)** - The schematic's id number.
    -   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The id
        number of the tradeskill that can make this schematic.
    -   **strName** **(String)** - The name of the item made by this
        schematic.
    -   **tSockets** **(Array of Table)** - Information on each of the
        sockets in the schematic.
        -   **eType** **(Item.CodeEnumMicrochipType)** - The type of
            microchip that can be slotted in this socket.
        -   **nParent** **(Integer)** - The index of the socket that
            must be set before this one.
        -   **fRatio** **(Float)** - The modifier applied to the value
            of the microchip in this slot.
        -   **itemDefaultChip** **([Item](../Classes/Item.md))** - The
            microchip that was set in this slot by the game.
        -   **itemCurrentChip** **([Item](../Classes/Item.md))** - The
            microchip currently in this slot.
        -   **bIsChangeable** **(Boolean)** - Whether the microchip set
            in this slot is locked or not.
        -   **nThreshold** **(Integer)** - The threshold value for this
            microchip slot.
    -   **itemOutput** **([Item](../Classes/Item.md))** - The item that
        will be created by this schematic.

------------------------------------------------------------------------

`Function`

GetPreviewInfo(nSchematicId, tCrafting)
---------------------------------------

### Description

Gets information to draw a preview of the item that will be created by
the specified schematic.

### Params

-   **nSchematicId** **(Integer)** - The id number for the schematic
    that we want to preview.
-   **tCrafting** **(Table)** - The parameters representing the player's
    chooses while crafting.
    -   **nApSpSplitDelta** **(Integer)** - The number of Ap/Sp
        increments to use when calculating the split. A positive number
        will make the item more support based.
    -   **itemPowerCore** **([Item](../Classes/Item.md))** - The item
        to use as the power core. This must be a valid power core for
        the item.
    -   **arStats** **(Array of Table)** - An array representing the
        player's crafting chooses per stat.
        -   **nChargeDelta** **(Integer)** - A number representing the
            number of charge increments to adjust the budget of the stat
            by.
        -   **eProperty** **(Unit.CodeEnumProperties)** - The property
            selected for this stat during crafting.

### Return Value

-   **[Item](../Classes/Item.md)** - The expected resulting item based
    on the provided parameters. If nSchematicId is also the current
    crafting schematic then the this result be more complete.

------------------------------------------------------------------------

`Function`

GetPropertyChipType() (Deprecated)
----------------------------------

------------------------------------------------------------------------

`Function`

GetRelearnCooldown()
--------------------

### Description

Gets the amount of time (in milliseconds) before the player can swap
their tradeskills.

### Return Value

-   **Integer** - The amount of time (in milliseconds) before the player
    can swap their tradeskills again.

------------------------------------------------------------------------

`Function`

GetRelearnCost(eTradeskillId)
-----------------------------

### Description

The amount of currency the player will have to spend to swap one of
their tradeskills with another.

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The id of
    the tradeskill that the player wants to learn.

### Return Value

-   **[Money](../Classes/Money.md)** - The price to swap tradeskills.

------------------------------------------------------------------------

`Function`

GetRunecraftingLevels()
-----------------------

------------------------------------------------------------------------

`Function`

GetRunecraftingPropertyIds()
----------------------------

------------------------------------------------------------------------

`Function`

GetRunecraftingSchematicFilters()
---------------------------------

------------------------------------------------------------------------

`Function`

GetRunecraftingSchematicList()
------------------------------

------------------------------------------------------------------------

`Function`

GetRuneSets()
-------------

------------------------------------------------------------------------

`Function`

GetRuneSetSchematicFilters()
----------------------------

------------------------------------------------------------------------

`Function`

GetRuneSetSchematicList()
-------------------------

------------------------------------------------------------------------

`Function`

GetSchematicCraftableCount(idSchematic) (Deprecated)
----------------------------------------------------

### Description

Gets the number of times a specified schematic can be crafted based on
the items in the player's inventory, supply satchel, and bank.

### Params

-   **idSchematic** **(Integer)** - The id number of the schematic.

### Return Value

-   **Integer** - The number of times the schematic can be created based
    on the items in the player's inventory, supply satchel, and bank.

------------------------------------------------------------------------

`Function`

GetSchematicInfo(idSchematic)
-----------------------------

### Description

Gets information on a specific schematic.

### Params

-   **idSchematic** **(Integer)** - The id number of the schematic that
    the function will look at.

### Return Value

-   **Table** - A table containing detailed information on the specified
    schematic, including information on any sub-schematics the schematic
    may have.
    -   **nSchematicId** **(Integer)** - The schematic's id number.
    -   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The id
        number of the tradeskill that uses the schematic.
    -   **eTier** **(CraftingLib.CodeEnumTradeskillTier)** - The
        tradeskill tier that the schematic belongs to.
    -   **strName** **(String)** - The name of the item created by the
        schematic.
    -   **fVectorX** **(Float)** - The x distance from the center of the
        coordinate crafting map that this schematic can be found. This
        is only useful for sub-schematics.
    -   **fVectorY** **(Float)** - The y distance from the center of the
        coordinate crafting map that this schematic can be found. This
        is only useful for sub-schematics.
    -   **fRadius** **(Float)** - The radius of the schematic on the
        coordinate crafting grid. This is only useful for
        sub-schematics.
    -   **nParentSchematicId** **(Integer)** - The id number for this
        schematic's parent schematic. This is only useful for
        sub-schematics.
    -   **itemOutput** **([Item](../Classes/Item.md))** - The item that
        is made if this schematic is successfully crafted.
    -   **achSource** **([Achievement](../Classes/Achievement.md))** -
        The achievement (read Tech Tree node) that unlocks this
        schematic.
    -   **achTier** **([Achievement](../Classes/Achievement.md))** - If
        the schematic is automatically learned, this variable contains
        the achievement for the tradeskill tier that the schematic
        belongs to.
    -   **nCraftXp** **(Integer)** - The amount of tradeskill XP the
        player gains when they successfully craft this schematic.
    -   **nFailXp** **(Integer)** - The amount of XP the player gains if
        their crafting attempt fails.
    -   **nLearnXp** **(Integer)**
    -   **bIsKnown** **(Boolean)** - Whether the player already knows
        the schematic or not.
    -   **bIsOneUse** **(Boolean)** - Whether the schematic is a
        one-time use schematic or not.
    -   **bIsAutoCraft** **(Boolean)** - Whether the schematic can be
        automatically crafted without doing coordinate / circuit board
        crafting.
    -   **bIsAutoLearn** **(Boolean)** - Whether the player
        automatically learns the schematic upon reaching the appropriate
        tradeskill tier or not.
    -   **nCraftAtOnceMax** **(Integer)** - The number of times the
        player can craft the schematic in one attempt. This variable is
        depricated.
    -   **arMaterials** **(Array of Table)** - Information on the
        materials needed to craft this schematic.
        -   **nAmount** **(Integer)** - The number of this particular
            item needed to craft this schematic.
        -   **itemMaterial** **([Item](../Classes/Item.md))** - An item
            needed to craft this schematic.
    -   **nCreateCount** **(Integer)** - The number of items created
        when the player crafts the schematic.
    -   **nMaxAdditives** **(Integer)** - The number of additives that
        can be applied to the schematic per crafting attempt.
    -   **tSubRecipes** **(Array of Table)** - An array that contains
        info on each of the sub-schematics associated with this
        schematic.
        -   **nSchematicId** **(Integer)** - The id number of the
            sub-schematic.
        -   **strName** **(String)** - The name of this sub-schematic.
        -   **bIsKnown** **(Boolean)** - Whether the player has learned
            this sub-schematic or not.
        -   **fDiscoveryAngle** **(Float)** - The angle of the starting
            edge of a discoverable area, in degrees.
        -   **fDiscoveryDistanceMin** **(Float)** - The distance from
            the center of the coordinate crafting grid to the closest
            point in the discoverable area.
        -   **fDiscoveryDistanceMax** **(Float)** - The distance from
            the center of the coordinate crafting grid to the furthest
            point in a discoverable area.
        -   **bIsUndiscovered** **(Boolean)** - If the player has not
            discovered the sub-schematic, this will be true. Otherwise,
            it will be false.
        -   **fVectorX** **(Float)** - The sub-schematic's X position on
            the coordinate crafting grid.
        -   **fVectorY** **(Float)** - The sub-schematic's Y position on
            the coordinate crafting grid.
        -   **fRadius** **(Float)** - The radius of the sub schematic on
            the coordinate crafting grid.
        -   **itemOutput** **([Item](../Classes/Item.md))** - The item
            created by the sub-schematic.
        -   **nCount** **(Integer)** - The number of items created by
            this sub schematic.
    -   **arStats** **(Array of Table)** - An array that contains infor
        on each stat associated with this circuit board schematic.
        -   **nRatio** **(Float)** - Percentage of the budget normally
            spent on this stat.
        -   **eItemStatType** **(CraftingLib.CodeEnumItemStatType)** -
            The type of stat.
        -   **eProperty** **(Unit.CodeEnumProperties)** - The property
            this stat provides. Provided for stat types of UnitProperty.
        -   **arCraftingGroups** **(Array of
            CraftingLib.CodeEnumItemCraftingGroupFlag)** - The list of
            groups that this schematic supports. Provided for
            UnlockedGroup type stats.
    -   **monMaxCraftingCost** **([Money](../Classes/Money.md))** - If
        the schematic has a crafting cost then this will be the maximum
        crafting cost.

------------------------------------------------------------------------

`Function`

GetSchematicList(eTradeskillId, nItemCategory, eTier, bShowUnknown)
-------------------------------------------------------------------

### Description

Gets a list of schematics that meet the requirements that are passed
into this function.

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The
    function will return the schematics that the player knows for this
    tradeskill.
-   **nItemCategory** **(Integer)** - The function will only return
    schematics that create items that fall under this category.
-   **eTier** **(CraftingLib.CodeEnumTradeskillTier)** - The function
    will return schematics that belong to this tradeskill tier.
-   **bShowUnknown** **(Boolean)** - Whether the function should return
    schematics that the player has not unlocked or not.

### Return Value

-   **Array of Table** - An array that contains info on each of the
    schematics that meet the requirements passed into the function.
    -   **nSchematicId** **(Integer)** - The schematic's id number.
    -   **strName** **(String)** - The name of the schematic.
    -   **eItemType** **(Item.CodeEnumItemType)** - The type of the item
        that is created by the schematic.
    -   **eTier** **(CraftingLib.CodeEnumTradeskillTier)** - The
        tradeskill tier that the schematic belongs to.
    -   **bIsKnown** **(Boolean)** - Whether the player has learned the
        schematic or not.
    -   **bIsOneUse** **(Boolean)** - Whether the schematic can only be
        used once or not.
    -   **strItemTypeName** **(String)** - The item's type, in string
        form.
    -   **tSubRecipes** **(Array of Table)** - An array that contains
        info on this schematic's sub-schematics.
        -   **nSchematicId** **(Integer)** - The id number for the
            sub-schematic.
        -   **strName** **(String)** - The name of the schematic.
        -   **bIsKnown** **(Boolean)** - Whether the player has learned
            the sub-schematic or not.

------------------------------------------------------------------------

`Function`

GetTierForAchievementCategory(idCategory)
-----------------------------------------

### Description

Gets the tradeskill tier that matches the achievement category that is
passed in.

### Params

-   **idCategory** **(Integer)** - The id for the achievement category
    that the function will match to a tradeskill tier.

### Return Value

-   **CraftingLib.CodeEnumTradeskillTier** - The tier that corresponds
    with the achievement category that was passed in.

------------------------------------------------------------------------

`Function`

GetTradeskillInfo(eTradeskillId)
--------------------------------

### Description

Returns a table with info about the chosen tradeskill

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The id for
    the tradeskill that the function will return info on.

### Return Value

-   **Table** - Detailed information on the tradeskill, including its
    description, XP requirements, requirements to relearn, and talents.
    -   **strName** **(String)** - The tradeskill's name.
    -   **strDescription** **(String)** - A description of the
        tradeskill.
    -   **nXpMax** **(Integer)** - The maximum amount of XP the player
        can earn for this tradeskill.
    -   **nTierMax** **(Integer)** - The number of tiers the tradeskill
        has.
    -   **bIsHobby** **(Boolean)** - Whether the tradeskill is a hobby
        or not. The only hobby currently in game is Cooking.
    -   **bIsAutoLearn** **(Boolean)** - Whether the tradeskill is
        automatically learned by the player at a certain level or not.
    -   **bIsHarvesting** **(Boolean)** - Whether the tradeskill is a
        harvesting tradeskill or not.
    -   **bIsCircuitBoardCrafting** **(Boolean)** - Whether the
        tradeskill's schematics use Circuit Board Crafting or not.
    -   **bIsCoordinateCrafting** **(Boolean)** - Whether the
        tradeskill's schematics use Coordinate Crafting or not.
    -   **tXpTiers** **(Array of Integer)** - An array that contains the
        amount of XP required to reach each tier of the tradeskill.
    -   **tAxisNames** **(Array of String)** - The names of the
        directions in the coordinate crafting grid for this tradeskill.
    -   **bIsActive** **(Boolean)** - Whether the player currently knows
        the tradeskill or not.
    -   **nXP** **(Integer)** - The amount of XP the player has earned
        for this tradeskill.
    -   **eTier** **(CraftingLib.CodeEnumTradeskillTier)** - The tier
        that the player has reached in the tradeskill.
    -   **nXpForTier** **(Integer)** - The amount of XP the player has
        earned while in the current tier.
    -   **nXpForNextTier** **(Integer)** - The amount of XP the player
        needs to reach their next tradeskill tier.
    -   **nTalentPoints** **(Integer)** - The number of talent points
        the player has unlocked.
    -   **monRelearnCost** **([Money](../Classes/Money.md))** - The
        amount and type of currency needed to relearn this tradeskill
    -   **nRelearnCooldownDays** **(Integer)** - The number of days
        until the player can relearn this tradeskill.
    -   **tTalentTiers** **(Array of Table)** - Information on each tier
        of talents for this tradeskill.
        -   **Array of Table** - These tables have no name. They are
            indexed by sequential numbers, starting at 1.
            -   **nId** **(Integer)** - The id number of the talent.
            -   **bIsActive** **(Boolean)** - Whether the player has
                activated this talent or not.
        -   **nId** **(Integer)** - The talent tier's id.
        -   **nPointsNeeded** **(Integer)** - The number of talent
            points that are needed to unlock this tier of talents.

------------------------------------------------------------------------

`Function`

GetTradeskillTalentRespecCost(eTradeskillId)
--------------------------------------------

### Description

Gets the amount and type of currency needed to reset the tradeskill's
talents.

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The
    function will check the talent respec cost for this tradeskill.

### Return Value

-   **[Money](../Classes/Money.md)** - The type and amount of currency
    needed to reset the tradeskill's talents.

------------------------------------------------------------------------

`Function`

GetTradeskillTalents(eTradeskillId, bDebugPrint)
------------------------------------------------

### Description

Gets a list of all the talents for a particular tradeskill.

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The
    function will get the talents for the tradeskill with this ID.
-   **bDebugPrint** **(Boolean)** - If this is set to true, then the
    player will see debug information in their chat log.

### Return Value

-   **Array of Table** - Information on each of the talent tiers for the
    tradeskill that was passed in to this function.
    -   **nPointsRequired** **(Integer)** - The number of points
        required to reach this talent tier.
    -   **tTalents** **(Array of Table)** - Information on each talent
        in this tier.
        -   **nTalentId** **(Integer)** - The id number for the talent.
        -   **bActive** **(Boolean)** - Whether the player has activated
            this talent or not.
        -   **strIcon** **(String)** - The name of the icon that should
            be displayed for the talent.
        -   **strName** **(String)** - The talent's name.
        -   **strTooltip** **(String)** - The tooltip that should be
            displayed for the talent.

### Usage/Example

```lua
    If bDebugPrint is set to true, each talent tier for the tradeskill will be listed in chat in sequential order.  The format for each line is:
    <Number of points needed to reach this talent tier>: <ID numbers for each talent in this tier>

    Numbers with a * next to it are tiers that the player has reached, or talents that they have selected, depending on what type of number it is next to.
```

------------------------------------------------------------------------

`Function`

GetTradeskillTierXp(eTradeskillId, eTradeskillTier)
---------------------------------------------------

### Description

Gets the amount of XP required to reach a specific tradeskill tier.

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The id
    number of the Tradeskill that this function query.
-   **eTradeskillTier** **(CraftingLib.CodeEnumTradeskillTier)** - The
    function will return the XP amount required to reach this tier.

### Return Value

-   **Integer** - The amount of XP required to reach the tradeskill /
    tier combination that was passed into the function.

------------------------------------------------------------------------

`Function`

GetUniversalSchematicsOwned()
-----------------------------

------------------------------------------------------------------------

`Function`

GetValidRuneItems(itemSelected, nSlot)
--------------------------------------

### Description

Gets a list of all of the valid runes for a specific rune slot. This
list filters based on slot type and removes duplicate runes.

### Params

-   **itemSelected** **([Item](../Classes/Item.md))** - The function
    will return the valid runes for this item.
-   **nSlot** **(Integer)** - The function will return all of the valid
    runes for the rune slot at this index.

### Return Value

-   **Array of [Item](../Classes/Item.md)** - An array of runes that
    can be set to the specified rune slot.

------------------------------------------------------------------------

`Function`

GetValidSocketItems(idSchematic, nSocketIdx) (Deprecated)
---------------------------------------------------------

### Description

Gets a list of microchips that are valid for a specific socket in a
schematic.

### Params

-   **idSchematic** **(Integer)** - The function will use the schematic
    with this id, in combination with the socket index, to get the list
    of valid items that can be added to the socket.
-   **nSocketIdx** **(Integer)** - The function will get a list of items
    that can be added to this socket.

### Return Value

-   **Table** - A table that contains an array with every microchip in
    it.
    -   **arSkill** **(Array of [Item](../Classes/Item.md))** - An
        array that contains all the microchips available.

------------------------------------------------------------------------

`Function`

InstallRuneIntoSlot(itemSource, tInstalledRunes)
------------------------------------------------

### Description

Attempts to update the runes that should be installed on an item.

### Params

-   **itemSource** **([Item](../Classes/Item.md))** - The item that the
    rune will be installed in.
-   **tInstalledRunes** **(Array of Integer)** - An array of item ids
    for runes that should be installed on the item after the operation
    is complete.

### Usage/Example

```lua
    If the operation is successful, the ItemModified event should fire.
```

------------------------------------------------------------------------

`Function`

IsAtCraftingStation()
---------------------

### Description

Checks if the player is within range of a crafting station.

### Return Value

-   **Boolean** - Determines whether the player is within range of a
    crafting station or not.

------------------------------------------------------------------------

`Function`

IsAtEngravingStation()
----------------------

------------------------------------------------------------------------

`Function`

IsAtMasterCraftsman()
---------------------

------------------------------------------------------------------------

`Function`

kfCoordinateBonusLoyaltyRadius() (Deprecated)
---------------------------------------------

------------------------------------------------------------------------

`Function`

LearnTradeskill(eTradeskillId, eDroppedTradeskillId)
----------------------------------------------------

### Description

Grants the character the chosen tradeskill. If the character is already
at the maximum number of tradeskills allowed, this function also drops a
chosen tradeskill.

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The id of
    the Tradeskill that the player will learn.
-   **eDroppedTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The
    id of the tradeskill that the player wants to drop in order to learn
    the new one.

### Usage/Example

```lua
    Fires the Tradeskills_Learned event when successful.
```

------------------------------------------------------------------------

`Function`

PickTradeskillTalent(eTradeskillId, nTalentTier, idTalent)
----------------------------------------------------------

### Description

Attempts to activate the specified talent.

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The id of
    the tradeskill that the talent belongs to.
-   **nTalentTier** **(Integer)** - The talent tier that the talent
    belongs to.
-   **idTalent** **(Integer)** - The id number for the talent that was
    chosen.

### Usage/Example

```lua
    If the talent is successfully activated, the TalentsChanged event will fire.

    Note: Only one talent can be selected per tier.  If one is already selected in this tier,
```

------------------------------------------------------------------------

`Function`

RerollRuneSlot(itemSource, nSlotIdx) (Deprecated)
-------------------------------------------------

### Description

Attempts to change a rune slot to a different type.

### Params

-   **itemSource** **([Item](../Classes/Item.md))** - The item that
    contains the rune slot that the function will attempt to reroll.
-   **nSlotIdx** **(Integer)** - The index of the rune slot that the
    function will attempt to reroll.

### Usage/Example

```lua
    If this function is successful, the ItemModified event will fire.
```

------------------------------------------------------------------------

`Function`

ResetTradeskillTalents(eTradeskillId)
-------------------------------------

### Description

Attempts to reset the talents that are set for the specified tradeskill.

### Params

-   **eTradeskillId** **(CraftingLib.CodeEnumTradeskill)** - The
    function will attempt to reset the talents of the tradeskill with
    this id.

### Usage/Example

```lua
    No event is fired if this function is successful.  Instead, CraftingLib.GetTradeskillTalents should return a talent list where no talents are set.
```

------------------------------------------------------------------------

`Function`

ShowTradeskillTutorial()
------------------------

### Description

Starts up the tutorial for tradeskills if tutorials are not disabled and
the tutorial is not flagged as "seen".

### Usage/Example

```lua
    This will fire the ShowTutorial event if the player has not disabled tutorials and the tradeskill tutorial is not flagged as "seen".  Otherwise, nothing will happen.
```

------------------------------------------------------------------------

`Function`

UnlockRuneSlot(itemSource, nSlotIdx) (Deprecated)
-------------------------------------------------

### Description

Attempts to unlock a rune slot on an item.

### Params

-   **itemSource** **([Item](../Classes/Item.md))** - The function will
    attempt to unlock a rune slot that belongs to this item.
-   **nSlotIdx** **(Integer)** - The index of the rune slot that the
    function will attempt to unlock.

### Usage/Example

```lua
    Fires the ItemModified event if the slot is successfully unlocked.
```

------------------------------------------------------------------------

`Function`

ValidateSocketItem(idSchematic, nSocketIdx, idInventory) (Deprecated)
---------------------------------------------------------------------

### Params

-   **idSchematic** **(Integer)** - The id for the schematic that the
    socket belongs to.
-   **nSocketIdx** **(Integer)** - The index of the socket that the
    function will validate.
-   **idInventory** **(Integer)** - The id number for the inventory slot
    that this item is in.
