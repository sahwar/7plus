# Accessor #
Accessor is a multi-purpose window introduced in 7plus 2.1.0.

![http://i45.tinypic.com/w14p74.png](http://i45.tinypic.com/w14p74.png)

It is similar to launchers like Launchy or Exekutor. By default you can open it by pressing **ALT + SPACE**, but you can change it to any other hotkey or make it show up through some other obscure way by modifying the Accessor event. Type a command and possible matches and actions will appear in the list below. If you press Enter, the action displayed on the right of the textbox is executed. For many results there are multiple actions available which can be accessed by right clicking a list item.

## Plugins ##
The Accessor comes with many different plugins. A plugin takes care of a specific task, such as browsing the file system or looking up the weather. Most plugins have a specific keyword that is required to use them. You can adjust this keyword and other settings in the "Accessor Plugins" settings page. You can also gain an overview over the available plugins [here](AccessorPlugins.md).

## Keywords ##
In addition to the plugins the Accessor supports the concept of keywords, which means that the keyword is internally expanded to a command. A popular example for this are web searches. You can type "w AutoHotkey" and you'll get the same results as if you typed "http://en.wikipedia.org/wiki/Special:Search?search=AutoHotkey". In short:
  * Keywords are only supported at the start of the entered text.
  * Words typed after the keyword can be inserted into the command at predefined places. For this you can use ${1} - ${9} placeholders in the settings.
  * New keywords can be created through the settings window or through the Keyword plugin.

## Buttons ##
There are also three different types of buttons on the Accessor window:

  * The Query buttons (upper row, left side) are used to quickly enter a specific text in the textbox. They serve as reminder for the keywords and different plugins that are available in Accessor so you don't need to remember all keywords. By right clicking this button it's possible to assign the currently entered text to this button and to set a new icon for the button.

  * The Fast Folder buttons (upper row, right side) provide quick access to the Fast Folders defined in 7plus. Clicking one of these buttons or pressing its hotkey will open an Explorer window in the folder or navigate the window that was active when Accessor was opened to it. It's possible to assign a Fast Folder in Accessor by selecting a result that represents a directory and clicking on an empty button or by using the context menu of the result.

  * The Program buttons are used to execute programs. They are comparable to the quick launch buttons in earlier versions of windows or to pinned buttons in WIN 7 and later. They can be accessed by pressing their hotkeys, even when the Accessor window isn't open. Programs are assigned to a button by selecting a program from the result list in Accessor and clicking on an empty button or using the context menu of the result.

## Other tips ##
  * You can press CTRL + Up / Down to access the history of previously entered text.
  * Many times Accessor will take note of the current context (i.e. the active program, selected file or selected text) and use this information to show other results, order them differently or integrate the selected text or file as parameter in the query. A popular example is selecting a word, open Accessor and enter "w" to search for the word on Wikipedia.
  * Accessor learns about your usage habits and orders the results so that often used results will appear at or near the top of the list. You can also assign different priorities to the single plugins to modify the ordering manually.