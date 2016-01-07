# Program Launcher Plugin #

This plugin allows to run programs by typing a part of the program's name in Accessor.

The plugin uses a cache in which the paths to the programs are stored. By default, only the .lnk files in the start menu and some other common paths are included, but it is also possible to add custom include paths in the settings.

For speed and clarity reasons, it is not suggested to include large folders like the Program Files or Windows directory. Instead, this plugin maintains a dynamic cache in which it stores programs which have been running during the program's runtime. This way you can run a program once and this plugin will know about it in the future.
Another way to add a program to this cache is by running it through the [file system accessor plugin](docsAccessorFileSystem.md).

This plugin is able to resolve .lnk files to their correct paths to avoid duplications.
You may also use the "run" (default) keyword to exclude the results of other plugins from the list and show all indexed programs.

Like the [file system accessor plugin](docsAccessorFileSystem.md), you can:
  * Open a program with arguments
  * Open its executable path in explorer or CMD
  * Copy its executable path to the clipboard
  * Show the context menu of the executable file

This plugin has some advanced configuration settings. For each cache path its possible to define custom actions which appear in the context menu. An example for this might be a cache path for music files, where the default action would play the file. A custom action can be defined to enqueue the file to the current playlist (if the player has an appropriate command line option).

## Other uses ##
This plugin features another mode which is used to open a file with a program from one of these plugins. To access this mode, select a file in Accessor, Explorer or similar windows and press **CTRL + O**. Accessor will open with "ow " typed into it. Simply type a part of the program's name now to open the selected file with the program.