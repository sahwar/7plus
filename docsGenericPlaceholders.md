# Placeholders #
Placeholders are an important concept in the event system, as they allow you to dynamically set parameters of conditions and actions. Placeholders are formatted like this: ${Placeholder}
You can use placeholders everywhere you see a placeholder button.
Below is a list of placeholders in 7plus. Some actions also define custom placeholders, take a look in the documentation of the action to see it. In most cases they are also directly mentioned in the configuration dialog.

| **Placeholder** | **Description** |
|:----------------|:----------------|
|${DateTime}      |Language-specific time and date (4:55 PM Saturday, November 27, 2010)|
|${DateTimeLongDate}|Language-specific long date (Friday, April 23, 2010)|
|${DateTimeShortDate}|Language-specific short date (02/29/10)|
|${DateTimeTime}  |Language-specific time (5:26 PM)|
|${DateTime`[`Format`]`}|Other `[`Format`]`, see [here](http://www.autohotkey.com/docs/commands/FormatTime.htm)|
|${P}             |Path of last active explorer window|
|${PP}            |Previous path of explorer window|
| **Selected files in explorer, below are some samples                |**|
|${Sel1}          |Filepath of first selected file|
|${Sel2DQ}        |Directory of second selected file, quoted|
|${Sel3N}         |Filename of third selected file, no extension|
|${Sel4NE}        |Filename of fourth selected file, including extension|
|${SelN}          |Filepaths of all selected files, separated by spaces|
|${SelNNEM}       |Filenames+extensions of all selected files, separated by new lines|
|${U}             |Handle of window under mouse|
|${MC}            |Class of window under mouse|
|${MNN}           |ClassNN of control under mouse|
|${MX}            |Mouse X coordinate|
|${MY}            |Mouse Y coordinate|
|${MXA}           |Mouse X coordinate, relative to active window|
|${MYA}           |Mouse Y coordinate, relative to active window|
|${MXU}           |Mouse X coordinate, relative to window under mouse|
|${MYU}           |Mouse Y coordinate, relative to window under mouse|
|${Clip}          |Clipboard contents|
|${Input}         |Result of previous [input](docsActionsInput.md) action|
|${MessageResult} |Result of previous [SendMessage](docsActionsSendMessage.md) action (Send only!)|
|${wParam}        |wParam value if this condition/action was triggered by [OnMessage trigger](docsTriggersOnMessage.md)|
|${lParam}        |lParam value if this condition/action was triggered by [OnMessage trigger](docsTriggersOnMessage.md)|
|${A}             |Active window handle|
|${Class}         |Active window class|
|${Title}         |Active window title|
|${Control}       |Focussed control [ClassNN](docsGenericClassNN.md)|
|${TitlePath}     |Path in active window title|
|${TitleFilename} |Path and filename in active window title|