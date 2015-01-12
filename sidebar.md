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
