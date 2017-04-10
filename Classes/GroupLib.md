GroupLib
========

------------------------------------------------------------------------

`Enum`

ActionResult
------------

-   **LeaveSuccess**
-   **LeaveFailed**
-   **DisbandSuccess**
-   **DisbandFailed**
-   **KickSuccess**
-   **KickFailed**
-   **PromoteSuccess**
-   **PromoteFailed**
-   **FlagsSuccess**
-   **FlagsFailed**
-   **MemberFlagsSuccess**
-   **MemberFlagsFailed**
-   **NotInGroup**
-   **ChangeSettingsFailed**
-   **ChangeSettingsSuccess**
-   **MentoringInvalidMentor**
-   **MentoringInvalidMentee**
-   **InvalidGroup**
-   **MentoringSelf**
-   **ReadyCheckFailed**
-   **MentoringNotAllowed**
-   **MarkingNotPermitted**
-   **InvalidMarkIndex**
-   **InvalidMarkTarget**
-   **MentoringInCombat**
-   **MentoringLowestLevel**
-   **MentoringNoAction**
-   **OrderInvalidMember**
-   **OrderFailedLeader**
-   **AlreadyInGroupInstance**
-   **OrderFailedInUse**

------------------------------------------------------------------------

`Enum`

Difficulty
----------

-   **Normal**
-   **Veteran**
-   **Count**

------------------------------------------------------------------------

`Enum`

HarvestLootRule
---------------

-   **RoundRobin**
-   **FirstTagger**

------------------------------------------------------------------------

`Enum`

InvitationMethod
----------------

-   **Open**
-   **Neutral**
-   **Closed**

------------------------------------------------------------------------

`Enum`

LootRule
--------

-   **FreeForAll**
-   **RoundRobin**
-   **NeedBeforeGreed**
-   **Master**

------------------------------------------------------------------------

`Enum`

LootThreshold
-------------

-   **Average**
-   **Good**
-   **Excellent**
-   **Superb**
-   **Legendary**
-   **Inferior**
-   **Artifact**

------------------------------------------------------------------------

`Enum`

RemoveReason
------------

-   **Left**
-   **Kicked**
-   **Disconnected**
-   **Disband**
-   **RemovedByServer**
-   **VoteKicked**

------------------------------------------------------------------------

`Enum`

Result
------

-   **PlayerNotFound**
-   **RealmNotFound**
-   **Sent**
-   **Accepted**
-   **Declined**
-   **NoPermissions**
-   **Grouped**
-   **Pending**
-   **ExpiredInviter**
-   **IsInvited**
-   **InvitedYou**
-   **Full**
-   **RoleFull**
-   **NoInvitingSelf**
-   **ExpiredInvitee**
-   **ServerControlled**
-   **GroupNotFound**
-   **NotAcceptingRequests**
-   **Busy**
-   **SentToLeader**
-   **LeaderOffline**
-   **WrongFaction**
-   **PrivilegeRestricted**

------------------------------------------------------------------------

`Event`

Group\_AcceptInvite
-------------------

------------------------------------------------------------------------

`Event`

Group\_Changed (Deprecated)
---------------------------

------------------------------------------------------------------------

`Event`

Group\_DeclineInvite
--------------------

------------------------------------------------------------------------

`Event`

Group\_Disbanded (Deprecated)
-----------------------------

### Description

Handles the output of a group leave and if the group empties and
disbands.

### Params

-   **nReason** **(Integer)** - The reason for the group leave. This can
    be a kick or a leave.
-   **nGroupMemberIndex** **(Integer)** - The affected group member's
    index in the group.
-   **nGroupActorIndex** **(Integer)** - The kicker actor member's index
    in the group.

------------------------------------------------------------------------

`Event`

Group\_Invite\_Declined (Deprecated)
------------------------------------

### Description

Outputs the refused invitation to a group invite.

### Params

-   **tTableRef** **(Table)** - Table reference to the invited player
    from the current context.

------------------------------------------------------------------------

`Event`

Group\_Invite\_Result
---------------------

### Params

-   **nTableRef** **(Lua Table)**

------------------------------------------------------------------------

`Event`

Group\_Invited
--------------

### Params

-   **nTableRef** **(Lua Table)**

------------------------------------------------------------------------

`Event`

Group\_Other\_Joined (Deprecated)
---------------------------------

### Params

-   **nTableRef** **(Lua Table)**

------------------------------------------------------------------------

`Event`

Group\_Other\_Left (Deprecated)
-------------------------------

### Params

-   **nTableRef** **(Lua Table)**

------------------------------------------------------------------------

`Event`

Group\_Other\_Promoted (Deprecated)
-----------------------------------

### Description

Outputs the promotion of a group member.

### Params

-   **tTableRef** **(Table)** - Table reference to the player from the
    current context.

------------------------------------------------------------------------

`Event`

Group\_Player\_Joined (Deprecated)
----------------------------------

------------------------------------------------------------------------

`Event`

Group\_Player\_Left (Deprecated)
--------------------------------

------------------------------------------------------------------------

`Event`

Group\_Player\_Promoted (Deprecated)
------------------------------------

------------------------------------------------------------------------

`Event`

Group\_QuestList
----------------

### Params

-   **unitId** **([Unit](../Classes/Unit.md))**
-   **nTableRef** **(Lua Table)**

------------------------------------------------------------------------

`Function`

AcceptInvite(strMessage)
------------------------

### Description

Runs m\_clientGroup's AcceptInvite method with strMessage.

### Params

-   **strMessage** **(String)**

------------------------------------------------------------------------

`Function`

AcceptMentoring()
-----------------

------------------------------------------------------------------------

`Function`

AcceptRequest()
---------------

------------------------------------------------------------------------

`Function`

AmILeader()
-----------

### Description

Does a lua\_pushboolean if CharacterUnit is the leader.

------------------------------------------------------------------------

`Function`

CancelMentoring()
-----------------

------------------------------------------------------------------------

`Function`

CanGotoGroupInstance()
----------------------

------------------------------------------------------------------------

`Function`

CloseMentoringAOIDialog()
-------------------------

------------------------------------------------------------------------

`Function`

CloseMentoringDialog()
----------------------

------------------------------------------------------------------------

`Function`

ConvertToRaid()
---------------

------------------------------------------------------------------------

`Function`

DeclineInvite()
---------------

------------------------------------------------------------------------

`Function`

DenyRequest()
-------------

------------------------------------------------------------------------

`Function`

DisbandGroup(strMessage)
------------------------

### Description

Runs m\_clientGroup's DisbandGroup method.

### Params

-   **strMessage** **(String)**

------------------------------------------------------------------------

`Function`

GetGroupMaxSize()
-----------------

### Description

Does a lua\_pushinteger of GetGroupmaxSize.

------------------------------------------------------------------------

`Function`

GetGroupMember(nGroupIndex)
---------------------------

### Description

Does a PushGroupMemberToLua of the group member specified by
nGroupIndex, else nil.

### Params

-   **nGroupIndex** **(Integer)**

------------------------------------------------------------------------

`Function`

GetInstanceDifficulty()
-----------------------

------------------------------------------------------------------------

`Function`

GetInvite()
-----------

------------------------------------------------------------------------

`Function`

GetJoinRequestMethod()
----------------------

------------------------------------------------------------------------

`Function`

GetLootRules()
--------------

------------------------------------------------------------------------

`Function`

GetMemberCount()
----------------

### Description

Does a lua\_pushinteger of GetMemberCounty.

------------------------------------------------------------------------

`Function`

GetMemberVisibility()
---------------------

------------------------------------------------------------------------

`Function`

GetMentoringList()
------------------

------------------------------------------------------------------------

`Function`

GetReferralMethod()
-------------------

------------------------------------------------------------------------

`Function`

GetUnitForGroupMember(nGroupIndex)
----------------------------------

### Description

Returns a new unit that is a copy of the group member specified by
nGroupIndex.

### Params

-   **nGroupIndex** **(Integer)**

------------------------------------------------------------------------

`Function`

GotoGroupInstance()
-------------------

------------------------------------------------------------------------

`Function`

InGroup()
---------

### Description

Does a lua\_pushboolean of InGroup.

------------------------------------------------------------------------

`Function`

InInstance()
------------

------------------------------------------------------------------------

`Function`

InInstanceWithMember()
----------------------

------------------------------------------------------------------------

`Function`

InRaid()
--------

------------------------------------------------------------------------

`Function`

Invite(strPlayerName, strRealmName, strMessage)
-----------------------------------------------

### Description

Runs m\_clientGroup's Invite method with strPlayerName, strRealmName,
and strMessage.

### Params

-   **strPlayerName** **(String)**
-   **strRealmName** **(String)**
-   **strMessage** **(String)**

------------------------------------------------------------------------

`Function`

IsMemberInGroupInstance()
-------------------------

------------------------------------------------------------------------

`Function`

IsReadyCheckOnCooldown()
------------------------

------------------------------------------------------------------------

`Function`

Join()
------

------------------------------------------------------------------------

`Function`

Kick(nIndex, strMessage)
------------------------

### Description

Runs m\_clientGroup's Kick method specified by nIndex and with
strMessage.

### Params

-   **nIndex** **(Integer)**
-   **strMessage** **(String)**

------------------------------------------------------------------------

`Function`

LeaveGroup(strMessage)
----------------------

### Description

Runs m\_clientGroup's DenyInvite method with strMessage.

### Params

-   **strMessage** **(String)**

------------------------------------------------------------------------

`Function`

PrepareInfractionReportInvite()
-------------------------------

------------------------------------------------------------------------

`Function`

Promote(nIndex)
---------------

### Description

Runs m\_clientGroup's Promote method specified by nIndex.

### Params

-   **nIndex** **(Integer)**

------------------------------------------------------------------------

`Function`

ReadyCheck()
------------

------------------------------------------------------------------------

`Function`

SetCanMark()
------------

------------------------------------------------------------------------

`Function`

SetInstanceDifficulty()
-----------------------

------------------------------------------------------------------------

`Function`

SetInvitePermission()
---------------------

------------------------------------------------------------------------

`Function`

SetJoinRequestMethod()
----------------------

------------------------------------------------------------------------

`Function`

SetKickPermission()
-------------------

------------------------------------------------------------------------

`Function`

SetLootRules()
--------------

------------------------------------------------------------------------

`Function`

SetMainAssist()
---------------

------------------------------------------------------------------------

`Function`

SetMainTank()
-------------

------------------------------------------------------------------------

`Function`

SetOrder()
----------

------------------------------------------------------------------------

`Function`

SetRaidAssistant()
------------------

------------------------------------------------------------------------

`Function`

SetReady()
----------

------------------------------------------------------------------------

`Function`

SetReferralMethod()
-------------------

------------------------------------------------------------------------

`Function`

SetRoleDPS()
------------

------------------------------------------------------------------------

`Function`

SetRoleHealer()
---------------

------------------------------------------------------------------------

`Function`

SetRoleLocked()
---------------

------------------------------------------------------------------------

`Function`

SetRoleTank()
-------------

------------------------------------------------------------------------

`Function`

SwapOrder()
-----------
