
## Test cases for clipboard handling (Copy/Cut/Paste)

### COPY-01
Copy and paste a file multiple times in a quick succession (using `Ctrl`+`V`). 

**expected**: the files are copied and only one of them is selected at any time (the last copy of the file). See [#1404501][1] for more info.

[1]: https://bugs.launchpad.net/pantheon-files/+bug/1404501

### COPY-02
Copy and paste a selection of files multiple times in a quick succession (using `Ctrl`+`V`). 

**expected**: the files are copied and only one of set of the selection is selected at any time (the last copy of the file).

## Trash related test cases 

### [TRASH-12](trash.md#trash-12)

### [TRASH-13](trash.md#trash-13)

### [TRASH-14](trash.md#trash-14)

### [TRASH-15](trash.md#trash-15)
