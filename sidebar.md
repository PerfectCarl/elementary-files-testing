## Test cases for the sidebar

### SIDE-01

Rename a bookmark using the `Rename` entry in the context menu or by hitting `F2`

**expected**: the name of the bookmark is editable and any click any where on the sidebar is ignored. 
If the mouse is not over the sidebar,  `F2` doesn't make the bookmark editable

### SIDE-02

Start renaming a bookmark and cancel the operation in the following ways: 
   - moving the mouse outside of the sidebar
   - hitting the `Escape` key 
   - hitting the `Arrow up` key
   - hitting `Arrow down` key
   
**expected**: the renaming operation is cancelled 

### SIDE-03
Rename a bookmark to an empty string

**expected**: the renaming operation is cancelled and the old name is used instead

### SIDE-04
Remove the bookmark file `~/.config/gtk-3.0/bookmarks` while Files is closed.  Open Files.

**expected**: the bookmark file is re-created containing the user special directories.

### SIDE-05
Remove the bookmark file `~/.config/gtk-3.0/bookmarks` while Files is open.  Close and open Files.

**expected**: the bookmark file is re-created containing the user special directories.

### SIDE-06
Remove the folder `~/.config/gtk-3.0` while Files is closed.  Open Files.

**expected**: the folder is recreated and the bookmark file is re-created therein, containing the user special directories.

### SIDE-07
Drag a folder item, for which there is no existing bookmark, from the view onto the Personal Section of the SideBar, dropping between two existing bookmarks.

**expected**: A line appears between the bookmarks to indicate where the drop will occur; a "copy" emblem appears on the drag icon.  On dropping, a new bookmark is created where indicated by the line, having a folder icon.

### SIDE-08
Drag a file (non-foldr) item, for which there is no existing bookmark, from the view onto the Personal Section of the SideBar, dropping between two existing bookmarks.

**expected**: A line appears between the bookmarks to indicate where the drop will occur; a "copy" emblem appears on the drag icon.  On dropping, a new bookmark is created where indicated by the line, having a mime-type icon.

### SIDE-09
Repeat o7 and 08 using the "Bookmark" option in the file item context menu.

**expected**: A new bookmark is created at the bottom of the custom bookmark list, just above the Trash bookmark.

### SIDE-09a
Repeat 07, o8 and 09 using a file item already having a bookmark.

**expected**: No bookmark is created. No "Bookmark" option appears in the context menu.

### SIDE-10
Drag a custom personal bookmark out of the Sidebar.

**expected**: An animation appears and the bookmark is removed.

### SIDE-10a
Attempt to drag a system bookmark out of the Sidebar.

**expected**: Nothing happens.

### SIDE-11
Secondary click on a custom personal bookmark and select the "Remove" option.

**expected**: The bookmark disappears. If the view is showing the corresponding folder. it continues to do so (the actual folder is not deleted).

### SIDE-11a
Secondary click on a system bookmark

**expected**:There is no "Remove" option.

### SIDE-12
Send a folder that has a personal custon bookmark to trash.

**expected** The bookmark disappears and does not return if the folder is restored.

### SIDE-13
Drag and file item (s) from the view and drop them onto bookmark representing folder with write permissions.

**expected** The files are copied or moved into the bookmarked folder, according to the rules applying to drag and drop between folders in the same or different filesystems or partitions and according to any modifier key also pressed (see drag and drop tests). Dropping onto the bookmark of the files' parent results in a context menu giving the option to create a link.

### SIDE-13
Navigate from one bookmarked folder to another using the location bar or history (not the sidebar).

**expected** The highlighted bookmark is synchronised with the current view.
