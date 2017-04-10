ICCommLib (Deprecated)
======================

Table of Content
---------------- 

<!-- toc -->

------------------------------------------------------------------------

`Constant`
knInvalidICCommMessageId

`Enum`

CodeEnumICCommChannelType
-----------------------------

-   **Global**
-   **Group**
-   **Guild**

CodeEnumICCommJoinResult
-----------------------------

-   **TooManyChannels**
-   **NoGuild**
-   **NoGroup**
-   **BadName**
-   **Join**
-   **Left**
-   **MissingEntitlement**

CodeEnumICCommMessageResult
-----------------------------

-   **Sent**
-   **Throttled**
-   **NotInChannel**
-   **InvalidText**
-   **MissingEntitlement**

------------------------------------------------------------------------

`Function`

JoinChannel(strChannel, eChannelType, guildContext)
-------------------------------------------------------------------

### Description

Attempts to join a channel with then given name of the provided type. If the type is Guild then the guild userdata must also be passed in for context.

### Params

-   **strChannel** **(String)** - name of requested channel.
-   **eChannelType** **(Integer)** - Type of channel to create, CodeEnumICCommChannelType
-   **guildContext** **([Guild](../Classes/Guild.html))** - guild context to be passed in when the channel type is Guild
    
### Return Value

-   **[ICComm](../Classes/ICComm.html)** - An instance of the ICComm channel

------------------------------------------------------------------------

`Function`

GetUploadCapacityByType(eChannelType)

-------------------------------------------------------------------

`Function`

GetDownloadCapacityByType(eChannelType)

-------------------------------------------------------------------
