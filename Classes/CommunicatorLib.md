CommunicatorLib
===============

### Description

A library that provides addons a way to manipulate communicator messages
sent by NPCs.

------------------------------------------------------------------------

`Event`

Communicator\_EndIncoming
-------------------------

### Description

Fires when an incoming communicator times out and becomes a "missed
call"

------------------------------------------------------------------------

`Event`

Communicator\_ShowQuestMsg
--------------------------

### Params

-   **idMsg** **(Integer)** - The id number for the message.
-   **idCreature** **(Integer)** - The id number for the NPC that sent
    the communicator message.
-   **queShown** **([Quest](../Classes/Quest.md))** - The quest that
    the message will offer the player.
-   **strText** **(String)** - The quest text that the message will
    show.

------------------------------------------------------------------------

`Event`

Communicator\_ShowSpamMsg
-------------------------

### Description

Fires if a communicator message is sent to the player but does not have
a valid Quest tied to it.

### Params

-   **idMsg** **(Integer)** - The id number of the communicator message.
-   **idCreature** **(Integer)** - The id number of the creature that
    sent the message.
-   **strText** **(String)** - The text that should be shown in the
    message.
-   **bPriorty** **(Boolean)** - Whether the message should have
    priority over other messages.

------------------------------------------------------------------------

`Event`

Communicator\_SpamVOEnded
-------------------------

### Description

Fires when a communicator's voice over ends.

------------------------------------------------------------------------

`Event`

Communicator\_UpdateCallback
----------------------------

### Description

Fires whenever a communicator message gets updated in response to a
player abandoning, botching, or completing a quest.

### Params

-   **bHasCallback** **(Boolean)** - Whether the player gets an
    immediate communicator message or not.
-   **bRedeemsQuest** **(Boolean)** - Whether the callback allows the
    player to turn in a quest or not.

------------------------------------------------------------------------

`Function`

CallbackLastContact()
---------------------

### Description

Begin a communicator message with the NPC that sent the most recent
message.

------------------------------------------------------------------------

`Function`

CallContact(queCalling)
-----------------------

### Description

Begin the communicator message with the NPC associated with the
specified quest.

### Params

-   **queCalling** **([Quest](../Classes/Quest.md))** - The quest that
    the player is trying to accept or turn in via the communicator.

------------------------------------------------------------------------

`Function`

Close()
-------

### Description

Closes the communicator message that is currently open.

------------------------------------------------------------------------

`Function`

CommunicatorBackground\_TheEntity() (Deprecated)
------------------------------------------------

------------------------------------------------------------------------

`Function`

GetMessageLayoutForQuest(queSource)
-----------------------------------

### Description

Gets information regarding the layout of the portrait portion of a
communicator message that is tied to a quest.

### Params

-   **queSource** **([Quest](../Classes/Quest.md))** - The quest that
    the communicator message is tied to.

### Return Value

-   **Table**
    -   **ePortraitPlacement** **(Integer)** - The location on the
        window that the portrait is assigned to. This value lines up
        with the CommunicatorLib.CommunicatorPortraitPlacement set of
        constants.
    -   **eOverlay** **(Integer)** - The static overlay that should be
        placed over the portrait. This lines up with the
        CommunicatorLib.CommunicatorOverlay set of constants.
    -   **eBackground** **(Integer)** - The background that should be
        used with the portrait. This value lines up with the
        CommunicatorLib.CommunicatorBackground set of constants.

------------------------------------------------------------------------

`Function`

GetMessageLayoutForSpam(idMessage)
----------------------------------

### Description

Gets information regarding how the background on a spam message should
be layed out.

### Params

-   **idMessage** **(Integer)** - The id number for the spam message
    being queried.

### Return Value

-   **Table**
    -   **fDuration** **(Float)** - How long the message will remain on
        the screen, in seconds.
    -   **ePortraitPlacement** **(Integer)** - Where the character
        portrait should appear on the communicator window. This value
        corresponds with the
        CommunicatorLib.CommunicatorPortraitPlacement set of constants.
    -   **eOverlay** **(Integer)** - Indicated which overlay should be
        drawn over the portrait. This value corresponds with the
        CommunicatorLib.CommunicatorOverlay set of constants.
    -   **eBackground** **(Integer)** - Indicated which background
        should be used with the portrait. This value corresponds with
        the CommunicatorLib.CommunicatorBackground set of constants.

------------------------------------------------------------------------

`Function`

GetPathMissionDelivered(idMessage)
----------------------------------

### Description

Gets the Path Mission that the player unlocks via the communicator
message.

### Params

-   **idMessage** **(Integer)** - The id number for the communicator
    message.

### Return Value

-   **[PathMission](../Classes/PathMission.md)** - The Path Mission
    that is unlocked for the player via the communicator message with
    the specified id.

------------------------------------------------------------------------

`Function`

IgnoreCallback()
----------------

### Description

Cancel an incoming communicator message.

------------------------------------------------------------------------

`Function`

IsVisible()
-----------

### Description

Determines whether or not a communicator message is currently being
displayed.

### Return Value

-   **Boolean** - If the communicator message is being displayed, this
    value will be true.

------------------------------------------------------------------------

`Function`

PlaySpamVo(idMessage)
---------------------

### Description

Plays the voice over for the specified communicator message.

### Params

-   **idMessage** **(Integer)** - The id number for the communicator
    message that should play its Voice Over.

### Return Value

-   **Boolean** - Whether there was actually a voice over to play or
    not.

------------------------------------------------------------------------

`Function`

QueueMessage()
--------------

------------------------------------------------------------------------

`Function`

QueueNextCall(idMessage)
------------------------

### Description

Add the specified message to the message queue.

### Params

-   **idMessage** **(Integer)** - The id number of the message that will
    be thrown on the queue.
