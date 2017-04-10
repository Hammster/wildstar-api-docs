DialogSys
=========

### Description

Dialogs are the chat bubbles that appear when speaking with an NPC. They
can be used for accepting and turning in quests and other conversations
with NPCs. This library allows the player to get information on the
currently displayed dialog.

------------------------------------------------------------------------

`Function`

End()
-----

### Description

Cancels the current dialog.

------------------------------------------------------------------------

`Function`

GetCommCreatureId()
-------------------

### Description

Gets the id number of the NPC associated with the current dialog.

### Return Value

-   **Integer** - The id number of the NPC that is tied to the dialog.

------------------------------------------------------------------------

`Function`

GetNPC()
--------

### Description

Gets the unit associated with the dialog.

### Return Value

-   **[Unit](../Classes/Unit.md)** - The unit associated with the
    dialog.

------------------------------------------------------------------------

`Function`

GetNPCText(idQuest)
-------------------

### Description

Gets the string that contains the NPC's text. This will also play any VO
associated with this dialog.

### Params

-   **idQuest** **(Integer)** - The id number of the quest that the
    dialog is associated with.

### Return Value

-   **string** - The text that the dialog should show for the NPC.

------------------------------------------------------------------------

`Function`

GetResponses(idQuest)
---------------------

### Description

Gets a list of possible responses that the player can send.

### Params

-   **idQuest** **(Integer)** - The id number of the quest that is
    giving the player responses.

### Return Value

-   **Array of String** - The list of responses the player can select
    for the dialog.

------------------------------------------------------------------------

`Function`

GetResponseText()
-----------------

### Description

Gets the text that the player is responding to.

### Return Value

-   **String** - The text that the player's responses o

------------------------------------------------------------------------

`Function`

GetState()
----------

### Description

Gets the dialog's current state.

### Return Value

-   **Integer** - The dialog's current state. This value lines up with
    the DialogSys\_DialogState set of constants.

------------------------------------------------------------------------

`Function`

GetViewableQuest(idQuest)
-------------------------

### Description

Grabs the quest with the specified id if it is the one that the dialog
is using.

### Params

-   **idQuest** **(Integer)** - The id number of the quest that the
    function will try to match with any quest that the current dialog is
    displaying.

### Return Value

-   **[Quest](../Classes/Quest.md)** - The quest with the specified id.
    If the dialog was not showing a quest or was showing a quest with a
    different id, this will be nil.

------------------------------------------------------------------------

`Function`

IsItemQuestGiver()
------------------

### Description

Checks if the dialog was triggered by an item that is granting a quest.

### Return Value

-   **Boolean** - Whether the quest is granted by an item or not.
