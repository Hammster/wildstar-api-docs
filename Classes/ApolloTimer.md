ApolloTimer
===========

------------------------------------------------------------------------

`Function`

Create(fInterval, bRepeat, strFunctionName, tLuaEventHandler)
--------

### Description

Function to create a new instance for a timer that will call a function continuously or only once after a specified time.

### Params
-   **fInterval** **(Integer)** - The time in seconds between calling the callback function.
-   **bRepeat** **(Boolean)** - Should the timer fire continuously or only once.
-   **strFunctionName** **(String)** - The name of the function that will be called when the specified time has passed.
-   **tLuaEventHandler** **(Table)** - The addons "self".

### Return Value
-  **[ApolloTimer](../Classes/ApolloTimer.md)** - An instance of the new timer.

### Remarks

The created timer instance is active by default after creation so it's advised to stop it right away if it's desired to start/stop at a later time.

### Usage/Example

```lua
    function Addon:CreateAutostartTimer()
        self.timerAutostart = ApolloTimer.Create(2.0, true, "OnAutoStartTimerUpdate", self)
    end

    function Addon:OnAutoStartTimerUpdate()
        -- Execute code continuously every 2 seconds
    end


    function Addon:CreateDelayedTimer()
        self.timerDelayed = ApolloTimer.Create(2.0, true, "OnDelayedTimerUpdate", self)
        self.timerDelayed:Stop()
    end

    function Addon:OnDelayedTimerUpdate()
        -- Execute code continuously every 2 seconds
    end
```
------------------------------------------------------------------------

`Function`

is()
----

------------------------------------------------------------------------

`Method`

\_\_eq() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

------------------------------------------------------------------------

`Method`

Set(fInterval, bRepeat)
-----

### Description

Adjust the parameters of an existing instance of a timer.

### Params
-   **fInterval** **(Integer)** - The time in seconds between calling the callback function.
-   **bRepeat** **(Boolean)** - Should the timer fire continuously or only once.

### Usage/Example

```lua
    function Addon:SetTimer()
        self.timer:Set(1.0, false)
        self.timer:Start()
    end
```
------------------------------------------------------------------------

`Method`

Start()
-------

### Description

Start the instace of a timer. After the set time the specified function will be called continously or only once.

### Usage/Example

```lua
    function Addon:StartTimer()
        self.timer:Start()
    end
```
------------------------------------------------------------------------

`Method`

Stop()
------

### Description

Stop the instance of a timer.

### Usage/Example

```lua
    function Addon:StopTimer()
        self.timer:Stop()
    end
```
