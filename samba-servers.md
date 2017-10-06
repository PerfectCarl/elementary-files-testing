## Test cases for accessing remote samba servers

Testing requires access to at least one accessible Samba server on the local network.  That server should provide at least one public share and one password-protected share.  The server should be in the default workgroup 'WORKGROUP' and broadcast its presence on the network. All other Samba configuration settings are assumed to be such as to not prevent the tests from succeeding. Single-click mode is assumed (otherwise double-clicking will be required for some actions). Depending on the speed of the network and the number of servers some delay may be experienced in refreshing the network view.  It is assumed that the password to the remote samba server has not already been stored locally at the start of testing (see test 06).

The functioning of additional plugin context menu items with samba servers is outside the scope of this test suite.  See test suites for individual plugins.

### SAMBA-01
Click on the `Entire Network` bookmark in the sidebar.

**Expected:** The view shows an icon for each samba server detected on the network. Other types of server may also appear. In addition a folder named 'Windows Network' is displayed.

### SAMBA-02
Click on the `Windows Workgroup` an icon in the Network view.

**Expected:** The view shows an icon for each Windows workgroup detected (usually named WORKGROUP).

### SAMBA-03
Click on the icon for the workgroup containing the test server.

**Expected:** The view shows an icon for each server detected in the workgroup, including the test server.

### SAMBA-04
Click on the icon representing the test server, either in the Entire Network view or in the Workgroup view.

**Expected:** The view shows an icon for each share expected on the test server.

### SAMBA-05
Click on the public test share icon.

**Expected:** The share is mounted and a bookmark with an eject button appears in the sidebar under the Network category. The view shows the folders and files contained in the shared folder. Files are not thumbnailed.

### SAMBA-06
Click on the password protected test share icon.

**Expected:** A dialog appears requesting entry of Username, Domain (Workgroup) and Password.  The first two are pre-filled with the current user name and default workgroup.  In addition, the dialog gives three options for the password: `Forget password immediately`, `Remember until you logout` and `Remember forever`.


### SAMBA-07
(a) Complete the dialog with valid credentials for the test share, selecting `Forget immediately`, and press `Connect`.

**Expected:** The share is mounted and a bookmark with an eject button appears in the sidebar under the Network category.  The view shows the folders and files contained in the shared folder.

(b) Eject the share as per SAMBA-08 and then repeat SAMBA-06.

**Expected** The password dialog reappears.

(c) Remount the share as per SAMBA-07 (a) but select `Remember until you logout`.  Eject the share and remount as before.

**Expected** The share mounts without requiring password entry.

(d) Eject the share, close Files, log out, log back in, restart Files.  Mount the password share as before.

**Expected** The password dialog appears as in SAMBA-06.

(e) At the password dialog, click `Cancel`.

**Expected** The dialog closes and the view shows 'This does not belong to you ... You do not have permission to view this folder' message.

### SAMBA-08
Click the eject button next to the mounted password-protected share.

**Expected:** The eject button becomes a spinner. Provided there are no open files on the share, the share is unmounted and the spinner and bookmark disappear; the view shows the user's home folder.  If files are being held open then a gvfs dialog appears listing the applications blocking unmounting of the share. The Files eject operation times out after a certain delay, in which case the bookmark remains with the eject button.

### SAMBA-09
Type 'network://' into the pathbar and press `Enter` or the `Navigate` icon.

**Expected:** The view shows an icon for each samba server detected on the network. Other types of server may also appear. In addition a folder named 'Windows Network' is displayed. 

### SAMBA-10
Type 'smb://' into the pathbar and press `Enter` or the `Navigate` icon.

**Expected:** The view shows a folder named 'Windows Workgroup'.

### SAMBA-11
In network view (network://), secondary click on a samba server icon.

**Expected** A context menu appears showing a limited number of options including:  `Open in`, `Bookmark` and `Properties`.  Plugins might add additional options.

### SAMBA-12
In network view (network://), secondary click on a Windows Workgroup icon.

**Expected** A context menu appears showing a limited number of options including:  `Open in`, `Bookmark` and `Properties`.  Plugins might add additiunmountingonal options.

### SAMBA-13
In the samba server context menu, click on `Open in` and then (a) `New Tab` (b) `New Window`.

**Expected** The shares available on the server are displayed in (a) a new tab (b) a new window. 

### SAMBA-14
In the Windows Network context menu, click on `Open in` and then (a) `New Tab` (b) `New Window`.

**Expected** The Windows domains (workgroups) available on the network are displayed in (a) a new tab (b) a new window. 

### SAMBA-15
In Windows Network view (smb://), secondary click on a domain (workgroup) icon.

**Expected** A context menu appears showing a limited number of options including:  `Open in`,`Bookmark` and `Properties`.  Plugins might add additional options.

### SAMBA-16
In the domain (workgroup) context menu, click on `Open in` and then (a) `New Tab` (b) `New Window`.

**Expected** The samba servers available in the domain (workgroup) are displayed in (a) a new tab (b) a new window.

### SAMBA-17a
In the samba server context menu, click on `Bookmark`.

**Expected** A bookmark is created named 'Windows shares on [NAME OF SERVER]'

### SAMBA-17b
Click on the bookmark created in SAMBA-17a

**Expected** A view showing the shared folders available on that samba server is shown.

### SAMBA-17c
Close and re-open Files.

** Expected ** The bookmark created in SAMBA-17a persists and continues to function.

### SAMBA-18a
In the domain/workgroup context menu, click on `Bookmark`.

**Expected** A bookmark is created named 'Windows shares on [NAME ON DOMAIN]'

### SAMBA-18b
Click on the bookmark created in SAMBA-18a

**Expected** A view showing the servers available on that domain is shown.

### SAMBA-18c
Close and re-open Files.

** Expected ** The bookmark created in SAMBA-18a persists and continues to function.

### SAMBA-19
In a samba server view, secondary-click on a public or password-protected share icon.

**Expected** A context menu appears showing a limited number of options including:  `Open in`, `Bookmark` and `Properties`.  Plugins might add additional options.

### SAMBA-20
In the samba share context menu, click on `Open in` and then (a) `New Tab` (b) `New Window`.

**Expected** The share is mounted and a bookmark with an eject button appears in the sidebar under the Network category.  A view showing the folders and files contained in the shared folder appears in (a) a new tab (b) a new window.

### SAMBA-21a
In the samba share context menu, click on `Bookmark`.

**Expected**  A bookmark is created named '[NAME OF SHARE] on [NAME OF SERVER]'

### SAMBA-21b
Click on the bookmark created in SAMBA-21a

**Expected** The share is mounted and a bookmark with an eject button appears in the sidebar under the Network category.  The view shows the folders and files contained in the shared folder. If the share is password-protected then a dialog first appears as described under SAMBA-06.

### SAMBA-21c
Unmount the share, close and re-open Files.

**Expected** The bookmark created in SAMBA-21a persists and continues to function.

### SAMBA-22
In the samba server context menu, click on `Properties`.

**Expected**  (TO BE DECIDED/IMPLEMENTED)

### SAMBA-23
In the Windows Workgroup context menu, click on `Properties`.

**Expected**  (TO BE DECIDED/IMPLEMENTED)

### SAMBA-24
In the domain/workgroup context menu, click on `Properties`.

**Expected**  (TO BE DECIDED/IMPLEMENTED)

### SAMBA-25
Open a local folder in one window and a public samba shared folder in another window.

(a)
Drag a file from the local folder to the samba shared folder using the primary button.

**Expected**  The file is copied to the samba shared folder.  If the transfer takes more than approximately 1 second, a progress dialog is displayed.  The views refresh to show the changes.

(b) Drag a file from the local folder to the samba shared folder using the secondary button.

**Expected**  A menu is displayed giving the choices `Move here`, `Copy here` and `Cancel`.  On selecting an option the file is moved or copied as expected. `A Link here` option should not be displayed. The views refresh to show the changes.

(c) Repeat tests (a) and (b) dragging from the remote folder to the local folder.

**Expected**  As for tests 25(a) and 25(b)

### SAMBA-26
Repeat test SAMBA-25 using tabs instead of windows.

**Expected** As for SAMBA-25.

### SAMBA-27
(a) Copy a file from a local to samba shared folder using Ctrl-C and Ctrl-V to copy the file

**Expected** The file is copied and the views update.

(b) Move a file from a local to samba shared folder using Ctrl-X and Ctrl-V to move the file

**Expected** The file is moved and the views update.

(c) Repeat SAMBA-27 (a) and (b) copying/moving from shared to local folder.

(d) Repeat SAMBA-27 (a) and (b) copying/moving from shared to shared folder.

### SAMBA-28
(a) Open a samba shared folder (with write access).  Select one file item. Secondary-click and choose the `Rename` option, or press `F2`.

**Expected** The file item enters rename mode.

(b) Rename the file with a valid name and press `Enter`

**Expected** The file is renamed and the view refreshes to show the new name.

### SAMBA-29
Select a folder within a samba share.  Select `Open in` > `New Tab` from context menu.

**Expected** A new tab opens at the specified folder.

### SAMBA-30
Select a folder within a samba share.  Select `Open in` > `New Window` from context menu.

**Expected** A new window opens at the specified folder.

### SAMBA-31
Select a folder within a samba share.  Select `Open in` > `New Terminal` from context menu.

**Expected** A terminal window opens at the specified folder.

### SAMBA-32
Navigate to a samba server.  Secondary-click on a shared folder.

**Expected** The context menu displays `Open in`, `Bookmark` and `Properties` items.  If the clipboard holds a file it displays a `Paste into Folder` item.  It does not display `Cut`, `Copy` or `Delete` items.  The `Open in` submenu contains `New Tab` and `New Window` items.

### SAMBA-33
Navigate to a samba server.  Secondary-click on the background.

**Expected** The context menu displays `Open in`, `Bookmark` and `Properties` items.  Even if the clipboard holds a file it does not display a `Paste` item.  It does not display `Cut`, `Copy` or `Delete` items. The `Open in` submenu contains `New Tab` and `New Window` items.

### SAMBA-34
Navigate to a samba shared folder.  Secondary-click on the background.

**Expected** The context menu displays `Open in`, `New`, `Sort by`, `Bookmark` `Show hidden` and `Properties` items.  If the clipboard holds a file it displays a `Paste` item.  It does not display `Cut`, `Copy` or `Delete` items. The `Open in` submenu contains `New Tab`, `New Window` `Terminal` items and items for applicable applications.  The `New` submenu contains `Empty File` and `Folder` items; if the user Template special folder contains templates these are also added as items to the `New` submenu.

### SAMBA-35
Navigate to a samba shared folder. Secondary-click on a folder within it.

**Expected** The context menu displays the same items as for a local folder except that the `Move to Trash` item is changed to `Delete permanently`.

### SAMBA-36
Navigate to a samba shared folder. Secondary-click on a file within it.

**Expected** The context menu displays the same items as for a local file of the same type except that the `Move to Trash` item is changed to `Delete permanently`.
