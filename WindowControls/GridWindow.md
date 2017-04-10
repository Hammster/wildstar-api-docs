GridWindow
==========

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

GridDoubleClick
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **iRow** **(Integer)**
-   **iCol** **(Integer)**

------------------------------------------------------------------------

`Event`

GridSelChange
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **iRow** **(Integer)**
-   **iCol** **(Integer)**

------------------------------------------------------------------------

`Event`

GridSelChanging
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **iRow** **(Integer)**
-   **iCol** **(Integer)**
-   **iCurrRow** **(Integer)**
-   **iCurrCol** **(Integer)**
-   **bAllowChange** **(Boolean)**

------------------------------------------------------------------------

`Event`

GridSort
--------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **iCol** **(Integer)**

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

`Method`

AddRow(strText, strImage, newLuaData)
-------------------------------------

### Description

Adds a row to the caller. If newLuaData is set, this will push it on the
stack and ref it as well.

### Params

-   **strText** **(String)**
-   **strImage** **(String)** - (Default value: '')
-   **newLuaData** **(LuaData)** - (Default value: LUA\_NOREF)

------------------------------------------------------------------------

`Method`

DeleteAll()
-----------

### Description

Deletes all rows and resets the count, current selection, the focus, and
the tooltip.

------------------------------------------------------------------------

`Method`

DeleteRow(nRow)
---------------

### Description

Deletes the row at iRow if found and updates the caller's rowMax.

### Params

-   **nRow** **(UINT)**

------------------------------------------------------------------------

`Method`

DeleteRowsByData(luaData)
-------------------------

### Description

Deletes the row that lua\_equals luaData if found and updates the
caller's rowMax.

### Params

-   **luaData** **(LuaData)**

------------------------------------------------------------------------

`Method`

EnableCell(nRow, nCol, newEnable)
---------------------------------

### Description

Sets the enable of the caller's cell at iRow and iCol to newEnable.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**
-   **newEnable** **(bool)**

------------------------------------------------------------------------

`Method`

EnableRow(nRow, newEnable)
--------------------------

### Description

Sets all enable of all the caller's cell at iRow to newEnable.

### Params

-   **nRow** **(Integer)**
-   **newEnable** **(bool)**

------------------------------------------------------------------------

`Method`

EnsureCellVisible(nRow, nCol)
-----------------------------

### Description

Insures the right, left, bottom, and top of the caller's cell at iRow
and iCol are visible in the clip area.\
Updates the HScrollPos and VScrollPos.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**

------------------------------------------------------------------------

`Method`

GetCellData()
-------------

------------------------------------------------------------------------

`Method`

GetCellLuaData()
----------------

------------------------------------------------------------------------

`Method`

GetCellText()
-------------

------------------------------------------------------------------------

`Method`

GetColumnCount()
----------------

### Description

Does a lua\_pushinteger of the caller's column count as an integer.

------------------------------------------------------------------------

`Method`

GetColumnWidth()
----------------

------------------------------------------------------------------------

`Method`

GetCurrentColumn()
------------------

### Description

Does a lua\_pushinteger of the caller's current column as an integer,
will do a lua\_pushnil if the current column is -1.

------------------------------------------------------------------------

`Method`

GetCurrentRow()
---------------

### Description

Does a lua\_pushinteger of the caller's current row as an integer, will
do a lua\_pushnil if the current row is -1.

------------------------------------------------------------------------

`Method`

GetFocusColumn()
----------------

### Description

Does a lua\_pushinteger of the caller's focus column as an integer, will
do a lua\_pushnil if the focus column is -1.

------------------------------------------------------------------------

`Method`

GetFocusRow()
-------------

### Description

Does a lua\_pushinteger of the caller's focus row as an integer, will do
a lua\_pushnil if the focus row is -1.

------------------------------------------------------------------------

`Method`

GetRowCount()
-------------

### Description

Does a lua\_pushinteger of the caller's row count as an integer.

------------------------------------------------------------------------

`Method`

GetSortColumn()
---------------

------------------------------------------------------------------------

`Method`

HitTest(ptX, ptY)
-----------------

### Description

Determines if ptX and ptY are a validCell of the caller and determines
the iRow and iCol if possible.

### Params

-   **ptX** **(Integer)**
-   **ptY** **(Integer)**

------------------------------------------------------------------------

`Method`

IsCellSelected(nRow, nCol)
--------------------------

### Description

Does a lua\_pushboolean if the caller's cell at iRow and iCol is
selected.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**

------------------------------------------------------------------------

`Method`

IsSortAscending()
-----------------

------------------------------------------------------------------------

`Method`

SelectCell(nRow, nCol)
----------------------

### Description

Selects the caller's cell at iRow and iCol.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**

------------------------------------------------------------------------

`Method`

SelectCellByData(bEqual, bFireEvent)
------------------------------------

### Description

Scans through the caller's cells trying to match bEqual. If a match is
found and bFireEvent is true, the cell is selected.

### Params

-   **bEqual** **(bool)**
-   **bFireEvent** **(bool)**

------------------------------------------------------------------------

`Method`

SetCellBGBase()
---------------

------------------------------------------------------------------------

`Method`

SetCellData(nRow, nCol, strText, strImage, newLuaData)
------------------------------------------------------

### Description

Sets the data at the caller's cell at iRow and iCol to sText, sImage,
and luaData. If newLuaData is set, this will push it on the stack and
ref it as well.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**
-   **strText** **(String)**
-   **strImage** **(String)** - (Default value: '')
-   **newLuaData** **(LuaData)** - (Default value: LUA\_NOREF)

------------------------------------------------------------------------

`Method`

SetCellDoc(nRow, nCol, strText)
-------------------------------

### Description

Loads an xml document into buffer at sText, then sets the caller's cell
at iRow and iCol to the document, creating a new one if not allocated.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**
-   **strText** **(String)**

------------------------------------------------------------------------

`Method`

SetCellIconOverlays(nRow, nCol, strLeft, strRight)
--------------------------------------------------

### Description

Sets the icon overlay at the caller's cell at iRow and iCol to strLeft
and strRight.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**
-   **strLeft** **(String)** - (Default value: '')
-   **strRight** **(String)** - (Default value: '')

------------------------------------------------------------------------

`Method`

SetCellImage(nRow, nCol, strImage)
----------------------------------

### Description

Sets the cellimage of the caller's cell at iRow and iCol to sImage.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**
-   **strImage** **(String)**

------------------------------------------------------------------------

`Method`

SetCellImageColor()
-------------------

------------------------------------------------------------------------

`Method`

SetCellLuaData()
----------------

------------------------------------------------------------------------

`Method`

SetCellSortText()
-----------------

------------------------------------------------------------------------

`Method`

SetCellText(nRow, nCol, strText)
--------------------------------

### Description

Sets the celltext of the caller's cell at iRow and iCol to sText.

### Params

-   **nRow** **(Integer)**
-   **nCol** **(Integer)**
-   **strText** **(String)**

------------------------------------------------------------------------

`Method`

SetColumnText(nCol, strText)
----------------------------

### Description

Sets the column text of the caller's cell at iCol to sText.

### Params

-   **nCol** **(Integer)**
-   **strText** **(String)**

------------------------------------------------------------------------

`Method`

SetColumnWidth()
----------------

------------------------------------------------------------------------

`Method`

SetCurrentColumn(nCol)
----------------------

### Description

Sets the selection to caller's column at iCol.

### Params

-   **nCol** **(Integer)**

------------------------------------------------------------------------

`Method`

SetCurrentRow(nRow)
-------------------

### Description

Sets the selection to caller's column at iRow.

### Params

-   **nRow** **(Integer)**

------------------------------------------------------------------------

`Method`

SetHeaderBGBase()
-----------------

------------------------------------------------------------------------

`Method`

SetSortColumn()
---------------
