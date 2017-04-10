ChatChannel (Deprecated)
========================

### Prefix: chan

### Description

One of the channels that chat messages can be sent to.

------------------------------------------------------------------------

`Function`

is(oVariable) (Deprecated)
--------------------------

### Description

Checks whether a variable is a ChatChannel or not.

### Params

-   **oVariable** **(Variable)** - The function will verify that this
    variable is a ChatChannel.

### Return Value

-   **Boolean** - Whether the variable is a ChatChannel or not.

------------------------------------------------------------------------

`Method`

\_\_eq(chanComparison) (Deprecated)
-----------------------------------

### Description

Checks whether a ChatChannel is equal to the ChatChannel that called
this function.

### Params

-   **chanComparison** **([ChatChannel](../Classes/ChatChannel.md))** -
    The ChatChannel that will be compared to the one that called this
    function.

### Return Value

-   **Boolean** - Whether the two ChatChannels are equal or not.

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

ChatChannel's garbage collection function. This will delete the
ChatChannel from memory.

------------------------------------------------------------------------

`Method`

CanLeave() (Deprecated)
-----------------------

### Description

Checks if the player is able to leave the ChatChannel.

### Return Value

-   **Boolean** - Whether the player is able to leave the ChatChannel or
    not.

------------------------------------------------------------------------

`Method`

CanSend() (Deprecated)
----------------------

### Description

Determines if the player is able to send messages on this ChatChannel.

### Return Value

-   **Boolean** - Whether the player is able to send chat messages on
    this ChatChannel or not.

------------------------------------------------------------------------

`Method`

GetAbbreviation() (Deprecated)
------------------------------

### Description

Gets an abbreviation for the ChatChannel that can be used in slash
commands to quickly select the channel.

### Return Value

-   **String** - The ChatChannel's abbreviation.

------------------------------------------------------------------------

`Method`

GetAlternate(nIndex) (Deprecated)
---------------------------------

### Description

Checks for alternate abbreviations for the ChatChannel.

### Params

-   **nIndex** **(Integer)** - The index of the alternate abbreviation
    for the ChatChannel.

### Return Value

-   **String** - The alternate abbreviation for the ChatChannel.

------------------------------------------------------------------------

`Method`

GetBans() (Deprecated)
----------------------

### Description

Gets a list of players who are banned in this ChatChannel.

### Return Value

-   **Array of Table** - An array of information about the players that
    have been banned from the channel.
    -   **strMemberName** **(String)** - The player's name.
    -   **bIsChannelOwner** **(Boolean)** - Whether the player owns the
        channel or not.
    -   **bIsModerator** **(Boolean)** - Whether the player is a
        moderator of the channel or not.
    -   **bIsMuted** **(Boolean)** - Whether the player is muted in the
        channel or not.

------------------------------------------------------------------------

`Method`

GetCommand() (Deprecated)
-------------------------

### Description

Gets the slash command used to select the ChatChannel.

### Return Value

-   **String** - The command used to select the ChatChannel.

------------------------------------------------------------------------

`Method`

GetData() (Deprecated)
----------------------

### Description

Gets the data that was added to the channel with SetData()

### Return Value

-   **Variable** - The data that was added to the ChatChannel with
    SetData.

------------------------------------------------------------------------

`Method`

GetMembers() (Deprecated)
-------------------------

### Description

Gets a list of players that are in the ChatChannel.

### Return Value

-   **Array of Table** - An array that contains information on all of
    the players that are in the ChatChannel.
    -   **strMemberName** **(String)** - The name of the player.
    -   **bIsChannelOwner** **(Boolean)** - Whether the player owns the
        channel.
    -   **bIsModerator** **(Boolean)** - Whether the player is a
        moderator of the channel.
    -   **bIsMuted** **(Boolean)** - Whether the character has been
        muted.

------------------------------------------------------------------------

`Method`

GetName() (Deprecated)
----------------------

### Description

Gets the ChatChannel's name.

### Return Value

-   **String** - The name of the ChatChannel.

------------------------------------------------------------------------

`Method`

GetProfanity() (Deprecated)
---------------------------

### Description

Checks whether the Profanity Filter is turned on for the ChatChannel.

### Return Value

-   **Boolean** - Whether the Profanity Filter is turned on for the
    ChatChannel.

------------------------------------------------------------------------

`Method`

GetType() (Deprecated)
----------------------

### Description

Gets the ChatChannel's id number.

### Return Value

-   **Integer** - The channel's id number.

------------------------------------------------------------------------

`Method`

IsCustom() (Deprecated)
-----------------------

### Description

Determines if the ChatChannel is a player made channel.

### Return Value

-   **Boolean** - Whether the ChatChannel is a player made channel or
    not.

------------------------------------------------------------------------

`Method`

IsModerator() (Deprecated)
--------------------------

### Description

Checks if the player is a moderator of the ChatChannel.

### Return Value

-   **Boolean** - Whether the player is a moderator of the ChatChannel.

------------------------------------------------------------------------

`Method`

IsMuted() (Deprecated)
----------------------

### Description

Determines if the player is muted in the ChatChannel.

### Return Value

-   **Boolean** - Whether the player is muted or not.

------------------------------------------------------------------------

`Method`

IsOwner() (Deprecated)
----------------------

### Description

Determines if the player owns the ChatChannel.

### Return Value

-   **Boolean** - Whether the player owns the ChatChannel.

------------------------------------------------------------------------

`Method`

Kick(strPlayerName) (Deprecated)
--------------------------------

### Description

Attempts to remove a player from the ChatChannel.

### Params

-   **strPlayerName** **(String)** - The name of the player that the
    function will attempt to remove from the ChatChannel.

### Usage/Example

```lua
    If this call is successful, players will receive the ChatAction event.
```

------------------------------------------------------------------------

`Method`

Leave() (Deprecated)
--------------------

### Description

Attempts to remove the player from the ChatChannel.

### Usage/Example

```lua
    If the attempt was successful, the player will receive the ChatLeave event.
```

------------------------------------------------------------------------

`Method`

PassOwner(strPlayerName) (Deprecated)
-------------------------------------

### Description

Attempts to make another player the owner of the ChatChannel.

### Params

-   **strPlayerName** **(String)** - The name of the player that the
    function will attempt to transfer ownership to.

### Usage/Example

```lua
    If ownership was successfully passed, the ChatAction event will fire.
```

------------------------------------------------------------------------

`Method`

Post(strMessage, strSenderName, unitSpeaker, bTextBubble) (Deprecated)
----------------------------------------------------------------------

### Description

Attempts to send a string to all members of the ChatChannel.

### Params

-   **strMessage** **(String)** - The message that will be sent through
    the ChatChannel.
-   **strSenderName** **(String)** - The name of the player that sent
    the message. This value defaults to an empty string.
-   **unitSpeaker** **([Unit](../Classes/Unit.md))** - The unit that
    entered the message.
-   **bTextBubble** **(Boolean)** - Whether a text bubble should be
    shown for this piece of text.

### Usage/Example

```lua
    If this function is successful, then players in the channel will receive the ChatMessage event.
```

------------------------------------------------------------------------

`Method`

RequestMembers() (Deprecated)
-----------------------------

### Description

Requests a list of the players in the ChatChannel.

### Usage/Example

```lua
    If this is successful, the player will receive the ChatList event.
```

------------------------------------------------------------------------

`Method`

Send(strMessage) (Deprecated)
-----------------------------

### Description

Sends a message over the ChatChannel.

### Params

-   **strMessage** **(String)** - The message that will be sent over the
    ChatChannel.

### Usage/Example

```lua
    Players in the ChatChannel will receive the ChatMessage event after this function has finished.
```

------------------------------------------------------------------------

`Method`

SetData(oVariable) (Deprecated)
-------------------------------

### Description

Saves data in the ChatChannel. This data can be accessed again by
calling the GetData function.

### Params

-   **oVariable** **(Variable)** - The data that will be tied to the
    ChatChannel.

------------------------------------------------------------------------

`Method`

SetModerator(strPlayerName, bMakeModerator) (Deprecated)
--------------------------------------------------------

### Description

Attempts to set a player's Moderator status in the ChatChannel.

### Params

-   **strPlayerName** **(String)** - The name of the player whose
    Moderator status will be updated by this function.
-   **bMakeModerator** **(Boolean)** - Whether the player's Moderator
    flag should be granted (true) or removed (false). This defaults to
    false if no value is passed in.

### Usage/Example

```lua
    If the player's Moderator status was successfully changed, the ChatAction event will be fired.
```

------------------------------------------------------------------------

`Method`

SetMute(strPlayerName, bMuted) (Deprecated)
-------------------------------------------

### Description

Attempts to set a player's Mute status for the ChatChannel.

### Params

-   **strPlayerName** **(String)** - The player whose Mute flag should
    be changed by the function.
-   **bMuted** **(Boolean)** - Whether the Mute flag should be added to
    the player (true) or removed (false). This defaults to false if no
    value is passed in.

### Usage/Example

```lua
    If this function is successful, the ChatAction event will be fired.
```

------------------------------------------------------------------------

`Method`

SetPassword(strPassword) (Deprecated)
-------------------------------------

### Description

Attempts to add a password to the ChatChannel or modify an existing one.

### Params

-   **strPassword** **(String)** - The ChatChannel's new password.

### Usage/Example

```lua
    If this is successful, the ChatAction event will be fired.
```

------------------------------------------------------------------------

`Method`

SetProfanity(bProfanityFilterOn) (Deprecated)
---------------------------------------------

### Description

Attempts to change the ChatChannel's Profanity Filter status.

### Params

-   **bProfanityFilterOn** **(Boolean)** - Whether the Profanity Filter
    should be turned on or off for the channel.
