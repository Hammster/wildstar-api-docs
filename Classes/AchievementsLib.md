AchievementsLib
===============

### Description

Contains a list of functions that are helpful for building and
orgainzing the Achievements UI or anything that requires achievement
information.

------------------------------------------------------------------------

`Function`

GetAchievementCategoryTree(bGetGuildAchievements)
-------------------------------------------------

### Description

Gets a tree structure for the different types of achievements for the
UI. The heirarchy goes Categories &gt; Groups &gt; Subgroups.

### Params

-   **bGetGuildAchievements** **(Boolean)** - Whether the function
    should return Guild Achievements or not.

### Return Value

-   **Array of Table** - A table with information on the categories,
    groups, and subgroups of achievements.
    -   **nCategoryId** **(Integer)** - The id number for the category.
    -   **strCategoryName** **(String)** - The category's name.
    -   **tGroups** **(Array of Table)** - A table with the groups found
        within this category.
        -   **nGroupId** **(Integer)** - The id for the achievement
            group.
        -   **strGroupName** **(String)** - The name for the achievement
            group.
        -   **tSubGroups** **(Array of Table)** - A table with
            information on the sub groups within this group.
            -   **nSubGroupId** **(Integer)** - The id number for the
                sub group of achievements.
            -   **strSubGroupName** **(String)** - The name of the sub
                group of achievements.

------------------------------------------------------------------------

`Function`

GetAchievementPoints()
----------------------

### Description

Returns the number of achievement points that the player has earned from
completed achievements.

### Return Value

-   **Integer** - The number of points the player has earned.

------------------------------------------------------------------------

`Function`

GetAchievements(bIsGuild)
-------------------------

### Description

Gets a list of all achievements or guild achievements.

### Params

-   **bIsGuild** **(Boolean)** - Determines whether the function should
    return guild achievements or not.

### Return Value

-   **Array of [Achievement](../Classes/Achievement.md)** - An array
    with every achievement of the specified type.

------------------------------------------------------------------------

`Function`

GetAchievementsForCategory(idCategory, bRecurse, bGetGuild)
-----------------------------------------------------------

### Description

Gets a list of all the achievements for the given category.

### Params

-   **idCategory** **(Integer)** - The category of achievements that
    should be returned.
-   **bRecurse** **(Boolean)** - Whether or not the function should
    recurse through the category's subcategories when searching.
-   **bGetGuild** **(Boolean)** - Whether the function should return
    guild achievements or not.

### Return Value

-   **Array of [Achievement](../Classes/Achievement.md)** - An array
    that contains all of the achievements for the given category (and
    subcategories if bRecurse was set to true)

### Remarks

The function will only return achievements at the category level if
bRecurse is not set to true.

------------------------------------------------------------------------

`Function`

GetAchievementZones()
---------------------

### Description

Returns a list of all of the zones used in any achievement.

### Return Value

-   **Array of Table**
    -   **nId** **(Integer)** - The zone's id number.
    -   **strName** **(String)** - The name of the zone.

### Remarks

There's really no way to map an achievement to the zone with this
function at the moment. It still returns valid information, but it might
not be very useful.

------------------------------------------------------------------------

`Function`

GetCategoriesForZone()
----------------------

------------------------------------------------------------------------

`Function`

GetCategoryForMatchingGame()
----------------------------

------------------------------------------------------------------------

`Function`

GetGuildAchievementPoints()
---------------------------

### Description

Returns the number of Guild Achivement Points the player's current guild
has earned.

### Return Value

-   **Integer** - The number of Guild Achievement Points that the guild
    has earned.

------------------------------------------------------------------------

`Function`

GetRecentCompletedAchievements(nMaxCount, bGetGuild)
----------------------------------------------------

### Description

Gets the latest achievements that the player has earned.

### Params

-   **nMaxCount** **(Integer)** - The maximum number of values you want
    the achievement to return.
-   **bGetGuild** **(Boolean)** - Whether the function should return
    guild achievements or not.

### Return Value

-   **Array of [Achievement](../Classes/Achievement.md)** - An array of
    the most recent achievements the player has earned, in order of most
    recent to least.

------------------------------------------------------------------------

`Function`

GetTradeskillAchievementCategoryTree(eTradeskill)
-------------------------------------------------

### Description

Gets a list of all of the categories and subcategories for a
tradeskill's tech tree.

### Params

-   **eTradeskill** **(CraftingLib.CodeEnumTradeskill)** - The function
    will return the tech tree for this tradeskill.

### Return Value

-   **Array of Table** - A table containing the name of the tradeskill
    and its subcategories.
    -   **nGroupId** **(Integer)** - The id number for the tradeskill.
    -   **strGroupName** **(String)** - The tradeskill's name.
    -   **tSubGroups** **(Array of Table)** - An array of the different
        ranks for the tradeskill.
        -   **nSubGroupId** **(Integer)** - The id number for the rank
            of the tradeskill.
        -   **strSubGroupName** **(String)** - The name of this rank of
            the tradeskill.

### Remarks

The Group returned in this function is always the tradeskill itself,
with its subgroups being the different ranks of that tradeskill.

------------------------------------------------------------------------

`Function`

GetTradeskillAchievementLayout(nSubcategoryId)
----------------------------------------------

### Description

Gets a list of all of the achievements for a specific tradeskill rank.

### Params

-   **nSubcategoryId** **(Integer)** - The id number for the
    tradeskill's rank.

### Return Value

-   **Array of [Achievement](../Classes/Achievement.md)** - An array of
    the achievements for the specified tradeskill rank.

### Remarks

Once this list is populated, call Achievement:GetTradeskillLayout() to
get the achievement's position in the tech tree.

------------------------------------------------------------------------

`Function`

GetTradeskillAchievements(eTradeskill)
--------------------------------------

### Description

Gets all of the achievements for a specific tradeskill.

### Params

-   **eTradeskill** **(CraftingLib.CodeEnumTradeskill)** - The function
    will return the achievements for this tradeskill.

### Return Value

-   **Array of [Achievement](../Classes/Achievement.md)** - An array
    that contains all of the achievements for the specified tradeskill
