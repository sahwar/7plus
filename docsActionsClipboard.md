# Clipboard #
This action writes to the clipboard. It can write text, put files in clipboard so they can be pasted in file managers, and it can also write the contents of a file to the clipboard.

Depending on what you select, the "Content" field is either the text that is meant to be written to the clipboard, or a path to a file.

In most cases, you will want to clear the clipboard, so there aren't any remains from other programs. Most of the time it will also work without clearing, but some programs may have problems if you don't.
Alternatively you can select Append to clipboard, in which case the text or files will be appended to text/files which are already present in the clipboard. This is not supported for image files, as there is no point to it in this case.
For files, you can choose to put them in the clipboard as a cut operation, so they will be moved when you paste them instead of being copied.

If you want to use a ${SelN} [placeholder](docsGenericPlaceholders.md) to copy files, make sure to use ${SelNM}, as this is the only supported one for this action for now!

# Usage examples #
  * 7plus uses this action to copy the paths of selected files to the clipboard.
  * See [how to get class names](docsExamplesGetClassName.md).