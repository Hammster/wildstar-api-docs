Window
======

### Prefix: wnd

Table of Content
----------------

<!-- toc -->

------------------------------------------------------------------------

`Enum`

CodeEnumArrangeOrigin
---------------------

-   **LeftOrTop**
-   **Middle**
-   **RightOrBottom**

------------------------------------------------------------------------

`Enum`

MoveMethod
----------

-   **Nothing**
-   **Simple**
-   **EaseInSine**
-   **EaseOutSine**
-   **EaseInOutSine**
-   **EaseInQuad**
-   **EaseOutQuad**
-   **EaseInOutQuad**
-   **EaseInCubic**
-   **EaseOutCubic**
-   **EaseInOutCubic**
-   **EaseInQuart**
-   **EaseOutQuart**
-   **EaseInOutQuart**
-   **EaseInQuint**
-   **EaseOutQuint**
-   **EaseInOutQuint**
-   **EaseInExpo**
-   **EaseOutExpo**
-   **EaseInOutExpo**
-   **EaseInCirc**
-   **EaseOutCirc**
-   **EaseInOutCirc**
-   **EaseInBack**
-   **EaseOutBack**
-   **EaseInOutBack**

------------------------------------------------------------------------

`Event`

AnimEnded
---------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strAnimDataId** **(String)**

------------------------------------------------------------------------

`Event`

AnimStarted
-----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strAnimDataId** **(String)**

------------------------------------------------------------------------

`Event`

AnimStopped
-----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strAnimDataId** **(String)**

------------------------------------------------------------------------

`Event`

DragDrop
--------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **x** **(Integer)**
-   **y** **(Integer)**
-   **wndSource** **([Window](../WindowControls/Window.md))**
-   **strType** **(String)**
-   **iData** **(Integer)**
-   **bDragDropHasBeenReset** **(Boolean)**

------------------------------------------------------------------------

`Event`

DragDropCancel
--------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strType** **(String)**
-   **iData** **(Integer)**
-   **eReason** **(EDragDropCancelReason)**
-   **bDragDropHasBeenReset** **(Boolean)**

------------------------------------------------------------------------

`Event`

DragDropClear
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

DragDropEnd
-----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strType** **(String)**
-   **iData** **(Integer)**
-   **bDragDropHasBeenReset** **(Boolean)**

------------------------------------------------------------------------

`Event`

DragDropNothingCursor
---------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strType** **(String)**
-   **iData** **(Integer)**

------------------------------------------------------------------------

`Event`

DragDropTargetNotify
--------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **bMe** **(Boolean)**

------------------------------------------------------------------------

`Event`

GenerateTooltip
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eToolTipType** **(EToolTipType)**
-   **x** **(Integer)**
-   **y** **(Integer)**

------------------------------------------------------------------------

`Event`

MouseButtonDown
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)**
-   **nLastRelativeMouseX** **(Integer)**
-   **nLastRelativeMouseY** **(Integer)**
-   **bDoubleClick** **(Boolean)**
-   **bStopPropagation** **(Boolean)**

------------------------------------------------------------------------

`Event`

MouseButtonUp
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **eMouseButton** **(EMouseButton)**
-   **nLastRelativeMouseX** **(Integer)**
-   **nLastRelativeMouseY** **(Integer)**

------------------------------------------------------------------------

`Event`

MouseEnter
----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **x** **(Integer)**
-   **y** **(Integer)**

------------------------------------------------------------------------

`Event`

MouseExit
---------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **x** **(Integer)**
-   **y** **(Integer)**

------------------------------------------------------------------------

`Event`

MouseMove
---------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **nLastRelativeMouseX** **(Integer)**
-   **nLastRelativeMouseY** **(Integer)**

------------------------------------------------------------------------

`Event`

MouseWheel
----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **nLastRelativeMouseX** **(Integer)**
-   **nLastRelativeMouseY** **(Integer)**
-   **fScrollAmount** **(Float)**
-   **bConsumeMouseWheel** **(Boolean)**

------------------------------------------------------------------------

`Event`

QueryBeginClickStick (Deprecated)
---------------------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **x** **(Integer)**
-   **y** **(Integer)**
-   **bClickStickStarted** **(Boolean)**

------------------------------------------------------------------------

`Event`

QueryBeginDragDrop (Deprecated)
-------------------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **x** **(Integer)**
-   **y** **(Integer)**
-   **bDragDropStarted** **(Boolean)**

------------------------------------------------------------------------

`Event`

QueryCursor
-----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

QueryDragDrop
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **x** **(Integer)**
-   **y** **(Integer)**
-   **wndSource** **([Window](../WindowControls/Window.md))**
-   **strType** **(String)**
-   **iData** **(Integer)**
-   **eResult** **(EDragDropQueryResult)**

------------------------------------------------------------------------

`Event`

TopLevelWindowMove
------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

UDE
---

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowClosed
------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowGainedFocus (Deprecated)
------------------------------

### Description

Fires when a window gains focus

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowHide
----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowKeyDown
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **strKeyName** **(String)**
-   **nScanCode** **(Integer)**
-   **nMetakeys** **(Integer)**

------------------------------------------------------------------------

`Event`

WindowKeyEscape
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowKeyReturn
---------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowKeyTab
------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowLoad
----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowLostFocus (Deprecated)
----------------------------

### Description

Fires when a window lost focus

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowMove
----------

### Description

When a window is moved

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **nOldLeft** **(Integer)** - The left x position before the move
-   **nOldTop** **(Integer)** - The top y position before the move
-   **nOldRight** **(Integer)** - The right x position before the move
-   **nOldBottom** **(Integer)** - The bottome y position before the
    move

------------------------------------------------------------------------

`Event`

WindowShow
----------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowSizeChanged
-----------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Event`

WindowToFront
-------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **bOkToBringToFront** **(Boolean)**

------------------------------------------------------------------------

`Event`

WindowTransitionComplete
------------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Function`

is()
----

------------------------------------------------------------------------

`Method`

\_\_eq() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

AddEventHandler()
-----------------

------------------------------------------------------------------------

`Method`

AddPixie(iLayer, bLine, bRestart, strText, strFont, flagsText, fWidth, strSprite, fRotation, loc, cr, crText)
-------------------------------------------------------------------------------------------------------------

### Params

-   **iLayer** **(Integer)** - The pixie layer that the picie should be
    created at
-   **bLine** **(Boolean)** - Draws the pixie as a line
-   **bRestart** **(Boolean)**
-   **strText** **(String)** - The text to add to the pixie
-   **strFont** **(String)** - The font to use for the pixie
-   **flagsText** **(Table)** - The flags for the the text
-   **fWidth** **(Float)** - The width of the pixie. This is only used
    if the pixie is drawn as a line.
-   **strSprite** **(String)** - The name of the sprite used for the
    pixie. This is only used for pixies that aren't drawn as a line.
-   **fRotation** **(Float)** - The number of degrees the pixie is
    rotated. This is only used for pixies that are not drawn as a line.
-   **loc** **(Table)** - The boundaries of the pixie. This table
    contains the offsets and points for the boundary.
    -   **fPoints** **(Array of Float)** - The points at the edges of
        the pixie. Values are ordered as Left, Top, Right, Bottom.
    -   **nOffsets** **(Array of Integer)** - The offsets for the pixie.
        These are ordered as Left, Top, Right, Bottom.
-   **cr** **([CColor](../Classes/CColor.md))** - The color of the
    pixie
-   **crText** **([CColor](../Classes/CColor.md))** - The color of the
    text in the pixie

### Return Value

-   **Integer** - The pixie's ID number

------------------------------------------------------------------------

`Method`

AddStyle(strStyle)
------------------

### Params

-   **strStyle** **(String)**

------------------------------------------------------------------------

`Method`

AddStyleEx(strStyle)
--------------------

### Params

-   **strStyle** **(String)**

------------------------------------------------------------------------

`Method`

ArrangeChildrenHorz(nOrigin)
----------------------------

### Params

-   **nOrigin** **(Integer)**

------------------------------------------------------------------------

`Method`

ArrangeChildrenTiles(nOrigin)
-----------------------------

### Params

-   **nOrigin** **(Integer)**

------------------------------------------------------------------------

`Method`

ArrangeChildrenVert(nOrigin)
----------------------------

### Params

-   **nOrigin** **(Integer)**

------------------------------------------------------------------------

`Method`

AttachAnim(strAnimDataId)
-------------------------

### Params

-   **strAnimDataId** **(String)**

------------------------------------------------------------------------

`Method`

BringChildToTop(wndChild)
-------------------------

### Params

-   **wndChild** **([Window](../WindowControls/Window.md))**

------------------------------------------------------------------------

`Method`

ClearFocus()
------------

### Description

Runs the caller's ClearFous method.

------------------------------------------------------------------------

`Method`

ClearInterrupt()
----------------

------------------------------------------------------------------------

`Method`

ClientPointToWindowPoint(nPosX, nPosY)
--------------------------------------

### Params

-   **nPosX** **(Integer)**
-   **nPosY** **(Integer)**

------------------------------------------------------------------------

`Method`

Close()
-------

### Description

Runs the caller's Close method.

------------------------------------------------------------------------

`Method`

Contains(nPosX, nPosY)
----------------------

### Description

Does a lua\_pushboolean if the caller contains the point at iPosX and
iPosY.

### Params

-   **nPosX** **(Integer)**
-   **nPosY** **(Integer)**

------------------------------------------------------------------------

`Method`

ContainsMouse()
---------------

### Description

Does a lua\_pushboolean if the caller contains the point at the current
mouse location.

------------------------------------------------------------------------

`Method`

Destroy()
---------

### Description

Calls Destroy() on the caller.

------------------------------------------------------------------------

`Method`

DestroyAllPixies()
------------------

------------------------------------------------------------------------

`Method`

DestroyChildren()
-----------------

### Description

Calls Destroy() on the caller's children.

------------------------------------------------------------------------

`Method`

DestroyPixie()
--------------

------------------------------------------------------------------------

`Method`

DetachAnim()
------------

### Description

Runs the caller's release method on m\_pAnimPlayer.

------------------------------------------------------------------------

`Method`

Enable(bEnable)
---------------

### Description

Sets the caller's m\_bEnabled boolean to bEnable.

### Params

-   **bEnable** **(Boolean)**

------------------------------------------------------------------------

`Method`

EnsureChildVisible(wndChild)
----------------------------

### Params

-   **wndChild** **([Window](../WindowControls/Window.md))**

------------------------------------------------------------------------

`Method`

FindChild(strName)
------------------

### Description

Returns the child of this window that has the specified name.

### Params

-   **strName** **(String)** - The name of the child window

### Return Value

-   **[Window](../WindowControls/Window.md)** - The child window with
    strName if found. Otherwise, this returns nil.

### Usage/Example

```lua
    self.wndMain = Apollo.LoadForm("WindowForms.xml", "MainWindow", nil, self)
    self.wndChild = self.wndMain:FindChild("ChildWindow")
    self.wndChild:Show(false)
```

### Remarks

This function will recursively search through all children of the
window.

------------------------------------------------------------------------

`Method`

FindChildByUserData()
---------------------

------------------------------------------------------------------------

`Method`

GetAnchorOffsets()
------------------

### Description

Does a lua\_pushinteger of the Offset Anchor's Left, Top, Right, then
Bottom.

------------------------------------------------------------------------

`Method`

GetAnchorPoints()
-----------------

### Description

Does a lua\_pushnumber of the Anchor's Left, Top, Right, then Bottom.

------------------------------------------------------------------------

`Method`

GetAnimElapsedTime()
--------------------

### Description

Does a lua\_pushnumber of the caller's ElapsedTime.

------------------------------------------------------------------------

`Method`

GetBGColor()
------------

### Description

Runs the caller's GetBGColor method in a CColor\_new.

------------------------------------------------------------------------

`Method`

GetBGOpacity()
--------------

------------------------------------------------------------------------

`Method`

GetChildren()
-------------

------------------------------------------------------------------------

`Method`

GetClientRect()
---------------

------------------------------------------------------------------------

`Method`

GetData()
---------

### Description

Does a lua\_rawgeti on the caller's m\_iLuaDataRefId.

------------------------------------------------------------------------

`Method`

GetFrame()
----------

------------------------------------------------------------------------

`Method`

GetGlobalRadioSel(strRadio)
---------------------------

### Params

-   **strRadio** **(String)**

------------------------------------------------------------------------

`Method`

GetGlobalRadioSelButton(strRadio)
---------------------------------

### Params

-   **strRadio** **(String)**

------------------------------------------------------------------------

`Method`

GetHeight()
-----------

### Description

Return the height of the window

### Return Value

-   **Integer** - The height of the window in pixels

------------------------------------------------------------------------

`Method`

GetHScrollPos()
---------------

### Description

Does a lua\_pushinteger of the caller's HScrollPos.

------------------------------------------------------------------------

`Method`

GetHScrollRange()
-----------------

### Description

Does a lua\_pushinteger of the caller's m\_sbHorz range.

------------------------------------------------------------------------

`Method`

GetId()
-------

### Description

Does a lua\_pushinteger on the caller's Id.

------------------------------------------------------------------------

`Method`

GetLocation()
-------------

### Description

Returns a new WindowLocation specified by the current window location.

------------------------------------------------------------------------

`Method`

GetMouse()
----------

### Description

Does a lua\_newtable with the x and y value of the mouse.

------------------------------------------------------------------------

`Method`

GetName()
---------

### Description

Does a lua\_pushwstring of the caller's name, sending "" if null.

------------------------------------------------------------------------

`Method`

GetNCOpacity()
--------------

------------------------------------------------------------------------

`Method`

GetOpacity()
------------

### Description

Does a lua.PushDouble of the caller's opacity.

------------------------------------------------------------------------

`Method`

GetOriginalLocation()
---------------------

------------------------------------------------------------------------

`Method`

GetParent()
-----------

### Description

Returns the caller's parent, or does a lua\_pushnil if null.

------------------------------------------------------------------------

`Method`

GetPixieInfo(iLayer)
--------------

### Description

Returns the caller's children pixie data, or does a lua\_pushnil if null. Keep in mind it does not return all values of a pixie.

### Params

-   **iLayer** **(Integer)** - The layer number of the pixie, `Pixie 1` from the form would be `iLayer = 1`

### Return Values

-   **cr** **[ApolloColor](../Classes/ApolloColor.md)** - The sprite color modifier
-   **fRotation** **Float** - Degree of rotation
-   **loc** **Table** - Relative position to parent
-   **strSprite** **String** - Name of the sprite

------------------------------------------------------------------------

`Method`

GetPos()
--------

### Description

Does a lua\_pushinteger of the caller's min x and min y.

------------------------------------------------------------------------

`Method`

GetRadioSel(strRadio)
---------------------

### Description

Does a lua\_pushinteger of the radio selection corresponding to sRadio.

### Params

-   **strRadio** **(String)**

------------------------------------------------------------------------

`Method`

GetRadioSelButton(strRadio)
---------------------------

### Params

-   **strRadio** **(String)**

------------------------------------------------------------------------

`Method`

GetRect()
---------

### Description

Get the rect of the window

### Usage/Example

```lua
    local nLeft, nTop, nRight, nBottom = self.wndMain:GetRect()
```

------------------------------------------------------------------------

`Method`

GetRotation()
-------------

### Description

Does a lua\_pushnumber of the caller's rotation after a
RadiansToDegrees.

------------------------------------------------------------------------

`Method`

GetScale()
----------

### Description

Does a lua\_pushnumber of the caller's scale.

------------------------------------------------------------------------

`Method`

GetSizingMaximum()
------------------

------------------------------------------------------------------------

`Method`

GetSizingMinimum()
------------------

------------------------------------------------------------------------

`Method`

GetSprite()
-----------

### Description

Does a lua\_pushwstring of the SpriteInfo's name, or "" if it is null.

------------------------------------------------------------------------

`Method`

GetText()
---------

### Description

Does a lua\_pushwstring of the caller's text.

------------------------------------------------------------------------

`Method`

GetTextColor()
--------------

------------------------------------------------------------------------

`Method`

GetTransLocation()
------------------

------------------------------------------------------------------------

`Method`

GetVScrollPos()
---------------

### Description

Does a lua\_pushinteger of the caller's VScrollPos.

------------------------------------------------------------------------

`Method`

GetVScrollRange()
-----------------

### Description

Does a lua\_pushinteger of the caller's m\_sbVert range.

------------------------------------------------------------------------

`Method`

GetWidth()
----------

### Description

Return the width of the window

### Return Value

-   **Integer** - The width of the window in pixels

------------------------------------------------------------------------

`Method`

GetWindowSubclass()
-------------------

------------------------------------------------------------------------

`Method`

HasTooltip()
------------

------------------------------------------------------------------------

`Method`

HasTooltipSecondary()
---------------------

------------------------------------------------------------------------

`Method`

Invoke()
--------

------------------------------------------------------------------------

`Method`

IsAnimPlaying()
---------------

### Description

Does a lua\_pushboolean of the caller's IsPlaying boolean.

------------------------------------------------------------------------

`Method`

IsChildOfMouseTarget()
----------------------

------------------------------------------------------------------------

`Method`

IsEnabled()
-----------

### Description

Does a lua\_pushboolean of the caller's enable boolean.

------------------------------------------------------------------------

`Method`

IsMouseTarget()
---------------

------------------------------------------------------------------------

`Method`

IsParentOfMouseTarget()
-----------------------

------------------------------------------------------------------------

`Method`

IsShown()
---------

### Description

Does a lua\_pushboolean of the caller's IsShown boolean.

------------------------------------------------------------------------

`Method`

IsStyleExOn()
-------------

------------------------------------------------------------------------

`Method`

IsStyleOn()
-----------

------------------------------------------------------------------------

`Method`

IsValid()
---------

------------------------------------------------------------------------

`Method`

IsVisible()
-----------

### Description

Does a lua\_pushboolean of the caller's IsVisible boolean.

------------------------------------------------------------------------

`Method`

LoadTooltipForm(strFile, strForm, tTable)
-----------------------------------------

### Params

-   **strFile** **(String)**
-   **strForm** **(String)**
-   **tTable** **(LuaTable)** - (Optional)

------------------------------------------------------------------------

`Method`

LoadTooltipFormSecondary(strFile, strForm, tTable)
--------------------------------------------------

### Params

-   **strFile** **(String)**
-   **strForm** **(String)**
-   **tTable** **(LuaTable)** - (Optional)

------------------------------------------------------------------------

`Method`

Move(nLeft, nTop, nWidth, nHeight)
----------------------------------

### Description

Move and resize the window

### Params

-   **nLeft** **(Integer)**
-   **nTop** **(Integer)**
-   **nWidth** **(Integer)**
-   **nHeight** **(Integer)**

------------------------------------------------------------------------

`Method`

MoveMethod() (Deprecated)
-------------------------

------------------------------------------------------------------------

`Method`

MoveToLoc()
-----------

### Description

Should be deprecated

------------------------------------------------------------------------

`Method`

MoveToLocation(wndLoc)
----------------------

### Params

-   **wndLoc**
    **([WindowLocation](../WindowControls/WindowLocation.md))**

------------------------------------------------------------------------

`Method`

PauseAnim()
-----------

### Description

Runs the caller's pause method on m\_pAnimPlayer.

------------------------------------------------------------------------

`Method`

PlayAnim(fDelay)
----------------

### Params

-   **fDelay** **(Float)**

------------------------------------------------------------------------

`Method`

RecalculateContentExtents()
---------------------------

------------------------------------------------------------------------

`Method`

RemoveEventHandler()
--------------------

------------------------------------------------------------------------

`Method`

RemoveStyle(strStyle)
---------------------

### Params

-   **strStyle** **(String)**

------------------------------------------------------------------------

`Method`

RemoveStyleEx(strStyle)
-----------------------

### Params

-   **strStyle** **(String)**

------------------------------------------------------------------------

`Method`

Reposition()
------------

### Description

Runs the caller's Reposition method.

------------------------------------------------------------------------

`Method`

ResetSubclass()
---------------

------------------------------------------------------------------------

`Method`

RestartPixieSprite()
--------------------

------------------------------------------------------------------------

`Method`

SendChildToBottom()
-------------------

------------------------------------------------------------------------

`Method`

SetAnchorOffsets(nLeft, nTop, nRight, nBottom)
----------------------------------------------

### Params

-   **nLeft** **(Integer)**
-   **nTop** **(Integer)**
-   **nRight** **(Integer)**
-   **nBottom** **(Integer)**

------------------------------------------------------------------------

`Method`

SetAnchorPoints(nLeft, nTop, nRight, nBottom)
---------------------------------------------

### Params

-   **nLeft** **(Integer)**
-   **nTop** **(Integer)**
-   **nRight** **(Integer)**
-   **nBottom** **(Integer)**

------------------------------------------------------------------------

`Method`

SetAnimElapsedTime(fTime)
-------------------------

### Params

-   **fTime** **(Float)**

------------------------------------------------------------------------

`Method`

SetAnimPlaybackRate(fRate)
--------------------------

### Params

-   **fRate** **(Float)**

------------------------------------------------------------------------

`Method`

SetBGColor(clr)
---------------

### Params

-   **clr** **([CColor](../Classes/CColor.md))**

------------------------------------------------------------------------

`Method`

SetBGOpacity()
--------------

------------------------------------------------------------------------

`Method`

SetCanResize()
--------------

------------------------------------------------------------------------

`Method`

SetClientSprite(wndB)
---------------------

### Description

Sets the caller's ClientSprite to wndB's ClientSprite.

### Params

-   **wndB** **([Window](../WindowControls/Window.md))**

------------------------------------------------------------------------

`Method`

SetData(lData)
--------------

### Params

-   **lData** **(LuaData)**

------------------------------------------------------------------------

`Method`

SetFocus()
----------

### Description

Runs the caller's SetFocus method.

------------------------------------------------------------------------

`Method`

SetFont(strText)
----------------

### Description

Sets the font by alias on the caller after running a UTF8ToUCS2 on
strText.

### Params

-   **strText** **(String)**

------------------------------------------------------------------------

`Method`

SetGlobalRadioSel(strRadio)
---------------------------

### Params

-   **strRadio** **(String)**

------------------------------------------------------------------------

`Method`

SetHScrollInfo(nRange, nPageSize, nIncrement)
---------------------------------------------

### Params

-   **nRange** **(Integer)**
-   **nPageSize** **(Integer)**
-   **nIncrement** **(Integer)**

------------------------------------------------------------------------

`Method`

SetHScrollPos(nNewPos)
----------------------

### Params

-   **nNewPos** **(Integer)**

------------------------------------------------------------------------

`Method`

SetInterrupt()
--------------

------------------------------------------------------------------------

`Method`

SetLoaded(bLoaded)
------------------

### Description

Sets the caller's m\_bLoaded boolean to bLoaded.

### Params

-   **bLoaded** **(Boolean)**

------------------------------------------------------------------------

`Method`

SetName(strName)
----------------

### Description

Sets the caller's name to sName.

### Params

-   **strName** **(String)**

------------------------------------------------------------------------

`Method`

SetNamedAnchor(fPoint, nOffset, bOverwrite)
-------------------------------------------

### Params

-   **fPoint** **(Float)**
-   **nOffset** **(Integer)**
-   **bOverwrite** **(Boolean)**

------------------------------------------------------------------------

`Method`

SetNCOpacity()
--------------

------------------------------------------------------------------------

`Method`

SetOpacity(fOpacity, fRate)
---------------------------

### Params

-   **fOpacity** **(Float)** - (Default value: 1.0)
-   **fRate** **(Float)** - (Default value: -1.0)

------------------------------------------------------------------------

`Method`

SetRadioSel(strRadio, nSelection)
---------------------------------

### Params

-   **strRadio** **(String)**
-   **nSelection** **(Integer)** - (Default value: 0)

------------------------------------------------------------------------

`Method`

SetRadioSelButton(strRadio, bButton)
------------------------------------

### Params

-   **strRadio** **(String)**
-   **bButton** **([Button](../WindowControls/Button.md))**

------------------------------------------------------------------------

`Method`

SetRotation(fNewRotation)
-------------------------

### Description

Sets the caller's rotation to fNewRotation after a DegreesToRadians.

### Params

-   **fNewRotation** **(Float)**

------------------------------------------------------------------------

`Method`

SetScale(fNewScale)
-------------------

### Description

Sets the caller's scale.

### Params

-   **fNewScale** **(Float)**

------------------------------------------------------------------------

`Method`

SetSelfAnchor()
---------------

------------------------------------------------------------------------

`Method`

SetSizingMaximum(nWidth, nHeight)
---------------------------------

### Description

Sets the caller's sizing maximum to iWidth and iHeight.

### Params

-   **nWidth** **(Integer)**
-   **nHeight** **(Integer)**

------------------------------------------------------------------------

`Method`

SetSizingMinimum(nWidth, nHeight)
---------------------------------

### Description

Sets the caller's sizing minimum to iWidth and iHeight.

### Params

-   **nWidth** **(Integer)**
-   **nHeight** **(Integer)**

------------------------------------------------------------------------

`Method`

SetSprite(strSprite)
--------------------

### Params

-   **strSprite** **(String)**

------------------------------------------------------------------------

`Method`

SetSpriteProgress(fTime)
------------------------

### Params

-   **fTime** **(Float)**

------------------------------------------------------------------------

`Method`

SetSpriteRate(fTime)
--------------------

### Params

-   **fTime** **(Float)**

------------------------------------------------------------------------

`Method`

SetSpriteTargetDuration(fTime)
------------------------------

### Params

-   **fTime** **(Float)**

------------------------------------------------------------------------

`Method`

SetSpriteTime(fTime)
--------------------

### Params

-   **fTime** **(Float)**

------------------------------------------------------------------------

`Method`

SetStyle(strText, bOn)
----------------------

### Params

-   **strText** **(String)**
-   **bOn** **(Boolean)** - (Optional, Default to GetStyleBit on
    strText)

------------------------------------------------------------------------

`Method`

SetStyleEx(strStyle)
--------------------

### Params

-   **strStyle** **(String)**

------------------------------------------------------------------------

`Method`

SetText(strNewText)
-------------------

### Params

-   **strNewText** **(String)**

------------------------------------------------------------------------

`Method`

SetTextColor(clr)
-----------------

### Params

-   **clr** **([CColor](../Classes/CColor.md))**

------------------------------------------------------------------------

`Method`

SetTextFlags(strText, bOn)
--------------------------

### Params

-   **strText** **(String)**
-   **bOn** **(Boolean)** - (Optional, Skipped if strText does not
    yields a StyleBit)

------------------------------------------------------------------------

`Method`

SetTextRaw()
------------

------------------------------------------------------------------------

`Method`

SetTooltip(strTip)
------------------

### Description

Sets the tooltip on the caller after running a UTF8ToUCS2 on strTip.

### Params

-   **strTip** **(String)**

------------------------------------------------------------------------

`Method`

SetTooltipDoc(pXml)
-------------------

### Params

-   **pXml** **(XmlDocumentRef)**

------------------------------------------------------------------------

`Method`

SetTooltipDocSecondary(pXml)
----------------------------

### Params

-   **pXml** **(XmlDocumentRef)**

------------------------------------------------------------------------

`Method`

SetTooltipForm()
----------------

------------------------------------------------------------------------

`Method`

SetTooltipFormSecondary()
-------------------------

------------------------------------------------------------------------

`Method`

SetTooltipToWindow(wndB)
------------------------

### Description

Sets the caller's tooltip doc and tooltip secondary doc to wndB's
values.

### Params

-   **wndB** **([Window](../WindowControls/Window.md))**

------------------------------------------------------------------------

`Method`

SetTooltipType(nType)
---------------------

### Description

Sets the tooltip type on the caller after casting nType to a
ETooltipPositionType.

### Params

-   **nType** **(ETooltipPositionType)**

------------------------------------------------------------------------

`Method`

SetVScrollInfo(nRange, nPageSize, nMinInc)
------------------------------------------

### Params

-   **nRange** **(Integer)**
-   **nPageSize** **(Integer)**
-   **nMinInc** **(Integer)**

------------------------------------------------------------------------

`Method`

SetVScrollPos(nNewPos)
----------------------

### Params

-   **nNewPos** **(Integer)**

------------------------------------------------------------------------

`Method`

SetWindowSubclass()
-------------------

------------------------------------------------------------------------

`Method`

SetWindowTemplate()
-------------------

------------------------------------------------------------------------

`Method`

Show(bShow, bImmediate)
-----------------------

### Description

Runs the caller's show method with bShow and bImmediate.

### Params

-   **bShow** **(Boolean)**
-   **bImmediate** **(Boolean)**

------------------------------------------------------------------------

`Method`

ToFront()
---------

### Description

Runs the caller's BringWindowToFront method.

------------------------------------------------------------------------

`Method`

TransitionMove(nMinX, nMinY, nOffX, nOffY, fRate, bContinuous)
--------------------------------------------------------------

### Description

Calls a transition move with pLocBegin null and pLocEnd specified by
dMinX, dMinY, dMinX+dOffX, dMinY+dOffY, fRate, and bContinuous.

### Params

-   **nMinX** **(Double)**
-   **nMinY** **(Double)**
-   **nOffX** **(Double)**
-   **nOffY** **(Double)**
-   **fRate** **(Float)**
-   **bContinuous** **(Boolean)**

------------------------------------------------------------------------

`Method`

TransitionMoveFrom(nMinX, nMinY, nOffX, nOffY, fRate, bContinuous)
------------------------------------------------------------------

### Description

Calls a transition move with pLocEnd null and pLocBegin specified by
dMinX, dMinY, dMinX+dOffX, dMinY+dOffY, fRate, and bContinuous.

### Params

-   **nMinX** **(Double)**
-   **nMinY** **(Double)**
-   **nOffX** **(Double)**
-   **nOffY** **(Double)**
-   **fRate** **(Float)**
-   **bContinuous** **(Boolean)**

------------------------------------------------------------------------

`Method`

TransitionPulse(fScale, fRate, bContinuous) (Deprecated)
--------------------------------------------------------

### Params

-   **fScale** **(Float)**
-   **fRate** **(Float)**
-   **bContinuous** **(Boolean)**

------------------------------------------------------------------------

`Method`

UnpauseAnim()
-------------

### Description

Runs the caller's unpause method on m\_pAnimPlayer.

------------------------------------------------------------------------

`Method`

UpdatePixie()
-------------

------------------------------------------------------------------------

`Method`

WindowPointToClientPoint(nPosX, nPosY)
--------------------------------------

### Params

-   **nPosX** **(Integer)**
-   **nPosY** **(Integer)**
