SliderBar
=========

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

SliderBarChanged
----------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **fNewValue** **(Float)**
-   **fOldValue** **(Float)**

------------------------------------------------------------------------

`Event`

SliderBarChanging
-----------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **fNewValue** **(Float)**
-   **fOldValue** **(Float)**
-   **bOkToChange** **(Boolean)**

------------------------------------------------------------------------

`Method`

GetValue()
----------

### Description

Does a lua\_pushnumber of the caller's value as a float.

------------------------------------------------------------------------

`Method`

IsThumbDragging()
-----------------

------------------------------------------------------------------------

`Method`

SetMinMax(fMin, fMax, fTickAmount)
----------------------------------

### Description

Sets the caller's properties to fMin, fMax, and fTickAmount.

### Params

-   **fMin** **(Float)**
-   **fMax** **(Float)**
-   **fTickAmount** **(Float)** - (Default value: 1)

------------------------------------------------------------------------

`Method`

SetValue(fValue)
----------------

### Description

Set the caller's value to fValue.

### Params

-   **fValue** **(Float)**
