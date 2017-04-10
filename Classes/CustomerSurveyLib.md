CustomerSurveyLib
=================

### Description

A library that allows the player to interact with queued customer
surveys.

------------------------------------------------------------------------

`Enum`

CodeEnumSurveyType
------------------

### Description

The different types of surveys that the player can receive.

-   **General**
-   **Quest**
-   **PathMission**
-   **Challenge**

------------------------------------------------------------------------

`Function`

GetPending(nIndex)
------------------

### Description

Gets a pending customer survey that the player has not filled out.

### Params

-   **nIndex** **(Integer)** - The index of the survey that will be
    returned. If no value is provided, the function will get the first
    pending survey.

### Return Value

-   **[CustomerSurveyTypeLib](../Classes/CustomerSurveyTypeLib.md)** -
    The pending survey.

------------------------------------------------------------------------

`Function`

GetPendingCount()
-----------------

### Description

Gets the number of surveys that are waiting to be filled out by the
player.

### Return Value

-   **Integer** - The number of surveys that are waiting to be filled
    out by the player.
