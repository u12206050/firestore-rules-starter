# firestore-rules-starter
The initial Firebase Firestore rules file with helper functions


## ARGUMENT TYPES

    id:     string    (ID of document or user)

    field:  string    (Name of property)

    value:  any       (Value of property)

    fields: string[]  (List of property names)

    min:    number 

    max:    number

    role:   string    (Name of the role)





## FUNCTIONS



Is the user logged in?

    isSignedIn()

Does the given id match the logged in user's uid?

    isUserId(id)

Is the given field a reference of the current user

    isUserRef(field)

Only use after checking if the field exists

    val(field)

Do only these fields exist on the document?

    allowedFields(fields)

Have any of these fields changed?

    hasNotChanged(fields)

Is this field unchanged?

    equals(field)



TYPES

    isString(field)

    isValueString(value)

    isInteger(field)

    isValueInteger(value)

    isFloat(field)

    isValueFloat(value)

    isBool(field)

    isValueBool(value)

    isTimestamp(field)

    isValueTimestamp(value)



Check the field's length. Use 0 to ignore upper or lower limit

    hasLength(field, min, max)

    hasValueLength(value, min, max)

Is field's value within the given range, inclusive

    inRange(field, min, max)

    valueInRange(value, min, max)

Use to check for optional values

    isNull(field)

    isValueNull(value)

Matches a string to an email regex pattern

    isEmail(field)

    isValueEmail(value)



Ensure document is created with only the given fields

    createdWith(fields)



Does this field match the given value

    matches(field, value)


Roles Fn

    userHasRole(role)


Data Fn

    getUserData()

    existingData()

    incomingData()

    currentUser()
