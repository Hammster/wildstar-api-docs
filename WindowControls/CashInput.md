CashInput
==========

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

AmountChanged
-----------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened
-   **moneyNewAmount** **([Money](../Classes/Money.md))**
-   **moneyOldAmount** **([Money](../Classes/Money.md))**

------------------------------------------------------------------------

`Method`

SetAmount(oAmount)
-----------------------------------------------------

### Description

Sets the current amount for the control taking in either an integer value or a money object that will update the money system and use the value from the money object.

### Params

-   **oAmount** **(Integer)** or **([Money](../Classes/Money.md))**

------------------------------------------------------------------------

`Method`

GetAmount()
-----------------------------------------------------------------------------------------

### Description

Gets the current input amount as a **([Money](../Classes/Money.md))** object.

### Return Value
**([Money](../Classes/Money.md))**

------------------------------------------------------------------------

`Method`

SetAmountLimit(oAmount)
-----------

### Description

Sets the current amount maximum for the control taking in either an integer value or a money object.

### Params

-   **oAmount** **(Integer)** or **([Money](../Classes/Money.md))**

------------------------------------------------------------------------

`Method`

GetAmountLimit()
----------------

### Description

Gets the current input amount maximum as a **([Money](../Classes/Money.md))** object.

### Return Value
**([Money](../Classes/Money.md))**

------------------------------------------------------------------------

`Method`

SetMoneySystem(eCurrencyType, eAltType, itemExchange, eAccountCurrencyType)
----------------------

### Description

Sets the money system the control will use. The most left valid parameter will be used.

### Params

-   **eCurrencyType** **(ECurrencyType)**
-   **eAltType** **(ENonCurrencyType)**
-   **itemExchange** **([Item](../Classes/Item.md))**
-   **eAccountCurrencyType** **(EAccountCurrencyType)**
