ICCommLib
=========

### Constants

- knInvalidICCommMessageId

------------------------------------------------------------------------

`Enum`

CodeEnumICCommChannelType
-------------------------

-   **Global** (**Integer**)
-   **Group** (**Integer**)
-   **Guild** (**Integer**)

CodeEnumICCommJoinResult
------------------------

-   **TooManyChannels** (**Integer**)
-   **NoGuild** (**Integer**)
-   **NoGroup** (**Integer**)
-   **BadName** (**Integer**)
-   **Join** (**Integer**)
-   **Left** (**Integer**)
-   **MissingEntitlement** (**Integer**)

CodeEnumICCommMessageResult
---------------------------

-   **Sent** (**Integer**)
-   **Throttled** (**Integer**)
-   **NotInChannel** (**Integer**)
-   **InvalidText** (**Integer**)
-   **MissingEntitlement** (**Integer**)

------------------------------------------------------------------------

`Function`

JoinChannel(strChannel, eChannelType, guildContext)
---------------------------------------------------

### Description

Attempts to join a channel with then given name of the provided type. If the type is Guild then the guild userdata must also be passed in for context.

### Params

-   **strChannel** **(String)** - name of requested channel.
-   **eChannelType** **(Integer)** - Type of channel to create, CodeEnumICCommChannelType.
-   **guildContext** **([Guild](../Classes/Guild.md))** - guild context to be passed in when the channel type is Guild.

### Return Value

-   **[ICComm](../Classes/ICComm.md)** - An instance of the ICComm channel.

------------------------------------------------------------------------

`Function`

GetUploadCapacityByType(eChannelType)
-------------------------------------

### Description

Gets the bits/second upload capacity for given eChannelType or self context. A limit can be surpassed up to 50KB for the single message that surpasses the limit but it will take twice as long for the throttle to be removed.

### Params

-   **eChannelType** **(Integer)** - Type of channel to create, CodeEnumICCommChannelType.

### Return Value

-   **Integer** - Bits per second.

-------------------------------------------------------------------

`Function`

GetDownloadCapacityByType(eChannelType)
---------------------------------------

### Description

Gets the bits/second download capacity for given eChannelType or self context.

### Params

-   **eChannelType** **(Integer)** - Type of channel to create, CodeEnumICCommChannelType.

### Return Value

-   **Integer** - Bits per second.

-------------------------------------------------------------------
