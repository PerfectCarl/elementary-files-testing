# Testing document for [pantheon-files](lp:~jeremywootten/pantheon-files/fix-crash-when-trashing)

## Trash

###TRASH-01
Delete a local file with the `delete` key on the keyboard

**Expected:** the file is moved to the Trash

##TRASH-02
Delete a local file with the `shift`+`delete` key on the keyboard

**Expected:** the file is moved permanently after a confirmation dialog is displayed

###TRASH-03
Drag a local file to the trash sidebar

**Expected:** the file is moved to the Trash

###TRASH-04
Drag a local file to the trash folder opened in another window

**Expected:** the file is moved to the Trash

###TRASH-05
Drag file located in the trash folder to the trash sidebar

**Expected:** nothing happens

###TRASH-06
Drag a local file to the trash sidebar with the right mouse button down

**Expected:** ??

###TRASH-07
Drag a local file to the trash sidebar with the right mouse button down

**Expected:** ??

##TRASH-08
Delete a read only file 

**Expected:** a dialog is displayed explaining that the action can not be performed

##TRASH-09 
Empty the trash with files in it

**Expected:** the trash is emptied. If many files are present in the trash a dialog showing progress might be displayed

SAME WITH shared folder

TRASH and mounted drive
