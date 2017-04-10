CREDDExchangeLib
================

### Description

This library is one of the primary ways that the player interacts with
the CREDD Exchange. This does not include creating and fulfilling
orders, which is handled by the ActionConfirmButton.

------------------------------------------------------------------------

`Enum`

CodeEnumAccountOperation
------------------------

### Description

The different types of account operations that the player can perform.

-   **MTXPurchase**
-   **ClaimPending**
-   **ReturnPending**
-   **TakeItem**
-   **GiftItem**
-   **RedeemCoupon**
-   **GetCREDDExchangeInfo**
-   **SellCREDD**
-   **BuyCREDD**
-   **CancelCREDDOrder**
-   **ExpireCREDDOrder**
-   **SellCREDDComplete**
-   **BuyCREDDComplete**
-   **CREDDRedeem**
-   **RequestDailyLoginRewards**

------------------------------------------------------------------------

`Enum`

CodeEnumAccountOperationResult
------------------------------

### Description

Results of various account operations. This includes reasons the
operation might have failed, as well as "Ok" for successful operations.

-   **Ok**
-   **GenericFail**
-   **DBError**
-   **MTXError**
-   **InvalidOffer**
-   **InvalidPrice**
-   **NotEnoughCurrency**
-   **NeedTransaction**
-   **InvalidAccountItem**
-   **InvalidPendingItem**
-   **InvalidInventoryItem**
-   **NoConnection**
-   **NoCharacter**
-   **AlreadyClaimed**
-   **MaxEntitlementCount**
-   **NoRegift**
-   **NoGifting**
-   **InvalidFriend**
-   **InvalidCoupon**
-   **CannotReturn**
-   **Prereq**
-   **CREDDExchangeNotLoaded**
-   **NoCREDD**
-   **NoMatchingOrder**
-   **InvalidCREDDOrder**
-   **Cooldown**
-   **MissingEntitlement**
-   **AlreadyClaimedMultiRedeem**

------------------------------------------------------------------------

`Function`

CancelOrder(crdOrder)
---------------------

### Description

Removes a CREDD Exchange Order from the Exchange.

### Params

-   **crdOrder**
    **([CREDDExchangeOrder](../Classes/CREDDExchangeOrder.md))** - The
    order that the player wishes to cancel.

### Usage/Example

```lua
    The CREDDExchangeInfoResults event is fired in response to this, informing the UI of the status of the operation.
```

------------------------------------------------------------------------

`Function`

GetCREDDHistory()
-----------------

### Description

Requests player's buy and sell history from the server.

### Usage/Example

```lua
    The server will send the results in the CREDDOperationHistoryResults event.
```

------------------------------------------------------------------------

`Function`

RequestExchangeInfo()
---------------------

### Description

Requests a list for the CREDD Exchange's stats and CREDDExchangeOrders.

### Usage/Example

    The server will fire the CREDDExchangeInfoResults event in response
