# ContextMenu #

The ContextMenu trigger is used to add context menu entries to file context menus. It allows integration of 7plus events in explorer.

Use ${Context} placeholder for the list of selected files when the context menu was invoked. This is preferred over the ${SelNM} placeholder because it will also work in alternative file browsers.

The context menu entries will only be visible while 7plus is running. The shell extension will stay registered though. Uninstallation of 7plus will unregister the shell extension.

# Settings #
  * Name: The name that will appear in the context menu.
  * Description: The text that will show up in the explorer status bar.
  * Submenu: If set, the context menu will contain an entry with this value, and the context menu entry defined here will appear in the submenu.
  * File types: Here you can set the file extensions which will have this context menu entry. Leave empty for no files, `*` for all extensions, or use a comma-seperated list of extensions (without dot). 7plus will only show context menu entries that match all selected files.
  * Show in directory context menus: If set, it will show up when directories are selected.
  * Show in directory background context menus: If set, it will show up when the background of a directory is right-clicked.
  * Show in desktop context menu: If set, it will show up in the desktop context menu.
  * Show in "My Computer" context menu: If set, it will show up in the "My Computer" context menu.
  * Don't show with multiple files selected: If set, it will only be visible when there is only one file selected.

Register shell extension: To show context menu entries, 7plus needs to register a shell extension that is loaded in the explorer process and communicates with 7plus. Normally this is done automatically, but if you don't see your context menu entries you can try clicking this button.

Unregister shell extension: If there are problems with the shell extension or you don't use them, you can unregister the shell extension to save some resources. Context menu entries will NOT work then! (Except for those showing in "My Computer", they are handled differently.