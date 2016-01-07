# 7plus Version 2.4.0 Changelog #

New Functions:
  * Added search and replace dialog for file names and file contents
  * Added directory context menu item for flat view
  * Added URL shortener (WIN+S with URL in clipboard)
  * Added ImgUr.com image upload action. Anonymous image uploading is now possible. ImgUr limits it to 50 uploads/hour/API key, so please let me know if you notice that 7plus runs out of upload quota.
  * In addition to the previous entry, default windows PrintScreen functionality was overwritten to show a reworked version of the ImageConverter window. It is now possible to take screenshots of screen/window/user area and choose whether to save the screenshot, copy it to clipboard or upload it to FTP/ImgUr.
  * Added a settings page with generic windows settings (No bloat, only important ones!)
  * New Accessor plugin: Run. It executes the entered text directly, like Start menu->Run does. Useful when the command is not recognized by the Program Launcher plugin.
  * New Accessor plugin and new Trigger for defining custom Accessor commands that will trigger events.
  * New trigger: DirectoryChangeTrigger. It triggers if a specified directory or a file is modified and can be used for backup/synchronization purposes.
  * Added ALT+Right drag window resize
  * Added "Automatically close Windows Update reboot notification dialog"
  * Added screen corner triggers and made AeroFlip3D an event rather than a setting
  * Added a new hotkey event (CTRL+M) to merge all explorer windows into a single one with tabs
  * Added a "Show complex events" button and categorized events by complexity. By default 7plus will now show only about half of the available events. The others can still be enabled though.
  * Added the ability to create new files of any type by selecting a base file in the New File action that is copied to the target destination
  * Added KeyDelay setting for SendKeys action
  * Added ShowEvents option (available only through manual editing of Settings.ini in [General](General.md) category) to show execution order of events
  * Added DoubleClick option to MosueClick action
  * Added ClipPaste action to paste a specific entry from the clipboard manager list without showing the menu (Useful when active window must not be changed, i.e. explorer renaming)
  * Added Win+A hotkey to toggle always on top

Bugfixes:
  * Fixed missing \ when copying paths of network shares
  * Fixed not being able to navigate to network drives
  * Reimplemented middle mouse button features in event system to avoid some problems with this button. As a result of this, a few additional conditions were added.
  * Fixed Alt window drag not being able to drag a window to the outer left side of the screen
  * Fixed some access right modifications for registry keys required for explorer buttons. If they didn't show up before they should do so now. It may be necessary to disable/enable the FastFolder setting to make them show up.
  * Fixed colon character in Accessor.
  * Improved Program launcher Accessor plugin program caching. It now refreshes the program list whenever the OK button of the plugin settings window is pressed.
  * Fixed reload action for binary version
  * Fixed an issue in uninstaller that prevented deletion of 7plus directory

Changes:
  * Complete rewrite of the event system and about half of all the trigger/conditions/actions code. This will make 7plus much easier to maintain and a few (unnoticed) bugs could also be fixed along the way.
  * Huge code rewrite for some key portions related to explorer. As a result, status bar enhancements and explorer tabs are now visible on all explorer windows at once.
  * Complete rewrite of Slide Windows feature. It should be much better now, with more options, multi-monitor support, support for child windows and no windows getting lost anymore.
  * Redesign of the "Edit Event" and "Edit Subevent" window. There is now only one window in which everything can be edited. Events won't be disabled anymore while these windows are open.
  * Moved hotkey editing into the trigger configuration GUI so it can be edited in the same window. Also it will now show the previously selected hotkey.
  * Some code cleanup and improvements for Accessor. Sort order of results is also slightly improved.
  * Clipboard history is now stored in encrypted form. In addition, if there is no enabled event that makes use of the clipboard history it will not be stored at all for privacy reasons.
  * Made some more static features of 7plus dynamic by integrating them into the event system.
  * French documentation language available thanks to lecuyerf! User interface translation will probably follow in the next version, possibly also with German language. If you want to help with translation, feel free to join this project!

If you like this program and want to support its development, please consider donating!