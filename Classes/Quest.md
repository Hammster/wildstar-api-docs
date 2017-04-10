Quest
=====

### Prefix: que

------------------------------------------------------------------------

`Enum`

QuestRepeatPeriod
-----------------

-   **None**
-   **Daily**
-   **Weekly**
-   **Monthly**
-   **Yearly**

------------------------------------------------------------------------

`Function`

GetActiveQuest()
----------------

------------------------------------------------------------------------

`Function`

GetCallbackList()
-----------------

------------------------------------------------------------------------

`Function`

is()
----

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

\_\_gt() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

\_\_lt() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

Abandon()
---------

### Description

Runs the caller's AbandonQuest method.

------------------------------------------------------------------------

`Method`

AcceptShare()
-------------

### Description

Runs m\_clientGroup's AcceptSharedQuest method with true.

------------------------------------------------------------------------

`Method`

CalcRewardXP()
--------------

### Description

Does a lua\_pushinteger of GetXp.

------------------------------------------------------------------------

`Method`

CanAbandon()
------------

### Description

Does a lua\_pushboolean of IsInAbandonableState.

------------------------------------------------------------------------

`Method`

CanCompleteObjective(iReq)
--------------------------

### Description

Does a lua\_boolean of CanCompleteObjective specified by iReq.

### Params

-   **iReq** **(Integer)**

------------------------------------------------------------------------

`Method`

CanShare()
----------

### Description

Does a lua\_pushboolean of CanShare.

------------------------------------------------------------------------

`Method`

DisplayObjectiveProgressBar()
-----------------------------

------------------------------------------------------------------------

`Method`

GetCategory()
-------------

------------------------------------------------------------------------

`Method`

GetChatLinkString()
-------------------

------------------------------------------------------------------------

`Method`

GetColoredDifficulty()
----------------------

------------------------------------------------------------------------

`Method`

GetCompletedSummary()
---------------------

### Description

Does a lua\_pushstring of the quest completed summary after a
UCS2ToUTF8.

------------------------------------------------------------------------

`Method`

GetCompletionObjectiveShortText()
---------------------------------

------------------------------------------------------------------------

`Method`

GetCompletionObjectiveText()
----------------------------

------------------------------------------------------------------------

`Method`

GetConLevel()
-------------

### Description

Does a lua\_pushinteger of conLevel.

------------------------------------------------------------------------

`Method`

GetContactInfo()
----------------

### Description

Does several updates and lua pushes, including creatureId, IdName, and
spriteName at the end.

------------------------------------------------------------------------

`Method`

GetDistance()
-------------

------------------------------------------------------------------------

`Method`

GetEpisode()
------------

------------------------------------------------------------------------

`Method`

GetGroup()
----------

### Description

Does a lua\_pushstring of the group name after a UCS2ToUTF8.

------------------------------------------------------------------------

`Method`

GetId()
-------

### Description

Does a lua\_pushinteger of the id.

------------------------------------------------------------------------

`Method`

GetIntroductionText()
---------------------

------------------------------------------------------------------------

`Method`

GetMapRegions()
---------------

------------------------------------------------------------------------

`Method`

GetMinLevel()
-------------

------------------------------------------------------------------------

`Method`

GetMoreInfoText()
-----------------

------------------------------------------------------------------------

`Method`

GetObjectiveCompleted(iReq)
---------------------------

### Description

Does a lua\_pushinteger of GetNumCompleted specified by iReq, or 0 if
null.

### Params

-   **iReq** **(Integer)**

------------------------------------------------------------------------

`Method`

GetObjectiveCount()
-------------------

### Description

Does a lua\_pushinteger of GetNumObjectives.

------------------------------------------------------------------------

`Method`

GetObjectiveDescription(iReq)
-----------------------------

### Description

Does a lua\_pushstring of a UCS2ToUTF8 description specified by iReq, or
empty string if null.

### Params

-   **iReq** **(Integer)**

------------------------------------------------------------------------

`Method`

GetObjectiveMaxTime()
---------------------

------------------------------------------------------------------------

`Method`

GetObjectiveNeeded(iReq)
------------------------

### Description

Does a lua\_pushinteger of GetNumRequired specified by iReq, or 0 if
null.

### Params

-   **iReq** **(Integer)**

------------------------------------------------------------------------

`Method`

GetObjectiveShortDescription()
------------------------------

------------------------------------------------------------------------

`Method`

GetObjectiveTimeRemaining(iReq)
-------------------------------

### Description

Does a lua\_pushinteger of IsObjectiveTimed of an objective specified by
iReq.

### Params

-   **iReq** **(Integer)**

------------------------------------------------------------------------

`Method`

GetPathQuestType()
------------------

------------------------------------------------------------------------

`Method`

GetQuestItemCount()
-------------------

### Description

Does a lua\_pushinteger of the quest item count.

------------------------------------------------------------------------

`Method`

GetQuestItemData(iIndex)
------------------------

### Description

Does a lua\_newtable with item and num specified by iIndex.

### Params

-   **iIndex** **(Integer)**

------------------------------------------------------------------------

`Method`

GetQuestTimeRemaining()
-----------------------

### Description

Does a lua\_pushinteger of GetQuestTimeRemaining.

------------------------------------------------------------------------

`Method`

GetRepeatPeriod()
-----------------

------------------------------------------------------------------------

`Method`

GetRewardData()
---------------

### Description

Does two lua\_newtables describing fields relating to the reward and
money of the quest.

------------------------------------------------------------------------

`Method`

GetSpell()
----------

------------------------------------------------------------------------

`Method`

GetState()
----------

### Description

Does a lua\_pushinteger of the quest state.

------------------------------------------------------------------------

`Method`

GetSubType()
------------

------------------------------------------------------------------------

`Method`

GetSummary()
------------

### Description

Does a lua\_pushstring of the quest summary after a UCS2ToUTF8.

------------------------------------------------------------------------

`Method`

GetTitle()
----------

### Description

Does a lua\_pushstring of the quest title after a UCS2ToUTF8.

------------------------------------------------------------------------

`Method`

GetTrackBlinkTime()
-------------------

### Description

Does a lua\_pushnumber of blink time / 1000.0.

------------------------------------------------------------------------

`Method`

GetTradeskillSchematicsRequired()
---------------------------------

------------------------------------------------------------------------

`Method`

GetType()
---------

------------------------------------------------------------------------

`Method`

GetVisibleObjectiveData()
-------------------------

### Description

Does a lua\_newtable with index, description, needed, completed, and
isReward.

------------------------------------------------------------------------

`Method`

GetZoneId()
-----------

------------------------------------------------------------------------

`Method`

IsAbleToAdvanceInRaid()
-----------------------

------------------------------------------------------------------------

`Method`

IsActiveQuest()
---------------

### Description

Does a lua\_pushboolean if quest is active for the player and tracked.

------------------------------------------------------------------------

`Method`

IsBreadcrumb()
--------------

------------------------------------------------------------------------

`Method`

IsCommunicatorReceived()
------------------------

------------------------------------------------------------------------

`Method`

IsCommunicatorReceivedFromRec()
-------------------------------

------------------------------------------------------------------------

`Method`

IsContract()
------------

------------------------------------------------------------------------

`Method`

IsIgnored()
-----------

------------------------------------------------------------------------

`Method`

IsImbuementQuest()
------------------

------------------------------------------------------------------------

`Method`

IsInactive()
------------

------------------------------------------------------------------------

`Method`

IsInLog()
---------

### Description

Does a lua\_pushboolean of IsVisibleInLog.

------------------------------------------------------------------------

`Method`

IsKnown()
---------

### Description

Does a lua\_pushboolean if quest state is known.

------------------------------------------------------------------------

`Method`

IsMentioned()
-------------

### Description

Does a lua\_pushboolean if quest data is mentioned.

------------------------------------------------------------------------

`Method`

IsMoreInfoNonSequential()
-------------------------

------------------------------------------------------------------------

`Method`

IsObjectiveTimed(iReq)
----------------------

### Description

Does a lua\_pushboolean of IsObjectiveTimed of an objective specified by
iReq.

### Params

-   **iReq** **(Integer)**

------------------------------------------------------------------------

`Method`

IsOnlyAdvanceInPvp()
--------------------

------------------------------------------------------------------------

`Method`

IsOptionalForEpisode()
----------------------

------------------------------------------------------------------------

`Method`

IsPathQuest()
-------------

------------------------------------------------------------------------

`Method`

IsQuestTimed()
--------------

### Description

Does a lua\_pushboolean of IsQuestTimed.

------------------------------------------------------------------------

`Method`

IsSelectedInLog()
-----------------

### Description

Does a lua\_pushboolean of IsSelectedInLog.

------------------------------------------------------------------------

`Method`

IsTracked()
-----------

### Description

Does a lua\_pushboolean if quest data is tracked.

------------------------------------------------------------------------

`Method`

ObjectiveIsReward(iReq)
-----------------------

### Description

Does a lua\_boolean if iReq is &lt; 0 or equal to the number of
objectives.

### Params

-   **iReq** **(Integer)**

------------------------------------------------------------------------

`Method`

ObjectiveIsVisible(iReq)
------------------------

### Description

Does a lua\_boolean of IsObjectiveVisible specified by iReq, or empty
string if null.

### Params

-   **iReq** **(Integer)**

------------------------------------------------------------------------

`Method`

PulseTrackBlinkTime(uTime)
--------------------------

### Params

-   **uTime** **(Float - that is immediately \* 1000.0 and cast to a
    UINT32)**

------------------------------------------------------------------------

`Method`

RejectShare()
-------------

### Description

Runs m\_clientGroup's AcceptSharedQuest method with false.

------------------------------------------------------------------------

`Method`

SetActiveQuest(bActive)
-----------------------

### Params

-   **bActive** **(Boolean)**

------------------------------------------------------------------------

`Method`

SetSelectedInLog()
------------------

### Description

Runs the quest log's SetSelectedQuestId method with the caller.

------------------------------------------------------------------------

`Method`

SetTracked(bTracked)
--------------------

### Params

-   **bTracked** **(Boolean)**

------------------------------------------------------------------------

`Method`

Share()
-------

### Description

Runs m\_clientGroup's ShareQuest with pLuaQuest's id.

------------------------------------------------------------------------

`Method`

ShowHintArrow()
---------------

------------------------------------------------------------------------

`Method`

ToggleActiveQuest()
-------------------

------------------------------------------------------------------------

`Method`

ToggleIgnored()
---------------

------------------------------------------------------------------------

`Method`

ToggleTracked()
---------------
