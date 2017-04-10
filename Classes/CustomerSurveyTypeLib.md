CustomerSurveyTypeLib
=====================

### Prefix: svy

### Description

Surveys that are sent out to players during betas and on the PTR. These
are disabled in the live game.

------------------------------------------------------------------------

`Method`

\_\_eq(svyCompare) (Deprecated)
-------------------------------

### Description

Determines if two CustomerSurveys are the same.

### Params

-   **svyCompare**
    **([CustomerSurveyTypeLib](../Classes/CustomerSurveyTypeLib.md))** -
    The CustomerSurvey that is being compared to the one that called
    this function.

### Return Value

-   **Boolean** - Whether the two CustomerSurveys are the same or not.

------------------------------------------------------------------------

`Method`

Cancel()
--------

### Description

Cancels the current survey. If the survey stopped the player from
leaving the game, they will now be able to leave.

------------------------------------------------------------------------

`Method`

GetComment()
------------

### Description

Gets the text from the Comment section of the survey.

### Return Value

-   **String** - The text that is in the Comment section of the survey.

------------------------------------------------------------------------

`Method`

GetQuestions(nIndex)
--------------------

### Description

Gets the text for the questions on the survey.

### Params

-   **nIndex** **(Integer)** - If this is passed in, the function will
    return a single string for the question at this index.

### Return Value

-   **Array of String** - An array of all of the survey's questions. If
    nIndex was set, this will be a single string and not an array.

------------------------------------------------------------------------

`Method`

GetResults(nIndex)
------------------

### Description

Gets a list of the player's responses to the survey.

### Params

-   **nIndex** **(Integer)** - If this is passed in, the function will
    only return the result for the question at this index.

### Return Value

-   **Array of Integer** - An array of integers with the player's
    responses to the survey. If nIndex was set, then this will be a
    single integer instead of an array.

------------------------------------------------------------------------

`Method`

GetSurveyType()
---------------

### Description

Gets the survey's type.

### Return Value

-   **CustomerSurveyLib.CodeEnumSurveyType** - The survey's type.

### Remarks

The survey's type corresponds with what triggered it.

------------------------------------------------------------------------

`Method`

GetTitle()
----------

### Description

Gets the survey's title.

### Return Value

-   **String** - The survey's title.

------------------------------------------------------------------------

`Method`

isCustomerSurvey()
------------------

### Description

Checks if this variable is a CustomerSurvey.

### Return Value

-   **Boolean** - Whether this is a CustomerSurvey or not.

------------------------------------------------------------------------

`Method`

SendResult()
------------

### Description

Attempts to send the CustomerSurvey to Carbine.

### Return Value

-   **Boolean** - Whether the CustomerSurvey was successfully sent or
    not.

------------------------------------------------------------------------

`Method`

SetComment(strComment)
----------------------

### Description

Sets the survey's comment section.

### Params

-   **strComment** **(String)** - The text that will become the survey's
    comment.

------------------------------------------------------------------------

`Method`

SetResults(arResponses)
-----------------------

### Description

Sets a result for each question in the survey.

### Params

-   **arResponses** **(Array of Integer)** - An array that contains
    responses for each of the survey's questions.

------------------------------------------------------------------------

`Method`

SetResults(nQuestion, nResponse) (Deprecated)
---------------------------------------------

### Description

Sets the result for a specific question in the survey.

### Params

-   **nQuestion** **(Integer)** - The index for the question that the
    response belongs to.
-   **nResponse** **(Integer)** - The index of the response.
