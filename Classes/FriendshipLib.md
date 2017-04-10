FriendshipLib
=============

### Description

A library that contains functions for interacting with the game's Friend
and Account Friend systems.

------------------------------------------------------------------------

`Function`

AccountAddByEmail(strAddress, strNote)
--------------------------------------

### Description

Attempts to send an account friend invite to the account that is
registered to the specified email address.

### Params

-   **strAddress** **(String)** - The email address associated with the
    account that the player wants to send the invite to.
-   **strNote** **(String)** - A note that will be sent to the player
    that receives the account friend invite.

------------------------------------------------------------------------

`Function`

AccountAddByUpgrade(idFriend, strNote)
--------------------------------------

### Description

Attempts to send an invitation to upgrade a Friend to an Account Friend.

### Params

-   **idFriend** **(Integer)** - The Friend id of the player that will
    receive the Account Friend Invite.
-   **strNote** **(String)** - A note that the person who receives the
    Account Friend invite will see in the invite.

------------------------------------------------------------------------

`Function`

AccountInviteMarkSeen()
-----------------------

### Description

Marks an account invite as "Seen" by the system.

### Remarks

This flag has no set use, however the UI tends to use it to inform the
player that they have pending invites.

------------------------------------------------------------------------

`Function`

AccountInviteRespond(idFriend, bAccepted)
-----------------------------------------

### Description

Sends a response to an Account Invite that the player has received.

### Params

-   **idFriend** **(Integer)** - The id of the friend invite that the
    player is responding to.
-   **bAccepted** **(Boolean)** - Whether the player accepted the invite
    or not.

------------------------------------------------------------------------

`Function`

AccountRemove(idFriend)
-----------------------

### Description

Removes the specified Account Friend from the player's friends' list

### Params

-   **idFriend** **(Integer)** - The Friend id of the Account Friend
    that the player wants to remove.

------------------------------------------------------------------------

`Function`

AddByGroupIndex(eType, nMemberIdx)
----------------------------------

### Description

Attempts to change the friendship status of a player in your current
group.

### Params

-   **eType** **(Integer)** - The friendship status that the player
    wants to add to the specified group member. This value lines up with
    the FriendshipLib.CharacterFriendshipType set of constants.
-   **nMemberIdx** **(Integer)** - The index of the player within the
    group.

### Usage/Example

```lua
    This will send an invite if the type sent is Friend or Account friend.
```

------------------------------------------------------------------------

`Function`

AddByName(eFriendshipType, strName, strRealmName, strNote)
----------------------------------------------------------

### Description

Changes the friendship type with the player with the specified name.

### Params

-   **eFriendshipType** **(Integer)** - The friendship type that the
    player will change to. This value lines up with
    FriendshipLib.CharacterFriendshipType set of constants.
-   **strName** **(String)** - The name of the player whose friendship
    type will be updated.
-   **strRealmName** **(String)** - The name of the realm that the
    player is on. This is only necessary for players that are not on the
    same realm.
-   **strNote** **(String)** - A note that will be sent to the specified
    player if the friendship type is either Friend or Account Friend.
    This note will be visible in the invite that the player receives.

### Usage/Example

```lua
    If the Friendship Type is Friend or Account Friend, an invite will be sent to the player.  Other changes in Friend status do not need confirmation from the other player.
```

------------------------------------------------------------------------

`Function`

AddBySuggested()
----------------

------------------------------------------------------------------------

`Function`

AddByUnit()
-----------

------------------------------------------------------------------------

`Function`

GetAccountById()
----------------

------------------------------------------------------------------------

`Function`

GetAccountInviteById()
----------------------

------------------------------------------------------------------------

`Function`

GetAccountInviteList()
----------------------

------------------------------------------------------------------------

`Function`

GetAccountList()
----------------

------------------------------------------------------------------------

`Function`

GetById()
---------

------------------------------------------------------------------------

`Function`

GetInviteById()
---------------

------------------------------------------------------------------------

`Function`

GetInviteList()
---------------

------------------------------------------------------------------------

`Function`

GetList()
---------

------------------------------------------------------------------------

`Function`

GetLocations()
--------------

------------------------------------------------------------------------

`Function`

GetPersonalStatus()
-------------------

------------------------------------------------------------------------

`Function`

GetSuggestedById()
------------------

------------------------------------------------------------------------

`Function`

GetSuggestedList()
------------------

------------------------------------------------------------------------

`Function`

GetUnitById()
-------------

------------------------------------------------------------------------

`Function`

InviteMarkSeen()
----------------

------------------------------------------------------------------------

`Function`

IsLoaded()
----------

------------------------------------------------------------------------

`Function`

IsLocked()
----------

------------------------------------------------------------------------

`Function`

NeighborInvite()
----------------

------------------------------------------------------------------------

`Function`

PrepareInfractionReportInvite()
-------------------------------

------------------------------------------------------------------------

`Function`

Remove()
--------

------------------------------------------------------------------------

`Function`

RespondToInvite()
-----------------

------------------------------------------------------------------------

`Function`

SetAutoResponseMessages()
-------------------------

------------------------------------------------------------------------

`Function`

SetAwayFromKeyboardMessage()
----------------------------

------------------------------------------------------------------------

`Function`

SetDoNotDisturbMessage()
------------------------

------------------------------------------------------------------------

`Function`

SetFriendPrivateData()
----------------------

------------------------------------------------------------------------

`Function`

SetLock()
---------

------------------------------------------------------------------------

`Function`

SetNote()
---------

------------------------------------------------------------------------

`Function`

SetPersonalIgnoreStrangersState()
---------------------------------

------------------------------------------------------------------------

`Function`

SetPersonalPresenceState()
--------------------------

------------------------------------------------------------------------

`Function`

SetPublicDisplayName()
----------------------

------------------------------------------------------------------------

`Function`

SetPublicNote()
---------------

------------------------------------------------------------------------

`Function`

SetType()
---------

------------------------------------------------------------------------

`Function`

VisitResidence()
----------------
