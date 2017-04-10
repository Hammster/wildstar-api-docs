MailSystemLib
=============

------------------------------------------------------------------------

`Function`

AtMailbox()
-----------

### Description

Does a lua\_pushboolean if CharacterUnit is in range of a mailbox.

------------------------------------------------------------------------

`Function`

DeleteMultipleMessages()
------------------------

------------------------------------------------------------------------

`Function`

GetAttachmentMaxCount()
-----------------------

------------------------------------------------------------------------

`Function`

GetInbox()
----------

### Description

Does a lua\_newtable of the inbox contents.

------------------------------------------------------------------------

`Function`

GetItemFromInventoryId(nSlot)
-----------------------------

### Description

Returns a new instance of an item that is a copy of an Inventory item
specified by nSlot.\
// NOTE: This function should be moved to a
LuaGameLibrary\_InventorySystem

### Params

-   **nSlot** **(Integer)**

------------------------------------------------------------------------

`Function`

GetMessageCharacterLimit()
--------------------------

------------------------------------------------------------------------

`Function`

GetNameCharacterLimit()
-----------------------

------------------------------------------------------------------------

`Function`

GetRealmCharacterLimit()
------------------------

------------------------------------------------------------------------

`Function`

GetSendCost()
-------------

------------------------------------------------------------------------

`Function`

GetSubjectCharacterLimit()
--------------------------

------------------------------------------------------------------------

`Function`

Is()
----

------------------------------------------------------------------------

`Function`

IsThereUnreadMail()
-------------------

### Description

Does a lua\_pushboolean if there is unread mail.

------------------------------------------------------------------------

`Function`

MarkMultipleMessagesAsRead()
----------------------------

------------------------------------------------------------------------

`Function`

TakeAllAttachmentsFromMultipleMessages()
----------------------------------------

------------------------------------------------------------------------

`Method`

DeleteMessage(pEmail)
---------------------

### Description

Runs pEmail's DeleteMessage.

### Params

-   **pEmail** **(CClientEmail)** - (May be passed by default with :
    operator)

------------------------------------------------------------------------

`Method`

GetExpirationTime(pEmail)
-------------------------

### Description

Does a lua\_pushnumber of the email's expiration time, or nil if null.

### Params

-   **pEmail** **(CClientEmail)** - (May be passed by default with :
    operator)

------------------------------------------------------------------------

`Method`

GetIdStr()
----------

------------------------------------------------------------------------

`Method`

GetMessageInfo(pEmail)
----------------------

### Description

Does a lua\_newtable of the email's info, or nil if null.

### Params

-   **pEmail** **(CClientEmail)** - (May be passed by default with :
    operator)

------------------------------------------------------------------------

`Method`

GetSenderType()
---------------

------------------------------------------------------------------------

`Method`

MarkAsRead(pEmail)
------------------

### Description

Runs pEmail's MarkAsRead.

### Params

-   **pEmail** **(CClientEmail)** - (May be passed by default with :
    operator)

------------------------------------------------------------------------

`Method`

PayCoD()
--------

------------------------------------------------------------------------

`Method`

PrepareInfractionReport()
-------------------------

------------------------------------------------------------------------

`Method`

ReturnToSender()
----------------

------------------------------------------------------------------------

`Method`

TakeAllAttachments(pEmail)
--------------------------

### Description

Runs pEmail's TakeAllAttachments.

### Params

-   **pEmail** **(CClientEmail)** - (May be passed by default with :
    operator)

------------------------------------------------------------------------

`Method`

TakeAttachment()
----------------

### Description

// Currently has no implementation

------------------------------------------------------------------------

`Method`

TakeMoney()
-----------
