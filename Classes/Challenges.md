Challenges
==========

### Prefix: clg

### Description

Challenges are timed goals that the player will unlock as they kill NPCs
and explore Nexus. Most challenges are repeatable and offer rewards,
such as crafting materials, decor, and equipment.

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Determines if the variable is a Challenge or not.

### Params

-   **oVariable** **(Variable)** - The variable that the function will
    check.

### Return Value

-   **Boolean** - Whether the variable is a Challenge or not.

------------------------------------------------------------------------

`Method`

\_\_eq() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

Challenge's garbage collection function. This will delete the Challenge
from memory.

------------------------------------------------------------------------

`Method`

GetAllTierCounts()
------------------

### Description

Returns the goal number for each tier of the Challenge

### Return Value

-   **Array of Table** - An array that contains the amount of progress
    that the player must reach for each of the Challenge's tiers.
    -   **nGoalCount** **(Integer)** - The amount of progression
        required for the challenge. If the challenge is percentage
        based, this value is 100. Otherwise, it is an exact number of
        objectives that the player must reach.

------------------------------------------------------------------------

`Method`

GetCompletionCount()
--------------------

### Description

Gets the number of times the player has completed the challenge.

### Return Value

-   **Integer** - The number of times the player has completed the
    challenge.

------------------------------------------------------------------------

`Method`

GetCompletionTotal()
--------------------

### Description

Gets the number of times this Challenge can be completed.

### Return Value

-   **Integer** - The number of times the player can complete the
    challenge. If this value is -1, then the challenge can be completed
    an infinate number of times.

------------------------------------------------------------------------

`Method`

GetCurrentCount()
-----------------

### Description

Gets the player's progress towards this Challenge.

### Return Value

-   **Integer** - The amount of progress the player has made towards the
    current challenge.

------------------------------------------------------------------------

`Method`

GetCurrentTier()
----------------

### Description

Gets the tier of this Challenge that the player is working towards.

### Return Value

-   **Integer** - The challege tier that the player is working towards.

------------------------------------------------------------------------

`Method`

GetDescription()
----------------

### Description

Gets the text that describes the challenge.

### Return Value

-   **String** - The Challenge's description.

------------------------------------------------------------------------

`Method`

GetDisplayTier()
----------------

### Description

Returns the current tier for the Challenge that the UI should display as
active.

### Return Value

-   **Integer** - The tier that the UI should display as active.

------------------------------------------------------------------------

`Method`

GetDistance()
-------------

------------------------------------------------------------------------

`Method`

GetDuration()
-------------

------------------------------------------------------------------------

`Method`

GetId()
-------

### Description

Returns the id number of the challenge

### Return Value

-   **Integer** - The Challenge's id number.

------------------------------------------------------------------------

`Method`

GetLastRewardTier()
-------------------

### Description

Returns the last tier of the Challenge that the player completed during
the current attempt.

### Return Value

-   **Integer** - The last tier that was completed of the challenge
    during the current attempt.

------------------------------------------------------------------------

`Method`

GetMapLocation()
----------------

### Description

The location that the hint arrow points the player towards for the
challenge.

### Return Value

-   **Table** - The X, Y, and Z coordinates that the hint arrow leads
    the player to.
    -   **x** **(Float)** - The X coordinate
    -   **y** **(Float)** - The Y coordinate
    -   **z** **(Float)** - The Z coordinate

------------------------------------------------------------------------

`Method`

GetMapRegions()
---------------

### Description

Gets the point that the helper arrow leads to and a list of all of the
hexes that the challenge uses.

### Return Value

-   **Table** - A list that contains map info on the challenge.
    -   **tHexes** **(Array of [Vector2](../Classes/Vector2.md))** - A
        list of x/y coordinates for the hexes where the Challenge takes
        place
    -   **tIndicator** **([Vector3](../Classes/Vector3.md))** - The
        x/y/z coordinates where the Challenge can be started

------------------------------------------------------------------------

`Method`

GetMapStartLocation()
---------------------

### Description

Gets the coordinates where the Challenge can be started

### Return Value

-   **Table** - The coordinates where the challenge can be started.
    -   **x** **(Float)** - The X coordinate
    -   **y** **(Float)** - The Y coordinate
    -   **z** **(Float)** - The Z coordinate

------------------------------------------------------------------------

`Method`

GetMapStartRegions()
--------------------

### Description

Returns the coordinates for the hexes where the Challenge takes place

### Return Value

-   **Array of [Vector2](../Classes/Vector2.md)** - An array of hex
    coordinates where the objectives for the challenge can be found.

------------------------------------------------------------------------

`Method`

GetName()
---------

### Description

Gets the challenge's name.

### Return Value

-   **String** - The name of the challenge.

------------------------------------------------------------------------

`Method`

GetRewardTrack()
----------------

------------------------------------------------------------------------

`Method`

GetStartLocationRestrictionId()
-------------------------------

### Description

Returns the location id that the player must be in to start the
challenge. This value can be used with GameLib.IsInLocation() to
determine if the player is in the correct location to start a challenge.

### Return Value

-   **Integer** - The id number of the challenge's start location.

------------------------------------------------------------------------

`Method`

GetTimer()
----------

------------------------------------------------------------------------

`Method`

GetTimeStr() (Deprecated)
-------------------------

### Description

Gets the challenge's current timer and returns it in string form.

### Return Value

-   **String** - The amount of time left on the timer, in
    "minute:second" format.

### Usage/Example

```lua
    This timer is context sensitive.  If the challenge is active, it shows the amount of time the player has to complete it.  If the player has left the challenge area, it shows the amount of time before the player fails the challenge because they left the area.  If the challenge is on cooldown, it returns the amount of time until it is no longer on cooldown.
```

------------------------------------------------------------------------

`Method`

GetTotalCount()
---------------

### Description

Gets the total amount of progress the player has to earn to complete the
current tier of the challenge.

### Return Value

-   **Integer** - The amount of progress needed to complete the current
    challenge tier. This value is 100 for percentage based progress, or
    a smaller number for challenges that require a fixed amount of
    progress.

------------------------------------------------------------------------

`Method`

GetType()
---------

### Description

Gets a challenge's type.

### Return Value

-   **Integer** - The challenge's type. This corresponds with the
    ChallengeLib.ChallengeType set of int constants.

### Remarks

Only one challenge of each type can be active at a given time.

------------------------------------------------------------------------

`Method`

GetZoneInfo()
-------------

### Description

Gets information on the zone where the challenge is found.

### Return Value

-   **Table** - A table with information on where the challenge is
    located.
    -   **idZone** **(Integer)** - The id number of the zone where the
        challenge can be found.
    -   **strZoneName** **(String)** - The name of the zone where the
        challenge is located.

------------------------------------------------------------------------

`Method`

GetZoneRestrictionInfo()
------------------------

### Description

Gets information on the area that the challenge is restricted to.

### Return Value

-   **Table** - A table with information on the area that the challenge
    is restricted to.
    -   **idSubZone** **(Integer)** - The id number of the subzone that
        the challenge is restricted to.
    -   **strLocationName** **(String)** - The name of the area that the
        challenge is restricted to.
    -   **strSubZoneName** **(String)** - The name of the subzone that
        the challenge is restricted to.

------------------------------------------------------------------------

`Method`

IsActivated()
-------------

### Description

Finds out whether the challenge is currently running or not.

### Return Value

-   **Boolean** - Whether the challenge is currently running or not.

------------------------------------------------------------------------

`Method`

IsFullyComplete()
-----------------

### Description

Determines if the challenge has been completed the maximum number of
times or not.

### Return Value

-   **Boolean** - Whether the challenge has been completed the maximum
    number of times or not.

------------------------------------------------------------------------

`Method`

IsInCooldown()
--------------

### Description

Determines whether the challenge is currently on cooldown.

### Return Value

-   **Boolean** - Whether the challenge is on cooldown or not.

------------------------------------------------------------------------

`Method`

IsTimeTiered()
--------------

### Description

Determines whether the reward tiers are based on the player's completion
time or not.

### Return Value

-   **Boolean** - Whether the reward tiers are based on the player's
    completion time or not.

------------------------------------------------------------------------

`Method`

NeedsHintArrow()
----------------

### Description

Determines whether the challenge has a set starting area or zone
restrictions.

### Return Value

-   **Boolean** - Whether the challenge needs to have a hint arrow or
    not.

------------------------------------------------------------------------

`Method`

ShouldCollectReward() (Deprecated)
----------------------------------

### Description

Determines if the player has not collected their reward for the
challenge.

### Return Value

-   **Boolean** - Whether the player has an uncollected reward or not.

------------------------------------------------------------------------

`Method`

ShouldDisplayPercentProgress()
------------------------------

### Description

Determines whether the challenge displays its progress as a percent or
as an exact number.

### Return Value

-   **Boolean** - Whether the player's progress should be shown as a
    percent or not.
