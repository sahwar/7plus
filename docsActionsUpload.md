# Upload #
This action can upload multiple files on an FTP server, and copy the links to the clipboard afterwards.

| **Parameter** | **Description** |
|:--------------|:----------------|
|Source file(s) |One or more files to upload. Multiple files need to be quoted and separated by spaces or unquoted and separated by newlines. Use ${SelNQ} or ${SelNM} for selected files in explorer if you need to.|
|Hostname       |The hostname of the ftp server. Do not prepend "`ftp://`" or similar, just use "hostname.com".|
|Port           |Usually 21.      |
|Username       |FTP username.    |
|Password       |FTP password.    |
|Target folder  |Target subfolder on the FTP server in which the files should be uploaded.|
|Target files   |Leave empty to use original filenames, or enter filename(without extension) or extension (starting with ".") to replace this part of the original filename.|
|URL            |URL under which the files are accessible. This is only needed if the links should be copied to the clipboard.|
|Silent         |If set, no notification will be seen when upload is finished or failed. Otherwise, a tooltip will appear and a sound beep will be played.|
|Copy links to clipboard|If set and URL is specified, upon success the links to the files will be copied to the clipboard.|

# Usage examples #
  * 7plus uses this to upload selected files from explorer when CTRL+U is pressed (default setting),to take and upload screenshots on Alt/Win +Insert (default setting) and to upload images and text from clipboard on Win+Delete hotkey (default setting).
  * You can also use this to automatically upload file backups to a server on a timed basis by using a [timer](docsTriggersTimer.md) and a ${DateTime} [placeholder](docsGenericPlaceholders.md).
  * Combining the CTRL+U upload function with an [if condition](docsConditionsIf.md), you can upload to different servers depending on the location of the source files. This could be useful if you do web development and need to upload files from different projects.

# Notes #
  * To use the built-in FTP features, you need to enter your FTP account data in each of those events.
  * When you create a new upload action, the FTP data from the previous existing upload action is preselected for convenience.
  * Passwords are stored encrypted.