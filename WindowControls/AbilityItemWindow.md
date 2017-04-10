AbilityItemWindow
=================

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

AbilitySelected
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Method`

GetAbilityDescription()
-----------------------

### Description

Does a lua\_pushwstring of the ability's description from the tool tip
id, or "" if the ability is not found.

------------------------------------------------------------------------

`Method`

GetAbilityId()
--------------

### Description

Does a lua\_pushinteger of the caller's m\_iSpellId.

------------------------------------------------------------------------

`Method`

GetAbilityName()
----------------

### Description

Does a lua\_pushwstring of the ability's name from the name id, or "" if
the ability is not found.

------------------------------------------------------------------------

`Method`

GetAbilityTierId()
------------------

------------------------------------------------------------------------

`Method`

SetAbilityId(nSpellId)
----------------------

### Description

Sets the caller's ability id to nSpellId.

### Params

-   **nSpellId** **(Integer)** - (Default value: -1)

------------------------------------------------------------------------

`Method`

SetSelected(bSelected)
----------------------

### Description

Sets the caller's m\_bSelected boolean to bSelected.

### Params

-   **bSelected** **(Boolean)**
