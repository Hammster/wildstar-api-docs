P2PTrading
==========

------------------------------------------------------------------------

`Event`

P2PCancelTrade
--------------

------------------------------------------------------------------------

`Event`

P2PTradeChange
--------------

------------------------------------------------------------------------

`Event`

P2PTradeInvite
--------------

### Params

-   **idInvitor** **([Unit](../Classes/Unit.md))**

------------------------------------------------------------------------

`Event`

P2PTradeResult
--------------

### Description

nTradeResult: Integer

------------------------------------------------------------------------

`Function`

AcceptInvite()
--------------

### Description

Does a lua\_pushinteger of P2PTradeAcceptInvite.

------------------------------------------------------------------------

`Function`

AddItem(nInventoryItem)
-----------------------

### Description

Does a lua\_pushinteger of the result of P2PTradeAddItem of item
location specified by nInventoryItem.

### Params

-   **nInventoryItem** **(Integer)**

------------------------------------------------------------------------

`Function`

AmICommitted()
--------------

### Description

Does a lua\_pushboolean of GetCharacterUnit's trade bCommited.

------------------------------------------------------------------------

`Function`

CancelTrade()
-------------

### Description

Does a lua\_pushinteger of the result of P2PTradeCancel.

------------------------------------------------------------------------

`Function`

CanInitiateTrade(unitP)
-----------------------

### Description

Does a lua\_pushinteger of the result of CanInitiateP2PTrade, or a
boolean false if null.

### Params

-   **unitP** **(CUnit)**

------------------------------------------------------------------------

`Function`

DeclineInvite()
---------------

### Description

Does a lua\_pushinteger of P2PTradeDeclineInvite.

------------------------------------------------------------------------

`Function`

GetMyTradeMoney()
-----------------

------------------------------------------------------------------------

`Function`

GetPartnerTradeMoney()
----------------------

------------------------------------------------------------------------

`Function`

GetTradeItems()
---------------

### Description

Does a lua\_newtable with an index and tradeable items.

------------------------------------------------------------------------

`Function`

InitiateTrade(unitP)
--------------------

### Description

Does a lua\_pushinteger of the result of P2PTradeInitiate.

### Params

-   **unitP** **(CUnit)**

------------------------------------------------------------------------

`Function`

IsPartnerCommitted()
--------------------

### Description

Does a lua\_pushboolean of the trade partner's bCommited.

------------------------------------------------------------------------

`Function`

IsTrading()
-----------

### Description

Does a lua\_pushboolean of IsP2PTrading.

------------------------------------------------------------------------

`Function`

PrepareInfractionReport()
-------------------------

------------------------------------------------------------------------

`Function`

RemoveItem(nInventoryItem)
--------------------------

### Description

Does a lua\_pushinteger of the result of P2PTradeRemoveItem of item
location specified by nInventoryItem.

### Params

-   **nInventoryItem** **(Integer)**

------------------------------------------------------------------------

`Function`

SetMoney()
----------

------------------------------------------------------------------------

`Function`

UnCommit()
----------
