Button
======

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

ButtonCheck
-----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)** - The mouse button being
    clicked.

------------------------------------------------------------------------

`Event`

ButtonDown
----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)** - The mouse button being
    clicked.

------------------------------------------------------------------------

`Event`

ButtonHoldBegin
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)** - The mouse button being
    clicked.

------------------------------------------------------------------------

`Event`

ButtonSignal
------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)** - The mouse button being
    clicked.

------------------------------------------------------------------------

`Event`

ButtonUncheck
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)** - The mouse button being
    clicked.

------------------------------------------------------------------------

`Event`

ButtonUp
--------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)** - The mouse button being
    clicked.

------------------------------------------------------------------------

`Event`

ButtonUpCancel
--------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)** - The mouse button being
    clicked.

------------------------------------------------------------------------

`Event`

QueryBeginDragDrop
------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Method`

AttachWindow()
--------------

------------------------------------------------------------------------

`Method`

ChangeArt(strButtonBase)
------------------------

### Description

Updates the art of the button. The art is updated if a button is passed.
The button's string is also updated with the passed parameter.

### Params

-   **strButtonBase** **(Varies - String or Button)**

------------------------------------------------------------------------

`Method`

GetContentId()
--------------

### Description

Does a lua\_pushinteger of the caller's content Id as an integer.

------------------------------------------------------------------------

`Method`

GetContentType()
----------------

### Description

Does a lua\_pushwstring of the caller's content type as a string.

------------------------------------------------------------------------

`Method`

IsChecked()
-----------

### Description

Does a lua\_pushboolean of the caller's IsChecked as a boolean.

------------------------------------------------------------------------

`Method`

SetCheck(bCheck)
----------------

### Description

Sets the caller's check to bCheck.

### Params

-   **bCheck** **(Bool)**

------------------------------------------------------------------------

`Method`

SetContentId(nContentId)
------------------------

### Description

Sets the caller's content id to uContentId.

### Params

-   **nContentId** **(Integer)**

------------------------------------------------------------------------

`Method`

SetContentType(strContentType)
------------------------------

### Description

Sets the caller's content type to sContentType.

### Params

-   **strContentType** **(String)**

------------------------------------------------------------------------

`Method`

SetDisabledTextColor(clr)
-------------------------

### Description

Sets the caller's m\_crStateText in the BS\_Disabled state to clr.

### Params

-   **clr** **([CColor](../Classes/CColor.md))**

------------------------------------------------------------------------

`Method`

SetFlybyTextColor(clr)
----------------------

### Description

Sets the caller's m\_crStateText in the BS\_Flyby state to clr.

### Params

-   **clr** **([CColor](../Classes/CColor.md))**

------------------------------------------------------------------------

`Method`

SetInnerMargin()
----------------

------------------------------------------------------------------------

`Method`

SetNormalTextColor(clr)
-----------------------

### Description

Sets the caller's m\_crStateText in the BS\_Normal state to clr.

### Params

-   **clr** **([CColor](../Classes/CColor.md))**

------------------------------------------------------------------------

`Method`

SetPressedFlybyTextColor(clr)
-----------------------------

### Description

Sets the caller's m\_crStateText in the BS\_PressedFlyby state to clr.

### Params

-   **clr** **([CColor](../Classes/CColor.md))**

------------------------------------------------------------------------

`Method`

SetPressedTextColor(clr)
------------------------

### Description

Sets the caller's m\_crStateText in the BS\_Pressed state to clr.

### Params

-   **clr** **([CColor](../Classes/CColor.md))**
