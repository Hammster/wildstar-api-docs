ChatSystemLib
=============

------------------------------------------------------------------------

`Function`

Command(strCommand)
-------------------

### Description

Processes the slash command that is sent through the function.

### Params

-   **strCommand** **(String)** - The command that the chat system will
    process, along with any parameters required by the command.

### Remarks

This function will process both commands that are built into the game
and commands that are registered using Apollo.RegisterSlashCommand.

------------------------------------------------------------------------

`Function`

GetChannels()
-------------

### Description

Gets a list of channels that the player is in.

### Return Value

-   **Array of [ChatChannel](../Classes/ChatChannel.md)** - An array of
    ChatChannels that the player is currently in.

------------------------------------------------------------------------

`Function`

GetCommands()
-------------

### Description

Gets a list of commands that are available to the player.

### Return Value

-   **Array of String** - An array that contains the names of all of the
    commands that are available to the player.

### Remarks

The command list contains both game commands and any command registered
via Apollo.RegisterSlashCommand

------------------------------------------------------------------------

`Function`

GetEmotes()
-----------

### Description

Gets a list of all of the emote commands available to the player.

### Return Value

-   **Array of String** - An array of emote commands that the player can
    use.

------------------------------------------------------------------------

`Function`

JoinChannel(eChannel, strChannelName, strPassword, nOrder)
----------------------------------------------------------

### Description

Attempts to join the specified channel.

### Params

-   **eChannel** **(Integer)** - The channel that the player wants to
    join. This value lines up with the ChatSystemLib.ChatChannel set of
    constants and is only used if the player is trying to join a channel
    that was set up by the game.
-   **strChannelName** **(String)** - The name of the custom channel
    that the player is trying to join.
-   **strPassword** **(String)** - The password that is required to join
    the chat channel.
-   **nOrder** **(Integer)** - The channel number assigned to the new
    channel. This will assign it to the next available channel number by
    default.

### Usage/Example

```lua
    If the player is attempting to join a non-custom channel, then eChannel is the only parameter that should be sent.  Otherwise, everything except eChannel should be used.
```

------------------------------------------------------------------------

`Function`

PostOnChannel(eChannelId, strMessage, strSenderName, unitSource, bBubble)
-------------------------------------------------------------------------

### Description

Posts a text message to a specific chat channel.

### Params

-   **eChannelId** **(Integer)** - The channel that the message will be
    posted to. This value lines up with the ChatSystemLib.ChatChannel
    set of constants.
-   **strMessage** **(String)** - The message that will be sent via the
    channel.
-   **strSenderName** **(String)** - The name of the player or NPC that
    the channel will say that the message came from.
-   **unitSource** **([Unit](../Classes/Unit.md))** - The unit that the
    message came from.
-   **bBubble** **(Boolean)** - Whether the unit should show a speech
    bubble or not.

------------------------------------------------------------------------

`Function`

PrepareInfractionReport(idChatLine)
-----------------------------------

### Description

Creates an IncidentReport based on a specified chat line.

### Params

-   **idChatLine** **(Integer)** - The id number for the chat line that
    the report will be created from.

### Return Value

-   **rptChat** - An IncidentReport that is populated with information
    pulled from the specified chat line.

------------------------------------------------------------------------

`Function`

SplitInput(strInput)
--------------------

### Description

Checks a string for a slash command and divides it into the command and
its arguments.

### Params

-   **strInput** **(String)** - The string that the function will split.

### Return Value

-   **Table**
    -   **chatCommand**
        **([ChatChannel](../Classes/ChatChannel.md))** - The channel
        that the command was sent over.
    -   **bValidCommand** **(Boolean)** - Whether the command is
        recognized by the game or not.
    -   **strCommand** **(String)** - The slash command portion of the
        string.
    -   **strMessage** **(String)** - The arguments that were sent along
        with the slash command.
