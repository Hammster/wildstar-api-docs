AlienFxLib
==========

### Description

Integration with Alienware's Alien FX library allowing lua to control
hardware lights.

------------------------------------------------------------------------

`Enum`

EnumDeviceTypes
---------------

-   **Unknown**
-   **Notebook**
-   **Desktop**
-   **Server**
-   **Display**
-   **Mouse**
-   **Keyboard**
-   **Gamepad**
-   **Speaker**
-   **Other**

------------------------------------------------------------------------

`Function`

CanUse()
--------

### Description

Can the AlienFx library be used.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Function`

GetDeviceCount()
----------------

### Description

How many devices are connected.

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Function`

GetDeviceDescription(nDeviceIndex)
----------------------------------

### Description

The description and type of the device.

### Params

-   **nDeviceIndex** **(Integer)**

### Return Value

-   **Table**
    -   **strDescription** **(String)**
    -   **eType** **(AlienFxLib.EnumDeviceTypes)**

------------------------------------------------------------------------

`Function`

GetLightColor(nDeviceIndex, nLightIndex)
----------------------------------------

### Description

What color is a certain light currently displaying.

### Params

-   **nDeviceIndex** **(Integer)**
-   **nLightIndex** **(Integer)**

### Return Value

-   **[CColor](../Classes/CColor.md)**

------------------------------------------------------------------------

`Function`

GetLightCount(nDeviceIndex)
---------------------------

### Description

How many lights does a device have.

### Params

-   **nDeviceIndex** **(Integer)**

### Return Value

-   **Integer**

------------------------------------------------------------------------

`Function`

GetLightDescription(nDeviceIndex, nLightIndex)
----------------------------------------------

### Description

Get the description of a light.

### Params

-   **nDeviceIndex** **(Integer)**
-   **nLightIndex** **(Integer)**

### Return Value

-   **String**

------------------------------------------------------------------------

`Function`

GetLightLocation(nDeviceIndex, nLightIndex)
-------------------------------------------

### Description

Get a lights x,y,z physical position, in centimeters, of any given light
relative to the lower, left, rear corner of the device's bounding box.

### Params

-   **nDeviceIndex** **(Integer)**
-   **nLightIndex** **(Integer)**

### Return Value

-   **Table**
    -   **nX** **(Integer)**
    -   **nY** **(Integer)**
    -   **nZ** **(Integer)**

------------------------------------------------------------------------

`Function`

IsReady()
---------

### Description

Is the Alien Fx library ready to be used.

### Return Value

-   **Boolean**

------------------------------------------------------------------------

`Function`

Reset()
-------

------------------------------------------------------------------------

`Function`

SetLightColor(nDeviceIndex, nLightIndex, crLightColor)
------------------------------------------------------

### Params

-   **nDeviceIndex** **(Integer)**
-   **nLightIndex** **(Integer)**
-   **crLightColor** **([CColor](../Classes/CColor.md))**

------------------------------------------------------------------------

`Function`

SetLocationColor(nLocationMask, crLightColor)
---------------------------------------------

### Description

Sets all lights for a location mask to a certain color.

### Params

-   **nLocationMask** **(Integer)** - Is a 32-bit mask that denotes one
    or more light positions in terms of the device's bounding box. There
    are 27 bits for each smaller cube within this bounding box, divided
    evenly.
-   **crLightColor** **([CColor](../Classes/CColor.md))**
