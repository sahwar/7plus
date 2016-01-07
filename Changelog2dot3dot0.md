# 7plus Version 2.3.0 Changelog #

7plus is now on Twitter. Follow on http://twitter.com/7_plus !

New Functions:
  * Context menu support on files and folders. This is implemented through a shell extension
  * Dynamic timer: Start a message/shutdown/run timer by middle clicking the clock
  * Support for generic menus. It's now possible to design and show (sub)menus and trigger events with the entries.
  * Window finder tool for easily selecting window titles/classes/executables in event config
  * Batch Image converter for converting and resizing lots of images at once (through explorer context menu)
  * MD5 Checksum window for generating MD5 checksums (through explorer context menu)
  * Progress notification window for FTP upload, and uploading doesn't make the system unresponsive anymore
  * Volume control OSD for displaying current volume and mute status
  * "Run with parameters..." context menu option for executable files
  * "Toggle hidden files" context menu option for directory backgrounds
  * "Upload" context menu option for files
  * Added history function for Accessor (CTRL + UP/DOWN Arrow)
  * Enhanced the input action to support multiple data types (paths, text, numbers, selections,...) and added a condition to ControlEvent action that allows it to react to a selection. Placeholders from this action are now globally accessible in any event.
  * Added a "Copy Event" feature to the ControlEvent action. This will copy an event temporarily so it can be used in parallel. This is very useful for timers.
  * Added CTRL+WIN+Tab: Write tab character
  * Added CTRL+WIN+Enter: Write newline
  * Added a file switcher for SciTE4AutoHotkey that works exactly like the one for Notepad++. It requires that the latest version of SciTE4AutoHotkey is installed, which is v3 beta 5a at the time of this release.

Bugfixes:
  * Fixed Registry permissions which stopped FastFolders from showing up in explorer bar
  * Removed unnecessary dependancy on Visual C++ Runtime 2010
  * "Proper" 64 bit support. 2.2.0 was quite buggy in this regard...If you encountered a bug and you were using the x64 version, it is probably fixed
  * Fixed Win+C not working on desktop
  * Fixed Clipboard manager not working in cmd
  * Fixed ALT+Drag preventing Alt+Click
  * Fixed Invert Selection
  * Fixed "Create Folder" not working on network drives
  * Fixed portable mode startup error messsage and reload issue
  * Fixed FastFolders numpad keys triggering directory change in file dialog boxes with the filename box selected
  * Improved Accessor performance and added a few related plugin settings
  * Fixed an invalid key combination in "Picture viewer: Rotate image right with R" event and added versions of the Picture viewer events for XP
  * Fixed clipboard manager not updating sometimes (Not fixed on XP due to OS limitation)

Changes:
  * 7plus now uses the task scheduler instead of autorun in Vista and 7 to avoid UAC dialogs
  * All tooltips and some message boxes have been replaced by nicer looking notification windows
  * Added an introduction page that is shown on first run. It contains some tips and some basic settings like Autorun.
  * Added uninstall information for the 7plus uninstaller to the registry.
  * 7plus now recognizes if a newer version was extracted manually over an older version and will perform the required update steps.
  * The Flat view function is now an event.

If you like this program and want to support its development, please consider donating!