Money
=====

### Prefix: mon

------------------------------------------------------------------------

`Enum`

CodeEnumCurrencyType
--------------------

-   **Credits**
-   **Renown**
-   **ElderGems**
-   **CraftingVouchers**
-   **Prestige**
-   **GroupCurrency**
-   **ShadeSilver**
-   **Glory**

------------------------------------------------------------------------

`Enum`

CodeEnumGroupCurrencyType
-------------------------

-   **None**
-   **WarCoins**

------------------------------------------------------------------------

`Function`

is()
----

------------------------------------------------------------------------

`Function`

new()
-----

------------------------------------------------------------------------

`Method`

\_\_eq() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

AddToTooltip(self, strText, strColor, strSize, strAlign)
--------------------------------------------------------

### Params

-   **self** **(XmlDocumentRef)**
-   **strText** **(String)**
-   **strColor** **(String)** - (Default value: FFFFFFFF)
-   **strSize** **(String)** - (Default value: Header4)
-   **strAlign** **(String)** - (Default value: Left)

------------------------------------------------------------------------

`Method`

AppendToTooltip(self)
---------------------

### Params

-   **self** **(XmlDocumentRef)**

------------------------------------------------------------------------

`Method`

GetAccountCurrencyType()
------------------------

------------------------------------------------------------------------

`Method`

GetAltType()
------------

------------------------------------------------------------------------

`Method`

GetAmount()
-----------

### Description

Does a lua\_pushinteger of the amount specified by currencyValue.

------------------------------------------------------------------------

`Method`

GetDenomAmounts()
-----------------

### Description

Does a lua\_newtable with an index and the denom amounts.

------------------------------------------------------------------------

`Method`

GetDenomInfo()
--------------

### Description

Does a lua\_newtable with an index, amount, name, rate, textWidth, and
sprite.

------------------------------------------------------------------------

`Method`

GetExchangeItem()
-----------------

------------------------------------------------------------------------

`Method`

GetMoneyString(bSkipZeros)
--------------------------

### Description

Does a lua\_pushwstring of the localized money amount.

### Params

-   **bSkipZeros** **(Boolean)** - (Default value: true)

------------------------------------------------------------------------

`Method`

GetMoneyType()
--------------

### Description

Does a lua\_pushinteger of the type.

------------------------------------------------------------------------

`Method`

GetTypeString()
---------------

### Description

Does a lua\_pushwstring of the localized id type.

------------------------------------------------------------------------

`Method`

IsZero()
--------

### Description

Does a lua\_pushboolean if the amount equals 0 specified by
currencyValue.

------------------------------------------------------------------------

`Method`

Multiply()
----------

------------------------------------------------------------------------

`Method`

SetAccountCurrencyType()
------------------------

------------------------------------------------------------------------

`Method`

SetAltType()
------------

------------------------------------------------------------------------

`Method`

SetAmount(nNewAmount)
---------------------

### Params

-   **nNewAmount** **(Integer)**

------------------------------------------------------------------------

`Method`

SetExchangeItem()
-----------------

------------------------------------------------------------------------

`Method`

SetMoneyType(nNewType)
----------------------

### Description

Sets the type to an enum ECurrencyType specified by nNewType.

### Params

-   **nNewType** **(Integer for enum ECurrencyType. A mapping is
    available earlier in the page.)**
