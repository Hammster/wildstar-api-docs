CashWindow
==========

### Parent: [Window](../WindowControls/Window.md)

------------------------------------------------------------------------

`Event`

CashWindowAmountChanged
-----------------------

### Params

-   **wndHandler** **([Window](../WindowControls/Window.md))** - The
    window that fires the event
-   **wndControl** **([Window](../WindowControls/Window.md))** - The
    window control with the event happened

------------------------------------------------------------------------

`Method`

GetAMLDocForAmount(nAmount, bUseZeroes, clr, strFont)
-----------------------------------------------------

### Description

Does a lua\_pushwstring of the result of the caller's GenerateAMLDoc
specified by nAmount, bUseZeroes, clr, and strFont.

### Params

-   **nAmount** **(Integer)**
-   **bUseZeroes** **(Boolean)**
-   **clr** **([CColor](../Classes/CColor.md))**
-   **strFont** **(String)**

------------------------------------------------------------------------

`Method`

GetAMLDocForPrice(nAmount1, nCurrencyType1, nAmount2, nCurrencyType2, bDisabled, strFont)
-----------------------------------------------------------------------------------------

### Description

Does a lua\_pushwstring of the result of the caller's GenerateAMLDoc
specified by the parameters. The price is calculated with the first four
integers.

### Params

-   **nAmount1** **(Integer)**
-   **nCurrencyType1** **(Integer)**
-   **nAmount2** **(Integer)**
-   **nCurrencyType2** **(Integer)**
-   **bDisabled** **(Boolean)**
-   **strFont** **(String)** - (Default value: "Default")

------------------------------------------------------------------------

`Method`

GetAmount()
-----------

### Description

Does a lua\_pushinteger of the caller's amount.

------------------------------------------------------------------------

`Method`

GetAmountLimit()
----------------

------------------------------------------------------------------------

`Method`

GetCurrency()
-------------

### Description

Returns a new LuaGameTypes\_Money of the caller's value.

------------------------------------------------------------------------

`Method`

GetDisplayWidth()
-----------------

------------------------------------------------------------------------

`Method`

SetAmount(nAmount, bInstant)
----------------------------

### Params

-   **nAmount** **(Integer)**
-   **bInstant** **(Boolean)**

------------------------------------------------------------------------

`Method`

SetAmountLimit()
----------------

------------------------------------------------------------------------

`Method`

SetExchangeItem()
-----------------

------------------------------------------------------------------------

`Method`

SetMoneySystem(nWhich)
----------------------

### Params

-   **nWhich** **(ECurrencyType)**
