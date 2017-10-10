
## Test cases for Drag and Drop within and between Views

The drag and drop actions can be carried out using primary or secondary key and with or without pressing a modifier key.   Tests should be carried out using all combinations to test for unexpected results.  Tests should also be carried out with  IconView, ListView and ColumnView. Unless otherwise stated it is assumed both source and destination have the necessary permissions.

### DND-01
Using the primary button and no modifier, drag single local file and drop into another writable local folder in the same file system that is open in the same view.

**Expected**  The drag icon bears the "Move" emblem when over the destination folder.  The destination folder displays its "can accept drop" form. If the mouse is hovered over the destination folder before dropping, then the destination automatically opens in the view.  Further hovering and auto-opening can be performed to get a new destination.  On dropping, the file is moved into the destination folder.  The operation can be undone with Ctrl-Z and redone with Ctrl-Shift-Z.

### DND-02
Using the secondary button and no modifier, drag single local file and drop into another writable local folder in the same file system that is open in the same view.

**Expected**  The drag icon bears the "Ask" emblem when over the destination folder.  The destination folder displays its "can accept drop" form.  If the mouse is hovered over the destination folder before dropping, then the destination automatically opens in the view.  Further hovering and auto-opening can be performed to get a new destination. On dropping, a context menu opens giving options to Move, Copy, Link or Cancel. If not cancelled, the operation can be undone with Ctrl-Z and redone with Ctrl-Shift-Z.  
