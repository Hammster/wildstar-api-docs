CashInput
==========

### Parent: [Window](../WindowControls/Window.html)

Table of Content
---------------- 

<!-- toc -->

------------------------------------------------------------------------

`Event`

AmountChanged
-----------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.html))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.html))** - The
    window control with the event happened
-   **moneyNewAmount** **([Money](../Classes/Money.html))** 
-   **moneyOldAmount** **([Money](../Classes/Money.html))** 

------------------------------------------------------------------------

`Method`

SetAmount(oAmount)
-----------------------------------------------------

### Description

Sets the current amount for the control taking in either an integer value or a money object that will update the money system and use the value from the money object.

### Params

-   **oAmount** **(Integer)** or **([Money](../Classes/Money.html))**

------------------------------------------------------------------------

`Method`

GetAmount()
-----------------------------------------------------------------------------------------

### Description

Gets the current input amount as a **([Money](../Classes/Money.html))** object.

### Return Value
**([Money](../Classes/Money.html))**

------------------------------------------------------------------------

`Method`

SetAmountLimit(oAmount)
-----------

### Description

Sets the current amount maximum for the control taking in either an integer value or a money object.

### Params

-   **oAmount** **(Integer)** or **([Money](../Classes/Money.html))**

------------------------------------------------------------------------

`Method`

GetAmountLimit()
----------------

### Description

Gets the current input amount maximum as a **([Money](../Classes/Money.html))** object.

### Return Value
**([Money](../Classes/Money.html))**

------------------------------------------------------------------------

`Method`

SetMoneySystem(eCurrencyType, eAltType, itemExchange, eAccountCurrencyType)
----------------------

### Description

Sets the money system the control will use. The most left valid parameter will be used.

### Params

-   **eCurrencyType** **(ECurrencyType)**
-   **eAltType** **(ENonCurrencyType)**
-   **itemExchange** **([Item](../Classes/Item.html))**
-   **eAccountCurrencyType** **(EAccountCurrencyType)**
