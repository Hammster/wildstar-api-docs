CombatFloater
=============

------------------------------------------------------------------------

`Enum`

CodeEnumCCStateApplyRulesResult
-------------------------------

### Description

The possible results when something attempts to apply a Crowd Control
state to a unit.

-   **Ok**
-   **InvalidCCState**
-   **NoTargetSpecified**
-   **Target\_Immune**
-   **Target\_InfiniteInterruptArmor**
-   **Stacking\_DoesNotStack**
-   **Stacking\_ShorterDuration**
-   **Target\_InterruptArmorReduced**
-   **Target\_InterruptArmorBlocked**
-   **DiminishingReturns\_TriggerCap**

------------------------------------------------------------------------

`Enum`

CodeEnumCombatMomentum
----------------------

### Description

The different types of Combat Momentum bonuses that a player can earn.

-   **Impulse**
-   **KillingPerformance**
-   **KillChain**
-   **Evade**
-   **Interrupt**
-   **CCBreak**

------------------------------------------------------------------------

`Enum`

CodeEnumExpReason
-----------------

### Description

The possible sources that a player can gain experience from.

-   **Invalid**
-   **Load**
-   **Cheat**
-   **KillCreature**
-   **Quest**
-   **ClusterBonus**
-   **Spell**
-   **Exploration**
-   **QuestEpisodeCompletion**
-   **PathMission**
-   **PathEpisode**
-   **KillPerformance**
-   **MultiKill**
-   **KillingSpree**
-   **TelegraphInterrupt**
-   **TelegraphEvade**
-   **Momentum**
-   **Rested**
-   **PublicEvent**
-   **DailyQuest**
-   **PeriodicQuest**

------------------------------------------------------------------------

`Enum`

CodeEnumFloaterCollisionMode
----------------------------

### Description

The collision modes that floating combat text can be set to.

-   **IgnoreCollision**
-   **Horizontal**
-   **Vertical**

------------------------------------------------------------------------

`Enum`

CodeEnumFloaterEffect
---------------------

### Description

A list of particle effects that can be added to floating combat text

-   **Flames**
-   **BluishWhite**
-   **Sparks**
-   **Spiral**
-   **Cloud**
-   **Splotches**
-   **SlashBlood**
-   **Impact**
-   **SplatBlood**
-   **Helix**
-   **ShadowFire**
-   **Cold**
-   **Stars**

------------------------------------------------------------------------

`Enum`

CodeEnumFloaterLocation
-----------------------

### Description

The location on a unit that the floating text would spawn from.

-   **Top**
-   **Head**
-   **Chest**
-   **Back**
-   **Bottom**

------------------------------------------------------------------------

`Event`

DamageOrHealingDone
-------------------

### Description

Fires whenever damage or healing is done to a unit within the player's
area of interest.

### Params

-   **unitCaster** **([Unit](../Classes/Unit.md))** - The unit that
    used the ability that caused the damage or healing.
-   **unitTarget** **([Unit](../Classes/Unit.md))** - The unit that
    received the damage or healing.
-   **eDamageType** **(GameLib.CodeEnumDamageType)** - The type of
    damage that was done to the target.
-   **nHealthChange** **(Integer)** - The amount that the target's
    health was changed by.
-   **nShieldAbsorbAmount** **(Integer)** - The amount of damage that
    was absorbed by the unit's shields.
-   **nAbsorbedAmount** **(Integer)** - The amount of damage that was
    absorbed by the unit's absorption shield.
-   **bIsCritical** **(Boolean)** - Whether the damage or healing effect
    was a critical hit.
-   **strSpellName** **(String)** - The name of the ability that caused
    the damage or healing.

------------------------------------------------------------------------

`Function`

AddDigitSpriteSet(strSpriteSetName)
-----------------------------------

### Description

Registers a sprite set that contains digits with the combat floater
system.

### Params

-   **strSpriteSetName** **(String)** - The path and file name of the
    sprite set that was registered with the system.

### Return Value

-   **Integer** - The index that is assigned to the sprite set that was
    added to the system.

------------------------------------------------------------------------

`Function`

AddTextBGSprite(strSpriteName)
------------------------------

### Description

Registers a background sprite with the float text system.

### Params

-   **strSpriteName** **(String)** - The path and file name of the
    sprite that should be registered with the system.

### Return Value

-   **Integer** - The index that was assigned to the sprite after it was
    registered.

------------------------------------------------------------------------

`Function`

HideTextFloater()
-----------------

### Description

Hides the CombatFloater from the screen.

------------------------------------------------------------------------

`Function`

SetMaxFloaterCount(nMaxFloaterCount)
------------------------------------

### Description

Sets the maximum number of floaters that can be on the screen at any one
time.

### Params

-   **nMaxFloaterCount** **(Integer)** - The new maximum number of
    floaters.

------------------------------------------------------------------------

`Function`

SetMaxFloaterPerUnitCount(nNewMaxFloaterCount)
----------------------------------------------

### Description

Sets the maximum number of floating text messages that will be shown for
any single unit at the same time.

### Params

-   **nNewMaxFloaterCount** **(Integer)** - The new maximum number of
    floaters per unit.

------------------------------------------------------------------------

`Function`

ShowParticleEffect(unitSource, tSettings)
-----------------------------------------

### Description

Displays a particle effect.

### Params

-   **unitSource** **([Unit](../Classes/Unit.md))** - The unit that the
    floater is attached to.
-   **tSettings** **(Table)** - A table that contains the various
    options that should be set for the particle effect.
    -   **eEffect** **(CombatFloater.CodeEnumFloaterEffect)** - The type
        of particle effect that should be shown.
    -   **nDuration** **(Integer)** - How long the particle effect
        should last for, in seconds.
    -   **fDuration** **(Float)** - How long the particle effect should
        last, in seconds.
    -   **eLocation** **(CombatFloater.CodeEnumFloaterLocation)** - The
        location on the unit that the effect should start from.

------------------------------------------------------------------------

`Function`

ShowTextFloater(unitSource, nValue, strValue, tOptions)
-------------------------------------------------------

### Description

Displays a text floater coming from the specified unit.

### Params

-   **unitSource** **([Unit](../Classes/Unit.md))** - The unit that the
    floater will be tied to.
-   **nValue** **(Integer)** - The value that should be shown on the
    floater. - The value that should be shown on the floater.
-   **strValue** **(String)** - The text that should be shown on the
    floater.
-   **tOptions** **(Table)** - A table that contains a laundry list of
    ways the text floater can be manipulated.
    -   **nColor** **(Integer)** - A hex value that contains the RGB
        color values that the floater should use.
    -   **arFrames** **(Table)** - A list of each frame of an animation
        that the floater will do.
        -   **fTime** **(Float)** - The amount of time that the frame
            should last, in seconds.
        -   **fScale** **(Float)** - The amount that the floater's text
            will be scaled by for this frame.
        -   **nColor** **(Integer)** - A hex value that contains the RGB
            values that the text will use this frame.
        -   **fAlpha** **(Float)** - The floater's alpha value this
            frame.
        -   **fRotation** **(Float)** - The amount that the floater is
            rotated this frame, in degrees.
        -   **fVelocityDirection** **(Float)** - The direction the text
            will move this frame, in degrees.
        -   **fVelocityDirectionRange** **(Float)** - The amount of
            variation allowed in the velocity's direction, in degrees.
        -   **fVelocityMagnitude** **(Float)** - The speed that the
            float text is moving at during this frame, in pixels.
        -   **fVelocityMagnitudeRange** **(Float)** - The amount of
            variation in the velocity's magnitude that can be used
            during this frame, in pixels.
        -   **fAccelerationDirection** **(Float)** - The direction that
            the float text will accelerate in during this frame, in
            degrees.
        -   **fAccelerationDirectionRange** **(Float)** - The amount of
            variation in the float text's acceleration direction, in
            degrees.
        -   **fAccelerationMagnitude** **(Float)** - The amount that the
            floater will accelerate by this frame, in pixels per second.
        -   **fAccelerationMagnitudeRange** **(Float)** - The variation
            in the acceleration's magnitude that is possible this frame,
            in pixels per second.
    -   **nDuration** **(Integer)** - How long the floater should stay
        on screen, in seconds. This is only needed if arFrames was not
        used.
    -   **fDuration** **(Float)** - How long the floater should stay on
        screen, in seconds. This is only needed if arFrames was not
        used.
    -   **nFadeInDuration** **(Integer)** - How long the floater should
        take to fade in, in seconds. This is only needed if arFrames was
        not used.
    -   **fFadeInDuration** **(Float)** - How long the floater should
        take to fade in, in seconds. This is only needed if arFrames was
        not used.
    -   **nFadeOutDuration** **(Integer)** - How long the floater should
        take to fade out, in seconds. This is only needed if arFrames
        was not used.
    -   **fFadeOutDuration** **(Float)** - How long the floater should
        take to fade out, in seconds. This is only needed if arFrames
        was not used.
    -   **nEndHoldDuration** **(Integer)** - How long the floater will
        hold its position before despawning, in seconds. This is only
        needed if arFrames was not used.
    -   **fEndHoldDuration** **(Float)** - How long the floater will
        hold its position before despawning, in seconds. This is only
        needed if arFrames was not used.
    -   **strFontFace** **(String)** - The name of the font face that
        the floater should use.
    -   **fSpinAroundRadius** **(Float)** - How many degrees the text
        will spin every second.
    -   **fVibrate** **(Float)** - The range that the floater will
        vibrate between in the X and Y directions.
    -   **eCollisionMode**
        **(CombatFloater.CodeEnumFloaterCollisionMode)** - The type of
        collision that the floater will use. This prevents collistion
        with other floaters.
    -   **fExpandCollisionBoxWidth** **(Float)** - The amount that is
        added to the floater's width when calculating collisions, in
        pixels.
    -   **fExpandCollisionBoxHeight** **(Float)** - The amount that is
        added to the floater's height when calculating collisions, in
        pixels.
    -   **eLocation** **(CombatFloater.CodeEnumFloaterLocation)** - The
        location on the unit that the floater will spawn from.
    -   **fOffsetDirection** **(Float)** - The direction that the
        floater will be offset from its spawn location, in degrees.
    -   **fOffset** **(Float)** - The amount that the floater will be
        offset from its spawn location, in pixels.
    -   **iUseDigitSpriteSet** **(Integer)** - The id number of the
        sprite set of digits that the text floater should use.
    -   **nDigitSpriteSpacing** **(Integer)** - The amount of space
        between each sprite from the sprite set.
    -   **iUseBGSprite** **(Integer)** - The id of the BG Sprite that
        the float text should use.
    -   **nBGSpriteMargin** **(Integer)** - The margin between the edges
        of the floater and the BG Sprite, in pixels.
    -   **nBGSpriteColor** **(Integer)** - A hex value that contains the
        RGB values that will be applied to the BGSprite.
    -   **fBGSpriteAlpha** **(Float)** - The alpha that is applied to
        the floater's BGSprite.
    -   **bUseScreenPos** **(Boolean)** - Whether the floater should use
        screen position instead of a location on a unit to determine its
        position.
    -   **bShowOnTop** **(Boolean)** - Whether the floater will draw
        over the top of other combat floaters and windows.
    -   **nDelay** **(Integer)** - The delay between the floater's start
        time and when it actually spawns.
    -   **bReposition** **(Boolean)** - Whether the floater can be moved
        or not.

### Usage/Example

```lua
    This
```

------------------------------------------------------------------------

`Function`

TestTextFloater(eDamageType, nHealthChange, nShieldAbsorbAmount, bCritical)
---------------------------------------------------------------------------

### Description

Passes the information given to the function back to the game in the
form of a DamageOrHealingDone event.

### Params

-   **eDamageType** **(GameLib.CodeEnumDamageType)** - The type of
    damage that should be sent with the DamageOrHealingDone event.
-   **nHealthChange** **(Integer)** - The amount that the player's
    health changed by (according to the test floater).
-   **nShieldAbsorbAmount** **(Integer)** - The amount of damage that
    the unit's shield absorbed (according to the floater)
-   **bCritical** **(Boolean)** - Whether the test floater should show a
    critical hit or not.

### Remarks

This function is primarily used to test out new floaters.
