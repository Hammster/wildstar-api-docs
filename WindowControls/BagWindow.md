BagWindow
=========

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

ItemClick
---------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Method`

AreAnyItemsNew(nNewBagSlot)
---------------------------

### Description

Does a lua\_pushboolean if there are new items in a bag slot specified
by nNewBagSlot.

### Params

-   **nNewBagSlot** **(Integer)**

------------------------------------------------------------------------

`Method`

AssignBag(nData, nWhichBag)
---------------------------

### Params

-   **nData** **(Integer)**
-   **nWhichBag** **(Integer)**

------------------------------------------------------------------------

`Method`

CanAssignBag(nSource, nDest)
----------------------------

### Description

Does a lua\_pushboolean if the bag can be assigned.

### Params

-   **nSource** **(Integer)**
-   **nDest** **(Integer)**

------------------------------------------------------------------------

`Method`

CanDropItemInBag(nData, nWhichBag)
----------------------------------

### Description

Does a lua\_pushboolean if an item can be dropped in a bag.

### Params

-   **nData** **(Integer)**
-   **nWhichBag** **(Integer)**

------------------------------------------------------------------------

`Method`

CanRemoveBag(nWhichBag)
-----------------------

### Description

Does a lua\_pushboolean if the bag can be removed.

### Params

-   **nWhichBag** **(Integer)**

------------------------------------------------------------------------

`Method`

DoAnyItemsBeginQuest()
----------------------

------------------------------------------------------------------------

`Method`

DropItemInBag(nData, nWhichBag)
-------------------------------

### Description

Does a lua\_pushboolean of true if successful (was not trying to drop a
bag in a bag or etc.)

### Params

-   **nData** **(Integer)**
-   **nWhichBag** **(Integer)**

------------------------------------------------------------------------

`Method`

GetBagCapacity()
----------------

### Description

Does a lua\_pushinteger of the caller's capacity.

------------------------------------------------------------------------

`Method`

GetBagId()
----------

### Description

Does a lua\_pushinteger of the caller's id.

------------------------------------------------------------------------

`Method`

GetBagItem()
------------

------------------------------------------------------------------------

`Method`

GetInventoryIdForBag(nBag)
--------------------------

### Description

Does a lua\_pushinteger of the inventory id.

### Params

-   **nBag** **(Integer)**

------------------------------------------------------------------------

`Method`

GetItem(nData)
--------------

### Params

-   **nData** **(Integer)**

------------------------------------------------------------------------

`Method`

GetTotalBagSlots()
------------------

### Description

Does a lua\_pushinteger of the total bag slots.

------------------------------------------------------------------------

`Method`

GetTotalEmptyBagSlots()
-----------------------

### Description

Does a lua\_pushinteger of the total empty bag slots.

------------------------------------------------------------------------

`Method`

IsBagEquipped(nWhichBag)
------------------------

### Description

Does a lua\_pushboolean if a bag is equipped.

### Params

-   **nWhichBag** **(Integer)**

------------------------------------------------------------------------

`Method`

IsItemABag(nData)
-----------------

### Description

Does a lua\_pushboolean if nData is a bag.

### Params

-   **nData** **(Integer)**

------------------------------------------------------------------------

`Method`

MarkAllItemsAsSeen()
--------------------

### Description

Runs the caller's MarkAllItems method.

------------------------------------------------------------------------

`Method`

SetBagId(nBagSlot)
------------------

### Params

-   **nBagSlot** **(Integer)**

------------------------------------------------------------------------

`Method`

SetBoxesPerRow(nBoxesPerRow)
----------------------------

### Params

-   **nBoxesPerRow** **(Integer)** - (Default value: 4)

------------------------------------------------------------------------

`Method`

SetCannotUseColor()
-------------------

------------------------------------------------------------------------

`Method`

SetCannotUseSprite()
--------------------

------------------------------------------------------------------------

`Method`

SetItemSortComparer()
---------------------

------------------------------------------------------------------------

`Method`

SetNewItemOverlaySprite()
-------------------------

------------------------------------------------------------------------

`Method`

SetNewQuestOverlaySprite()
--------------------------

------------------------------------------------------------------------

`Method`

SetSort()
---------

------------------------------------------------------------------------

`Method`

SetSquareSize(nX, nY)
---------------------

### Description

Sets the square size of the caller to nX and nY.

### Params

-   **nX** **(Integer)** - (Default value: current X)
-   **nY** **(Integer)** - (Default value: current Y)

------------------------------------------------------------------------

`Method`

StartSplitStack()
-----------------

------------------------------------------------------------------------

`Method`

SwapBagItems()
--------------

### Description

Currently has no implementation
