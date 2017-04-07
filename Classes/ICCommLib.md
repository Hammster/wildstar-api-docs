ICCommLib (Deprecated)
======================

Table of Content
---------------- 

<!-- toc -->

------------------------------------------------------------------------

`Enum`

ICCommJoinResult (Deprecated)
-----------------------------

-   **NoGuild**
-   **BadName**
-   **Join**
-   **TooManyChannels**
-   **Left**
-   **NoGroup**
-   **MissingEntitlement**

------------------------------------------------------------------------

`Function`

Is(userData) (Deprecated)
-------------------------

### Description

Does a lua\_pushboolean if the same metatable is on the stack.

### Params

-   **userData** **(UserData)**

------------------------------------------------------------------------

`Function`

JoinChannel(strChannel, strFunction, nLuaEventHandler) (Deprecated)
-------------------------------------------------------------------

### Description

Runs JoinChannel with strChannel, strFunction, and nLuaEventHandler.

### Params

-   **strChannel** **(String)** - that gets prefixed with ICC.
-   **strFunction** **(String)**
-   **nLuaEventHandler** **(LuaTable)** - but the Id is immediately
    converted to an Integer

------------------------------------------------------------------------

`Method`

\_\_eq() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

SendMessage() (Deprecated)
--------------------------

------------------------------------------------------------------------

`Method`

SendPrivateMessage() (Deprecated)
---------------------------------

------------------------------------------------------------------------

`Method`

SetControlFunction() (Deprecated)
---------------------------------
