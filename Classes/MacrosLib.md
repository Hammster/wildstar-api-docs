MacrosLib
=========

------------------------------------------------------------------------

`Function`

CreateMacro()
-------------

### Description

Does a lua\_pushinteger of the new macro's id.

------------------------------------------------------------------------

`Function`

DeleteMacro(nId)
----------------

### Description

Runs DeleteMacro specified by nId.

### Params

-   **nId** **(Integer)**

------------------------------------------------------------------------

`Function`

DoMacro(nId)
------------

### Description

Runs DoMacro specified by nId.

### Params

-   **nId** **(Integer)**

------------------------------------------------------------------------

`Function`

GetMacro(nId)
-------------

### Description

Does a LuaPushMacro specified by nId.

### Params

-   **nId** **(Integer)**

------------------------------------------------------------------------

`Function`

GetMacroIconList()
------------------

### Description

Does a lua\_newtable with an index and spritenames of the macro icons.

------------------------------------------------------------------------

`Function`

GetMacrosList()
---------------

### Description

Does a LuaPushMacro with an index of the macros.

------------------------------------------------------------------------

`Function`

SaveMacros()
------------

### Description

Does a lua\_pushboolean of the save's result.

------------------------------------------------------------------------

`Function`

SetMacroData(nId, bGlobal, strName, strIcon, strCommands)
---------------------------------------------------------

### Params

-   **nId** **(Integer)**
-   **bGlobal** **(Boolean)**
-   **strName** **(String)**
-   **strIcon** **(String)**
-   **strCommands** **(String)**
