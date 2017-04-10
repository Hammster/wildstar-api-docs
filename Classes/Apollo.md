Apollo
======

### Description

A library that primarily contains system-level functionality, such as
registering events, controling addons, detecting key presses, and
manipulating console variables.

------------------------------------------------------------------------

`Enum`

AddonLoadStatus
---------------

### Description

An enum that describes the load state of an addon. This is primarily
used alongside the depricated GetAsyncLoad functionality.

-   **Loading**
-   **Loaded**
-   **LoadingError**

------------------------------------------------------------------------

`Enum`

DragDropCancelReason
--------------------

### Description

An enum that describes why a player's attempt to drag and drop something
with their mouse was canceled.

-   **EscapeKey**
-   **DroppedOnNothing**
-   **ClickedOnNothing**
-   **ClickedOnWorld**
-   **WindowMove**

------------------------------------------------------------------------

`Enum`

DragDropQueryResult
-------------------

### Description

The set of results that the player can get when attempting to drag and
drop something using the mouse.

-   **PassOn**
-   **Ignore**
-   **Accept**
-   **Invalid**

------------------------------------------------------------------------

`Event`

DragDropSysBegin
----------------

### Description

Fires when the player starts a drag-drop operation by holding the mouse
button down while the cursor is over a BagWindow or ActionBarButton.

### Params

-   **wndSource** **([Window](../WindowControls/Window.md))** - The
    window that the object originated from.
-   **strType** **(String)** - The type of object that will be affected
    by the drag-drop operation. This should either be "DDBagItem" for
    items and "DDSpellbookItem" for spells.
-   **nStartLocation** **(Integer)** - The location where the object was
    grabbed.

------------------------------------------------------------------------

`Event`

DragDropSysEnd
--------------

### Description

Fires whenever the player lets go of the mouse button during a drag-drop
operation.

### Params

-   **strType** **(String)** - The type of object that was dragged by
    the operation.
-   **nEndLocation** **(Integer)** - The location where the object was
    dropped.

------------------------------------------------------------------------

`Event`

LuaError
--------

### Description

Fires whenever an error is thrown in an addon's code.

### Params

-   **tAddonInfo** **(Table)** - Information on the addon that threw the
    error.
    -   **eStatus** **(Integer)** - The addon's current status.
    -   **strName** **(String)** - The name of the addon where the error
        was thrown.
    -   **bCarbine** **(Boolean)** - Whether the addon that threw the
        error is a Carbine addon or a 3rd party addon.
    -   **strAuthor** **(String)** - The addon's author.
    -   **arErrors** **(Array of String)** - An array of strings that
        contain the error messages.
-   **strError** **(String)** - The error messages for the Lua error.
-   **bCanIgnore** **(Boolean)** - Whether the player can ignore the
    error or not.

### Remarks

It's worth noting that the information in tAddonInfo may not reflect the
addon that actually caused the error. If the source of the error is an
addon that is hooking into a function in another addon, tAddonInfo will
contain information on the addon that was hooked into, not the addon
that was the source of the error.

------------------------------------------------------------------------

`Event`

ModuleLoaded
------------

### Description

Fires when every addon has finished loading.

------------------------------------------------------------------------

`Event`

ModuleRestore (Deprecated)
--------------------------

------------------------------------------------------------------------

`Event`

SaveModules
-----------

### Description

Fires immediately before any addon calls its OnSave() function.

------------------------------------------------------------------------

`Event`

SystemKeyDown
-------------

### Description

Fires whenever the player presses a key.

### Params

-   **nKey** **(Integer)** - The ASCII code for the key that was
    pressed.

------------------------------------------------------------------------

`Event`

TextMessage (Deprecated)
------------------------

### Params

-   **iType** **(Integer)**
-   **strMessage** **(String)**

------------------------------------------------------------------------

`Function`

AddAddonErrorText(oAddon, strAddToError)
----------------------------------------

### Description

Adds a message to an addon's info.

### Params

-   **oAddon** **(String or Table)** - The addon that threw the error.
    This can either be an instance of the addon itself or the addon's
    name.
-   **strAddToError** **(String)** - The text that should be added to
    the addon's error list.

### Usage/Example

```lua
    The text that is added to the addon's error list can be found by calling Apollo.GetAddonInfo() on the item and accessing the arErrors element in the error that is returned.
```

------------------------------------------------------------------------

`Function`

AlertAppWindow()
----------------

### Description

Flashes the client's icon on the Windows taskbar if the game does not
have focus.

------------------------------------------------------------------------

`Function`

AssetFileSizeString(strFilename)
--------------------------------

### Description

Gets the file size of the specified asset.

### Params

-   **strFilename** **(String)** - The file name of the asset.

### Return Value

-   **String** - The asset's size, in bytes.

------------------------------------------------------------------------

`Function`

AssetFileTimeString(strFilename)
--------------------------------

### Description

Gets the date and time that the asset was last updated.

### Params

-   **strFilename** **(String)** - The asset's file name.

### Return Value

-   **String** - A string that contains the date and time when the
    specified asset was last updated.

------------------------------------------------------------------------

`Function`

BeginClickStick(wndSource, strType, strSprite, nStartLocation)
--------------------------------------------------------------

### Description

Causes the item or spell that the player clicked on to stick to the
cursor until the player clicks again. It is treated like drag-drop
functionality, only the player does not have to hold a button until the
end of the operation.

### Params

-   **wndSource** **([Window](../WindowControls/Window.md))** - The
    window where the click-stick operation began.
-   **strType** **(String)** - The type of item that the click stick is
    affecting. This value can be either "DDBagItem" or
    "DDSpellbookItem".
-   **strSprite** **(String)** - The file name of the sprite that
    replaces the cursor while the click-stick operation is active.
-   **nStartLocation** **(Integer)** - The location where the operation
    began.

------------------------------------------------------------------------

`Function`

BeginDragDrop(wndSource, strType, strSprite, nStartLocation)
------------------------------------------------------------

### Description

Starts a drag-drop operation on the item that the player clicked on.

### Params

-   **wndSource** **([Window](../WindowControls/Window.md))** - The
    window where the operation began.
-   **strType** **(String)** - The type of object that is being dragged
    in the operation. This can be either "DDBagItem" or
    "DDSpellbookItem".
-   **strSprite** **(String)** - The file name of the sprite that
    replaces the cursor during the operation.
-   **nStartLocation** **(Integer)** - The location where the drag-drop
    operation started.

------------------------------------------------------------------------

`Function`

CloseEscapableWindows()
-----------------------

### Description

Closes all of the windows that have the Escapable flag turned on.

### Return Value

-   **Boolean** - Whether any windows were closed or not.

------------------------------------------------------------------------

`Function`

CreateTimer(strTimerName, nInterval, bContinuous)
-------------------------------------------------

### Description

Creates a timer that can be run from Lua.

### Params

-   **strTimerName** **(String)** - The name of the timer.
-   **nInterval** **(Integer)** - How often the timer will fire.
-   **bContinuous** **(Boolean)** - Whether the timer will constantly
    run or only fire once before needing to be restarted. - Whether the
    timer will constantly run or only fire once before needing to be
    restarted.

### Usage/Example

```lua
    function TimerExample:OnLoad()
        Apollo.RegisterTimerHandler("TestTimer", "OnTestTimer", self)
        Apollo.CreateTimer("TestTimer", 1.0, false)
    end

    function TimerExample:OnTestTimer()
        Print("Timer has fired")
    end
```

### Remarks

Newly created timers are in the Running state and must be manually
stopped. Timers created this way have no functionality without a timer
handler that listens for when the timer fires. These timers are not
destroyed when they fire.\
\
While Apollo's timer functionality still works, we are moving more
towards using ApolloTimers. That doesn't mean that this functionality is
or will become depricated any time soon (we'll let you know when it
does), but you will see far fewer instances of us using them in code.

------------------------------------------------------------------------

`Function`

DisableAddon(strAddonName)
--------------------------

### Description

Disables the specified addon if it has any errors. Disabled addons do
not load after the UI is reloaded.

### Params

-   **strAddonName** **(String)** - The name of the addon that should be
    disabled.

------------------------------------------------------------------------

`Function`

DoesSpriteExist(strSpriteName)
------------------------------

### Description

Checks if a sprite with the given name exists in the Carbine sprite set.

### Params

-   **strSpriteName** **(String)** - The name of the sprite that the
    function looks for.

### Return Value

-   **Boolean** - Whether a sprite with the specified name was found or
    not.

------------------------------------------------------------------------

`Function`

DPF(strDebugMessage)
--------------------

### Description

Sends the string that is passed in to the client logs.

### Params

-   **strDebugMessage** **(String)** - The message that the function
    passes on to the client logs.

------------------------------------------------------------------------

`Function`

FindWindowByName(strWindowName)
-------------------------------

### Description

Searches through all of the addons that are registered with Apollo for a
window with the specified name.

### Params

-   **strWindowName** **(String)** - The name of the window that the
    function searches for.

### Return Value

-   **[Window](../WindowControls/Window.md)** - The window that was
    found by the search.

------------------------------------------------------------------------

`Function`

FormatNumber(oNumber, nDecimals, bCommas)
-----------------------------------------

### Description

Formats a number to include region-specific notations, such as
commas/periods in integers with 4+ digits, and truncates the value to a
specific number of decimal places.

### Params

-   **oNumber** **(Integer)** - The number that needs to be formatted.
    This can be either an integer or float.
-   **nDecimals** **(Integer)** - The number of decimal places to
    display
-   **bCommas** **(Boolean)** - Determines whether or not commas should
    be shown in numbers with 4 or more digits

### Return Value

-   **String** - The formatted number with all relevant punctuation

------------------------------------------------------------------------

`Function`

GetAddon(strAddonName)
----------------------

### Description

Gets all of the functions and variables from the instance of the
specified addon that is currently running.

### Params

-   **strAddonName** **(String)** - The name of the addon that the
    function will try to find.

### Return Value

-   **oAllTheThings** - All of the addon level variables contained in
    the addon, as well as a metatable with all of the addon's functions.

------------------------------------------------------------------------

`Function`

GetAddonInfo(strAddonName)
--------------------------

### Description

Gets a lot of performance information and a list of errors for the
specified addon.

### Params

-   **strAddonName** **(String)** - The name of the addon.

### Return Value

-   **Table** - A table that contains a large amount of information on
    the addon.
    -   **strFolder** **(String)** - The name of the folder where the
        addon is found.
    -   **strName** **(String)** - The addon's name.
    -   **strConfigureButtonText** **(String)** - The text that is shown
        on the addon's configure button.
    -   **bCarbine** **(Boolean)** - Whether the addon is an official
        Carbine addon or not.
    -   **strAuthor** **(String)** - The name of the addon's author.
    -   **bLoadOnStart** **(Boolean)** - Whether the addon is
        automatically loaded when the player logs in or the UI is
        reloaded.
    -   **nMemoryUsage** **(Integer)** - How much memory the addon takes
        up.
    -   **nTotalCalls** **(Integer)** - The number of API function calls
        the addon has made since it was started.
    -   **fTotalTime** **(Float)** - The total amount of processing time
        the addon has used since it was started, in milliseconds.
    -   **fLongestCall** **(Float)** - The longest it took to complete
        any one function call in the addon since the addon started.
    -   **fCallTimePerSecond** **(Float)** - The amount of processing
        time the addon is currently taking every second.
    -   **fCallTimePerFrame** **(Float)** - The amount of processing
        time the addon is currently taking every frame.
    -   **bRunning** **(Boolean)** - Whether the addon is currently
        running or not.
    -   **eStatus** **(OptionsScreen.CodeEnumAddonStatus)** - The
        addon's current status.
    -   **fLastModified** **(Float)** - The number of seconds since the
        addon was last modified.
    -   **bIgnoreVersion** **(Boolean)** - Whether the addon should
        ignore API version mismatches for loading purposes.
    -   **nAPIVersion** **(Integer)** - The API version that the addon
        uses.
    -   **bHasConfigure** **(Boolean)** - Whether the addon has a
        configure menu that was set up when the addon was registered.
    -   **arErrors** **(Array of String)** - An array of error messages
        that were caused by the addon.
    -   **strLastModified** **(String)** - The date and time that the
        addon was last modified.
    -   **strLastModifiedSort** **(String)** - The string used when
        sorting the addons by the date they were last modified. The
        string lists the year, month, day, and time.
    -   **arReplacedAddons** **(Array of String)** - The name of each
        addon that this addon replaces.

------------------------------------------------------------------------

`Function`

GetAPIVersion()
---------------

### Description

Gets the current API version used by the game.

### Return Value

-   **Integer** - Apollo's current API version.

------------------------------------------------------------------------

`Function`

GetAssetFolder()
----------------

### Description

Gets the name of the folder that contains all of the default UI's
assets.

### Return Value

-   **String** - The default UI's asset folder.

------------------------------------------------------------------------

`Function`

GetConsoleVariable(strVarName)
------------------------------

### Description

Gets the value of the specified console variable.

### Params

-   **strVarName** **(String)** - The name of the console variable whose
    value is requested.

### Return Value

-   **Value** - This value can be of any basic type (integer, float,
    boolean, string, nil), depending on which console variable is
    requested.

------------------------------------------------------------------------

`Function`

GetDisplaySize()
----------------

### Description

Gets the size of the client, as well as the size of the viewable portion
of the client window.

### Return Value

-   **Table** - The width and height of the window and the viewable
    portion of the window, as well as the scale that everything is drawn
    to.
    -   **nWidth** **(Integer)** - The window's width.
    -   **nHeight** **(Integer)** - The window's height.
    -   **nRawWidth** **(Integer)** - The width of the portion of the
        window where the game is actually shown.
    -   **nRawHeight** **(Integer)** - The height of the portion of the
        window where the game is actually shown.
    -   **fScale** **(Float)** - Objects in the game are scaled by this
        amount before being drawn.

### Remarks

In fullscreen mode, the width/height and raw width/height do not match
up exactly, but the difference is relatively insignificant. In windowed
mode, this is much more pronounced.

------------------------------------------------------------------------

`Function`

GetGameFonts()
--------------

### Description

Gets a list of all of the fonts that come with the game. Each font is
made up of a typeface and a font size.

### Return Value

-   **Array of Table** - An array with information of all of the fonts
    that are packaged with the game.
    -   **index** **(Integer)** - The index in the array, if the array
        was 0 based.
    -   **name** **(String)** - The name of the font.
    -   **face** **(String)** - The typeface used for the font.
    -   **size** **(Integer)** - The font size.

------------------------------------------------------------------------

`Function`

GetMaxResolutionWidth()
-----------------------

### Description

Returns the maximum width that the client can be set to.

### Return Value

-   **Integer** - The maximum resolution width.

------------------------------------------------------------------------

`Function`

GetMetaKeysDown()
-----------------

### Description

Gets a bit flag that tells which meta keys are currently pressed.

### Return Value

-   **Integer** - A bit flag of the Meta Keys that are currently pressed
    down. The value lines up with the GameLib.CodeEnumInputModifier
    enum.

### Usage/Example

```lua
    function Example:CheckMetaKey()
        local nKeysDown = Apollo.GetMetaKeysDown()
        local tKeys =
        {
            ["Shift"] = bit32.band(nKeysDown, GameLib.CodeEnumInputModifier.Shift) == GameLib.CodeEnumInputModifier.Shift,
            ["Control"] = bit32.band(nKeysDown, GameLib.CodeEnumInputModifier.Control) == GameLib.CodeEnumInputModifier.Control,
            ["Alt"] = bit32.band(nKeysDown, GameLib.CodeEnumInputModifier.Alt) == GameLib.CodeEnumInputModifier.Alt,
        }
        return tKeys
    end
```

------------------------------------------------------------------------

`Function`

GetMinResolutionWidth()
-----------------------

### Description

The minimum resolution width that the client can be set to.

### Return Value

-   **Integer** - The minimum resolution width.

------------------------------------------------------------------------

`Function`

GetMouse()
----------

### Description

Gets the mouse's position in screen coordinates.

### Return Value

-   **Table** - The mouse's current coordinates in screen space.
    -   **x** **(Integer)**
    -   **y** - Integer

------------------------------------------------------------------------

`Function`

GetMouseTargetWindow()
----------------------

### Description

Gets the window that the mouse is currently hovering over.

### Return Value

-   **[Window](../WindowControls/Window.md)** - The top-most window
    that the mouse is hovering over.

------------------------------------------------------------------------

`Function`

GetMoveMetaKey()
----------------

### Description

Gets the meta key that is bound to the Sprint action.

### Return Value

-   **GameLib.CodeEnumInputModifier** - The meta key that is bound to
    the Sprint action.

------------------------------------------------------------------------

`Function`

GetObjectSize(oVariable)
------------------------

### Description

Gets the memory size of an object.

### Params

-   **oVariable** **(Variable)** - The function will return the size of
    this variable. Any variable type can be passed in.

### Return Value

-   **Integer** - The size of the variable, in bytes.

------------------------------------------------------------------------

`Function`

GetPackage(strPackageName)
--------------------------

### Description

Returns information on a package that was registered with Apollo.

### Params

-   **strPackageName** **(String)** - The name of the package.

### Return Value

-   **Table** - Information about the package.
    -   **strName** **(String)** - The name of the package.
    -   **bAddon** **(Boolean)** - This value will return true if it is
        called within the lua file that registers the package. If it is
        called in an addon that simply uses the package, this returns
        false.
    -   **nVersion** **(Integer)** - The package's version.
    -   **strLoadError** **(String)** - Any load errors that may have
        occurred when attempting to get the package.
    -   **tAddonInfo** **(Table)** - A table that only exists if bAddon
        is true.
        -   **strAuthor** **(String)** - The name of the package's
            author.
        -   **nAPIVersion** **(Integer)** - The API version of that the
            addon was written with according to the Table of Contents.
    -   **tPackage** **(Table)** - All of the addon level variables and
        functions from the package in a convenient table.

------------------------------------------------------------------------

`Function`

GetScreenSize() (Deprecated)
----------------------------

### Description

Gets the size of the client window. This function has been replaced by
Apollo.GetDisplaySize()

------------------------------------------------------------------------

`Function`

GetStrata()
-----------

### Description

Gets an array of all of the window strata that are in use.

### Return Value

-   **Array of String** - The names of each strata that a window can be
    drawn in.

------------------------------------------------------------------------

`Function`

GetString(strCheck)
-------------------

### Description

Gets the localized string for the given string or id number.

### Params

-   **strCheck** **(String or Integer)** - The string or id that will
    poll the string.

### Return Value

-   **String** - The localized string that corresponds

------------------------------------------------------------------------

`Function`

GetTextWidth(strFontName, strInput)
-----------------------------------

### Description

Gets the number of pixels it takes to draw a specific piece of text with
a specific font.

### Params

-   **strFontName** **(String)** - The name of the font that to use in
    the width check.
-   **strInput** **(String)** - The text that the function is checking.

### Return Value

-   **Integer** - The width, in pixels, that it takes to draw the text
    with the given font.

------------------------------------------------------------------------

`Function`

GetTickCount()
--------------

### Description

Gets the number of milliseconds since the system was started.

### Return Value

-   **Integer** - The number of milliseconds that have elapsed since the
    system was started (up to 49.7 days)

------------------------------------------------------------------------

`Function`

GetWindowsInStratum(strStratum)
-------------------------------

### Description

Gets all of the windows in a specific stratum.

### Params

-   **strStratum** **(String)** - The function returns the windows found
    in the stratum whose name matches this string.

### Return Value

-   **Array of [Window](../WindowControls/Window.md)** - An array of
    windows found in the given stratum.

------------------------------------------------------------------------

`Function`

IsAltKeyDown()
--------------

### Description

Gets the state of the Alt key.

### Return Value

-   **Boolean** - Whether the Alt key is down or not.

------------------------------------------------------------------------

`Function`

IsCapsLockOn()
--------------

### Description

Gets the state of the Caps Lock button.

### Return Value

-   **Boolean** - Whether Caps Lock is on or not.

------------------------------------------------------------------------

`Function`

IsControlKeyDown()
------------------

### Description

Gets the state of the Control key.

### Return Value

-   **Boolean** - Whether the Control key is down or not.

------------------------------------------------------------------------

`Function`

IsShiftKeyDown()
----------------

### Description

Gets the state of the Shift key.

### Return Value

-   **Boolean** - Whether the Shift key is down or not.

------------------------------------------------------------------------

`Function`

IsSpriteLoaded(strSpriteName)
-----------------------------

### Description

Checks whether a specific sprite is loaded or not

### Params

-   **strSpriteName** **(String)** - The name of the sprite that the
    function is looking for.

### Return Value

-   **Boolean** - Whether the sprite is loaded or not.

------------------------------------------------------------------------

`Function`

IsWindowSubclassRegistered(strSubclassName)
-------------------------------------------

### Description

Determines whether the specified Window Subclass has been registered
with Apollo.

### Params

-   **strSubclassName** **(String)** - The name of the Window Subclass
    that the function will look for.

### Return Value

-   **Boolean** - Whether the Subclass is registered or not.

------------------------------------------------------------------------

`Function`

LinkAddon(tTarget, tSource)
---------------------------

### Description

Associates a module with a parent module in Apollo. This allows Apollo
to manage the addon's memory better.

### Params

-   **tTarget** **(Table)** - The "self" of the module that the function
    will link to.
-   **tSource** **(Table)** - The "self" of the module that is calling
    the function.

### Usage/Example

```lua
    local kOffsetEnum =
    {
        Left = 1,
        Top = 2,
        Right = 3,
        Bottom = 4,
    }

    function ContainerManager:OnDocumentReady()
        if self.xmlDoc == nil then
            return
        end

        self.luaLeftContainer = Container:new()
        self.luaRightContainer = Container:new()
        self.luaLeftContainer:Init(self)
        self.luaRightContainer:Init(self)

        self.luaLeftContainer:Move(-100, 0)
        self.luaRightContainer:Move(100, 0)
    end

    function Container:new(o)
        o = o or {}
        setmetatable(o, self)
        self.__index = self
        return o
    end

    function Container:Init(luaManager)
        Apollo.LinkAddon(luaManager, self)

        self.luaContainerManager = luaManager
        self.wndMain = Apollo.LoadForm(self.luaManager.xmlDoc, "ContainerWindow", nil, self)
    end

    function Container:Move(nDeltaX, nDeltaY)
        local tOffsets = {self.wndMain:GetAnchorOffsets()}

        tOffsets[kOffsetEnum.Left] = tOffsets[kOffsetEnum.Left] + nDeltaX
        tOffsets[kOffsetEnum.Right] = tOffsets[kOffsetEnum.Right] + nDeltaX

        tOffsets[kOffsetEnum.Top] = tOffsets[kOffsetEnum.Top] + nDeltaY
        tOffsets[kOffsetEnum.Bottom] = tOffsets[kOffsetEnum.Bottom] + nDeltaY

       self.wndMain:SetAnchorOffsets(unpack(tOffsets))
    end
```

------------------------------------------------------------------------

`Function`

LoadAnimations(strFileName)
---------------------------

### Description

Attempts to load a specific animation file.

### Params

-   **strFileName** **(String)** - The file name of the animation that
    the function will try to load.

### Return Value

-   **Boolean** - Whether the animation was successfully loaded or not.

------------------------------------------------------------------------

`Function`

LoadForm(strFile, strFormName, wndParent, tLuaEventHandler)
-----------------------------------------------------------

### Description

Loads a window from the specified form

### Params

-   **strFile** **(String or XmlDoc)** - The path to the XML document
    that contains the window, or the pre-loaded XML form.
-   **strFormName** **(String)** - The name of the window form that the
    function will try to load.
-   **wndParent** **([Window](../WindowControls/Window.md))** - The
    newly loaded window will be a child of this window. - The newly
    loaded window will be a child of this window.
-   **tLuaEventHandler** **(Table)** - The Lua object that owns the
    window. This value is usually "self", meaning the window that called
    the function. - The Lua object that owns the window. This value is
    usually "self", meaning the window that called the function.

### Return Value

-   **[Window](../WindowControls/Window.md)** - The window object that
    was loaded.

### Usage/Example

```lua
    self.wndMain = Apollo.LoadForm("SampleAddon.xml", "SampleAddonForm", nil, self)
```

------------------------------------------------------------------------

`Function`

LoadGlobalAnchors(strFile)
--------------------------

### Description

Loads the global anchors for the specified file.

### Params

-   **strFile** **(String)**

------------------------------------------------------------------------

`Function`

LoadSprites(strFile, strDoc)
----------------------------

### Description

Loads a sprite set.

### Params

-   **strFile** **(String or XmlDoc)** - The name of the form that
    contains the sprites, or the XmlDoc that contains them.
-   **strDoc** **(String)** - The name of the spriteDoc. This variable
    is optional.

------------------------------------------------------------------------

`Function`

LoadTemplates()
---------------

------------------------------------------------------------------------

`Function`

NoOp() (Deprecated)
-------------------

### Description

Does absolutely nothing.

------------------------------------------------------------------------

`Function`

ParseInput(strInput)
--------------------

### Description

Parses the input for slash commands. If the first character is not a
"/", it will not recognize the text as a slash command and will print it
to the Say chat channel.

### Params

-   **strInput** **(String)** - The string that the function will parse.

### Return Value

-   **String** - Returns the string for Console\_CommandNotFound if the
    slash command that was passed in was invalid. Otherwise, this
    returns an empty string.

------------------------------------------------------------------------

`Function`

RegisterAddon(tAddon, bHasConfigureFunction, arDependencies)
------------------------------------------------------------

### Description

Registers an addon to be loaded by Apollo. Addons that are not
registered do not work.

### Params

-   **tAddon** **(Table)** - The instance of the addon that is
    registering with Apollo. This is represented by "self". - The
    instance of the addon that is registering with Apollo. This is
    represented by "self".
-   **bHasConfigureFunction** **(Boolean)** - Whether addon has a
    Configure button in the Esc menu. If this value is true, then the
    addon needs an OnConfigure() function to handle the button signal
    event. - Whether addon has a Configure button in the Esc menu. If
    this value is true, then the addon needs an OnConfigure() function
    to handle the button signal event.
-   **arDependencies** **(Array of String)** - An array of addon names
    that must be loaded before this addon can be successfully loaded. -
    An array of addon names that must be loaded before this addon can be
    successfully loaded.

------------------------------------------------------------------------

`Function`

RegisterEventHandler(strEventName, strFunctionName, tLuaEventHandler)
---------------------------------------------------------------------

### Description

Matches an event that is fired with the Lua function that will handle
the event.

### Params

-   **strEventName** **(String)** - The name of the event to be handled.
-   **strFunctionName** **(String)** - The name of the function that
    will be called when the event is fired.
-   **tLuaEventHandler** **(Table)** - The addon's "self". - The addon's
    "self".

------------------------------------------------------------------------

`Function`

RegisterPackage(tPackage, strModule, nVersion, arDependencies)
--------------------------------------------------------------

### Description

Registers a package with Apollo so it can be used by other addons.

### Params

-   **tPackage** **(Table)** - The instance of the package that is
    registering with Apollo. This is usually represented by "self".
-   **strModule** **(String)** - The name of the package.
-   **nVersion** **(Integer)** - The packages version.
-   **arDependencies** **(Array of String)** - An array of addon or
    package names that must be loaded before this addon loads.

------------------------------------------------------------------------

`Function`

RegisterSlashCommand(strCommand, strFunction, tAddonHandler)
------------------------------------------------------------

### Description

Registers a slash command with Apollo and sets up a function to handle
the event fired when the command is used.

### Params

-   **strCommand** **(String)** - The slash command that will get
    registered with Apollo. This string should contain everything that
    comes after the / in the command.
-   **strFunction** **(String)** - The function that will handle the
    event that gets fired when the slash command is used.
-   **tAddonHandler** **(Table)** - The instance of the addon that will
    handle the event fired by the slash command. This is usually the
    addon's "self". - The instance of the addon that will handle the
    event fired by the slash command. This is usually the addon's
    "self".

------------------------------------------------------------------------

`Function`

RegisterTimerHandler(strTimerName, strFunction, tAddon)
-------------------------------------------------------

### Description

Pairs a timer with a function that will be called whenever the timer's
interval expires.

### Params

-   **strTimerName** **(String)** - The name of the timer that the
    function will pair with the handler function.
-   **strFunction** **(String)** - The function that will be called
    whenever the timer's interval expires.
-   **tAddon** **(Table)** - The instance of the addon that will handle
    the event fired when the timer's interval expires. This is usually
    the addon's "self". - The instance of the addon that will handle the
    event fired when the timer's interval expires. This is usually the
    addon's "self".

### Remarks

The default UI will replace RegisterTimerHandler calls with ApolloTimers
in the near future, but this method of using timers will not be
depricated.

------------------------------------------------------------------------

`Function`

RegisterWindowSubclass(strSubclassName, tAddon, tEvents)
--------------------------------------------------------

### Description

Registers a Window Subclass with Apollo.

### Params

-   **strSubclassName** **(String)** - The name of the Subclass.
-   **tAddon** **(Table)** - The instance of the module that is being
    registered. This is usually the module's "self".
-   **tEvents** **(Array of Table)** - An array of Event/Function
    Handler pairs that the Subclass wants to register with.
    -   **strEvent** **(String)** - The name of the event that the
        subclass wants to handle.
    -   **strFunction** **(String)** - The function within the subclass
        that will be called when the event is fired.

### Return Value

-   **Boolean** - Whether the subclass was sucessfully registered with
    Apollo or not.

### Remarks

Window Subclasses are a way to duplicate window functionality in
multiple addons.

------------------------------------------------------------------------

`Function`

RemoveEventHandler(strEventName, tModule)
-----------------------------------------

### Description

Removes an event handler from Apollo. This is primarily done for memory
management purposes.

### Params

-   **strEventName** **(String)** - The event that the module will stop
    handling.
-   **tModule** **(Table)** - The instance of the module that will stop
    handling the event. This is usually the module's "self".

------------------------------------------------------------------------

`Function`

ResetConsoleVariable(strConsoleVariableName)
--------------------------------------------

### Description

Returns a console variable to its default value.

### Params

-   **strConsoleVariableName** **(String)** - The name of the console
    variable that will be reset to its default.

------------------------------------------------------------------------

`Function`

SetConsoleVariable(strVariable, oValue)
---------------------------------------

### Description

Sets a console variable to a given value.

### Params

-   **strVariable** **(String)** - The name of the console variable that
    the function will update.
-   **oValue** **(CColor, String, Integer, Float, or Boolean)** - The
    new value of the console variable. The type of variable used must
    match the type needed by the Console Variable.

### Remarks

If a variable that is passed in can easily be converted to another type,
such as an integer to a boolean or vice versa, it will try to do so.

------------------------------------------------------------------------

`Function`

SetCursor(acCursor)
-------------------

### Description

Changes the cursor to another ApolloCursor.

### Params

-   **acCursor** **([ApolloCursor](../Classes/ApolloCursor.md))** - The
    cursor that will be shown after the function is called.

------------------------------------------------------------------------

`Function`

SetGlobalAnchor(strName, fPoint, nOffset, bOverwrite)
-----------------------------------------------------

### Description

Creates a named anchor that can be used for setting up windows for other
addons.

### Params

-   **strName** **(String)** - The name of the anchor.
-   **fPoint** **(Float)** - The anchor point for this anchor. - The
    anchor point for this anchor.
-   **nOffset** **(Integer)** - The offset from the anchor point that
    the named anchor should be set to. - The offset from the anchor
    point that the named anchor should be set to.
-   **bOverwrite** **(Boolean)** - Whether the function should overwrite
    any named anchors with the same name. - Whether the function should
    overwrite any named anchors with the same name.

------------------------------------------------------------------------

`Function`

SetMaxResolutionWidth(nWidth)
-----------------------------

### Description

Sets the maximum resolution width for the client.

### Params

-   **nWidth** **(Integer)** - The maximum resolution width that the
    client can be set to.

------------------------------------------------------------------------

`Function`

SetMinResolutionWidth(nWidth)
-----------------------------

### Description

Sets the minimum resolution width that the client can be set to.

### Params

-   **nWidth** **(Integer)** - The minimum width that the client can be
    set to.

------------------------------------------------------------------------

`Function`

SetMoveMetaKey(eMetaKey)
------------------------

### Description

Changes the meta key used for sprinting.

### Params

-   **eMetaKey** **(GameLib.CodeEnumInputModifier)** - The meta key that
    the sprint action should be bound to.

------------------------------------------------------------------------

`Function`

SetNavTextAnchor(nXAnchor, bGrowRight, nYAnchor, bGrowDown)
-----------------------------------------------------------

### Description

Changes how and where a tooltip is drawn.

### Params

-   **nXAnchor** **(Integer)** - The tooltip anchor point's x
    coordinate.
-   **bGrowRight** **(Boolean)** - If this is true, then the tooltip
    will be drawn to the right of the anchor point. If it is false, it
    will be drawn to the left.
-   **nYAnchor** **(Integer)** - The tooltip anchor point's y
    coordinate.
-   **bGrowDown** **(Boolean)** - If this is true, then the tooltip will
    be drawn below the anchor point. If it is false, it will be drawn
    above it.

------------------------------------------------------------------------

`Function`

StartTimer(strTimerName)
------------------------

### Description

Starts a timer that is not currently running.

### Params

-   **strTimerName** **(String)** - The name of the timer that the
    function should start.

### Remarks

Timers created by Apollo are being replaced by ApolloTimer objects in
the default UI. That does not mean that this functionality is being
depricated.

------------------------------------------------------------------------

`Function`

StopTimer(strTimerName)
-----------------------

### Description

Stops a timer that is currently running.

### Params

-   **strTimerName** **(String)** - The name of the timer that the
    function should stop.

------------------------------------------------------------------------

`Function`

StringLength()
--------------

------------------------------------------------------------------------

`Function`

StringToLower(strInput)
-----------------------

### Description

Changes all of the characters in a string to lower case.

### Params

-   **strInput** **(String)** - The string that will be changed to lower
    case.

### Return Value

-   **String** - The updated string.

------------------------------------------------------------------------

`Function`

SuspendAddon(strAddonName)
--------------------------

### Description

Turns off an addon that is throwing errors until the UI is reloaded.

### Params

-   **strAddonName** **(String)** - The name of the addon that the
    function will try to suspend.

### Remarks

If the addon that the function tries to suspend has no errors, it will
not be suspended.

------------------------------------------------------------------------

`Function`

UnlinkAddon(tTarget, tSource)
-----------------------------

### Description

Frees up the memory used by a linked addon.

### Params

-   **tTarget** **(Table)** - The addon that the module was linked to.
-   **tSource** **(Table)** - The instance of the module that is being
    unlinked. This is usually the module's "self".
