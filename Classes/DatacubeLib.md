DatacubeLib
===========

### Description

A library that allows the player to interact with and get information on
Datacubes, Journals, and Tales from Beyond the Fringe entries

------------------------------------------------------------------------

`Function`

GetDatacubesForVolume(idJournal)
--------------------------------

### Description

Gets a list of datacube sub-entries for a journal.

### Params

-   **idJournal** **(Integer)** - The id number for the journal entry
    that the results belong to.

### Return Value

-   **Array of Table** - An array of tables that contain information on
    each sub-entry associated with the specified journal.
    -   **nDatacubeId** **(Integer)** - The entry's id number.
    -   **eDatacubeType** **(Integer)** - This value lines up with the
        DatacubeLib.DatacubeType\_ set of contstants.
    -   **nWorldZoneId** **(Integer)** - The id of the world zone that
        the entry belongs to.
    -   **strZoneName** **(String)** - The name of the zone that the
        entry belongs to.
    -   **nVolumeId** **(Integer)** - The id number of the parent
        journal entry.
    -   **strText** **(String)** - The entry's text.
    -   **bIsComplete** **(Boolean)** - Whether the entry has been
        unlocked or not.
    -   **bHasSound** **(Boolean)** - Whether the entry has a sound file
        associated with it or not.
    -   **strTitle** **(String)** - The entry's title.

------------------------------------------------------------------------

`Function`

GetDatacubesForZone(idZone)
---------------------------

### Description

Gets a list of datacube entries that are found in a specific zone.

### Params

-   **idZone** **(Integer)** - The function will return the datacube
    entries found in the zone with this id.

### Return Value

-   **Array of Table** - An array of tables that contain information on
    each datacube entry in the specified zone.
    -   **nDatacubeId** **(Integer)** - The id number for the entry.
    -   **eDatacubeType** **(Integer)** - The type associated with the
        datacube. This value corresponds with the
        DatacubeLib.DatacubeType set of constants.
    -   **nWorldZoneId** **(Integer)** - The id for the world zone that
        the datacube entry is associated with.
    -   **strZoneName** **(String)** - The name of the zone that the
        datacube entry is unlocked in.
    -   **strText** **(String)** - The datacube entry's text.
    -   **bIsComplete** **(Boolean)** - Whether the entry is completed
        or not.
    -   **bHasSound** **(Boolean)** - Whether the entry has a sound
        attached to it.
    -   **strTitle** **(String)** - The entry's title.
    -   **nNumCompleted** **(Integer)** - The number of unlocks that
        have been found for the entry. This only applies to Chronicle
        type entries.
    -   **nNumTotal** **(Integer)** - The number of unlocks required to
        complete the entry. This only exist for Chronicle type entries.
    -   **strAsset** **(String)** - The file name for the sprite shown
        in the completed entry. This only applies to Chronicle type
        entries.

------------------------------------------------------------------------

`Function`

GetJournalsForZone(idZone)
--------------------------

### Description

Gets a list of all the journal entries within a zone.

### Params

-   **idZone** **(Integer)** - The function will return the journal
    entries found in this zone.

### Return Value

-   **Array of Table** - An array of tables that contain information on
    all of the journal entries within the zone.
    -   **nDatacubeId** **(Integer)** - The journal's id number.
    -   **strTitle** **(String)** - The journal's title.
    -   **strAsset** **(String)** - The sprite associated with the
        journal.
    -   **bIsComplete** **(Boolean)** - Whether the player has unlocked
        all of the sub-entries for the journal or not.
    -   **nNumCompleted** **(Integer)** - The number of sub-entries that
        the player has unlocked for this journal.
    -   **nNumTotal** **(Integer)** - The total number of sub-entries
        for the journal.

------------------------------------------------------------------------

`Function`

GetLastUpdatedDatacube()
------------------------

### Description

Gets the information for the last datacube entry that was updated for
the player.

### Return Value

-   **Table** - Information on the player's most recently updated
    datacube entry.
    -   **nDatacubeId** **(Integer)** - The entry's id number.
    -   **eDatacubeType** **(Integer)** - The type of entry. This value
        corresponds with the DatacubeLib.DatacubeType set of constants.
    -   **nWorldZoneId** **(Integer)** - The id of the zone that this
        entry is associated with.
    -   **strZoneName** **(String)** - The name of the zone that this
        journal is associated with.
    -   **nVolumeId** **(Integer)** - The id of the journal that this
        entry belongs to, if any.
    -   **strText** **(String)** - The entry's text.
    -   **bIsComplete** **(Boolean)** - Whether the entry has been
        unlocked or not.
    -   **bHasSound** **(Boolean)** - Whether the entry has a sound
        associated with it or not.
    -   **strTitle** **(String)** - The entry's title.
    -   **nNumCompleted** **(Integer)** - The number of unlocks the
        player has found for this entry. This variable only applies to
        Chronicle type entries.
    -   **nNumTotal** **(Integer)** - The total number of unlocks needed
        to finish the entry. This variable only applies to Chronicle
        type entries.
    -   **strAsset** **(String)** - The sprite used for the entry when
        it is completed. This variable only applies to Chronicle type
        entries.

------------------------------------------------------------------------

`Function`

GetTales()
----------

### Description

Gets information on all the Tales from Beyond the Fringe entries that
the player has unlocked at least one part of.

### Return Value

-   **Table** - Information on each Tales entry that the player has made
    progress on.
    -   **nDatacubeId** **(Integer)** - The id number for the entry.
    -   **eDatacubeType** **(Integer)** - The entry's type. This should
        be DatacubeLib.DatacubeType\_Chronicle for every entry returned
        by this function.
    -   **nWorldZoneId** **(Integer)** - The id of the zone that the
        entry is associated with.
    -   **strZoneName** **(String)** - The name of the zone that the
        entry is associated with.
    -   **nVolumeId** **(Integer)** - The id of the entry's parent
        journal entry. This value will be 0 if it has none.
    -   **strText** **(String)** - The entry's text.
    -   **bIsComplete** **(Boolean)** - Whether the player has found all
        of the unlocks for this Tales entry or not.
    -   **bHasSound** **(Boolean)** - Whether the entry has sound or
        not.
    -   **nNumCompleted** **(Integer)** - The number of unlocks the
        player has found for this entry.
    -   **nNumTotal** **(Integer)** - The number of unlocks needed to
        complete this entry.
    -   **strAsset** **(String)** - The sprite displayed when the entry
        is completed.

------------------------------------------------------------------------

`Function`

GetTalesForZone(idZone)
-----------------------

### Description

Gets a list of all of the Tales entries that the player has made
progress on within a specific zone.

### Params

-   **idZone** **(Integer)** - The function will get a list of Tales
    that are associated with the zone with this id.

### Return Value

-   **Array of Table** - Information on each of the Tales entries that
    the player has unlocked at least one entry for in the specified
    zone.
    -   **nDatacubeId** **(Integer)** - The entry's id number.
    -   **eDatacubeType** **(Integer)** - The entry's type. This value
        should always be DatacubeLib.DatacubeType\_Chronicle for this
        entry.
    -   **nWorldZoneId** **(Integer)** - The id of the zone that is
        associated with this entry.
    -   **strZoneName** **(String)** - The name of the zone that the
        entry is associated with.
    -   **nVolumeId** **(Integer)** - The id of the journal entry that
        serves as this entry's parent. This value should always be 0 for
        this entry.
    -   **strText** **(String)** - The entry's text.
    -   **bIsComplete** **(Boolean)** - Whether the player has
        interacted with all of the unlocks for this entry or not.
    -   **bHasSound** **(Boolean)** - Whether the entry has a sound
        associated with it or not.
    -   **strTitle** **(String)** - The entry's title.
    -   **nNumCompleted** **(Integer)** - The number of this entry's
        unlocks that the player has activated.
    -   **nNumTotal** **(Integer)** - The number of unlocks needed to
        complete this Tales entry.
    -   **strAsset** **(String)** - The sprite that should be shown when
        this entry is complete.

------------------------------------------------------------------------

`Function`

GetTotalCollectionSize(eDatacubeType)
-------------------------------------

### Description

Gets the total number of entries that the player has made progress on of
a specific type.

### Params

-   **eDatacubeType** **(Integer)** - The function will return the
    number of entries that the player knows about of this type. This
    value corresponds with the DatacubeLib.DatacubeType set of
    constants.

### Return Value

-   **Integer** - The number of entries of a specific type that the
    player has made progress on.

------------------------------------------------------------------------

`Function`

GetTotalDatacubesForZone(idZone)
--------------------------------

### Description

Gets the number of entries within a zone that have the Datacube type.

### Params

-   **idZone** **(Integer)** - The function will get the number of
    Datacube entries in the zone with this id.

### Return Value

-   **Integer** - The number of datacube entries in the specified zone.

------------------------------------------------------------------------

`Function`

GetTotalJournalsForZone(idZone)
-------------------------------

### Description

Gets the number of journal entries within a specific zone.

### Params

-   **idZone** **(Integer)** - The function will get the number of
    journal entries in the zone with this id.

### Return Value

-   **Integer** - The number of journal entries found in the specified
    zone.

------------------------------------------------------------------------

`Function`

GetTotalTalesForZone(idZone)
----------------------------

### Description

Gets the number of Tales entries in a specific zone.

### Params

-   **idZone** **(Integer)** - The function will get the number of Tales
    in the zone with this id.

### Return Value

-   **Integer** - The number of Tales entries in the specified zone.

------------------------------------------------------------------------

`Function`

GetTotalVolumeCount(idZone)
---------------------------

### Description

Gets the number of journal entries within a specific zone.

### Params

-   **idZone** **(Integer)** - The id of the zone that the function will
    look through.

### Return Value

-   **Integer** - The number of journal entries within the specified
    zone.

### Usage/Example

```lua
    This will only count top level journal entries, not sub-entries for each journal.
```

------------------------------------------------------------------------

`Function`

GetVolumes()
------------

### Description

Gets a info on each journal entry that the player has unlocked at least
one entry for.

### Return Value

-   **Array of Table** - Information on each journal entry that the
    player has unlocked at least one entry for.
    -   **nDatacubeId** **(Integer)** - The journal's id number.
    -   **strTitle** **(String)** - The journal's title.
    -   **strAsset** **(String)** - The name of the asset associated
        with this journal entry.
    -   **bIsComplete** **(Boolean)** - Whether the player has unlocked
        all of the journal's sub-entries or not.
    -   **nNumCompleted** **(Integer)** - The number of the journal's
        sub-entries that the player has unlocked.
    -   **nNumTotal** **(Integer)** - The number of sub-entries that the
        player needs to unlock to complete the journal.

------------------------------------------------------------------------

`Function`

GetZonesWithDatacubes()
-----------------------

### Description

Gets a list of each zone that has a Datacube entry.

### Return Value

-   **Array of Table** - The id number and name of each zone that has a
    Datacube entry associated with it.
    -   **nZoneId** **(Integer)** - The zone's id number.
    -   **strName** **(String)** - The zone's name.

------------------------------------------------------------------------

`Function`

GetZonesWithJournals()
----------------------

### Description

Gets a list of each zone that has a journal entry associated with it.

### Return Value

-   **Array of Table** - The id number and name of each zone that has a
    journal entry associated with it.
    -   **nZoneId** **(Integer)** - The zone's id number.
    -   **strName** **(String)** - The zone's name.

------------------------------------------------------------------------

`Function`

GetZonesWithTales()
-------------------

### Description

Gets a list of each zone with a Tales entry associated with it.

### Return Value

-   **Table** - A list with the id and name of each zone that has a
    Tales entry associated with it.
    -   **nZoneId** **(Integer)** - The zone's id.
    -   **strName** **(String)** - The zone's name.

------------------------------------------------------------------------

`Function`

IsDatacubeComplete(idDatacube)
------------------------------

### Description

Determines if an entry is complete. This generally means whether the
player has found all of the unlocks / sub-entries for the specified
entry.

### Params

-   **idDatacube** **(Integer)** - The id for the entry that the
    function will check.

### Return Value

-   **Boolean** - Whether the player has interacted with each of the
    entry's unlocks / sub-entries or not.

------------------------------------------------------------------------

`Function`

PlayDatacubeSound(idDatacube)
-----------------------------

### Description

Plays the sound associated with the entry.

### Params

-   **idDatacube** **(Integer)** - The function will cause the entry
    with this id to play its sound.

------------------------------------------------------------------------

`Function`

StopDatacubeSound(idDatacube)
-----------------------------

### Description

Stops the sound associated with a specific entry.

### Params

-   **idDatacube** **(Integer)** - The function will stop the sound
    associated with the datacube with this id.
