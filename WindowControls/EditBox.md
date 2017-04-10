EditBox
=======

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

EditBoxChanged
--------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strText** **(String)** - The new text

------------------------------------------------------------------------

`Event`

EditBoxChanging
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strNewText** **(String)**
-   **strOldText** **(String)**
-   **bAllowed** **(Boolean)**

------------------------------------------------------------------------

`Event`

EditBoxEscape
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

EditBoxReturn
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strText** **(String)**

------------------------------------------------------------------------

`Event`

EditBoxTab
----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strText** **(String)**

------------------------------------------------------------------------

`Event`

EditBoxTextTooLarge
-------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Method`

AddHistoryString(strHistoryString)
----------------------------------

### Description

Adds to the caller's string list the parameter sHistoryString.

### Params

-   **strHistoryString** **(String)**

------------------------------------------------------------------------

`Method`

AddLink()
---------

------------------------------------------------------------------------

`Method`

ClearHistoryStrings()
---------------------

### Description

Clears the caller's string list.

------------------------------------------------------------------------

`Method`

ClearText()
-----------

### Description

Sets the caller's text to null then collapses and moves the caller's
window rectangle.

------------------------------------------------------------------------

`Method`

CopyTextToClipboard() (Deprecated)
----------------------------------

### Description

Calls OnCopy() which copies the caller's text to clipboard.

------------------------------------------------------------------------

`Method`

GetAllLinks()
-------------

------------------------------------------------------------------------

`Method`

GetHistoryStrings()
-------------------

### Description

Does a lua push of the caller's string list count number and string.

------------------------------------------------------------------------

`Method`

GetMaxTextLength()
------------------

------------------------------------------------------------------------

`Method`

GetSel()
--------

------------------------------------------------------------------------

`Method`

GetText()
---------

### Description

Does a lua\_pushwstring of the caller's m\_pText as a string.

------------------------------------------------------------------------

`Method`

HitTest()
---------

------------------------------------------------------------------------

`Method`

InsertText()
------------

------------------------------------------------------------------------

`Method`

PasteTextFromClipboard()
------------------------

### Description

Calls OnPaste() which pastes the clipboard's contents into the caller's
text.

------------------------------------------------------------------------

`Method`

RemoveLinks()
-------------

------------------------------------------------------------------------

`Method`

SetMaxTextLength()
------------------

------------------------------------------------------------------------

`Method`

SetPrompt()
-----------

------------------------------------------------------------------------

`Method`

SetPromptColor()
----------------

------------------------------------------------------------------------

`Method`

SetSel(nBegin, nEnd)
--------------------

### Description

Sets the caller's selection range starting with iBegin and ending with
iEnd.

### Params

-   **nBegin** **(Integer)**
-   **nEnd** **(Integer)**

------------------------------------------------------------------------

`Method`

SetText(strText)
----------------

### Description

Sets the caller's text to sText.

### Params

-   **strText** **(String)**
