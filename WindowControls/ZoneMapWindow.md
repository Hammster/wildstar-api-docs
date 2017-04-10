ZoneMapWindow
=============

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Enum`

CodeEnumDisplayMode
-------------------

-   **SuperPanning**
-   **Panning**
-   **Scaled**
-   **Continent**
-   **World**
-   **SolarSystem**

------------------------------------------------------------------------

`Event`

ZoneMapWindowChange
-------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

ZoneMapWindowModeChange
-----------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Method`

AddLine()
---------

------------------------------------------------------------------------

`Method`

AddObject(tWorldLoc, strName, tInfo, tFlags)
--------------------------------------------

### Description

works like MiniMapWindow:AddObject, returns an id to the object

### Params

-   **tWorldLoc** **(WorldLocTable)** - World location to add the object
-   **strName** **(String)** - Name of the object
-   **tInfo** **(Table)**
-   **tFlags** **(Table)**

------------------------------------------------------------------------

`Method`

AddObjectByWorldLocId()
-----------------------

------------------------------------------------------------------------

`Method`

AddRegion()
-----------

------------------------------------------------------------------------

`Method`

AddUnit(unitId, tInfo, tFlags)
------------------------------

### Description

works like MiniMapWindow::AddUnit, returns an id to the object (which is
different than the unitId)

### Params

-   **unitId** **(Integer)**
-   **tInfo** **(Table)**
-   **tFlags** **(Table)**

### Return Value

-   **Integer** - id to the object (which is different than the unitId)

------------------------------------------------------------------------

`Method`

CanZoomZone()
-------------

------------------------------------------------------------------------

`Method`

CenterOnPlayer()
----------------

------------------------------------------------------------------------

`Method`

CreateOverlayType()
-------------------

------------------------------------------------------------------------

`Method`

GetAllLines()
-------------

------------------------------------------------------------------------

`Method`

GetAllNemesisRegionInfo()
-------------------------

------------------------------------------------------------------------

`Method`

GetAllSubZoneInfo()
-------------------

------------------------------------------------------------------------

`Method`

GetAllZoneInfo()
----------------

------------------------------------------------------------------------

`Method`

GetContinentInfo(strContinent)
------------------------------

### Description

return information (including a list of zones) of the continent referred
to by strContinent

### Params

-   **strContinent** **(String)** - The name of the continent

### Return Value

-   **Table**
    -   **Name** **(String)** - The name of the continent
    -   **arZones** **(Array of ZoneInfo)**

------------------------------------------------------------------------

`Method`

GetContinents()
---------------

### Description

return an array of continents

### Return Value

-   **Array of String**

------------------------------------------------------------------------

`Method`

GetContinentZoneInfo()
----------------------

------------------------------------------------------------------------

`Method`

GetCurrentContinentIndex()
--------------------------

------------------------------------------------------------------------

`Method`

GetDisplayMode()
----------------

### Description

return the current display mode (1=Panning, 2=Scaled, 3=Continent)

### Return Value

-   **EDisplayMode**

------------------------------------------------------------------------

`Method`

GetHexAtPoint(x, y)
-------------------

### Description

return the location of the hex in the given a point in the Window

### Params

-   **x** **(Integer)** - X position in the window
-   **y** **(Integer)** - Y position in the window

### Return Value

-   **Table** - x, y values for which hex is located at the specified
    point

------------------------------------------------------------------------

`Method`

GetHexGroupHexes()
------------------

------------------------------------------------------------------------

`Method`

GetLevelBandRegionInfo()
------------------------

------------------------------------------------------------------------

`Method`

GetLineInfo()
-------------

------------------------------------------------------------------------

`Method`

GetLinesAt()
------------

------------------------------------------------------------------------

`Method`

GetNecessaryHexCount()
----------------------

### Description

Does a lua\_pushinteger of the caller's m\_nCurrentNecessary.

------------------------------------------------------------------------

`Method`

GetNemesisRegionInfo()
----------------------

------------------------------------------------------------------------

`Method`

GetObjectRadius()
-----------------

------------------------------------------------------------------------

`Method`

GetObjectsAt(nPointX, nPointY)
------------------------------

### Description

Returns the results of PushRegionsAt nPointX and nPointY.

### Params

-   **nPointX** **(Integer)**
-   **nPointY** **(Integer)**

------------------------------------------------------------------------

`Method`

GetRegionsAt()
--------------

------------------------------------------------------------------------

`Method`

GetRevealedHexCount()
---------------------

### Description

Does a lua\_pushinteger of the caller's m\_nCurrentRevealed.

------------------------------------------------------------------------

`Method`

GetWorldLocAtPoint(x, y)
------------------------

### Description

return a table with x,y,z values for the world location at the
point(x,y). The y-component will be set to 0.0 and the z-component
represents the North/South axis.

### Params

-   **x** **(Integer)** - X position of a point in the window
-   **y** **(Integer)** - Y position of a point in the window

### Return Value

-   **WorldLocTable** - The world location in x,y, z. The y-component
    will be set to 0.0 and the z-component represents the North/South
    axis.

------------------------------------------------------------------------

`Method`

GetZoneInfo(nZone)
------------------

### Description

Does a lua\_newtable with the zone corresponding to nZone with its Name,
Index, North, South, East, and West.

### Params

-   **nZone** **(Integer)**

------------------------------------------------------------------------

`Method`

HideObjectsByType()
-------------------

------------------------------------------------------------------------

`Method`

HideObjectsByUserData()
-----------------------

------------------------------------------------------------------------

`Method`

HideRegionsByType()
-------------------

------------------------------------------------------------------------

`Method`

HideRegionsByUserData()
-----------------------

------------------------------------------------------------------------

`Method`

HighlightRegionsByType()
------------------------

------------------------------------------------------------------------

`Method`

HighlightRegionsByUserData()
----------------------------

------------------------------------------------------------------------

`Method`

IsShowingGhostWindow()
----------------------

------------------------------------------------------------------------

`Method`

IsShowLabelsOn()
----------------

### Description

Does a lua\_pushboolean if labels are on.

------------------------------------------------------------------------

`Method`

IsShowPlayerOn()
----------------

------------------------------------------------------------------------

`Method`

IsZoneReady()
-------------

### Description

Does a lua\_pushboolean if the caller's zone is ready.

------------------------------------------------------------------------

`Method`

RemoveAllLines()
----------------

------------------------------------------------------------------------

`Method`

RemoveAllObjects()
------------------

### Description

Runs the caller's RemoveAllRegionsByType method on
MapOverlay\_UserDefined.

------------------------------------------------------------------------

`Method`

RemoveAllRegions()
------------------

------------------------------------------------------------------------

`Method`

RemoveLine()
------------

------------------------------------------------------------------------

`Method`

RemoveObject(idObject)
----------------------

### Description

will remove the object that matches the idObject (including a unit)

### Params

-   **idObject** **(Integer)** - ID of the object

------------------------------------------------------------------------

`Method`

RemoveObjectsByType()
---------------------

------------------------------------------------------------------------

`Method`

RemoveObjectsByUserData()
-------------------------

------------------------------------------------------------------------

`Method`

RemoveRegionByType()
--------------------

------------------------------------------------------------------------

`Method`

RemoveRegionByUserData()
------------------------

------------------------------------------------------------------------

`Method`

RemoveUnit(idUnit)
------------------

### Description

remove the unit that matches the idUnit (could be redundant since you
can store the idObject and use that to remove the unit)

### Params

-   **idUnit** **(Integer)** - ID of the unit to be removed

------------------------------------------------------------------------

`Method`

SetActiveHexEdgeSprite()
------------------------

------------------------------------------------------------------------

`Method`

SetActiveHexSprite()
--------------------

------------------------------------------------------------------------

`Method`

SetDisplayMode(eMode)
---------------------

### Description

set the display mode to eMode (1=Panning, 2=Scaled, 3=Continent)

### Params

-   **eMode** **(EDisplayMode)** - The display mode to be changed to

------------------------------------------------------------------------

`Method`

SetGhostWindow()
----------------

------------------------------------------------------------------------

`Method`

SetInactiveHexEdgeSprite()
--------------------------

------------------------------------------------------------------------

`Method`

SetInactiveHexSprite()
----------------------

------------------------------------------------------------------------

`Method`

SetLabelBackerSprite()
----------------------

------------------------------------------------------------------------

`Method`

SetLabelTextColor()
-------------------

------------------------------------------------------------------------

`Method`

SetLineColor()
--------------

------------------------------------------------------------------------

`Method`

SetMaxDisplayMode()
-------------------

------------------------------------------------------------------------

`Method`

SetMinDisplayMode()
-------------------

------------------------------------------------------------------------

`Method`

SetObjectRadius()
-----------------

------------------------------------------------------------------------

`Method`

SetObjectsVisibility()
----------------------

------------------------------------------------------------------------

`Method`

SetOverlayTypeInfo()
--------------------

------------------------------------------------------------------------

`Method`

SetPlayerArrowSprite(strSpriteName)
-----------------------------------

### Description

Sets the sprite used for representing the player on the map

### Params

-   **strSpriteName** **(String)** - The name of the sprite to be used

------------------------------------------------------------------------

`Method`

SetZone(nZone)
--------------

### Params

-   **nZone** **(Integer)**

------------------------------------------------------------------------

`Method`

ShowLabels(bShowLabels)
-----------------------

### Params

-   **bShowLabels** **(Boolean)**

------------------------------------------------------------------------

`Method`

ShowLevelBandLabels()
---------------------

------------------------------------------------------------------------

`Method`

ShowObjectsByType()
-------------------

------------------------------------------------------------------------

`Method`

ShowObjectsByUserData()
-----------------------

------------------------------------------------------------------------

`Method`

ShowPlayer()
------------

------------------------------------------------------------------------

`Method`

ShowRegionsByType()
-------------------

------------------------------------------------------------------------

`Method`

ShowRegionsByUserData()
-----------------------

------------------------------------------------------------------------

`Method`

TogglePOIs()
------------

------------------------------------------------------------------------

`Method`

UnhighlightRegionsByType()
--------------------------

------------------------------------------------------------------------

`Method`

UnhighlightRegionsByUserData()
------------------------------
