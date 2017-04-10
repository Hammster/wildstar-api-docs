Spinner
=======

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

SpinnerChanged
--------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **fNewValue** **(Float)**
-   **fOldValue** **(Float)**

------------------------------------------------------------------------

`Event`

SpinnerChanging
---------------

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

GetMax()
--------

------------------------------------------------------------------------

`Method`

GetMin()
--------

------------------------------------------------------------------------

`Method`

GetValue()
----------

### Description

Does a lua\_pushnumber of the caller's value as a float.

------------------------------------------------------------------------

`Method`

SetIncRates(tThresholdsAndRates)
--------------------------------

### Description

Sets the caller's rates to the entries in tThresholdsAndRates.

### Params

-   **tThresholdsAndRates** **(Table)**

------------------------------------------------------------------------

`Method`

SetMinMax(fMin, fMax, nNumDecimals)
-----------------------------------

### Description

Sets the caller's properties to fMin, fMax, and iNumDecimals.

### Params

-   **fMin** **(Float)**
-   **fMax** **(Float)**
-   **nNumDecimals** **(Integer)**

------------------------------------------------------------------------

`Method`

SetValue(fValue)
----------------

### Description

Sets the caller's value to fValue.

### Params

-   **fValue** **(Float)**
