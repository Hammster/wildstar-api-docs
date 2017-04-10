Episode
=======

### Prefix: epi

### Description

Episodes are a set of quests that are linked by a storyline or area.

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Checks whether the variable that is passed in is an Episode or not.

### Params

-   **oVariable** **(Variable)** - The variable that the function will
    check. This variable can be of any type.

### Return Value

-   **Boolean** - Whether the variable that was passed in is an Episode
    or not.

------------------------------------------------------------------------

`Method`

\_\_eq(epiCompare) (Deprecated)
-------------------------------

### Description

Determines if two Episodes are the same.

### Params

-   **epiCompare** **([Episode](../Classes/Episode.md))** - The episode
    being compared to this Episode.

### Return Value

-   **Boolean** - Whether the two Episodes are the same or not.

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

Manually calls the garbage collector on this Episode.

------------------------------------------------------------------------

`Method`

EpisodeState\_Complete() (Deprecated)
-------------------------------------

------------------------------------------------------------------------

`Method`

GetAllQuests(idQuestCategory)
-----------------------------

### Description

Gets a list of all of the quests in the Episode that match the passed in
category id and that have been unlocked by the player.

### Params

-   **idQuestCategory** **(Integer)** - The function will return all
    quests with this category.

### Return Value

-   **Array of [Quest](../Classes/Quest.md)** - An array of quests that
    have the same category as the one that was passed in and have been
    unlocked by the player.

------------------------------------------------------------------------

`Method`

GetCategories()
---------------

### Description

Gets a list of all of the QuestCategories that are used by quests in the
Episode.

### Return Value

-   **Array of [QuestCategory](../Classes/QuestCategory.md)** - An
    array of QuestCategories that are used by quests in the Episode.

------------------------------------------------------------------------

`Method`

GetConLevel()
-------------

### Description

Gets the level that the player is expected to be in order to complete
the Episode.

### Return Value

-   **Integer** - The level that the player is expected to be to
    complete the Episode.

------------------------------------------------------------------------

`Method`

GetDesc()
---------

### Description

Gets the description that should be shown for the Episode when it is
incomplete.

### Return Value

-   **String** - The string that should be used as the Episode's
    description while it is incomplete.

------------------------------------------------------------------------

`Method`

GetHub()
--------

------------------------------------------------------------------------

`Method`

GetId()
-------

### Description

Gets the Episode's id.

### Return Value

-   **Integer** - The Episode's id.

------------------------------------------------------------------------

`Method`

GetProgress(idQuestCategory)
----------------------------

### Description

Gets information on the player's progress towards completing every quest
of a specific category in this Episode.

### Params

-   **idQuestCategory** **(Integer)** - The function will get the
    Episode's progress for Quests whose category uses this id.

### Return Value

-   **Table** - A count of how many Quests the player has completed and
    how many the Episode has for the specified category.
    -   **nTotal** **(Integer)** - The total number of Quests of the
        specified category that are in the Episode.
    -   **nCompleted** **(Integer)** - The number of Quests of the
        specified category that the player has completed.

------------------------------------------------------------------------

`Method`

GetQuest(idQuest)
-----------------

### Description

Gets the Quest with the specified id if it is in this Episode.

### Params

-   **idQuest** **(Integer)** - The id of the Quest that the function
    will look for.

### Return Value

-   **[Quest](../Classes/Quest.md)** - The Quest whose id matches the
    one passed in.

------------------------------------------------------------------------

`Method`

GetState()
----------

### Description

Gets the Episode's current state.

### Return Value

-   **Integer** - The Episode's current state. This value corresponds
    with the Episode.EpisodeState set of constants.

------------------------------------------------------------------------

`Method`

GetSummary()
------------

### Description

Gets the description that should be shown for the Episode once it's
complete.

### Return Value

-   **String** - The string that should be shown for the Episode's
    description once it's in the Completed state.

------------------------------------------------------------------------

`Method`

GetTitle()
----------

### Description

Gets the Episode's title.

### Return Value

-   **String** - The Episode's title.

------------------------------------------------------------------------

`Method`

GetTrackedQuests(idQuestCategory, bSortByDistance)
--------------------------------------------------

### Description

Gets a list of tracked quests that have the specified QuestCategory and
are part of the Episode.

### Params

-   **idQuestCategory** **(Integer)** - The id of the QuestCategory that
    the function will use to filter the results.
-   **bSortByDistance** **(Boolean)** - Whether the function should sort
    the results by distance, with the closest quests coming first in the
    list.

### Return Value

-   **Array of [Quest](../Classes/Quest.md)** - An array of Quests that
    are part of the Episode and have a QuestCategory whose id matches
    the one passed in.

------------------------------------------------------------------------

`Method`

GetVisibleQuests(bShowCompleted, bShowOutLeveled, bSortByName, idQuestCategory)
-------------------------------------------------------------------------------

### Description

Gets a list of Quests that are part of the Episode and match the filters
that are flagged with the variables that are passed in

### Params

-   **bShowCompleted** **(Boolean)** - Whether completed quests should
    be added to the list or not.
-   **bShowOutLeveled** **(Boolean)** - Whether Quests whose con level
    are 10 below the player's effective level should be added to the
    list or not.
-   **bSortByName** **(Boolean)** - Whether the list should be sorted
    alphabetically by name or not.
-   **idQuestCategory** **(Integer)** - The Quests that are returned
    will be filtered by this QuestCategory id.

### Return Value

-   **Array of [Quest](../Classes/Quest.md)** - An array of Quests that
    has been filtered and possibly sorted by the variables that were
    passed into the function.

------------------------------------------------------------------------

`Method`

GetZoneId()
-----------

### Description

Gets the id number of the zone that the Episode takes place in.

### Return Value

-   **Integer** - The id number of the zone that the Episode is in.

------------------------------------------------------------------------

`Method`

GetZoneName()
-------------

### Description

Gets the name of the zone that the Episode is found in.

### Return Value

-   **String** - The name of the zone that the episode is in.

------------------------------------------------------------------------

`Method`

IsRegionalStory()
-----------------

### Description

Checks if the Episode is a Regional Story. Regional Stories are Episodes
that take place in a specific region within a zone, but do not
breadcrumb to other areas.

### Return Value

-   **Boolean** - Whether the Episode is a Regional Story or not.

------------------------------------------------------------------------

`Method`

IsTaskOnly()
------------

### Description

Determines if the Episode only has Tasks. Tasks are Quests that are not
part of any larger chain.

### Return Value

-   **Boolean** - Whether the Episode's Quests are all Tasks or not.

------------------------------------------------------------------------

`Method`

IsWorldStory()
--------------

### Description

Determines if the Episode is a World Story or not. World Stories are
quest chains that span multiple zones.

### Return Value

-   **Boolean** - Whether the Episode is a World Story or not.

------------------------------------------------------------------------

`Method`

IsZoneStory()
-------------

### Description

Determines if the Episode is a Zone Story or not. Zone Stories are
Episodes that span an entire zone.

### Return Value

-   **Boolean** - Whether the Episode is a Zone Story or not.
