AccountItemLib
==============

------------------------------------------------------------------------

`Enum`

CodeEnumAccountCurrency
-----------------------

-   **None**
-   **CREDD**
-   **RealmTransfer**
-   **NameChange**
-   **Essence**
-   **MysticShiny**
-   **Omnibits**
-   **NCoins**
-   **Loyalty**
-   **ServiceToken**

------------------------------------------------------------------------

`Enum`

CodeEnumAccountOperation
------------------------

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

`Enum`

CodeEnumDailyLoginRewardTier
----------------------------

-   **Normal**
-   **Milestone**

------------------------------------------------------------------------

`Enum`

CodeEnumDailyLoginRewardType
----------------------------

-   **AccountItem**

------------------------------------------------------------------------

`Enum`

CodeEnumEntitlement
-------------------

-   **BaseCharacterProgressionCaps**
-   **BaseCharacterSlots**
-   **BaseCurrencyCaps**
-   **EconomyParticipation**
-   **GuildsAccess**
-   **FullSocialParticipation**
-   **CREDDUsage**
-   **InGameCSAccess**
-   **CostumeSlots**
-   **Signature**
-   **Free**
-   **ExtraAuctions**
-   **ExtraCommodity**
-   **ExtraBankSlots**
-   **FullGuildsAccess**
-   **WakeHereCooldownReduction**
-   **TwoStepVerification**
-   **LoyaltyBonusCoordinateCraftingRadius**
-   **ExtraCommodityOrders**
-   **ExtraDecorSlots**
-   **AdditionalCostumeUnlocks**
-   **LoyaltyExtraCommodityOrders**
-   **LoyaltyExtraAuctions**
-   **LoyaltyChallengeBonus**
-   **LoyaltyRestXpBonus**
-   **FraudCheck**

------------------------------------------------------------------------

`Function`

ClaimPendingItemGroup() (Deprecated)
------------------------------------

------------------------------------------------------------------------

`Function`

ClaimPendingSingleItem() (Deprecated)
-------------------------------------

------------------------------------------------------------------------

`Function`

GetAccountCurrency()
--------------------

------------------------------------------------------------------------

`Function`

GetAccountEntitlement()
-----------------------

------------------------------------------------------------------------

`Function`

GetAccountEntitlements()
------------------------

------------------------------------------------------------------------

`Function`

GetAccountItems()
-----------------

------------------------------------------------------------------------

`Function`

GetCharacterEntitlement()
-------------------------

------------------------------------------------------------------------

`Function`

GetCharacterEntitlements()
--------------------------

------------------------------------------------------------------------

`Function`

GetDailyLoginRewards()
----------------------

------------------------------------------------------------------------

`Function`

GetDailyLoginRewardsAvailable()
-------------------------------

------------------------------------------------------------------------

`Function`

GetEntitlementCount()
---------------------

------------------------------------------------------------------------

`Function`

GetInstantEventCount()
----------------------

------------------------------------------------------------------------

`Function`

GetLoginDays()
--------------

------------------------------------------------------------------------

`Function`

GetMaxEntitlementCount()
------------------------

------------------------------------------------------------------------

`Function`

GetPendingAccountItemGroups()
-----------------------------

------------------------------------------------------------------------

`Function`

GetPendingAccountSingleItems() (Deprecated)
-------------------------------------------

------------------------------------------------------------------------

`Function`

GiftPendingItemGroupToAccount() (Deprecated)
--------------------------------------------

------------------------------------------------------------------------

`Function`

GiftPendingItemGroupToCharacter() (Deprecated)
----------------------------------------------

------------------------------------------------------------------------

`Function`

GiftPendingItemToAccount() (Deprecated)
---------------------------------------

------------------------------------------------------------------------

`Function`

GiftPendingItemToCharacter() (Deprecated)
-----------------------------------------

------------------------------------------------------------------------

`Function`

MarkAllInventoryItemsAsSeen()
-----------------------------

------------------------------------------------------------------------

`Function`

MarkAllPendingItemsAsSeen()
---------------------------

------------------------------------------------------------------------

`Function`

RedeemCoupon() (Deprecated)
---------------------------

------------------------------------------------------------------------

`Function`

RequestDailyLoginRewards()
--------------------------

------------------------------------------------------------------------

`Function`

ReturnPendingItemGroup() (Deprecated)
-------------------------------------

------------------------------------------------------------------------

`Function`

ReturnPendingSingleItem() (Deprecated)
--------------------------------------

------------------------------------------------------------------------

`Function`

TakeAccountItem() (Deprecated)
------------------------------
