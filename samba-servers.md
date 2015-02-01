## Test cases for accessing remote samba servers

Testing requires access to at least one accessible Samba server on the local network.  That server should provide at least one public share and one password-protected share.  The server should be in the default workgroup 'WORKGROUP' and broadcast its presence on the network. All other Samba configuration settings are assumed to be such as to not prevent the tests from succeeding. Single-click mode is assumed (otherwise double-clicking will be required for some actions). Depending on the speed of the network and the number of servers some delay may be experienced in refreshing the network view.

### SAMBA-01
Click on the `Entire Network` bookmark in the sidebar.

**Expected:** The view shows a folder item for each samba server detected on the network.  In addition a folder named 'Windows Network' is displayed.

### SAMBA-02
Click on the `Windows Network` folder item in the Network view.

**Expected:** The view shows a folder item for each Windows workgroup detected (usually named WORKGROUP).

### SAMBA-03
Click on the folder item for the workgroup containing the test server.

**Expected:** The view shows a folder item for each server detected in the workgroup, including the test server.

### SAMBA-04
Click on the folder item representing the test server, either in the Entire Network view or in the Workgroup view.

**Expected:** The view shows a folder item for each share expected on the test server.

### SAMBA-05
Click on the public test share.

**Expected:** The share is mounted and a bookmark with an eject button appears in the sidebar under the Network category. The view shows the folders and files contained in the shared folder. Files are not thumbnailed.

### SAMBA-06
Click on the password protected share.

**Expected:** A dialog appears requesting entry of Username, Domain (Workgroup) and Password.  The first two are pre-filled with the current user name and default workgroup.  In addition, the dialog gives three options for the password: Forget immediately, remember until logout and remember forever.

### SAMBA-07
Complete the dialog with valid credentials for the test share and press `Connect`.

**Expected:** The share is mounted and a bookmark with an eject button appears in the sidebar under the Network category.  The view shows the folders and files contained in the shared folder.

### SAMBA-08
Click the eject button next to a mounted share.

**Expected:** The share is unmounted; the view shows the user's home folder.

