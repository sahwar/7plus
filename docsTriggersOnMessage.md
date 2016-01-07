# OnMessage #

This trigger gets activated when 7plus receives a window message. Programs send such messages to communicate with each other. You will probably only want to use this if you already know how windows messages work. To use it, simply specify the message number on which it should use.


# Tips #

  * You can also enter "Shellhook" to make it trigger when a shellhook message is received. Windows sends shellhook message to notify programs about various shell events, such as when a program gets activated or destroyed.
  * When you use this trigger, you can also use ${lParam} and ${wParam} [placeholders](docsGenericPlaceholders.md). In Shellhooks, lParam usually contains the related window this message is about, and wParam contains a number that specifies the type of action that happened.