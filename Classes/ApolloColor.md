ApolloColor
===========

### Prefix: cr

### Description

ApolloColors are the primary way that the UI uses colors. There are a
number predefined colors, which can be found under Virtual colors
section of Houston's color chooser. Addon developers can also create
their own ApolloColors using a string with the color's ARGB values in
hex format.

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Validates that the variable passed in is an ApolloColor.

### Params

-   **oVariable** **(Variable)** - The variable that we are checking.

### Return Value

-   **Boolean** - Whether the variable is an ApolloColor or not.

------------------------------------------------------------------------

`Function`

new()
-----

### Description

Creates a new ApolloColor object.

### Remarks

This can be created using a string with the ApolloColor's name, a string
with the color's ARGB values in hex, a table with the color's ARGB
values, or a set of integers using the ARGB values.

------------------------------------------------------------------------

`Function`

SetColor(strColorName, crUpdatedValues)
---------------------------------------

### Description

Sets a named ApolloColor to the value of a CColor.

### Params

-   **strColorName** **(String)** - The name of the ApolloColor that is
    being updated.
-   **crUpdatedValues** **([CColor](../Classes/CColor.md))** - The
    CColor that the ApolloColor is being updated to.

### Return Value

-   **Boolean** - Whether the ApolloColor was successfully updated or
    not.

------------------------------------------------------------------------

`Method`

\_\_eq(crChecking) (Deprecated)
-------------------------------

### Description

Checks if two ApolloColors are the same.

### Params

-   **crChecking** **([ApolloColor](../Classes/ApolloColor.md))** - The
    ApolloColor that the function will check against.

### Return Value

-   **Boolean** - Whether the two ApolloColors are equal or not.

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

ApolloColor's garbage collection function. This will delete the
ApolloColor from memory.

------------------------------------------------------------------------

`Method`

\_\_index(strIndex) (Deprecated)
--------------------------------

### Description

Returns the ApolloColor's value at the specified index.

### Params

-   **strIndex** **(String)** - The index of the value that should be
    returned. This will either be "r" for the color's red value, "b" for
    the color's blue value, "g" for the color's green value, or "a" for
    the color's alpha value.

### Return Value

-   **Float** - The color value at the specified index.

------------------------------------------------------------------------

`Method`

IsLinked()
----------

### Description

Determines whether the ApolloColor is using a virtual color or not.

### Return Value

-   **Boolean** - Whether the ApolloColor is set to a virtual color or a
    hardcoded value.

------------------------------------------------------------------------

`Method`

IsSameColorAs(crChecking)
-------------------------

### Description

Checks if two ApolloColors share the same color.

### Params

-   **crChecking** **([ApolloColor](../Classes/ApolloColor.md))** - The
    ApolloColor that we are checking against.

### Return Value

-   **Boolean** - Whether the ApolloColors share the same color.

### Usage/Example

```lua
    This function can compare virtual colors and hardcoded colors successfully.
```

------------------------------------------------------------------------

`Method`

ToTable()
---------

### Description

Returns a table with the ApolloColor's RGBA values.

### Return Value

-   **Table** - The color's RGBA values.
    -   **r** **(Float)** - The color's red value.
    -   **g** **(Float)** - The color's green value.
    -   **b** **(Float)** - The color's blue value.
    -   **a** **(Float)** - The color's alpha value.
