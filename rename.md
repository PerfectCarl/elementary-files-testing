## Test cases for renaming files

### RENAME-01
Select one file, with write access, in any view, secondary click on it.

**Expected:** a context menu appears containing the item "Rename" in the sensitive state.

### RENAME-02
Select one file, without write access, in any view, secondary click on it.

**Expected:** a context menu appears containing the item "Rename" in the insensitive state.

### RENAME-03
Select two or more files, with write access, in any view, secondary click on it.

**Expected:** a context menu appears containing the item "Rename" in the insensitive state.

### RENAME-04
Select one file, with write access, in any view, and press F2.

**Expected:** The selected file item enters rename mode.

### RENAME-05
Select one file, without write access, in any view, and press F2.

**Expected:** Nothing happens.

### RENAME-06
Select two or more files, in any view, and press F2.

**Expected:** Nothing happens.

### RENAME-07
Start renaming one file (not folder) as indicated above.

**Expected:** The filename is selected, excluding any extension.

### RENAME-08
Start renaming one folder as indicated above.

**Expected:** The whole filename is selected, including any extension.

### RENAME-09
Start renaming one file or folder as indicated above and start typing.

**Expected:** The selected part of the filename is replaced by the typed characters.

### RENAME-10
Start renaming one file or folder and edit part of the name.  Press Ctrl-Z

**Expected:** The changes are undone and the item stays in rename mode.

### RENAME-11
Start renaming one file or folder and edit part of the name.  Press Esc

**Expected:** The changes are undone and the item exits rename mode.

### RENAME-12
Start renaming one file or folder and edit to a valid, non-duplicate name.  Press Enter

**Expected:** The item exits rename mode and the file is renamed.

### RENAME-13
Start renaming one file or folder and delete the entire name.  Press Enter

**Expected:** The item exits rename mode and the file is not renamed.

### RENAME-14
Start renaming one file or folder and edit to a valid, non-duplicate name.  Click outside the item.

**Expected:** The item exits rename mode and the file is renamed.

### RENAME-15
Start renaming one file or folder.  Primary click inside the editable widget.

**Expected:** The item stays in rename mode; the text is unselected; the edit cursor moves to the clicked position.

### RENAME-16
Start renaming one file or folder.  Primary click and drag inside the item.

**Expected:** The item stays in rename mode; the text is selected between start and end of drag.
