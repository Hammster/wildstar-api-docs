PlayerPathLib
=============

------------------------------------------------------------------------

`Event`

PlayerPathExplorerPlaceBeacon
-----------------------------

### Params

-   **state** **(Integer)**
-   **complete** **(Boolean)**

------------------------------------------------------------------------

`Event`

PlayerPathExplorerZoneChange (Deprecated)
-----------------------------------------

### Params

-   **enter** **(Boolean)**

------------------------------------------------------------------------

`Event`

PlayerPathMissionActivate
-------------------------

### Params

-   **nTableRef** **(Lua Table)**

------------------------------------------------------------------------

`Event`

PlayerPathMissionDeactivate
---------------------------

### Params

-   **missionId** **(Integer)**

------------------------------------------------------------------------

`Event`

PlayerPathScientistScanData
---------------------------

### Params

-   **nTableRef** **(Lua Table)**

------------------------------------------------------------------------

`Event`

PlayerPathScientistScanEnd (Deprecated)
---------------------------------------

------------------------------------------------------------------------

`Event`

PlayerPathScientistScanStart (Deprecated)
-----------------------------------------

------------------------------------------------------------------------

`Event`

PlayerPathShow
--------------

------------------------------------------------------------------------

`Event`

PlayerPathUpdate (Deprecated)
-----------------------------

------------------------------------------------------------------------

`Function`

CanExplorerShowHint()
---------------------

------------------------------------------------------------------------

`Function`

ExplorerApplyRelicSpell()
-------------------------

------------------------------------------------------------------------

`Function`

ExplorerShowHint()
------------------

### Description

Displays a hint for the passed path mission

------------------------------------------------------------------------

`Function`

GetCurrentEpisode()
-------------------

### Description

Returns the PathEpisode that is currently active for the player\
\

------------------------------------------------------------------------

`Function`

GetCurrentSettlerHubMission()
-----------------------------

------------------------------------------------------------------------

`Function`

GetCurrentSettlerInfrastructure()
---------------------------------

------------------------------------------------------------------------

`Function`

GetEpisodes()
-------------

### Description

Returns a table with all of the PathEpisodes where the player has
unlocked at least one PathMission\

------------------------------------------------------------------------

`Function`

GetInfrastructureStatusForMission()
-----------------------------------

------------------------------------------------------------------------

`Function`

GetPathEpisodeForZone()
-----------------------

### Description

Does a PushEpisodeInfo of the episode Id at the current zone.

------------------------------------------------------------------------

`Function`

GetPathLevel()
--------------

### Description

Returns the character's current path level\
\

------------------------------------------------------------------------

`Function`

GetPathLevelCap()
-----------------

------------------------------------------------------------------------

`Function`

GetPathLevelData(nLevel)
------------------------

### Description

Does a lua\_newtable with level, xp, and the rewards specified at
nLevel, or nil if null.

### Params

-   **nLevel** **(Integer)**

### Usage/Example

```lua
    test usage
```

### Remarks

a remark!

------------------------------------------------------------------------

`Function`

GetPathXP()
-----------

### Description

Returns the total path XP that the player has earned

------------------------------------------------------------------------

`Function`

GetPathXPAtLevel()
------------------

### Description

Returns the amount of path XP needed to reach a given path level\
\

------------------------------------------------------------------------

`Function`

GetPathXPForLevel()
-------------------

### Description

Returns the amount of path XP the player has earned during the current
path level

------------------------------------------------------------------------

`Function`

GetPathXPForNextLevel()
-----------------------

### Description

Does a lua\_pushinteger of the character's path xp for next level

------------------------------------------------------------------------

`Function`

GetPlayerPathType()
-------------------

### Description

Does a lua\_pushinteger of GetPathType, or nil if null.

------------------------------------------------------------------------

`Function`

GetScannerName()
----------------

------------------------------------------------------------------------

`Function`

GetSettlerHubValues()
---------------------

### Description

Does a lua\_newtable with an index, name, value, and max of a settler's
hub.

------------------------------------------------------------------------

`Function`

GetUnlockedPathLevelCap()
-------------------------

------------------------------------------------------------------------

`Function`

PathAction()
------------

------------------------------------------------------------------------

`Function`

PathAction2()
-------------

------------------------------------------------------------------------

`Function`

ScientistAllGetScanBotProfiles()
--------------------------------

------------------------------------------------------------------------

`Function`

ScientistGetScanBotProfile()
----------------------------

------------------------------------------------------------------------

`Function`

ScientistGetScanBotUnit()
-------------------------

------------------------------------------------------------------------

`Function`

ScientistHasScanBot()
---------------------

------------------------------------------------------------------------

`Function`

ScientistSetScanBotProfile()
----------------------------

------------------------------------------------------------------------

`Function`

ScientistToggleScanBot()
------------------------

------------------------------------------------------------------------

`Function`

SetScannerName()
----------------
