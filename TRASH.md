# Testing document for [pantheon-files](lp:~jeremywootten/pantheon-files/fix-crash-when-trashing)

## Trash

###TRASH-01
Delete a local file with the `delete` key on the keyboard

**Expected:** the file is moved to the Trash

##TRASH-02
Delete a local file with the `shift`+`delete` key on the keyboard

**Expected:** the file is moved permanently after a confirmation dialog is displayed

###TRASH-03
Drag a local file to the trash bookmark with the mouse primary button

**Expected:** the file is moved to the Trash

###TRASH-04
Drag a local file to the trash folder opened in another window  with the mouse primary button

**Expected:** the file is moved to the Trash

###TRASH-05
Drag a file located in the trash folder to the trash bookmark with the mouse primary button

**Expected:** nothing happens

###TRASH-06
Drag a file located in the trash folder to the trash bookmark with the mouse secondary button

**Expected:** nothing happens

###TRASH-07
Drag a file located in the trash folder to another folder from another window

**Expected:** the file is restored

###TRASH-08
Drag a file located in the trash folder to a bookmark

**Expected:** the file is restored

###TRASH-09
Drag a file located in the trash folder to another tab

**Expected:** the file is restored

###TRASH-0x
Drag a local file to the trash bookmark with the mouse secondary button

**Expected:** ??

###TRASH-0x
Cut a file with `Ctrl`+`X` and paste it with `Ctrl`+`V` to the trash folder

**Expected:** the file is moved to the Trash

###TRASH-0x
Cut a file with `Ctrl`+`C` and paste it with `Ctrl`+`V` to the trash folder

**Expected:** a dialog is displayed explaining that the action can not be performed



##TRASH-0x
Delete a read only file 

**Expected:** a dialog is displayed explaining that the action can not be performed

##TRASH-0x 
Empty the trash with files in it

**Expected:** the trash is emptied. If many files are present in the trash a dialog showing progress might be displayed

##TRASH-0x 
Delete a file from the trash with the `shift`+`delete` or `delete` key

**Expected:** the file is permanently deleted


SAME WITH shared folder

TRASH and mounted drive
