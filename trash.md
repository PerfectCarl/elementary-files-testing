## Test cases for the trash feature

### TRASH-01
Delete a local file with the `delete` key on the keyboard

**Expected:** the file is moved to the trash. The action can be undone with Ctrl-Z.

### TRASH-02
Delete a local file with the `shift`+`delete` key on the keyboard

**Expected:** the file is deleted permanently after a confirmation dialog is displayed. The action cannot be undone with Ctrl-Z.

### TRASH-03
Drag a local file to the trash bookmark with the mouse primary button

**Expected:** the cursor displays the "move overlay" when overlapping the trash bookmark. The file is moved to the trash. The action can be undone with Ctrl-Z.

### TRASH-04
Drag a local file to the trash folder opened in another window  with the mouse primary button

**Expected:** the cursor displays the "move overlay" when overlapping the trash bookmark. The file is moved to the trash. The action can be undone with Ctrl-Z.

### TRASH-05
Drag a file located in the trash folder to the trash bookmark with the mouse primary button

**Expected:** nothing happens

### TRASH-06
Drag a file located in the trash folder to the trash bookmark with the mouse secondary button

**Expected:** nothing happens

### TRASH-07
Drag a file located in the trash folder to the trash folder opened in another window with the mouse primary button

**Expected:** nothing happens

### TRASH-08
Drag a file located in the trash folder to another trash folder from another window with the mouse secondary button

**Expected:** nothing happens

### TRASH-09
Drag a file located in the trash folder to another tab opened to the trash folder

**Expected:** nothing happens

### TRASH-10
Drag a file located in the trash folder to a bookmark

**Expected:** the cursor displays the "move overlay" and the file is restored. The action can be undone with Ctrl-Z.

### TRASH-11
Drag a file located in the trash folder to another tab and drop onto the view (not the tab).

**Expected:** The view switches to the tab hovered over. The cursor displays the "move overlay" while the over the view itself. When dropped, the file is restored. The action can be undone with Ctrl-Z (the tabs are not switched back).

### TRASH-12
Cut a file with `Ctrl`+`X` and paste it with `Ctrl`+`V` to the trash folder

**Expected:** the file is moved to the trash.  The action can be undone with Ctrl-Z.

### TRASH-13
Copy a file with `Ctrl`+`C` and paste it with `Ctrl`+`V` to the trash folder

**Expected:** a dialog is displayed explaining that the action can not be performed aand the file is not trashed.

### TRASH-14
Cut a file located in the trash with `Ctrl`+`X` and paste it with `Ctrl`+`V` to another folder

**Expected:** the file is restored from the Trash. The action can be undone with Ctrl-Z.

### TRASH-15
Copy a file located in the trash with `Ctrl`+`C` and paste it with `Ctrl`+`V` to another folder

**Expected:** a dialog is displayed explaining that the file cannot be copied and will be cut instead. The file is restored from trash.  The action can be undone with Ctrl-Z.

### TRASH-16
Delete a read only folder (chmod 444)

**Expected:** a dialog is displayed explaining that the action can not be performed

### TRASH-17a 
Open the trash view when there are trashed files.

**Expected:** The view displays a composite of all accessible trash folders. An infobar is displayed including a suitable message and a button marked "Empty the Trash".

### TRASH-17b 
Click the button marked "Empty the Trash" in the trash view when there are trashed files.

**Expected:** A dialog appears warning that all the files in **all** trash folders, including any on external media will be permanently deleted. The trash is emptied of files for which the user has the required permissions, that is when the user has write and execute permissions on the trash folder in which the file resides. If many files are present in the trash, a dialog showing progress might be displayed.  If the trash empties completely (including hidden files) then the view shows an appropriate message (e.g. "This folder is empty") and the infobar is hidden.  The action cannot be undone with Ctrl-Z.

### TRASH-18 
Delete a file from the trash with the `shift`+`delete` or `delete` key

**Expected:** the file is permanently deleted if the user has the required permissions otherwise a error dialog appears.  The action cannot be undone with Ctrl-Z.

### TRASH-19a 
Trash a file located on an external filesystem that supports trash using any of the methods listed above.

**Expected:** the file is moved to the user's trash folder on the external filesystem.  The trash icon changes to  the "not empty" state if it was previously empty.  Clicking on the trash icon displays a composite of the local and external trash directories, including the file just trashed.


### TRASH-19b 
Trash a file located on an external filesystem that does not support trash using any of the methods listed above.

**Expected:** a dialog confirming _permanent_ deletion of the file appears.

### TRASH-20a
Unmount a filesystem with trash folders.

**Expected:** the filesystem is unmounted without emptying the trash. The composite trash view no longer displays trashed files on the external filesystem.

### TRASH-20b
Remount a filesystem with trash folders containing trashed files.

**Expected:** The composite trash view re-displays trashed files on the external filesystem.

### TRASH-21
Secondary-click on a the bookmark of an external filesystem with trash folders containing files.

**Expected:** a context menu appears including an option to empty the trash.

### TRASH-22
Select the "Empty trash" option in test TRASH-21.  

**Expected:** the trash on the external filesystem is emptied (files permanently deleted) but not any other trash.  
If all other trash folders were empty then the state of the Trash icon changes to "Empty".

### TRASH-23
Secondary-click on a the bookmark of an external filesystem with trash folders that are empty.

**Expected:** a context menu appears that does not include an option to empty the trash.

### TRASH-24
Empty the composite trash using the Trash icon or Trash view.  

**Expected:** the trash on any mounted filesystem with trash folders is emptied as well as the local trash.

### TRASH-25
Try to rename a file in the trash by hitting `F2` 

**Expected:** nothing happens.
