# If #
This is a very versatile condition that can be used for lots of things. It allows you to compare two values against each other, using various methods explained below:

| **Operator** | **Description** |
|:-------------|:----------------|
|equals        |Evaluates to true if both values are equal.|
|is greater than|Evaluates to true if first value is greater than second. If one or both of the values are non-numeric, they are compared by alphabetical order.|
|is lower than |Evaluates to true if first value is lower than second. If one or both of the values are non-numeric, they are compared by alphabetical order.|
|contains      |Evaluates to true if the first value contains the second value.|
|matches regular expression|Evaluates to true if the first value matches the regular expression specified in second value. To learn more about regular expressions, see [here](http://www.autohotkey.com/docs/misc/RegEx-QuickRef.htm).|
|starts with   |Evaluates to true if the first value starts with the second value.|
|ends with     |Evaluates to true if the first value ends with the second value.|

# Tips #

  * A good application for this is to check if an explorer window is active. Explorer window uses different class names (CabinetWClass and ExploreWClass), depending on how it was launched. To check if an explorer window is active, both of these window classes have to be considered. Use regular expression operator, and enter "${Class}" as first value, and "(CabinetWClass|ExploreWClass)" as second value. The "(value1|value2)" regex can be regarded as "match value1 or value2".
  * You can construct alarms that trigger at certain times with a combination of a [timer](docsTriggerTimer.md) trigger that has a high frequency (say, triggers every 10 seconds) and an If condition. Set the first value of the If condition to "${DateTimeHHmm}", the operator to "equals", and the second value to "1324". This makes the timer launch its actions only when the time is 13:24.
  * Another useful application of this condition is to check if the active explorer window is in a specific path, or if specific files are selected. For this, use "${P}" or one of the various "${Sel}" [placeholders](docsGenericPlaceholders.md). Web developers might want to employ this to upload files from a specific folder to another FTP server.
  * It is also possible to react on specific clipboard contents.