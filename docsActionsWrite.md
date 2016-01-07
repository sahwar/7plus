# Write #
This action writes text or image to a file.
| **Parameter** | **Description** |
|:--------------|:----------------|
|Content        |The content that gets written to the file. If you use ${Clip} [placeholder](docsGenericPlaceholders.md) and there is an image in the clipboard, it will save that image to the file and use the separately specified image extension.|
|Target         |Path and filename of the target file. If an image is saved, the separately specified image extension is used as extension.|
|Image Quality  |Value between 1 and 100 that specifies the quality of an image that is saved. Unnecessary for saving text content.|
|Append text to file|If set, the text is appended to the target file if it already exists. Otherwise, the file is overwritten.|
|Image extension|If an image is saved, this file extension is used.|

# Usage examples #
  * You can use it to save clipboard contents, such as text or images, or to log various data, such as the active programs, along with the date.