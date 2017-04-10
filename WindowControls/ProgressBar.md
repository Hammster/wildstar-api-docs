ProgressBar
===========

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Method`

EnableGlow(bEdgeGlow)
---------------------

### Description

Enables the caller's glow if bEdgeGlow is true.

### Params

-   **bEdgeGlow** **(Boolean)**

------------------------------------------------------------------------

`Method`

GetClipPoints()
---------------

------------------------------------------------------------------------

`Method`

GetFloor()
----------

------------------------------------------------------------------------

`Method`

GetMax()
--------

------------------------------------------------------------------------

`Method`

GetProgress()
-------------

------------------------------------------------------------------------

`Method`

SetBarColor(clr)
----------------

### Description

Sets the caller's bar color to clr.

### Params

-   **clr** **([CColor](../Classes/CColor.md))**

------------------------------------------------------------------------

`Method`

SetClipPoints()
---------------

------------------------------------------------------------------------

`Method`

SetEmptySprite(strText)
-----------------------

### Description

Sets the caller's empty sprite to sText.

### Params

-   **strText** **(String)** - (Default value: "")

------------------------------------------------------------------------

`Method`

SetFillSprite(strText)
----------------------

### Description

Sets the caller's fill sprite to sText.

### Params

-   **strText** **(String)** - (Default value: "")

------------------------------------------------------------------------

`Method`

SetFloor(fFloor)
----------------

### Description

Sets the caller's floor to fFloor.

### Params

-   **fFloor** **(Float)**

------------------------------------------------------------------------

`Method`

SetFullSprite(strText)
----------------------

### Description

Sets the caller's full sprite to sText.

### Params

-   **strText** **(String)** - (Default value: "")

------------------------------------------------------------------------

`Method`

SetGlowSprite(strText)
----------------------

### Description

Sets the caller's glow sprite to sText.

### Params

-   **strText** **(String)** - (Default value: "")

------------------------------------------------------------------------

`Method`

SetMax(fMax)
------------

### Description

Sets the caller's max to fMax.

### Params

-   **fMax** **(Float)**

------------------------------------------------------------------------

`Method`

SetProgress(fProgress, fRate)
-----------------------------

### Description

Sets the caller's progress to fProgress and the rate to fRate.

### Params

-   **fProgress** **(Float)**
-   **fRate** **(Float)** - (Default value: 0.0)

------------------------------------------------------------------------

`Method`

SetRadialMax()
--------------

------------------------------------------------------------------------

`Method`

SetRadialMin()
--------------

------------------------------------------------------------------------

`Method`

SetTickLocations(nTickCount, fTickLoc)
--------------------------------------

### Description

Sets the tick locations of the progress bar with iTickCount being the
number of ticks and each parameter afterwards being an fTickLoc that
indicates the location of a tick.

### Params

-   **nTickCount** **(Integer - Every parameter after iTickCount will be
    an fTickLoc)**
-   **fTickLoc** **(Float)** - (Default value: 0.0)

------------------------------------------------------------------------

`Method`

SetTickSprites(strOff, strOn)
-----------------------------

### Description

Sets the caller's m\_sprTickOff Info to sOff and m\_sprTickOn Info to
sOn.

### Params

-   **strOff** **(String)** - (Default value: "")
-   **strOn** **(String)** - (Default value: sOff)
