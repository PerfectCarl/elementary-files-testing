
## Test cases actions with two or more windows

All other relevant test cases (Clipboard, Drag and Drop etc) should pass the same whether or not the destination is in the same or a second window.  These test cases cover known past issues related specifically to having two or more windows open.

### MULTIWINDOW-01
Open Files with two tabs open at the same location.  Choose "Open in new window" from second tab label context menu.  Press "Reload " button" in first and second windows.  Repeatedly press "Reload" rapidly.

**Expected**  The second tab disappears and a new window opens showing the same location. Currently, any selection is lost. Regardless of which "Reload" button is pressed, the view in both windows refresh.  No crash or other adverse effect should occur on repeated reloading.

### MULTIWINDOW-01a
Open two windows at the same location as before.  In one window, navigate away from that location.  Press reload.   Navigate back to the first location. Press reload again.

**Expected**  When the view show different locations, only the window containing the pressed button refreshes.  After navigating back to the first location then both windows refresh regardless of which reload button is pressed.

### MULTIWINDOW-02
Open two windows at the same location as before. in Icon View.  In one window, change the view mode to List View. Repeat 01

**Expected**  Both windows refresh and no crash or other adverse effect occurs.

