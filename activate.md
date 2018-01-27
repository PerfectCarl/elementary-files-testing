## Test cases for Activating one or more Files or Folders in a View.
Files and folders may be activated (opened) in a number of different ways, either by Files itself or a chosen default app for the appropriate mime-type.  Reference to "primary click" assumes the app is in the default `single-click` mode (unless specifically stated otherwise).  If the app is in `double-click` mode then substitute "double-click".  Folders clicked on are assumed to be readable unless stated otherwise.  Activating using the context menu is covered under context menu tests.

### ACTIVATE-01a
Primary click on a single selected or unselected folder while in Icon or List View.

Expected: The contents of the clicked folder are displayed in the same tab.  This should happen whether or not there are other selected files or folders in the view. The pathbar shows the new path.  The sidebar cursor syncs to the same folder if present amongst the bookmarks. The previous path is recorded in the history.

### ACTIVATE-01b
Primary click on a single selected or unselected folder while in Column View.

Expected: A new column opens and the contents of the clicked folder are displayed in that column.  Focus moves to this column but no file is selected. This should happen whether or not there are other selected files or folders in the clicked column. The pathbar shows the new path.  The sidebar cursor syncs to the same folder if present amongst the bookmarks. The previous path is recorded in the history. If the clicked column already shows subfolder columns then these close before the new column is created.

### ACTIVATE-01c
Double click on a single selected or unselected folder while in Column View with `single-click` mode set.

Expected: All columns close and the clicked folder is opened as the root of the view.

### ACTIVATE-01d
Middle click on a single selected or unselected folder while in any view.

Expected: The folder opens in a new tab.

### ACTIVATE-01e
Selected a single folder in any view. Press the space bar. 

Expected: The folder opens in a new tab.

### ACTIVATE-02a
In any view, select two to ten folders.  Primary click on them.

Expected:  Each selected folder opens in a new tab in the same view mode.

### ACTIVATE-02b
Select a lot, currently more than ten (limit may change), of folders.  Primary click on them.

Expected:  A dialog appears stating that this number of files will not be opened simultabeously.

### ACTIVATE-03a
Primary or middle click on a single selected or unselected file while in any View.

Expected: The appropriate (or chosen) default app is opened with that path as a parameter. e.g. a text file is shown in Code or another a text editor, a PDF is shown in Evince or another PDF viewer.

### ACTIVATE-03b
Primary or middle click on a small number (less than 10) multiple selected files of the same type while in any View.

Expected: The appropriate (or chosen) default app is opened with multiple file paths as a parameter. e.g. a text files are shown in Code or another a text editor, a PDFs is shown in Evince or another PDF viewer.  This may be in one or more windows depending on the default app.  A dialog may appear asking which app to use to open this mime type if no association as registered.


### ACTIVATE-03c
Primary or middle click on a small number (less than 10) multiple selected files of different types while in any View.

Expected: Unless there is an app registered as capable of opening all the file types selected then a dialog appears asking for the user to choose.  If not cancelled at this point then that app is opened passing all the file paths as parameters. This may or may not result in errors from that app.
