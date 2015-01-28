## Test cases for the trash feature

### TRASH-01
Delete a local file with the `delete` key on the keyboard

**Expected:** the file is moved to the trash

### TRASH-02
Delete a local file with the `shift`+`delete` key on the keyboard

**Expected:** the file is deleted permanently after a confirmation dialog is displayed

### TRASH-03
Drag a local file to the trash bookmark with the mouse primary button

**Expected:** the cursor displays the "move overlay" when overlapping the trash bookmark. The file is moved to the trash

### TRASH-04
Drag a local file to the trash folder opened in another window  with the mouse primary button

**Expected:** the cursor displays the "move overlay" when overlapping the trash bookmark. The file is moved to the trash

### TRASH-05
Drag a file located in the trash folder to the trash bookmark with the mouse primary button

**Expected:** nothing happens

### TRASH-06
Drag a file located in the trash folder to the trash bookmark with the mouse secondary button

**Expected:** nothing happens

### TRASH-07
Drag a file located in the trash folder to the trash folder opened in another window

**Expected:** nothing happens

### TRASH-08
Drag a file located in the trash folder to another trash folder from another window

**Expected:** nothing happens

### TRASH-09
Drag a file located in the trash folder to another tab opened to the trash folder

**Expected:** nothing happens

### TRASH-10
Drag a file located in the trash folder to a bookmark

**Expected:** the cursor displays the "move overlay" and the file is restored

### TRASH-11
Drag a file located in the trash folder to another tab

**Expected:** the cursor displays the "move overlay" and the file is restored

### TRASH-12
Cut a file with `Ctrl`+`X` and paste it with `Ctrl`+`V` to the trash folder

**Expected:** the file is moved to the trash

### TRASH-13
Copy a file with `Ctrl`+`C` and paste it with `Ctrl`+`V` to the trash folder

**Expected:** a dialog is displayed explaining that the action can not be performed

### TRASH-14
Cut a file located in the trash with `Ctrl`+`X` and paste it with `Ctrl`+`V` to another folder

**Expected:** the file is restored from the Trash

### TRASH-15
Copy a file located in the trash with `Ctrl`+`C` and paste it with `Ctrl`+`V` to another folder

**Expected:** a dialog is displayed explaining that the action can not be performed

### TRASH-16
Delete a read only folder (chmod 444)

**Expected:** a dialog is displayed explaining that the action can not be performed

### TRASH-17 
Empty the trash with files in it

**Expected:** the trash is emptied of files for which the user has the required permissions. If many files are present in the trash a dialog showing progress might be displayed.  If the trash empties completely (including hidden files) then the view shows an appropriate message (e.g. "This folder is empty").

### TRASH-18 
Delete a file from the trash with the `shift`+`delete` or `delete` key

**Expected:** the file is permanently deleted if the user has the required permissions otherwise a error dialog appears.

### TRASH-19 
Trash a file located on an external filesystem that supports trash using any of the methods listed above.

**Expected:** the file is moved to the user's trash folder on the external filesystem.  The trash icon changes to  the "not empty" state if it was previously empty.  Clicking on the trash icon displays a composite of the local and external trash directories, including the file just trashed.

### TRASH-20
Unmount a filesystem with trash folders.

**Expected:** the filesystem is unmounted without emptying the trash.

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
Try to rename a file in the trash byt hitting `F2` 

**Expected:** nothing happens.
