# 7plus Frequently Asked Questions and Common Features #
If you use 7plus for the first time, it may appear overwhelming in features, so here are some small pointers to get you started.
If you have further questions, please refer to the docs first (click the help buttons available on specific event/trigger/condition/action pages) before requesting help.

## About the Event System ##

7plus is mostly based around the **Event System**. An event consists of a trigger, multiple conditions and actions.
A trigger can be a hotkey, a timer, a context menu entry or many other things. When it triggers the event, the event is put on an event queue.
The events in this queue are (normally) processed one after another. At first, the conditions of an event are evaluated. A popular condition is that a specific window is active.
This is often used in combination with a hotkey trigger to make application specific hotkeys.
The actions are performed when all conditions evaluate to TRUE. There are all kinds of actions available that deal with windows, explorer, files or general system actions (run programs, write something to clipboard,...).
The combinations are nearly endless! :)

  * **Tip:** You can quickly find a specific event by using the categories on the left of the settings page or by typing a part of the event name, trigger text or event description in the search box at the top of the page. This can be useful if you're looking for a specific feature. Keep in mind that some features require more than one event; there might be different events for explorer, desktop and file dialogs for example.

For more details about the event system, please see [Event System Overview](EventsOverview.md).

## About the Accessor ##
The Accessor is a launcher similar to programs like Launchy or Exekutor. By default you can make it show up by pressing **ALT + SPACE**, but you can change it to any other hotkey or make it show up through some other obscure way by modifying the Accessor event. The Accessor comes with many different plugins. A plugin takes care of a specific task, such as browsing the file system or looking up the weather. Most plugins have a specific keyword that is required to use them. You can adjust this keyword and other settings in the "Accessor Plugins" settings page. You can also gain an overview over the available plugins there. When you type something in the text box at the top of the Accessor window, all matching results will show up in the list below. If you press Enter, the action displayed on the top button is executed. For many plugins there are multiple actions available which can be accessed by right clicking a list item.

See [here](Accessor.md) for more information about the Accessor.

## About Clipboard enhancements ##
7plus enhances the clipboard in various ways:
  * First, it provides a clipboard manager that keeps a history of previously copied text. It's also possible to create persistent clips that can be pasted anytime. To access these, press **WIN + V** and select them from the menu. Alternatively it's possible to search for them in the Accessor.
  * 7plus adds various enhancements to clipboard handling in Explorer. It makes it possible to paste text or images as files into the current directory. There are also some new hotkeys to append files to the currently copied files without replacing them and hotkeys to copy the name or path of the selected files.

## About Explorer enhancements ##
7plus adds many features to Explorer. Here are the most common ones:
  * 7plus features a concept named Fast Folders. These are 10 slots to which paths are assigned by pressing **CTRL + Numpad0-9** in Explorer or similar windows. They can be recalled in those windows by pressing the corresponding **Numpad** key. In Windows Vista and Windows 7 these paths will also appear as buttons in the Explorer band bar so they can be clicked like favorite buttons in browsers.
  * It adds the ability to use tabs in Explorer. You can create a new tab by pressing **CTRL + T**. The tabs appear on top of the title bar and can be activated by clicking on them or by pressing **CTRL + (SHIFT) + TAB**. They can be closed by middle clicking on the tab or by pressing **CTRL + W**. You can press **CTRL + M** when an Explorer window is active to merge all Explorer windows into one tabbed window.
  * 7plus can upload the selected files and folders to an FTP server by pressing **CTRL + U**.
  * 7plus adds dialogs to perform mass-rename and replace-in-files operations. They can be accessed by pressing **CTRL + (SHIFT) + H** in Explorer.
  * 7plus adds context menu entries to access some of its functions.
  * Another useful feature is double-clicking on empty space in Explorer to go upwards.

## About Window enhancements ##
7plus adds many improvements to the ways windows are used:
  * The always-on-top state of a window can be quickly toggled by right-clicking its title bar or by pressing **WIN + A**.
  * Windows can be moved outside of the screen by pressing **WIN + SHIFT + Arrow Key**. When they are activated or the mouse is moved at the border they slide into the screen temporarily to allow interaction.
  * Any window can be moved or resized by holding the ALT keys and grabbing it with the left or right mouse button anywhere (not just its borders).
  * Windows can be closed by middle-clicking on them in the taskbar.

## About Screenshot and Image Converter tools ##
7plus supports enhanced screenshot capturing and editing. Press **PrintScreen** to capture the current screen, **WIN + PrintScreen** to capture the current window and **ALT + PrintScreen** to select a region to capture. Captured screenshots can be edited by clicking on the image and can be stored on the hdd, an FTP server or an image hoster in the desired format.
It's also possible to mass convert or upload images from the hard disk through the context menu.

## About HotStrings ##
Hotstrings can be used to expand abbreviations (i.e. "btw" -> "by the way"). You can use PCRE-style regular expressions (see [here](http://www.autohotkey.com/docs/misc/RegEx-QuickRef.htm)) for the hotstring. This allows very precise control about the hotstring, but also makes it a bit more difficult to use unfortunately. The value field contains the keys that will be send when a hotstring is matched. You can also use keys like "{Enter}" to write a new line.

## About other useful features ##
7plus provides many more useful features. Often these are just tiny improvements which aren't documented here. However, here are some of the more important ones:
  * Sound volume can be quickly changed by scrolling the mouse wheel over the taskbar.
  * The selected text can be quickly searched with Google by pressing **WIN + G**.
  * Command prompt windows can be opened in the current directory with **WIN + C**.
  * For AHK developers: Temporary scripts can be executed by pressing **WIN + T** and pasting the script in the dialog box.

## Portable mode, admin permissions, interfacing with 7plus... ##

  * **Portable mode:** It is possible to run 7plus in portable mode by adding **"-portable"** to its command line. If you don't know how to do this, you can create a shortcut to 7plus.exe, go to file properties in explorer, and append **-portable** in the command text box (after the quotes). In addition, there is also a **%7plusDrive%** placeholder available in 7plus, so you can add events that refer to paths on an USB stick where 7plus is located.

  * **Admin permissions:** If you don't have admin permissions on a system, you can still use 7plus, even though some/many features won't be available then. It is not possible to work with other windows which are running elevated, and features like Fast Folders can't add buttons to the explorer window or the context menu. It is possible to always run 7plus in non-admin mode by setting "Run as admin" to "Never" on the Introduction settings page.

  * **Interfacing with other programs:** It is possible to make 7plus react to other events/triggers from other programs by sending a message to it. To get the correct window handle of 7plus, the preferred way is to read the window handle from **%TEMP%\7plus\hwnd.txt** which exists while 7plus is running. Alternatively you can just send it to any AutoHotkey window, unless you have a script running that handles the same message value. The message value which is used for this is **55555**. The wParam value is the ID of the event that you want to trigger. If you don't have the ability to send a window message to 7plus, you may run 7plus with a command line parameter instead while it is already running. Append " **-id [Number](Number.md)**" (without quotes) to the command line, where [Number](Number.md) is the ID of the event that you want to trigger. 7plus will then take care of sending the message to the running instance.

## 32 or 64 bit, binary or source? ##

You should always use the version which matches your system architecture, if you have a 32 bit version of windows, you'll need to use the 32 bit version, and if you have a 64 bit version of windows, you should use the 64 bit version of 7plus. While it is possible to use the 32 bit version on a 64 bit version of windows, this is strongly discouraged because some features are not going to work then. I have not tested every feature with this combination, but I know that Fast Folders can't display buttons on the explorer bar, and other things like context menu or features that access the windows registry are also likely affected.

If you use the binary or the source version mostly depends on your personal taste. The binary version is easier to use because you just need to extract and run it, while the source version requires that you have a recent build of AutoHotkey\_L Unicode installed that matches the bitness of the 7plus version you downloaded. This is mostly interesting for developers that want to modify the behavior of 7plus or open source advocates that like to see what is going on.

## Using the source version / Getting source version from SVN ##
You can get the latest available source code from Google Code using Subversion. To do this a Subversion client is required. I suggest using [TortoiseSVN](http://tortoisesvn.net). After installation please follow the descriptions on the project page (Source tab).
You will need to copy Explorer.dll, ShellExtension.dll and subinacl.exe from the subdirectories into the main 7plus directory. This is required because there are 2 versions of those files, one for x86 and one for x64, so choose the correct one. ShellExtension.dll can be found in the Release and x64\Release subdirectories of the ShellExtension directory. The other files are located in x64/x86 directories.

The source version should always be used with the latest available version of AutoHotkey\_L which is available here.
Make sure to use the Unicode version of the correct bitness.

As this code is actively developed upon, most of the time it's not going to be stable and will likely have errors. It's even possible that it isn't startable due to syntax errors, but this should happen rarely. If this happens you can either wait for the next commit of source code or switch to an earlier revision.

## Known problems ##
#### The buttons in the Explorer bar don't appear/appear multiple times/don't work! ####
It's best to start over by going into Settings, Fast Folders and clicking on "Remove custom Explorer buttons". Afterwards, click on Ok or Apply to recreate them. You should also know that this feature only works in Vista and 7 and not without admin privileges or in portable mode.

#### 7plus does not react to any hotkeys anymore! ####
I believe that this can happen sometimes if 7plus takes too long to react to key presses and Windows removes it from the keyboard hook chain. Simply restart 7plus to fix it.

## If you encounter other errors ##
There are a few things that you should try:

  * Try to start with a fresh event config file, or even better a fresh installation of 7plus. Uninstall 7plus and make sure that %Appdata%\7plus is deleted.
  * If you use any other tweaking software or special drivers (especially mouse and keyboard drivers that implement extra functionality, like Logitech SetPoint driver), try to disable them and use the standard windows keyboard/mouse drivers. Such software often implements features that conflict with the features in 7plus. Contrary, it may also happen that 7plus disturbs other programs. If you encounter such behavior please let me know.
  * Other software like anti-virus programs or firewalls may also cause problems. I'm not going to try to convince you that these programs are snake-oil (even though they are!), but don't be surprised if you find that they caused any issues.

If this doesn't help, please report the problems on the bugtracker.