CSIsLib
=======

### Description

Allows the UI to interact with Client Side Interaction minigames, such
as patern matching and timed clicking.

------------------------------------------------------------------------

`Function`

CancelActiveCSI()
-----------------

### Description

Stops the current Client Side Interaction

------------------------------------------------------------------------

`Function`

CSIProcessInteraction(mouseDown)
--------------------------------

### Description

Processes the user's input for the Client Side Interaction. Different
types of Client Side Interactions behave differently

### Params

-   **mouseDown** **(Boolean)** - Determines how to update the Client
    Side Interaction.\
    For Yes/No Interactions: true indicates that the user clicked yes,
    false indicates no\
    For PressAndHold: true indicates that the button was pressed down,
    false indicates that the button is up\
    For RapidTapping: true indicates that the button was pressed down\

### Usage/Example

```lua
    Functionality per CSI type:
    Precision:
    Button Down: Informs the CSI of a button click.
    Button Up: Nothing

    Metronome:
    Button Down: Informs the CSI of a button click
    ButtonUp: Nothing

    Rapid Tap:
    Button Down: Starts the CSI if it wasn't already running.  Informs the CSI of a button click.
    Button Up: Nothing

    Press and Hold:
    Button Down: Starts the CSI if it wasn't already running.  Tells the CSI that the button is being held.
    Button Up: Tells the CSI that the button isn't being held.

    Yes/No:
    ButtonDown: Treats the CSI as if the player clicked "Yes"
    ButtonUp: Treats the CSI as if the player clicked "No"
```

------------------------------------------------------------------------

`Function`

GetActiveCSI()
--------------

### Description

Gets a table containing information on the active CSI. Returns nil if
there is no active CSI.

### Return Value

-   **Table** - A table containing information on the current Client
    Side Interaction.
    -   **eType** **(CSIsLib.ClientSideInteractionType)** - The type of
        CSI that is active.
    -   **strContext** **(String)** - A string containing the text that
        should be displayed for the current CSI.
    -   **nThreshold** **(Integer)** - The number of misses allowed for
        this CSI before the user fails. This variable only exists for
        Metronome CSIs.

------------------------------------------------------------------------

`Function`

GetTimeRemainingForActiveCSI()
------------------------------

### Description

Gets the time remaining before the user fails the current CSI.

### Return Value

-   **Float** - The time remaining before the user fails, in seconds

------------------------------------------------------------------------

`Function`

IsCSIRunning()
--------------

### Description

Determines if the active CSI has been started.

### Return Value

-   **Boolean** - Whether the active CSI is running or not.

------------------------------------------------------------------------

`Function`

SelectCSIOption(option)
-----------------------

### Description

Enters the user's input for the current Client Side Interaction. This
includes final keypad entries for the Keypad interactions and the Id of
the buttons pressed in Memory interactions

### Params

-   **option** **(Integer)** - The number that was input for the Client
    Side Interaction. This includes the number for keypad entries and
    the Id number for Memory selections

------------------------------------------------------------------------

`Function`

StartActiveCSI()
----------------

### Description

Starts the currently active CSI.
