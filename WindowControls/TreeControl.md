TreeControl
===========

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

QueryBeginClickStick
--------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

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

`Event`

TreeDoubleClick
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **hNode** **(Handle)**

------------------------------------------------------------------------

`Event`

TreeNodeCollapse
----------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **hNode** **(Handle)**

------------------------------------------------------------------------

`Event`

TreeNodeExpand
--------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **hNode** **(Handle)**

------------------------------------------------------------------------

`Event`

TreeSelectionChanged
--------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **hSelected** **(Handle)**
-   **hPrevSelected** **(Handle)**

------------------------------------------------------------------------

`Event`

TreeSelectionChanging
---------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **hNode** **(Handle)**
-   **hSelected** **(Handle)**
-   **bAllowed** **(Boolean)**

------------------------------------------------------------------------

`Method`

AddNode(hParentHandle, strText, strImage, newLuaData)
-----------------------------------------------------

### Description

Adds a node to the caller. If newLuaData is set, this will push it on
the stack and ref it as well.\
Does a lua\_pushinteger of the node's handle back on the stack as an
integer.

### Params

-   **hParentHandle** **(Handle)**
-   **strText** **(String)**
-   **strImage** **(String)** - (Default value: "")
-   **newLuaData** **(LuaData)** - (Default value: LUA\_NOREF)

------------------------------------------------------------------------

`Method`

CollapseNode(hNodeHandle)
-------------------------

### Description

Collapses the node in the caller corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

DeleteAll()
-----------

### Description

Deletes all of the caller's nodes.

------------------------------------------------------------------------

`Method`

DeleteChildren(hNodeHandle)
---------------------------

### Description

Deletes the children of the node corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

DeleteNode(hNodeHandle)
-----------------------

### Description

Deletes the node corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

ExpandNode(hNodeHandle)
-----------------------

### Description

Expands the node corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

GetColumnWidth()
----------------

------------------------------------------------------------------------

`Method`

GetFirstChildNode(hNodeHandle)
------------------------------

### Description

Does a lua\_pushinteger of the first child node's ID as an integer
corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

GetFirstVisibleNode(hNodeHandle)
--------------------------------

### Description

Does a lua\_pushinteger of the first visible node's ID as an integer
corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

GetNextSibling(hNodeHandle)
---------------------------

### Description

Does a lua\_pushinteger of the next sibling node's ID as an integer
corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

GetNextVisibleNode(hNodeHandle)
-------------------------------

### Description

Does a lua\_pushinteger of the next visible node's ID as an integer
corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

GetNodeData(hNodeHandle)
------------------------

### Description

Does a lua\_rawgeti of the node's data corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

GetNodeText(hNodeHandle)
------------------------

### Description

Does a lua\_pushstring of the node's text corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

GetParentNode(hNodeHandle)
--------------------------

### Description

Does a lua\_pushinteger of the parent node's ID as an integer
corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**

------------------------------------------------------------------------

`Method`

GetSelectedNode()
-----------------

### Description

Does a lua\_pushinteger of the node's ID of the selected node.

------------------------------------------------------------------------

`Method`

HitTest(nXpos, nYpos)
---------------------

### Description

Does a lua\_pushinteger of the node's ID at iXpos and iYpos as an
integer.\
Does a lua\_pushboolean of the test's result if a button was hit as a
boolean.

### Params

-   **nXpos** **(Integer)**
-   **nYpos** **(Integer)**

------------------------------------------------------------------------

`Method`

NodeHasChildren()
-----------------

### Description

Does a lua\_pushboolean of the node's HasChildren corresponding to
hNodeHandle.\
Paramaters:\
hNodeHandle: Integer

------------------------------------------------------------------------

`Method`

SelectNode(hNodeHandle)
-----------------------

### Description

Selects the node corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)** - (Default value: 0)

------------------------------------------------------------------------

`Method`

SetColumnWidth(nCol, nWidth)
----------------------------

### Description

Sets the caller's nWidth of the column corresponding to iCol.

### Params

-   **nCol** **(Integer)**
-   **nWidth** **(Integer)**

------------------------------------------------------------------------

`Method`

SetHeaderImage()
----------------

------------------------------------------------------------------------

`Method`

SetHeaderText()
---------------

------------------------------------------------------------------------

`Method`

SetHeaderTextColor()
--------------------

------------------------------------------------------------------------

`Method`

SetMinimumNodeHeight(hNodeHandle, nMinHeight)
---------------------------------------------

### Description

Sets the MinimumNodeHeight to iMinHeight of the node corresponding to
hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**
-   **nMinHeight** **(Handle)**

------------------------------------------------------------------------

`Method`

SetNodeImage(hNodeHandle, strText)
----------------------------------

### Description

Sets the Image to sText of the node corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**
-   **strText** **(String)**

------------------------------------------------------------------------

`Method`

SetNodeText(hNodeHandle, strText)
---------------------------------

### Description

Sets the Text to sText of the node corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**
-   **strText** **(String)**

------------------------------------------------------------------------

`Method`

SetNodeTextColor(hNodeHandle, clr)
----------------------------------

### Description

Sets the color to clr of the node corresponding to hNodeHandle.

### Params

-   **hNodeHandle** **(Handle)**
-   **clr** **([CColor](../Classes/CColor.md))**
