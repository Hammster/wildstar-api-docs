DialogResponse
==============

### Prefix: dr

### Description

DialogResponses are the various options that the player can select when
conversing with NPCs and turning in quests.

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Determines whether a variable is a DialogResponse or not.

### Params

-   **oVariable** **(Variable)** - The object that the function will
    check.

### Return Value

-   **Boolean** - Whether the object is a dialog response or not.

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

Forces the garbage collector to be called on this variable.

------------------------------------------------------------------------

`Method`

GetQuestId()
------------

### Description

Gets the id of the quest associated with this dialog.

### Return Value

-   **Integer** - The id number of the quest associated with this dialog
    response.

------------------------------------------------------------------------

`Method`

GetRewardId()
-------------

### Description

Gets the id of the reward associated with this dialog response.

### Return Value

-   **Integer** - The id number of the reward associated with this
    response.

------------------------------------------------------------------------

`Method`

GetText()
---------

### Description

Gets the text for this DialogResponse.

### Return Value

-   **String** - The DialogResponse's text.

------------------------------------------------------------------------

`Method`

GetType()
---------

### Description

Gets the DialogResponse's type.

### Return Value

-   **Integer** - The response's type. This value corresponds with the
    DialogResponse.DialogResponseType enum.

------------------------------------------------------------------------

`Method`

GetUniqueId()
-------------

### Description

Gets the dialog's unique id number.

### Return Value

-   **Integer** - The dialog's unique id number.

------------------------------------------------------------------------

`Method`

Select()
--------

### Description

Tells the client that the player has chosen this DialogResponse
