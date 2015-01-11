# Testing document for [pantheon-files](lp:~jeremywootten/pantheon-files/fix-crash-when-trashing)

## Trash

###TRASH-01
Delete a local file/folder with the `delete` key on the keyboard
Expected: the file/folder is moved to the Trash

##TRASH-02
Delete a local file/folder with the `shift`+`delete` key on the keyboard
Expected: the file/folder is moved permanently after a confirmation dialog is displayed

###TRASH-03
Drag a local file/folder to the trash sidebar
Expected: the file/folder is moved to the Trash

###TRASH-04
Drag a local file/folder to the trash folder opened in another window
Expected: the file/folder is moved to the Trash

###TRASH-05
Drag file/folder located in the trash folder to the trash sidebar
Expected: nothing happens

###TRASH-06
Drag a local file/folder to the trash sidebar with the right mouse button down
Expected: ??

###TRASH-07
Drag a local file/folder to the trash sidebar with the right mouse button down
Expected: ??
