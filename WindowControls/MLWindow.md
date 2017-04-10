MLWindow
========

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

MLNodeClick
-----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Method`

BeginDoogie(fRate)
------------------

### Description

Starts printing text character by character at a rate of fRate.

### Params

-   **fRate** **(Float)** - (Default value: 50.f)

------------------------------------------------------------------------

`Method`

GetContentSize()
----------------

### Description

Does lua\_pushintegers of the caller's size.x and size.y as integers.

------------------------------------------------------------------------

`Method`

IsReadyToDraw()
---------------

### Description

Does a lua\_pushboolean if there is a wait for load as a boolean.

------------------------------------------------------------------------

`Method`

PauseDoogie(bPauseDoogie)
-------------------------

### Description

Pauses a character by character text printing animation if bPauseDoogie
is true.

### Params

-   **bPauseDoogie** **(Bool)**

------------------------------------------------------------------------

`Method`

SetAML(strAMLString)
--------------------

### Description

Sets the caller's m\_doc's text to a UTF8ToUCS2 conversion of
sAMLString.

### Params

-   **strAMLString** **(String)**

------------------------------------------------------------------------

`Method`

SetDoc(pDoc)
------------

### Description

Sets the caller's m\_doc's doc to pDoc and parses the doc.

### Params

-   **pDoc** **(XmlDocumentRef)**

------------------------------------------------------------------------

`Method`

SetHeightToContentHeight(nBuffer)
---------------------------------

### Description

Sets the caller's height size to iBuffer. Does lua\_pushintegers of the
caller's size.x and size.y as integers.

### Params

-   **nBuffer** **(INT32)**

------------------------------------------------------------------------

`Method`

StopDoogie()
------------

### Description

Stops a character by character text printing animation.
