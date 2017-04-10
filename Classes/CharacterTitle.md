CharacterTitle
==============

### Prefix: title

### Description

These are the titles that the character can set for themselves. These do
not include guild tags.

------------------------------------------------------------------------

`Function`

CanUseTitle()
-------------

### Description

Determines whether or not the player can use the specified title.

### Return Value

-   **Boolean** - Whether the player can use the title or not.

------------------------------------------------------------------------

`Function`

GetAvailableTitles()
--------------------

### Description

Gets a list of all of the titles that the player has unlocked.

### Return Value

-   **Array of [CharacterTitle](../Classes/CharacterTitle.md)** - An
    array of all of the titles that the player has unlocked.

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Determines whether a variable is a CharacterTitle or not.

### Params

-   **oVariable** **(Variable)** - The variable that the function will
    check.

### Return Value

-   **Boolean** - Whether the variable is a CharacterTitle or not.

------------------------------------------------------------------------

`Function`

IsActiveTitle(titleChecked)
---------------------------

### Description

Checks whether the a title is the one that the player has set as the
active title.

### Params

-   **titleChecked**
    **([CharacterTitle](../Classes/CharacterTitle.md))** - The function
    will check if this title is currently active.

### Return Value

-   **Boolean** - Whether the CharacterTitle is the active title.

------------------------------------------------------------------------

`Function`

SetTitle(titleActivated)
------------------------

### Description

Sends a request to the server to make a CharacterTitle the active title.

### Params

-   **titleActivated**
    **([CharacterTitle](../Classes/CharacterTitle.md))** - The title
    that the function will make active.

### Usage/Example

```lua
    If this is successful, the PlayerTitleChange event will be sent to the player.
```

------------------------------------------------------------------------

`Method`

\_\_eq(titleComparison) (Deprecated)
------------------------------------

### Description

Compares a CharacterTitle to the one that called this function to make
sure that they are equal.

### Params

-   **titleComparison**
    **([CharacterTitle](../Classes/CharacterTitle.md))** - The function
    will compare this CharacterTitle to the one that the function was
    called from.

### Return Value

-   **Boolean** - Whether the CharacterTitles were the same or not.

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

CharacterTitle's garbage collection function. This will delete the
CharacterTitle from memory.

------------------------------------------------------------------------

`Method`

CannotRemove()
--------------

### Description

Determines whether the player is able to remove this CharacterTitle.

### Return Value

-   **Boolean** - Whether the player is able to remove this
    CharacterTitle or not

### Remarks

This will very very rarely be true.

------------------------------------------------------------------------

`Method`

GetCategory()
-------------

### Description

Gets the category that the CharacterTitle falls under.

### Return Value

-   **String** - The CharacterTitle's category.

------------------------------------------------------------------------

`Method`

GetForUnit(unitChecked)
-----------------------

### Description

Checks what a unit's name would look like with the CharacterTitle.

### Params

-   **unitChecked** **([Unit](../Classes/Unit.md))** - The function
    will add the CharacterTitle to this unit's name.

### Return Value

-   **String** - The unit's name, if the CharacterTitle was applyed to
    it.

### Usage/Example

```lua
    If no unit is passed in, this will return a blank string.
```

------------------------------------------------------------------------

`Method`

GetLifetime()
-------------

### Description

Gets the amount of time, in milliseconds, that the title will be active
before it is removed from the player.

### Return Value

-   **Integer** - How long the title will remain active, in
    milliseconds.

### Usage/Example

```lua
    If this returns 0, the title will remain available to the player indefinitely.
```

------------------------------------------------------------------------

`Method`

GetSpell()
----------

### Description

Gets the spell that is granted to the player while the title is active.

### Return Value

-   **[Spell](../Classes/Spell.md)** - The spell that is granted to the
    player while the title is active.

### Usage/Example

```lua
    If there is no associated spell, this will return nil.
```

------------------------------------------------------------------------

`Method`

GetTitle()
----------

### Description

Gets the string that is added to the player's name while the title is
active.

### Return Value

-   **String** - The string that is added to the player's name when the
    title is active.
