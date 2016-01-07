# MouseClick #
This action is used to send mouse clicks.

| **Parameter** | **Description** |
|:--------------|:----------------|
|Button         |The mouse button which is used.|
|X              |X/horizontal position of the mouse in pixels.|
|Y              |Y/vertical position of the mouse in pixels.|
|Relative to current window|If set, the origin of X and Y is the top left corner of the active window. Otherwise, it's the top left corner of the screen.|
|Restore current position|If set, the mouse will be moved back to the position it was in before this action was started. If unset, it will stay at the click position.|

If X and Y are empty, the mouse is clicked at its current position.