MiniMapWindow
=============

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Method`

AddLine()
---------

------------------------------------------------------------------------

`Method`

AddObject(eType, tLoc, strName, tInfo, tFlags, oUnit)
-----------------------------------------------------

### Description

Does a lua\_pushinteger describing the result of the AddObject call.

### Params

-   **eType** **(Integer)**
-   **tLoc** **(Table)** - Contains the x, y, and z coordinates for the
    object to be placed
    -   **nX** **(Integer)** - The X coordinate where the object will be
        placed
    -   **nY** **(Integer)** - The Y coordinate where the object will be
        placed
    -   **nZ** **(Integer)** - The Z coordinate where the object will be
        placed
-   **strName** **(String)** - The name of the object
-   **tInfo** **(MMODisplayInfo)** - Determines what the object will
    look like on the minimap
-   **tFlags** **(Table)** - A set of flags determining how the object
    should be drawn
-   **oUnit** **(Object)** - The game object that is tied to the object
    on the minimap

------------------------------------------------------------------------

`Method`

AddPathIndicator()
------------------

### Description

No implementation yet

------------------------------------------------------------------------

`Method`

AddQuestIndicator(pQuest, strNum, iInfo, tCheckFlag)
----------------------------------------------------

### Params

-   **pQuest** **(LuaQuest)**
-   **strNum** **(String)** - (Default value: "")
-   **iInfo** **(MMODisplayInfo)**
-   **tCheckFlag** **(Used immediate in a CheckFlag call)**

------------------------------------------------------------------------

`Method`

AddUnit(pUnit, iInfo, tCheckFlag)
---------------------------------

### Description

Does a lua\_pushinteger describing the result of the AddUnit call.

### Params

-   **pUnit** **(CUnit)**
-   **iInfo** **(MMODisplayInfo)**
-   **tCheckFlag** **(Table)** - Used immediately in a CheckFlag call

------------------------------------------------------------------------

`Method`

ClientPointToWorldLoc(nPointX, nPointY)
---------------------------------------

### Description

Does a lua\_newtable with x, y, and z.

### Params

-   **nPointX** **(Integer)**
-   **nPointY** **(Integer)**

------------------------------------------------------------------------

`Method`

CreateOverlayType()
-------------------

------------------------------------------------------------------------

`Method`

GetLineInfo()
-------------

------------------------------------------------------------------------

`Method`

GetObjectsAtPoint(nPointX, nPointY)
-----------------------------------

### Description

Returns the results of PushObjectsAtPoint nPointX and nPointY.

### Params

-   **nPointX** **(Integer)**
-   **nPointY** **(Integer)**

------------------------------------------------------------------------

`Method`

GetZoomLevel()
--------------

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

RemoveAllLines()
----------------

------------------------------------------------------------------------

`Method`

RemoveAllObjects()
------------------

------------------------------------------------------------------------

`Method`

RemoveLine()
------------

------------------------------------------------------------------------

`Method`

RemoveObject(nObjectId)
-----------------------

### Params

-   **nObjectId** **(Integer)**

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

RemoveUnit(pUnitHandle)
-----------------------

### Params

-   **pUnitHandle** **(CUnitHandle)**

------------------------------------------------------------------------

`Method`

SetMapOrientation(nOrient)
--------------------------

### Params

-   **nOrient** **(EMiniMapOrientation)**

------------------------------------------------------------------------

`Method`

SetZoomLevel()
--------------

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

ZoomIn()
--------

### Description

Runs the caller's Zoom In method.

------------------------------------------------------------------------

`Method`

ZoomOut()
---------

### Description

Runs the caller's Zoom Out method.
