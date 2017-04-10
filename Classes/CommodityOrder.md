CommodityOrder
==============

### Prefix: order

### Description

A buy or sell order on the commodities exchange.

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Determines if a variable is a CommodityOrder or not.

### Params

-   **oVariable** **(Variable)** - The variable that the function will
    check.

### Return Value

-   **Boolean** - Whether the variable is a CommodityOrder or not.

------------------------------------------------------------------------

`Function`

newBuyOrder(itemTarget)
-----------------------

### Description

Creates a new Buy order for the given item.

### Params

-   **itemTarget** **([Item](../Classes/Item.md))** - The item that the
    buy order will try to purchase.

### Return Value

-   **[CommodityOrder](../Classes/CommodityOrder.md)** - The new buy
    order that was created.

### Remarks

The new order will have a count, and price per unit of 1 after it is
created.

------------------------------------------------------------------------

`Function`

newSellOrder(itemSelling)
-------------------------

### Description

Creates a new Sell order for the given item.

### Params

-   **itemSelling** **([Item](../Classes/Item.md))** - The item that
    the sell order will attempt to sell.

### Return Value

-   **[CommodityOrder](../Classes/CommodityOrder.md)** - A new Sell
    order for the given item.

### Remarks

The new order will have a count, and price per unit of 1 after it is
created.

------------------------------------------------------------------------

`Method`

\_\_eq(orderCompare) (Deprecated)
---------------------------------

### Description

Checks whether the given CommodityOrder is equal to the one that called
this function.

### Params

-   **orderCompare**
    **([CommodityOrder](../Classes/CommodityOrder.md))** - The
    CommodityOrder that will be compared to the one that called this
    function.

### Return Value

-   **Boolean** - Whether the two CommodityOrders are the same.

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

The garbage collection function for the CommodityOrder. This should
never have to be called from Lua.

------------------------------------------------------------------------

`Method`

Cancel()
--------

### Description

Cancels an active CommodityOrder

### Remarks

Any items or money remaining in the order will be mailed to the player
after it is canceled.

------------------------------------------------------------------------

`Method`

CanPost()
---------

### Description

Determines if the CommodityOrder can be posted.

### Return Value

-   **Boolean** - Whether the CommodityOrder can be posted or not.

### Remarks

A CommodityOrder cannot be posted if it is already posted, if the order
is for less than 1 item, if the price per unit is less than 1 copper, or
if the player is already at their maximum number of commodity orders.

------------------------------------------------------------------------

`Method`

GetCount()
----------

### Description

Gets the number of items left in the CommodityOrder

### Return Value

-   **Integer** - The number of items that the CommodityOrder will try
    to buy or sell before it ends.

------------------------------------------------------------------------

`Method`

GetExpirationTime()
-------------------

### Description

Gets the number of seconds between Jan 1st, 1970 and when the commodity
order will expire.

### Return Value

-   **Integer** - The number of seconds between Jan 1st, 1970 and when
    the commodity order will expire.

------------------------------------------------------------------------

`Method`

GetItem()
---------

### Description

Gets the item that the CommodityOrder is trying to buy or sell.

### Return Value

-   **[Item](../Classes/Item.md)** - The item that the CommodityOrder
    is looking for or selling.

------------------------------------------------------------------------

`Method`

GetListTime()
-------------

### Description

Gets the amount of time between Jan 1st, 1970 and when the Commodity
Order was posted, in seconds.

### Return Value

-   **[Time](../Classes/Time.md)** - The number of seconds between Jan
    1st, 1970 and when the Commodity Order was posted

------------------------------------------------------------------------

`Method`

GetPricePerUnit()
-----------------

### Description

Gets the amount of money that the CommodityOrder is buying or selling
its associated item for.

### Return Value

-   **[Money](../Classes/Money.md)** - How much the Commodity Order is
    trying to buy or sell its item for.

------------------------------------------------------------------------

`Method`

GetReservePricePerUnit() (Deprecated)
-------------------------------------

------------------------------------------------------------------------

`Method`

GetTax()
--------

### Description

Gets the amount of money that the player has to pay to post a Sell
order.

### Return Value

-   **[Money](../Classes/Money.md)** - The amount of money that is
    required to post the sell order.

------------------------------------------------------------------------

`Method`

IsBuy()
-------

### Description

Determines if a CommodityOrder is a buy order or sell order.

### Return Value

-   **Boolean** - If this is true, then the order is a buy order.
    Otherwise, it's a sell order.

------------------------------------------------------------------------

`Method`

IsForceImmediate()
------------------

### Description

Determines if the buy or sell order is set up to find the CommodityOrder
of the opposite type with the best price for the same item so it
completes immediately.

### Return Value

-   **Boolean** - Whether the CommodityOrder is trying to buy or sell
    the item immediately.

------------------------------------------------------------------------

`Method`

IsPosted()
----------

### Description

Determines if the CommodityOrder is already posted or not.

### Return Value

-   **Boolean** - Whether the CommodityOrder was already posted or not.

------------------------------------------------------------------------

`Method`

Post() (Deprecated)
-------------------

### Description

Attempts to post the CommodityOrder on the Commodities Market.

### Remarks

The PostCommodityOrderResult event will fire in response to this
function.

------------------------------------------------------------------------

`Method`

SetCount(nNewCount)
-------------------

### Description

Sets the number of items that the CommodityOrder is looking to buy or
sell before it is completed.

### Params

-   **nNewCount** **(Integer)** - The value that the function will try
    to change the CommodityOrder's count to.

### Return Value

-   **Boolean** - Whether the count was successfully updated or not.

------------------------------------------------------------------------

`Method`

SetForceImmediate(bSellNow)
---------------------------

### Description

Changes the CommodityOrder so it attempts to buy or sell its items for
the best price when it is posted.

### Params

-   **bSellNow** **(Boolean)** - The value that the CommodityOrder's
    "force immediate" flag will be changed to.

### Return Value

-   **Boolean** - Whether the CommodityOrder's "force immediate" flag
    was successfully set or not.

------------------------------------------------------------------------

`Method`

SetPrices(monPrice)
-------------------

### Description

Sets the price that the CommodityOrder will try to buy or sell its items
for.

### Params

-   **monPrice** **([Money](../Classes/Money.md))** - The amount that
    the commodity order will attempt to buy or sell its items for per
    unit.

### Return Value

-   **Boolean** - Whether the price was successfully set or not.
