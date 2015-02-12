
## Test cases for clipboard handling (Copy/Cut/Paste)

The copy, cut and paste actions can be carried out either using the keyboard (Ctrl-C, Ctrl-X and Ctrl-V) or selecting the appropriate option from the file context menu.   Tests should be carried out using both methods where possible.

### COPY-01
Copy a single local file and paste into another local folder that is open in another window.

**Expected** The file is copied into the destination folder. When the file has been created, a corresponding file icon appears in the view of the destination folder and is selected.

### COPY-02
Copy a single local folder and paste into another local folder that is open in another window.

**Expected** The folder and all files and folders contained therein are copied into the destination folder. When the folder has been created, a corresponding file icon appears in the view of the destination folder and is selected.  If the contents of the folder are large, a progress dialog appears with an option to cancel.  Cancelling the transfer leaves any folders and files that have already been created in place.

### COPY-03
Repeat tests 01 and 02 using a multiple selection of files and folders.

**Expected** The selection is copied to the destination and all items are selected.

### COPY-04
Repeat tests 01, 02 and 03 using a destination on a remote samba server.

**Expected** The selection is copied to the destination and the remote folder view is refreshed.

### COPY-05
Copy and paste a file multiple times in a quick succession (using `Ctrl`+`V`). 

**expected**: the files are copied and only one of them is selected at any time (the last copy of the file). See [#1404501][1] for more info.

[1]: https://bugs.launchpad.net/pantheon-files/+bug/1404501

### COPY-06
Copy and paste a selection of files multiple times in a quick succession (using `Ctrl`+`V`). 

**expected**: the files are copied and only one of set of the selection is selected at any time (the last copy of the file).

### COPY-07
Copy a read only file (using `Ctrl`+`C`).  Paste into another folder (using `Ctrl-V`).

**expected**: An error dialog is displayed with detail 'Permission denied'.

## Trash related test cases 

### [TRASH-12](trash.md#trash-12)

### [TRASH-13](trash.md#trash-13)

### [TRASH-14](trash.md#trash-14)

### [TRASH-15](trash.md#trash-15)
