# SelectFiles #
This action selects files matching a filter in explorer. The **Filter** is a comma-separated list of entries. You may also use wildcards, e.g. "`*`.jpg,`*`.png" to select all jpg and png files.
There are a few properties:
| **Parameter** | **Description** |
|:--------------|:----------------|
| Clear selection first | If not selected, the matching items will be appended to the current selection.|
| Deselect files | If selected, matching files will be removed from current selection instead of being selected.|
|Automatically add wildcards to start and end|If selected, a file will also match if the filter contains only a substring of its name without wildcards. It basically transforms "filter" to "`*`filter`*`".|

You can use [window filter](docsGenericWindowFilter.md) controls to specify the explorer window, but usually you'll want to leave it at "Active".

# Usage examples #
  * 7plus uses this in combination with the [input](docsActionsInput.md) action, to let the user enter a filter by which files are selected.