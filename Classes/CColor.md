CColor
======

### Prefix: cc

### Description

CColors are an older way of using colors in addons. All colors are in
ARGB format, with all values being between 0.0 and 1.0.\
While this functionality is not yet depricated, it may be in the future.
We highly recommend that developers use ApolloColors instead.

------------------------------------------------------------------------

`Function`

Complement(ccBaseColor)
-----------------------

### Description

Returns a CColor that complements the color that is passed in.

### Params

-   **ccBaseColor** **([CColor](../Classes/CColor.md))** - The color
    that the complement is made from.

### Return Value

-   **[CColor](../Classes/CColor.md)** - A color that complements the
    one that was passed in.

### Remarks

The values of the CColor that is returned are all 1.0 - value.

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Detects whether a variable is a CColor or not.

### Params

-   **oVariable** **(Variable)** - The variable that the function will
    check.

### Return Value

-   **Boolean** - Whether the variable is a CColor or not.

------------------------------------------------------------------------

`Function`

new(r, g, b, a)
---------------

### Description

Creates a new CColor using the specified values.

### Params

-   **r** **(Float)** - The red value of the color.
-   **g** **(Float)** - The green value of the color.
-   **b** **(Float)** - The blue value of the color.
-   **a** **(Float)** - The alpha value of the color. This value
    defaults to 1.0 if no alpha value is passed in.

### Return Value

-   **[CColor](../Classes/CColor.md)** - A CColor with the rgba values
    that were passed in.

------------------------------------------------------------------------

`Method`

\_\_add(ccModifier) (Deprecated)
--------------------------------

### Description

Adds another CColor's values to the CColor that called this function.

### Params

-   **ccModifier** **([CColor](../Classes/CColor.md))** - The CColor
    that the current CColor will be modified by.

### Return Value

-   **[CColor](../Classes/CColor.md)** - The sum of the two CColors.

------------------------------------------------------------------------

`Method`

\_\_div(fScale) (Deprecated)
----------------------------

### Description

Scales each value in the CColor by the given amount.

### Params

-   **fScale** **(Float)** - The amount that each value in the CColor
    will be scaled by.

### Return Value

-   **[CColor](../Classes/CColor.md)** - The modified CColor.

------------------------------------------------------------------------

`Method`

\_\_eq(ccCompare) (Deprecated)
------------------------------

### Description

Checks if a CColor matches this CColor.

### Params

-   **ccCompare** **([CColor](../Classes/CColor.md))** - The CColor
    that is being compared to the one that called the function.

### Return Value

-   **Boolean** - Whether the two CColors matched or not.

------------------------------------------------------------------------

`Method`

\_\_index(strIndex) (Deprecated)
--------------------------------

### Description

Gets the CColor's value for one of its primary colors or alpha.

### Params

-   **strIndex** **(String)** - The index of the value that the function
    will return. This can be:\
    "r" = red value\
    "b" = blue value\
    "g" = green value\
    "a" = alpha value

------------------------------------------------------------------------

`Method`

\_\_mul(fScale, ccMultiplier) (Deprecated)
------------------------------------------

### Description

Scales the values in the CColor by the value passed in.

### Params

-   **fScale** **(Float)** - The amount that each value in the CColor
    will be scaled by. Only a float or CColor needs to be passed in.
-   **ccMultiplier** **([CColor](../Classes/CColor.md))** - The CColor
    that the source color is multiplied by. Each value is multiplied by
    the corresponding value, so red x red, blue x blue, etc. Only a
    float or CColor should be passed in to the function, not both.

### Return Value

-   **[CColor](../Classes/CColor.md)** - The result of multiplying the
    original CColor with the value that was passed in.

------------------------------------------------------------------------

`Method`

\_\_newindex(strIndex, fValue) (Deprecated)
-------------------------------------------

### Description

Sets one of the CColor's color values.

### Params

-   **strIndex** **(String)** - The color value that the function will
    update.\
    "r" = red\
    "g" = green\
    "b" = blue\
    "a" = alpha
-   **fValue** **(Float)** - The color's new value.

### Return Value

-   **String** - An error string is sent if an invalid index is used.
    Otherwise, this function has no return value.

------------------------------------------------------------------------

`Method`

\_\_sub(ccSubtractor) (Deprecated)
----------------------------------

### Description

Subtracts a CColor's values from the CColor that called the function.

### Params

-   **ccSubtractor** **([CColor](../Classes/CColor.md))** - The color
    values of the CColor that called the function are subtracted by this
    CColor's color values.

### Return Value

-   **[CColor](../Classes/CColor.md)** - The CColor made up of the
    difference of the two CColors.

------------------------------------------------------------------------

`Method`

\_\_tostring() (Deprecated)
---------------------------

### Description

Converts a CColor to a string with the CColor's values

### Return Value

-   **String** - A string with the CColor's values. The string's format
    is "CColor(alpha,red,green,blue)

------------------------------------------------------------------------

`Method`

\_\_unm() (Deprecated)
----------------------

### Description

Multiplies each of the CColor's color values by -1.

### Return Value

-   **[CColor](../Classes/CColor.md)** - The new CColor created by the
    function.

------------------------------------------------------------------------

`Method`

Complement()
------------

### Description

Creates a new CColor that is complementary to the one that calls this
function.

### Return Value

-   **[CColor](../Classes/CColor.md)** - A color that complements the
    one that called the function.

### Remarks

The values of the CColor that is returned are all 1.0 - value.

------------------------------------------------------------------------

`Method`

Saturate()
----------

### Description

Locks the values in the color to values between 0.0 and 1.0.

### Return Value

-   **[CColor](../Classes/CColor.md)** - A new color that has been
    bound to values between 0.0 and 1.0.
