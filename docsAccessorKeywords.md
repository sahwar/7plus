# Accessor Keywords #
In addition to the keywords defined by some plugins, it is also possible to define custom keywords. Those keywords are located at the start of an Accessor command and will be replaced by a command string defined in the settings of 7plus. This is most useful for web searches, but it can also be used as a shortcut for important programs.

For URLs which require parameters (mostly searches), it is possible to use placeholders so that words entered after the keyword will be inserted at those places.

Example:

| Keyword | google |
|:--------|:-------|
| Command | http://google.com/search?q=${1} |
| Entered Accessor command | google 7plus |
| Resulting URL | http://google.com/search?q=7plus |

Of course more than one parameter is supported, in which case the parameters after the keyword are splitted at spaces. If a parameter contains spaces, it needs to be enclosed by quotes.