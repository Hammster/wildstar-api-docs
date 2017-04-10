ChallengesLib
=============

### Description

A library that allows the UI to interact with the challenge system.

------------------------------------------------------------------------

`Enum`

ChallengeTier
-------------

-   **Bronze**
-   **Silver**
-   **Gold**

------------------------------------------------------------------------

`Event`

ChallengeAbandon
----------------

### Description

Fires whenever the player abandons a challenge, clears their challenge
data, or reqests that the challenge is abandoned via the
ChallengesLib.ShowAbandonChallenge() function

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge that
    was abandoned.
-   **strDescription** **(String)** - The challenge's fail message.

------------------------------------------------------------------------

`Event`

ChallengeActivate
-----------------

### Description

Fires whenever a challenge is activated

### Params

-   **clgActivated** **(Challenge)** - The challenge that was activated.

------------------------------------------------------------------------

`Event`

ChallengeCompleted
------------------

### Description

Fires whenever the player completes a challenge.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge.
-   **strHeaderText** **(String)** - The channel's name.
-   **strDescription** **(String)** - The challenge's description text.
-   **nDuration** **(Integer)** - The amount of time (in milliseconds)
    that the Challenge Complete window will appear on the screen.

------------------------------------------------------------------------

`Event`

ChallengeFlashStartLocation
---------------------------

### Description

Fires whenever the player leaves the challenge area and the challenge
has a valid start location. It tells the UI that it should attempt to
lead the player back to the start location.

### Params

-   **idChallenge** **(Integer)** - The id number for the challenge that
    fired the event.
-   **strDescription** **(String)** - The message that should be
    communicated to the player when the UI receives this message.
-   **fDuration** **(Float)** - How long the start location should
    flash, in seconds.
-   **tLocation** **(Table)** - The coordinates that the player should
    be directed towards.
    -   **x** **(Float)**
    -   **y** **(Float)**
    -   **z** **(Float)**

------------------------------------------------------------------------

`Event`

ChallengeLeftArea
-----------------

### Description

Fires whenever the player leaves the challenge area.

### Params

-   **idChallenge** **(Integer)** - The id number for the challenge that
    fired the event.
-   **strHeader** **(String)** - The header that should be shown on the
    challenge tracker after this event is fired.
-   **strDescription** **(String)** - The message that should be shown
    to the player after the event is fired.
-   **bShow** **(Boolean)**

------------------------------------------------------------------------

`Event`

ChallengeTypeAlreadyActive
--------------------------

### Description

Fires whenever the player activates a challenge when they already have
an active challenge of the same type.

### Params

-   **idActivating** **(Integer)** - The id of the challenge that was
    activated.
-   **idAbandoned** **(Integer)** - The id of the challenge that was
    abandoned.

### Remarks

Only one challenge of each type can be active at any given time. If
another is activated, the previous one is abandoned.

------------------------------------------------------------------------

`Event`

ChallengeUnlocked
-----------------

### Description

Fires whenever a new challenge is unlocked.

### Params

-   **clgUnlocked** **(Challenge)** - The challenge that was unlocked.

------------------------------------------------------------------------

`Function`

AbandonChallenge(idChallenge)
-----------------------------

### Description

Abandons the challenge with the specified id.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge that
    will be abandoned.

### Usage/Example

```lua
    If the challenge was active, the server will respond with the ChallengeAbandon event.
```

------------------------------------------------------------------------

`Function`

AcceptRewards(idChallenge) (Deprecated)
---------------------------------------

### Description

Attempts to collect a reward from a challenge.

### Params

-   **idChallenge** **(Integer)** - The function will attempt to grant
    the player the reward from the challenge with this id.

### Usage/Example

```lua
    This should only be called after the ChallengeRewardReady event has been fired for the challenge.
```

------------------------------------------------------------------------

`Function`

AcceptSharedChallenge(idChallenge) (Deprecated)
-----------------------------------------------

### Description

Accepts a challenge that another player has shared with the player.

### Params

-   **idChallenge** **(Integer)** - The id number for the challenge that
    was shared with the player.

### Remarks

Challenge sharing is not currently implemented, so this is currently
depricated.

------------------------------------------------------------------------

`Function`

ActivateChallenge(idChallenge)
------------------------------

### Description

Activates the challenge with the specified id.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge that
    the player wants to activate.

### Usage/Example

```lua
    If the challenge was unlocked, not activated, and not on cooldown, the server will respond with the ChallengeActivate event.
```

------------------------------------------------------------------------

`Function`

AtChallengeStartLocation()
--------------------------

------------------------------------------------------------------------

`Function`

ChallengeTier() (Deprecated)
----------------------------

------------------------------------------------------------------------

`Function`

GenerateRewardList(idChallenge) (Deprecated)
--------------------------------------------

### Description

Requests the challenge reward list for the specified quest from the
server.

### Params

-   **idChallenge** **(Integer)** - The function will request the
    challenge reward list for the challenge with this id number.

### Usage/Example

```lua
    If the challenge has a reward that the player did not collect (Challenge:ShouldCollectReward() == true), the server will respond with the ChallengeRewardListReady event.
```

------------------------------------------------------------------------

`Function`

GetActiveChallengeList()
------------------------

### Description

Gets a list of all of the challenges that the player has unlocked.

### Return Value

-   **Table** - A map of all of the player's unlocked challenges,
    indexed by Id.

------------------------------------------------------------------------

`Function`

GetLootBonusMultiplier(nTier) (Deprecated)
------------------------------------------

### Description

Gets the bonus multiplier that a player can attach to a specific reward
for a particular challenge tier.

### Params

-   **nTier** **(Integer)** - The function will return the multiplier
    for this reward tier.

### Return Value

-   **Integer** - The multiplier that is granted to whatever reward the
    player selects in the challenge reward list.

------------------------------------------------------------------------

`Function`

GetRewardList(idChallenge) (Deprecated)
---------------------------------------

### Params

-   **idChallenge** **(Integer)** - The function will return the reward
    list for this challenge.

### Return Value

-   **Array of Table** - A mostly-array that contains information on the
    different rewards that the quest can grant. It is not a true array
    since strChallengeName is an index in the top level table, and not
    in any of the sub tables in the array.
    -   **strChallengeName** **(String)** - The name of the challenge.
        This variable is an index of the array and not part of the
        individual tables in the array.
    -   **nChallengeTier** **(Integer)** - The challenge tier that the
        player has to achieve to select this reward.
    -   **idReward** **(Integer)** - The reward's id number.
    -   **nAmount** **(Integer)** - The number of the item that the
        player gets if the reward is chosen.
    -   **itemReward** **([Item](../Classes/Item.md))** - The item that
        the player receives if this reward is selected.
    -   **monReward** **([Money](../Classes/Money.md))** - The money
        that the player receives if this reward is selected.
    -   **splReward** **([Spell](../Classes/Spell.md))** - The spell
        that is cast on the player if this reward is selected.
    -   **splAdvSpell** **([Spell](../Classes/Spell.md))** - The spell
        that is granted if this reward is selected. This type of spell
        is only granted during adventures.
    -   **nXP** **(Integer)** - The amount of XP that the player earns
        if this reward is selected. This type of reward should only
        appear in adventures.
    -   **nRepId** **(Integer)** - The id number for the faction that
        the player gains reputation with if this reward is selected.
        This reward type should only appear in adventures.
    -   **nRepAmount** **(Integer)** - The amount of reputation that the
        player gains if this reward is selected. This reward type should
        only appear in adventures.

------------------------------------------------------------------------

`Function`

GetRewardTrackByZone()
----------------------

------------------------------------------------------------------------

`Function`

GetRewardTrackInfo()
--------------------

------------------------------------------------------------------------

`Function`

GetRewardTrackPoints()
----------------------

------------------------------------------------------------------------

`Function`

GetTierName(nTier)
------------------

### Description

Gets the name for the specified challenge tier.

### Params

-   **nTier** **(Integer)** - The function will get the name of this
    tier.

### Return Value

-   **String** - The name of the challenge tier. If the tier number that
    was passed in was invalid, this will be an empty string.

------------------------------------------------------------------------

`Function`

GetTimeRemaining(idChallenge, eTimerFlags)
------------------------------------------

### Description

Gets the amount of time left for a specific timer used by the specified
challenge.

### Params

-   **idChallenge** **(Integer)** - The function will get the remaining
    time for the challenge with this id number.
-   **eTimerFlags** **(Integer)** - The type of timer that the function
    is searching for. The different types of timers are found in the
    ChallengesLib.ChallengeTimerFlags set of contstants.

### Return Value

-   **String** - The amount of time left for the challenge's timer, in
    string form.

------------------------------------------------------------------------

`Function`

ProcessRewards(idChallenge, nRewardIdx) (Deprecated)
----------------------------------------------------

### Description

Tells the server to choose the reward that the player will receive from
the challenge.

### Params

-   **idChallenge** **(Integer)** - The server will attempt to choose
    the reward for the challenge with this id number.
-   **nRewardIdx** **(Integer)** - The reward number that the player
    selected to receive the bonus multiplier.

### Usage/Example

```lua
    If this is called on a challenge that is not active, not on cooldown, and the player has received the challenge's reward list, then the server should fire the ChallengeRewardReady event once it has determined the reward the player will receive.
```

------------------------------------------------------------------------

`Function`

RejectSharedChallenge(idChallenge)
----------------------------------

### Description

Declines a shared challenge.

### Params

-   **idChallenge** **(Integer)** - The id number for the challenge that
    the function will reject.

------------------------------------------------------------------------

`Function`

ShowAbandonChallenge(idChallenge)
---------------------------------

### Description

Fires the ChallengeAbandoned event with a confirmation message.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge that
    the player is trying to abandon.

### Usage/Example

```lua
    It is worth noting that this function does NOT abandon the challenge.  The name of the event may give that impression, but it does not actually abandon it.
```

------------------------------------------------------------------------

`Function`

ShowHintArrow(idChallenge)
--------------------------

### Description

Shows the hint arrow that points to the area where the specified
challenge takes place.

### Params

-   **idChallenge** **(Integer)** - The id number of the challenge that
    should show its hint arrow.
